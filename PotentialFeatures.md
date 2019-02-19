# Potential Features

List of **Potential Features** for inclusion on SLA for OpenAPI.
An open list of topics and ideas to be discussed in the group.

## Potential Features

### Definition Aspects
- SLA as a business contract
- Granularity of definitions
    - Exposed Service SLA
    - Combined SLA
- API Constraints
    - Quota
    - Rate Limit
    - Time constraint
    - Authentication
- API Monetization
    - Pricing & plans
    - Metering
    - Rating
    - Billing

### Operation Aspects
- Runtime measuring
    - Server Level Indicators (SLI)
        - Availability
        - Latency
    - Server Level Objective (SLO)
        - Target metrics
- SLA Reporting
- Composition of services and expected combined SLAs

### How to represent it
- Microformats + linking vs monolith representation
- OAS spect can optionally link to an SLA definition.

## Agreed Features in Scope
  
- See [current draft proposal for v1](https://github.com/isa-group/SLA4OAI-TC/edit/master/FirstMinimalSpecification.md)

## Discarded Features in Scope

- TBD.

## Proposed Ideas

For previous discussion there is a recommendation by Google/Apigee:
- to focus first on defining an extension to describe technical concerns: SLI and SLO aspects as a clear technical concern and
- to keep SLA (as a business contract) out of the scope for a later extension.
