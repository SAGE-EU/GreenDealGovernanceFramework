---
icon: hands-holding-diamond
---

# Data Space Offering

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP6, WP7, WP4, and the Techie group, including inputs from Task 3.4 on value-added services. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._ &#x20;
{% endhint %}

The GDDS data space offering comprises the data products and services made available through the data space to support use case and/or data sharing group development and deployment, and to create value for participants. Offerings originate at three distinct levels, and the distinction matters for responsibility and governance:

* the **Data Space** provides the enabling layer: the core services (and, in the early operational phase, a limited set of value-added services) that make participation and trusted data exchange possible;
* **individual participants** provide the data products, and may also provide value-added services; and
* **use cases** and/or **data sharing groups** assemble data products and services into use-case-specific configurations that meet their particular needs.

**Data products** are provided by participants and consist of structured environmental and sustainability-related datasets, including but not limited to environmental, spatial, emissions, material-flow, and asset-level data. Providers make these products available in accordance with agreed interoperability standards and governance rules, while retaining the ability to set access and usage conditions that reflect their sovereignty requirements. Encouraging valuable data to be made as widely available as possible, while respecting the conditions providers attach to it, is central to the GDDS offering. Hence, in GDDS, data is not collected in a single, centralised repository. Instead, each participant organisation keeps its own sources of data, which are shared with other participants according to certain established rules that are enforced within the data space. Herein, data are federated through different organisations, and their control remains with the data rights holder. Data sovereignty is a key pillar of the GDDS, as it is important that data providers are able to define access policies: who can access the data, for what purpose and under what conditions, and for how long _(Source D3.1, Section 3)._

***

**The services** in the data space fall into two categories, core services and value-added services, distinguished by their purpose and by who provides them. Core services lower the barrier to making data available and to exchanging it under trusted conditions; value-added services increase the usefulness and market value of data products, for example through semantic linking, analytics, and reporting tools. The GDDS concentrates on providing core services and on encouraging a broad supply of value-added services from participants and third parties.

**Core services** are the essential capabilities required for the data space to function and for data to be exchanged securely and in compliance with applicable rules.  &#x20;

In the MVP1 of the GDDS, these core services are delivered as so-called ‘GDDS Core’ (see Figure below, source: D3.1, Section 3), and they fall into three groups: &#x20;

1. The identity and trust services comprise the Onboarding Portal, which registers and admits participants; the Participant Registry, which holds the authoritative record of participants, their roles, and their status, and serves as the trust-anchor component of the data space; the Authorisation Registry, which manages and evaluates delegated access rights at the point of exchange; and authentication through trusted identity providers. &#x20;
2. The discovery and brokerage services comprise the SAGE Portal, the central access point for participants and end users; the Federated Catalogue, which aggregates harmonised metadata from across the data space for dataset discovery; and Participant Discovery. &#x20;
3. Connectivity is provided through support for participants' Data Connectors, which allow data to be exchanged in a decentralised, sovereignty-preserving manner rather than through a central repository. Hence, participant interoperability is mainly achieved. In the GDDS, any type of Data Connector can be used, as long as it adheres to the contract and protocols required by SAGE. &#x20;

In respect of quality, the role of the GDDS is not to assure the quality of data products directly, but to provide robust and transparent mechanisms through which providers can document quality criteria and certifications, and consumers can judge quality for themselves and select the data that meets their needs. Core services are governed and maintained at the level of the GDDS ecosystem to guarantee a consistent level of trust, interoperability, and regulatory alignment.&#x20;

<img src="../.gitbook/assets/unknown (12).png" alt="Figure 5: Overview of GDDS Core (Source D3.1)" height="369" width="639">

**Value-added services** extend the core functionality of the data space through additional data processing, analytics, and domain-specific applications, for example, data-enrichment tools, analytics solutions, reporting modules, or sector-specific applications. They may be provided by a diverse range of participants, including third-party service providers, which fosters innovation and expands the ecosystem's capabilities. The GDDS may itself provide a limited set of value-added services to support the establishment of the ecosystem, but its primary role is to enable and encourage the participation of external service providers.&#x20;

A first value-added service provided by the GDDS to support the establishment of the ecosystem is the Infrastructure Manager, which helps participants deploy the technical components required to join and operate within the data space in a cloud environment (See D3.1 by WP3, Section 4.4.1). Its most immediate use is the deployment of participants' Data Connectors, but its capability is broader: it can provision cloud infrastructure and install and configure a range of software, including compute clusters and tools such as Kubernetes, Slurm, and Galaxy, across multiple cloud providers. This means the Infrastructure Manager can also give data consumers a place to run the analytics and other services they need, not only support data providers in connecting. &#x20;

A second value-added service developed within the GDDS is hale»cloud, a data conversion and harmonisation service operated by wetransform (See D3.1 by WP3, Section 4.4.2). It performs format conversion, structural transformation, semantic harmonisation, and reprojection of spatial and non-spatial data, enabling participants to integrate heterogeneous datasets into shared GDDS data models without needing to re-engineer their data structures themselves. hale»cloud is built on hale»studio an established open-source ETL tool. Both have been in production use for many years (TRL9). &#x20;

Beyond the services provided by the GDDS itself, several partners have proposed or are developing further value-added services, collected through the Task 3.4 questionnaire and documented in D3.1 (WP3), Section 4.4.3. These include SURF's Secure Analysis Environment (SANE), a secure processing environment following the Five Safes principle; Fujitsu's secure processing environment and integrated data marketplace framework; TOP-IX's Fulcrum Federated Cloud Exchange for sovereign, vendor-neutral resource sharing; and, from PSNC, a data harmonisation service, an Eclipse Dataspace Connector implementation, and an OGC SensorThings API generation service. Their maturity ranges from early prototypes to production-ready services, and the detailed descriptions for the PSNC services are still to be submitted. The GDDS does not operate these services; it enables and encourages their provision by participants and third parties, and their availability will be confirmed as the ecosystem develops.&#x20;

| SURF         | SANE (Secure Analysis Environment)        | IaaS/SaaS secure processing environment (SPE) built on SURF Research Cloud, following the Five Safes principle for working with sensitive data (TRL8).                                                 |
| ------------ | ----------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Fujitsu-BE   | SPE Deployment and Marketplace Framework  | Secure processing environment on dePIN infrastructure with an integrated data marketplace for monetising datasets, AI models and services (TRL6).                                                      |
| TOP-IX       | Fulcrum Federated Cloud Exchange          | Federated cloud service combining the InterCloud Exchange (governance) and the Computing Exchange Market (resource trading/discovery) to enable sovereign, vendor-neutral resource sharing (TRL5).     |
| PSNC         | Data Harmonization Service                | Service for harmonising heterogeneous input datasets into common data models. Detailed questionnaire submission pending.                                                                               |
| PSNC         | Eclipse Dataspace Connector (EDC)         | Connector implementation based on the Eclipse Dataspace Components framework. Detailed questionnaire submission pending.                                                                               |
| PSNC         | OGC SensorThings API Generation Service   | Service to generate OGC SensorThings API endpoints for sensor and IoT data sources. Detailed questionnaire submission pending.                                                                         |
| UPV          | Infrastructure Manager (IM)               | Orchestration tool that automates the deployment of cloud infrastructure and software, including participants' Data Connectors (described in detail in Section 4.4.1).                                 |
| wetransform  | hale»cloud                                | Data conversion and harmonisation service built on hale»studio (TRL9), enabling participants to integrate heterogeneous datasets into shared GDDS data models (described in detail in Section 4.4.2).  |

{% hint style="info" %}
_Note: Further information will be added on the currently mentioned value-added services, as well as some new services that may be added, including semantic transformation and reporting services, since they are still being defined by Working Group 3 under Task 3.4. (Source: D3.1 GDDS first version report (WP3).)_
{% endhint %}

***

**Data products and services** can be combined into packaged offerings, for example a dataset made available through a documented API, or a dataset bundled with a value-added service such as analytics or reporting tool. Packaging of this kind is done by the participant or use case that owns the offering, not by the data space itself. Where a use case builds a complete downstream application on top of data-space resources, such as an end-user dashboard or an integrated domain solution, that application typically sits outside the data space: the data space supplies the data and the enabling services, while the application remains the responsibility of the use case that operates it. Every offering made available through the data space carries a clear statement of its licence, terms of use, and the support the provider commits to; responsibility for that statement rests with the participant offering it, and the governance framework sets the minimum it must contain.

A clearly defined and well-structured data space offering supports usability, legal certainty, and trust, and in doing so supports the adoption and long-term sustainability of the GDDS.

The data products and services introduced here are described in the Operational Framework and the Technical Frameworks, and the rules that govern them, including admission, access and usage policies, and conformity, are set out in the Governance Framework.
