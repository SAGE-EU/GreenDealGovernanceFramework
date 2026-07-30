# Data Models

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering the WP5 working group. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

## Role of data models in the GDDS&#x20;

Within the GDDS, data models will form the backbone of semantic interoperability by providing a shared conceptual understanding of data exchanged between participants. A data model provides the semantic “dictionary” for a data product or service, defining data elements, their relationships, and their meaning. Using shared or compatible data models allows data providers and consumers to “speak the same language” when exchanging information — essential for avoiding misunderstandings, enabling automated processing, and ensuring that data from multiple sources can be combined meaningfully.&#x20;

Following the DSSC Blueprint, different abstraction levels of data models can be distinguished, including vocabularies, ontologies, application profiles, metadata schemas, and data schemas. In this context, it is important to differentiate between metadata schemas and actual data models. Metadata schemas primarily describe datasets, data products, services, and other digital assets — providing information such as provenance, ownership, quality, licensing, or access conditions — whereas data models define how the actual domain data is represented and structured, including its concepts, attributes, relationships, units, classifications, and constraints. Without a clear modelling layer, technical interoperability alone is insufficient, as data may be syntactically exchanged but semantically misunderstood or misused.&#x20;

## Heterogeneity of semantic practices across domains&#x20;

The SAGE use cases reveal a high degree of heterogeneity across the Green Deal domains they cover, both in terms of data modelling practices and semantic maturity. Some domains rely on well-established international or European standards (for example, geospatial and Earth observation-driven use cases based on INSPIRE, ISO 19115/19139, CF‑compliant NetCDF, or STAC), while others use sector‑specific models, proprietary schemas, or informal conventions with limited standardisation. Moreover, even in cases where semantic approaches are applied, these are predominantly focused on the metadata layer, supporting the description and discovery of datasets and services, while only a limited number of initiatives employ domain data models to semantically represent and structure the actual operational data, e.g., via standard-based information models like AIM and GDIM (for agriculture and Green Deal).&#x20;

Such heterogeneity reflects the multidisciplinary nature of the Green Deal ecosystem and should be regarded as an inherent characteristic rather than a limitation. The role of the GDDS is therefore not to eliminate diversity, but to enable interoperability across heterogeneous semantic ecosystems.

In several use cases, such as forestry and soil circularity, the core semantic units are domain‑specific operational concepts (e.g. forest stands, field plots, soil batches) that are essential for correct interpretation and decision‑making, yet are only partially standardised or harmonised at European level. For example, existing standard-based initiatives and domain models already provide foundations for semantic interoperability in some of these areas, including AIM (and its base domain models – INSPIRE/FOODIE, Agri SmartDataModels SAREF(4AGRI)), or GloSIS for soil information. In other domains, including textiles traceability and Digital Product Passports, semantics are structured around event‑based transaction models and identifiers that evolve rapidly alongside regulatory initiatives. As a result, semantic alignment is often achieved only at application level through internal harmonisation rather than through broadly adopted shared ontologies or vocabularies. This also highlights the potential role of the data space in providing value-added semantic interoperability services, enabling the harmonisation and transformation of exchanged data across heterogeneous models and standards. Lastly, shared semantic data models also improve machine interpretability, enabling advanced analytics, AI-driven applications, and cross-domain data integration.

## Federated and layered semantic approach&#x20;

Given this diversity, the GDDS will not impose a single, global data model. Instead, it will adopt a federated and layered semantic approach. Under this approach, GDDS encourages the reuse of existing, recognised domain standards wherever they are sufficiently mature and adopted, including international, European, or sectoral specifications. Examples include geospatial and environmental standards, supply chain and product traceability models, emissions accounting frameworks, and health or biodiversity classifications where applicable.&#x20;

Where no widely adopted standard exists, participants may continue to use domain specific or local models if these are clearly documented, versioned, and referenced in the metadata of the published data product. This reflects the use case reality, where forcing premature harmonisation would hinder participation and reuse rather than enable it. Where different semantic data models coexist, semantic interoperability may be achieved through explicit mappings, alignments, and transformation rules rather than requiring harmonisation towards a single common model. GDDS therefore encourages the publication and reuse of semantic mappings to facilitate cross-domain interoperability, reduce integration effort, and support the gradual convergence of semantic artefacts.

Moreover, following best practices and previous experiences, our data space concept also encourages an incremental model towards a full semantic integration based on the pay-as-you-go (PAYG) data management approach[ \[1\].](#user-content-fn-1)[^1] Inspired by Tim Berners-Lee's 5-star Linked Open Data deployment scheme, which helps data publishers assess the extent to which their datasets conform to Linked Data principles, the PAYG model provides a pragmatic maturity path towards progressively richer semantic interoperability. It offers flexibility by reducing the initial cost and barriers to joining the data space. The more the investment made to integrate with the support services, and the standards used to describe aspects of semantics in different services, the better (faster, cheaper, more robust, repeatable and transparent) the integration achievable in the dataspace. The five levels (and stars) of the model include: <br>

1\. Basic (minimum): data source is published in the data space with limited or no integration with support services.&#x20;

2\. Machine-readable: the data source publishes data in a machine-readable format. This enables services to provide a minimal level of support with basic functionality (e.g., browsing the data) where available basic interfaces are exposed.&#x20;

3\. Basic integration: the use of a non-proprietary (data) format and machine-readable metadata enables support services to provide essential services at the data-item/entity level with support for simple functionality (e.g., keyword search).&#x20;

4\. Advanced integration: the data is integrated with most support service features (e.g., structured queries) with an awareness of its relationships to other data sources, participants with basic support for federation.&#x20;

5\. Full semantic integration: the data is fully integrated into the support services (e.g., question answering) and linked to relevant participants. It plays its full role in the global view of the data space.&#x20;

The advanced integration and full semantics layers are both covered by the semantic interoperability aspects, where there is an agreement on the use of open standard formats, data models and APIs.&#x20;

## Declaration and transparency of semantic artefacts&#x20;

Crucially, semantic interoperability in GDDS is achieved not by enforcing uniform models, but by enabling semantic transparency and alignment. Each GDDS data offering shall explicitly declare the data model(s), vocabularies, code lists, or classifications used, as applicable and available, together with references to their authoritative definitions,  including their versions where applicable. &#x20;

Moreover, as proposed by the DSSC blueprint, based on the governance of the data space, data model providers supply these data models, where the data models are published and (potentially) stored in a vocabulary service that enables data models to be discovered throughout a data space. At the time of the data exchange, there should be a reference to the particular data model in the vocabulary service. The Vocabulary Service may host semantic artefacts directly or reference authoritative external repositories maintained by recognised standardisation bodies or domain communities.

This requirement allows other participants, intermediaries, and value-added service providers to assess semantic compatibility, perform mappings where needed, and build cross‑domain applications without ambiguity. For example, emissions related use cases require explicit references to calculation methodologies and classifications to make datasets comparable, while environmental valuation use cases depend on clearly declared ecosystem service classifications to support reuse and aggregation.&#x20;

{% hint style="warning" %}
_To note: Governance consideration: the Vocabulary Service concept is established here, but the governance authority responsible for managing, approving, and evolving models in the service remains unassigned. WP4 to define which body holds this responsibility and what the admission process for new models is._
{% endhint %}

## Levels of semantic abstraction and evolution&#x20;

Following the incremental approach described above, the GDDS will support multiple levels of semantic abstraction, ranging from lightweight vocabularies and code lists, through application profiles and schemas, to fully formalised ontologies where appropriate. Transitions between these levels are expected and supported, allowing participants to progressively increase semantic interoperability maturity according to their needs and capabilities. For example, a dataset described using controlled vocabularies may still be exchanged in formats such as JSON, CSV, or NetCDF, while higher-level semantic relationships can be captured through metadata, documentation, or semantic annotations. In more advanced scenarios, these relationships may also be formally represented using fully fledged ontologies and semantic data representations such as JSON-LD or RDF. Multiple abstraction levels are complementary rather than mutually exclusive and may coexist within a single data offering.

From a governance perspective, data models used within GDDS will be treated as living artefacts. Models evolve as domains mature, policies change, or new use cases emerge. GDDS will, therefore, promote explicit versioning, change documentation, and lifecycle management of semantic artefacts. Rather than centralising modelling authority, governance will focus on ensuring that models are discoverable, reusable, interoperable, referenced consistently, and aligned — where necessary — with cross‑domain and cross‑data‑space interoperability requirements. This approach will enable GDDS to remain flexible and inclusive while still supporting scalable interoperability across Green Deal domains.&#x20;

{% hint style="warning" %}
_Note: Governance consideration: a change management SOP for semantic artefacts has been identified as a required operational document (see also WP4 planning and sections above). This includes the procedure for requesting model updates, approval authority, backward compatibility obligations, and communication to affected participants._
{% endhint %}

[^1]: &#x20;Curry E. (2020) Fundamentals of Real-time Linked Dataspaces. In: Real-time Linked Dataspaces. Springer, Cham
