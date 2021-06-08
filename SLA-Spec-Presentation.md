# Service Level Agreement Spec for APIs
### OpenAPI SIG

---
# Abstract
API consumers expect Service Level Agreements (SLAs) for every API in production. However, the specification and documentation of SLAs is not something you cans do with OpenAPI west.
The SLA for OpenAPI Special Interest Group has been working on a Spec  express SLA definitions that works hand in hand with OAS.
In this talk, we will present the current state of the Spec , as well as the main use cases and benefits it leverages: ranging from SLA documentation, automatic SLA enforcement, automatic middleware configuration, to SLA verification,.
We’ll then discuss how you can help improve and extend the spec by contributing to discussions and tooling.

---
# SLA Spec

- DSL for defining a set of metrics and constraints regarding service availability, quality of the service like minimal and maximal throughput, latency, quotas, rate-limits, pricing plans
- Declarative YAML document
- Meant to be used alongside OpenAPI, which can't (and should not) describe runtime aspects

---

![75%](https://www.openapis.org/wp-content/uploads/sites/3/2021/03/SLA-concepts.png)

---
# Why now?

- API & Services Proliferation!
- Hard to keep track of configuration in each deployment, each environment
- Hard to replicate and review configurations
- Need a precise way to specify runtime behavior, one that can be checked in, diffed and used for testing, repeatably
- Avoid misconfiguration, which leaves your service open to Security and Availability problems

---
# How to use it

1. Start with a document specifying what you need
2. Review with your team for correctness
3. Document becomes part of deployment
4. Validate using automation
5. Use as basis for next iteration so you can have a precise record of each state

---
# How it benefits API Consumers

- Accurate SLA/Plans Documentation, know what to expect
- Clients can understand better how to use a Service
- Automatically adjust its consumption (e.g. throttling)
- 3d party assurance for stated availability

---
# How it benefits DevOps

- Service/Gateway Configuration
- SLA/Plans Testing, Validation, Compliance
- Helps review and rollback configuration changes

---
# How it benefits Business

- Enforces limits
- Accountability and Precision around plans & monetization
- Easier to evolve monetization and plans

---
# How it benefits Toolmakers

- Provide more value in your products
- Render customized documentation for each environment
- Users can use and deploy more gateways since it's easier to configure and control them

---
# Where to go from here

- Contribute!
    - Need to improve for reuse & Overlays
- Implement!
    - Gateway plugins: Kong, Tyk, Ambassador
    - Documentation: Readme, SwaggerUI, Stoplight Elements, Optic
    - Testing & Monitoring: Postman, SoapUI, Moesif, APIMetrics

---
# Summary

- Declare SLA quotas, limits, plans
- Service/Gateway Configuration
- SLA/Plans Documentation
- SLA/Plans Testing, Validation, Compliance

---
# Info

- [1.0 Version](https://github.com/isa-group/SLA4OAI-Specification/blob/main/versions/1.0.0-Draft.md)
- [Team](https://github.com/isa-group/SLA4OAI-TC)
- [GitHub](https://github.com/isa-group/SLA4OAI-Specification)

---
