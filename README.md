# SLA4OAI Technical Committee Wiki

This wiki is the central page for the Technical Committee behind the [SLA4OAI Specification](https://github.com/isa-group/SLA4OAI-Specification): an extension for [OpenAPI Specification](https://github.com/OAI/OpenAPI-Specification) in order to describe Service Level Agreements (SLA) in RESTFul APIs including elements such as quota, rates or usage plans.

This committee is open to all the different members in OAI and the API developer community in general. If you are interested in participate please subscribe to the following list: [sla@openapi.groups.io](https://openapi.groups.io/g/sla)

In the next sections, you can find the meetings, minutes, material, and the roadmap for future actions. 

## History

 - 2016 - A first draft (v0.9.1) f the specification has evolved from an academic initiative started by [ISA Research Group](http://www.isa.us.es) at [University of Seville](http://www.us.es).
 - 2017 - Extension is presented to OpenAPI Technical Specification Committee that expressed their positive feedback about it. 
 - 2018 - OpenAPI Governance Board aproved the creation of a *Specific Interest Group* to coordinate this extension. This group is originally formed by different members from the OAI consortium.
 - 2018 - The specific interest group starts its activities.
 - 2019 - A [common view](docs/2019_ESEC_FSE_IndustryTrack_The_role_of_SLAs_in_the_API_industry.pdf) on the conceptual model and priorities to be addressed is defined.
 - 2021 - SLA4OAI v1 draft is presented to Open API TC as an extension for OAS and opened for community feedback. 
 
## Roadmap

Proposed milestones for the specification:
 - **2021Q3/4** - Open call for tooling/community feedback
 - **2022Q1** - Discuss new v2 features
 - **2022Q3/4** - Work on v2 of SLA4OAI

## Consolidated Material

[The Role of Limitations and SLAs in the API Industry (SLA4OAI-TC)](docs/2019_ESEC_FSE_IndustryTrack_The_role_of_SLAs_in_the_API_industry.pdf) presented at the Industrial Track of the 27th ACM Joint European Software Engineering Conferenceand Symposium on the Foundations of Software Engineering (ESEC/FSE ’19)

## Working Material
[SLA4OAI Manifest](./Manifest.md). This document contains the key foundational decisions to guide SLA4OAI.

[Minimal specification for SLA4OAI v1](FirstMinimalSpecification.md). This document exposes the core elements that will be included in version 1 of the spec.

[Use Cases](UseCases.md) List of *User Stories* to consider for the specification.

[Potential features to include in following versions](PotentialFeatures.md). Set of features grouped in areas that will be discussed in future versions of SLA4OAI.

Perspectives of SLA from the different participants: 
- [Pablo Fernandez (ISA-Group)](https://drive.google.com/open?id=1sBjd8FR4zVqF5wYBzvnWrpncCmO2AJv1) as discussed on the 2018-11-07 call.
- [Isaac Hepworth (Google/Apigee)](docs/API%20Service%20Levels%20and%20OpenAPI.pdf) as discussed on the 2018-12-03 call.

## Calls
This section contains the key content and minutes from the different calls.

### 2021.05.04

*Participants: Tim Burks (Apigee), Paul Cray (Apimetrics), Emmanuel Paraskakis (Level 250), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

Minutes of the meeting:
1. Discussed next steps and participation on [ASC 2021](https://events.linuxfoundation.org/openapi-asc/).

#### Material

- [Video of the call](https://drive.google.com/file/d/1GAEYUqkBgqfAN4QWbON5y8yOzEVLCwcF/view?usp=sharing)


### 2020.12.17

*Participants: Tim Burks (Apigee), Paul Cray (Apimetrics), Madhurranjan Mohaan (Google), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

Minutes of the meeting:
1. Discused Issues and Pull Request:

  - [7](https://github.com/isa-group/SLA4OAI-Specification/issues/7) Simplify language proposal by Tim. Accepted. Pablo made a [PR 13](https://github.com/isa-group/SLA4OAI-Specification/pull/13) for it.
  - [8](https://github.com/isa-group/SLA4OAI-Specification/issues/8) Global rates and quotas: reuse mechanism. Accepted. Tim to prepare a PR using a [globbing strategy](https://en.wikipedia.org/wiki/Glob_(programming)). 
  - [9](https://github.com/isa-group/SLA4OAI-Specification/issues/9) -> [PR 12](https://github.com/isa-group/SLA4OAI-Specification/pull/12) merged.
  - [10](https://github.com/isa-group/SLA4OAI-Specification/issues/10) -> [PR 11](https://github.com/isa-group/SLA4OAI-Specification/pull/11) merged.
  
2. Specification looks good enough to participant to be scalated to TSC and open to public to call for feedback.
3. Next meeting proposed for Thursday: 2021.01.14 

#### Material

- [Video of the call](https://drive.google.com/file/d/1TY2jwAtfzC53MvfZF-fvIVE85FfgKXuz/view)

### 2020-10-29

*Participants: Nikhil Kolekar (Independent), Paul Cray (Apimetrics), Khushan Adatiya (Google), Phil Sturgeon (SpotLight), Kin Lane (Postman), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

Minutes of the meeting and action plan:
- Agreement to keep pushing on the minimal spec to be complete as soon as possible. (Pablo)
- Awaiting for PRs and proposal for the next meeting.
- Nikhil commitment to contribute with a PR to incorporate support for subscriptions.
- Study the possibilty to rewrite as an Overlay. (Pedro & Phil)
- Khushan to catch up and recopilate contributions from Google.

#### Material

 - [Video of the call](https://drive.google.com/file/d/1d4moGcT1PrP29pWU4yKenmIutXPhuK2f/view?usp=sharing)

### 2020-07-14
*Participants:  Nikhil Kolekar (Independent), 	Dave O'Neil (Apimetrics), Paul Cray (Apimetrics), Madhurranjan Mohaan (Google), Hyungjun Lim  (Google), Khushan Adatiya (Google), Fran Mendez (AsyncAPI), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

This session introduced the work by Paul and Dave (Apimetrics). Later the team review the current minimal specification, procedure to follow and discussion of suggested changes to be made.

#### Material
 - [Video of the call](https://drive.google.com/file/d/1asNfdVA9_bzzWEor3VlytQXngX1L9idF/view?usp=sharing)
 - [Slides](https://docs.google.com/presentation/d/1m0Bl_htl4UAo52DPEMGzlpkBrfwuy0LRxLNaOOpa1CQ/edit?usp=sharing)


### 2020-04-01
*Participants:  Nikhil Kolekar (Independent), Emmanuel Paraskakis (Smartbear), Phil Sturgeon (Spotlight), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

In this meeting a proposal for contents of a first minimal viable spec and the process to leverage it as a formal extension to OAS comitee.

#### Material
 - [Video of the call](https://drive.google.com/file/d/1IYhH1UlGa5z6uHI70VF_QpBEqYLqazOS/view?usp=sharing)
 - [Slides](https://drive.google.com/open?id=1tAkegexohOlW6-Sn-Q3q12kkg_5pPvsF06qeB7bIlns)


### 2019-02-19
*Participants:  Nikhil Kolekar (Paypal), Isaac Hepworth (Google), Mike Ralphson, Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

In this meeting Nikhil presented his PoV about SLAs and APIs given his experience in operating and creating APIs at scale inside Paypal. Summary of the aspect covered follows:

- API Performance and SLOs
- Drivers for Customer Experience
- SLO for APIs
- Metrics
- Measurement
- Monitoring

[Video recording (42 minutes)](https://drive.google.com/open?id=1DR6z103Q1YU589euhz1BCcd8YXCWD5k1)


### 2018-12-03
*Participants: Madhurranjan Mohaan (Google), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

In this meeting Madhurranjan presented his global point of view about SLAs in APIs:

Introduction of the concepts:

Technical concepts:
- **SLO**: Service Level Objective (promise to users, expected limit values)
- **SLI**: Service Level Indication (real measure in the system at a given point in time for a set of users)

Business concepts:
- **SLA**: Service Level Agreement (business contract associated with an API as an *aggregation of services* with specific SLOs and prices)

#### Material
 - [Audio of the call](https://drive.google.com/open?id=17zDfDFmZw8IF_JhWtW7L2qWUofPEkguI)
 
### 2018-11-07
*Participants: Nikhil Kolekar (Paypal), Madhurranjan Mohaan (Google), Isaac Hepworth (Google), Scott Ganyo (Google), Kin Lane (API Evangelist), Mike Ralphson, Jeffrey ErnstFriedman (Linux Fundation), Pablo Fernandez (ISA Group), and Pedro J. Molina (Metadev & ISA Group)*

Pablo Fernandez:
- Presented the global perspective of the SLA4OAI specification including a foundational manifest, the current initial draft and the potential roadmap to follow. 

Presentation of different members and feeback:

Kin Lane: 
- Keep it modular and separate aspects: SL Objectives, Plans, Metrics, etc. (decoupled)
- Aspects than can be referenced externaly for different concerns
- Relation to API Licenses

Nikhil Kolekar:
- Paypal working in SLA for 3 years
- Focus on SLO (Objectives): response times, latencty as warranties.
- Proposes studing different cases on Service subscription (depending on roles) and classes of services

Madhurranjan Mohaan: 
- Experience on Apigee + Google
- Identify roles involved: api developers, api managers, operations, consumers
- Service Level: Indications, Objectives and Agreement
- Grouping levels and use cases:
    - Simple services: SLI and SLO
    - Group of services: SLA as an combined contract
- Declarative SLI and SLO
- Runtime measuring + integrating with alerting tools
- Identify roles and use cases for each role

Mike Ralphson:
- Keep separate concerns and modular

Pedro J. Molina:
- Call to action:
    - Goal define a neutral extension for SLA usable by the industry
    - Enroll anyone interested
    - Define scope, be pragmatic, keep it as siple as possible


#### Material
 - [Video of the call](https://drive.google.com/open?id=1R7TNYZQruRXmaIJuREls9lRslapptNFY)
 - [Slides](https://drive.google.com/open?id=1sBjd8FR4zVqF5wYBzvnWrpncCmO2AJv1)



