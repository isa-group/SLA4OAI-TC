# SLA4OAI

## Minimal Specification Proposal

This proposal introduces a minimal sample to explore te syntax and semantics needed to describe SLI, SLO, SLA concepts useful to describe APIs and contracts from multiples point of views.

The main objective is to foster discussion about the essential concepts and create consensus on a minimum and as simple as possible specficiation proposal.

### 0. Meta-model

Figure 1 describes the metamodel used.

![Figure 1. Metamodel](metamodel.png)

### 1. Extension Format

SLA extension can be mapped in an external YAML or JSON file. The OpenAPI specification main document can link to SLA defitions using the standard extension and `$ref` linking mechanims:

```yaml
openapi: 3.0
  ...
  x-sla:
    $ref: ./sla.yml
  ...
```

## Base Example

```yaml
sla: 1.0
context:
  id: petstore-sample
  type: plans
  api:
    $ref: ./petstore-service.yml
  provider: ISAGroup
```

### 2. Header

SLA defitions (following the same guidelines applied in OpenAPI) starts with describing the document type `sla` and the version following [Semantic Versioning](https://semver.org/) conventions.

### 3. Context

Context block provide metadata to describe the type of SLA information to be provided.

- `id` provide a unique name (_mandatory_).
- `type` can take the values `plans` or `aggrement` (_mandatory_).
- `provider` describe the organization providing the service (_optional_).

### 4. Metrics

```yaml
metrics:
  animalTypes:
    type: integer
    format: int64
    description: Number of different animal types.
    resolution: check
  resourceInstances:
    type: integer
    format: int64
    description: Number of pet resources
    resolution: consumption
  requests:
    type: "int64"
    description: "Number of requests"
    resolution: consumption
  responseTimeMs:
    type: "double"
    unit: "ms"
    description: "Response time in milliseconds"
    resolution: consumption
```

Metrics sections describes the relevant tecnical indcators and business metrics for the SLA.

There could be pure technical ones like response time, throughtput, or band-width but also business ones like sales per period, usage metrics, etc.

For each metric to be defined:

- `type` and `format` describes the data-type following same conventions as OpenAPI 3.x.
- `description` provides a label for the metric been defined.
- `resolution` could be `check` or `consumption` (_optional_).
  - `check` is a precondition that can be evaluated before granting permission for the service (no need to evaluate the payload).
  - `consumption` is a check that needs to inspect the message to decide if limits will be overpassed or not. 

- `unit` (when applicable) describes the units to be used for the measure. e.g. `ms`, `req/s`, etc.

### 5. Pricing

Pricing block describes a price model fon an especific plan. Describing the `cost`, the `currency` (expresed in [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) form) and the billing period `billing`.

```yaml
pricing:
  cost: 0
  currency: EUR
  billing: monthly
```

### 6. Availability

```yaml
availability: R/00:00:00Z/15:00:00Z
```

Availiability, when applicable, describes a time-windows where the API is available (using the [ISO 8601 Time Intervals](https://en.wikipedia.org/wiki/ISO_8601#Time_intervals) format).

### 7. Quota Limits

Quotas limits are resource contraints imposed globally (e.g. _max. disk usage_) or scoped to *static* temporal windows (e.g. _holidays as 24 labout days per year_ - in a period of a *natural year*).

For a formal definition of Rates and Quotas see [1].

```yaml
rates:
  /pets/{id}:
    get:
      requests:
        - max: 1
          period: secondly
```

Quotas section describes limits to endpoints based on expression over metrics. Samples:

- maximum 10 request per minute by account to `GET /pets`
- maximum 40 request per hour by tenant to `GET /pets`
- maximum 3 request per minute by account to `POST /pets`
- maximum of 5 resource instances on `POST /pets`
- maximum of 2 animal types on `POST /pets`

### 8. Rate Limits

Rates section describes limits to endpoints based on expression measured with respect to metrics for a *dynamic* window time.

```yaml
rates:
  /pets/{id}:
    get:
      requests:
        - max: 1
          period: secondly
```

Samples:

- maximum 1 request per second to `GET /pets/{id}`

```yaml
guarantees:
  global:
    global:
      - objective: responseTimeMs <= 800
        period: daily
        window: dynamic
```

### 9. Guarantees

Description of the API warranties commitment by the service provider.

Example:

- main objective: response time under 800 ms (measured daily).

### 10. Plans

Describes different plans including different prices and level of service. Level of service can be improved or limited depending of the plan.

```yaml
plans:
  free:
    rates:
      /pets/{id}:
        get:
          requests:
            - max: 1
              period: secondly
  pro:
    availability: R/00:00:00Z/23:59:59Z
    pricing:
      cost: 50
    configuration:
      filteringType: multipleTags
      xmlFormat: 'true'
    quotas:
      /pets:
        get:
          requests:
            - max: 20
              period: minutely
              scope: account
            - max: 100
              period: hourly
              scope: tenant
        post:
          requests:
            - max: 100
              period: minutely
          resourceInstances:
            - max: 500
          animalTypes:
            - max: 5
    guarantees:
      global:
        global:
          - objective: responseTimeMs <= 250
            period: daily
            window: dynamic
```

### 11. Plans application

First `base` keyword is proposed as the common base plan. All limits and guaraties applied to base applies to all plans.

Then, a specific plan inherits definitions from `base` and can override any limit to make it more concrete or relaxed.

### 12. Keywords

- `base` is used as the common properties applicable to all plans (can be overriden).
- `global` is used in the guarantees section to describe API common guarantiees (cab be overriden by specific plans).

## References

1. An Analysis of RESTful APIs Offerings
in the Industry. A. Gamez-Diaz(B), P. Fernandez, and A. Ruiz-Cortes. In M. Maximilien et al. (Eds.): ICSOC 2017, LNCS 10601, pp. 589–604, 2017. DOI: [10.1007/978-3-319-69035-3_43](https://doi.org/10.1007/978-3-319-69035-3_43)