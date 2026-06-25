# Data Exchange

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering the WP5 working group. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Data Exchange building block defines how data is transferred between GDDS participants in a secure, interoperable, and policy-compliant manner. While data models establish shared meaning, data exchange mechanisms operationalise this meaning by enabling datasets, streams, and services to be accessed and used across organisational and technical boundaries.&#x20;

Data exchange in GDDS is understood broadly, encompassing not only bulk dataset downloads but also API-based access, streaming data, event-based updates, and algorithm-to-data or compute-to-data patterns where data movement is restricted. Whatever the mode, the process shall be secure, standardised, and discoverable.&#x20;

It covers both the Data Plane (the actual data transmission) and its integration with the Control Plane (identification, authorisation, policy enforcement, and transaction state management).&#x20;

## Federated data exchange principles&#x20;

GDDS supports a federated data exchange paradigm in which data remains with the data provider or is accessed through provider-controlled infrastructure, unless explicitly agreed otherwise. Exchange mechanisms therefore, integrate seamlessly with identity management, access control, usage policies, and contractual conditions as defined in the Data Sovereignty and Trust section of this Rulebook.&#x20;

Insights from the SAGE use cases show that a single data exchange protocol is neither feasible nor desirable across all Green Deal domains. Earth observation and environmental monitoring use cases rely on large raster products and time series, while supply chain and reporting-oriented use cases are centred on transactional data exchange and controlled sharing between identified partners.&#x20;

## Diversity of exchange patterns in use cases&#x20;

Data exchange in GDDS is understood broadly, encompassing not only bulk dataset downloads, but also API‑based access, streaming data, event‑based updates, and algorithm‑to‑data or compute‑to‑data patterns where data movement is restricted. The SAGE use cases illustrate this diversity clearly: Earth observation and environmental monitoring use cases rely on large raster products and time series, while supply chain and reporting oriented use cases are centred on transactional data exchange and controlled sharing between identified partners.&#x20;

Insights from these use cases show that a single data exchange protocol is neither feasible nor desirable across all Green Deal domains. Instead, GDDS adopts a principle of protocol flexibility with a preferred interoperability baseline, allowing different exchange protocols to coexist while relying on shared governance, identity, metadata, semantic interoperability, and policy frameworks to ensure trusted and interoperable data exchange. &#x20;

Participants are free to use protocols that are appropriate for their domain and data characteristics, provided that these protocols are based on open standards or widely adopted specifications and are properly described in the data product metadata. Beyond generic exchange mechanisms such as REST APIs, GraphQL, or SPARQL endpoints, the GDDS encourages, where applicable, the adoption of domain-relevant standard interfaces and APIs, such as OGC APIs and STAC in geospatial and Earth observation contexts. &#x20;

Moreover, APIs and exchanged data structures should reference the semantic meaning of the exchanged information, enabling participants to correctly interpret and process the data. Therefore, APIs should be linked to corresponding data models, vocabularies, or ontologies describing the semantics of the exchanged content.&#x20;

## Recommended interfaces and semantic linkage&#x20;

To support interoperability and ease of onboarding, GDDS defines a recommended set of exchange patterns and interfaces that participants are encouraged to adopt where possible. These recommendations do not replace domain practices but provide a common interoperability layer that simplifies cross sector access and federation with other European data spaces.&#x20;

All exchange interfaces must be explicitly linked to their corresponding data models so that semantic interpretation is unambiguous. This linkage is particularly important for cross domain reuse, where consumers may not share the same domain knowledge as the original data provider.&#x20;

## Control Plane integration and operational aspects&#x20;

Data exchange within GDDS is tightly coupled to the Control Plane, which handles authentication, authorisation, policy evaluation, contract negotiation, and transaction state management. Before data is exchanged, access and usage conditions are evaluated; during exchange, relevant events are logged to support observability and compliance; and after exchange, usage may continue to be monitored where policies impose ongoing obligations. This is especially relevant for regulated data, restricted datasets, and use cases involving sensitive environmental, commercial, or health related information.&#x20;

From an operational perspective, GDDS may support multiple exchange modes, including pull‑based access, push‑based delivery, subscription and streaming, and parameterised queries (e.g. spatial or temporal subsetting). For example, in a pull-based transfer approach, the data consumer initiates the exchange by requesting or querying data from the provider when needed. The provider exposes APIs, endpoints, or data services, and the consumer retrieves the data on demand. This approach is commonly used for discovery-driven access, periodic retrieval, analytics, and federated querying scenarios. Respectively, in a push-based transfer approach, the data provider initiates the exchange by sending data automatically to subscribed consumers or designated endpoints whenever new data becomes available or specific events occur. This model is typically used for real-time streams, notifications, alerts, event-driven architectures, and continuous synchronisation workflows. Participants are expected to declare supported exchange modalities, versions, and constraints in a machine‑readable way to facilitate automated brokerage and orchestration. Versioning and backward compatibility are essential considerations, as long‑lived Green Deal datasets often evolve over time while remaining in active use.&#x20;
