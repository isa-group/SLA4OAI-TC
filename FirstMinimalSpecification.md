# Minimal specification for SLA4OAI v1

In order to have first operational specification that covers an initial set of features we propose the following aspects, grouped in two levels of criticity based on an informed [analysis of SLAs APIs in the industry](https://link.springer.com/chapter/10.1007%2F978-3-319-69035-3_43):

## High priority
- **Context**. There should be a way to specify the SLA context describing aspects like SLA version, stakeholders or the validity period. 
See [ContextObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#522-contextobject) for an initial proposal.
- **Metrics**. There should be a way to describe which elements would be computed in order to analyse SLA fullfillment. 
See [MetricsObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#527-metricobject) for an initial proposal.
- **Quotas**. There should be a way to describe the limitations of use for a fixed/static period of time.
See [QuotasObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5210-quotasobject) for an initial proposal.
- **Rates**. There should be a way to describe the limitations of use for a dynamic period of time. 
See [RatesObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#527-ratescobject) for an initial proposal.

## Low priority
- **Guarantee**. There should be a way to describe the commitments over a certain metrics. 
See [GuaranteesObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5212-guaranteesobject) for an initial proposal.

- **Configuration**. There should be a way to describe the attributes constraints that would be used to drive the API behaviour
See [ConfigurationObject in current draft](https://github.com/isa-group/SLA4OAI-Specification/blob/master/Specification.md#5218-configurationsobject) for an initial proposal.


