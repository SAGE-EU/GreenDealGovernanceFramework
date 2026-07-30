# Publication and Discovery

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Publication & Discovery capability enables providers of data and services to expose their offerings (with metadata, terms, and access conditions) and make them visible to other data space participants. Consumers, in turn, use this capability to search, identify, and request access to offerings that best fit their needs. The capability supports both human-oriented discovery through portal interfaces and machine-to-machine discovery through standard APIs.

In the Green Deal Data Space (GDDS), this capability is central for creating transparency and trust between stakeholders. It ensures that:

* > Providers can effectively showcase datasets, services, and tools.
* > Consumers can discover offerings aligned with their technical, legal, and sustainability needs.
* > The catalogue mechanism _(centralised, decentralised, or hybrid)_ balances openness with controlled access, reflecting governance rules.

It directly contributes to **Article 33 of the EU Data Act** (interoperability, discoverability, and accessibility of data spaces).

***

## Catalogue architecture and implementation&#x20;

The GDDS Catalogue is implemented as a modular web application: a Python FastAPI backend and an Angular frontend, supported by Apache Solr as the search engine and a PostgreSQL database. Metadata records are retrieved from the Federated Catalogue API and synchronised into the search index through a dedicated transformer service (also implemented in Python using FastAPI), which ensures a consistent metadata structure and efficient indexing. This architecture enables scalable ingestion, fast querying, and flexible filtering of metadata across multiple catalogues. The Catalogue is based on the CYFRONET technical solution.&#x20;

The Catalogue integrates with the Federated Catalogue: on selecting a dataset, the user is redirected to the Federated Catalogue dashboard for detailed metadata and to initiate access negotiation and data transfer.&#x20;

## Federated authentication and single sign-on&#x20;

The integration of the iSHARE Trust Framework components enables federated authentication via trusted identity providers (for example, based on Keycloak) operated by or on behalf of organisations registered within the data space. This provides users with a single sign-on experience, allowing them to authenticate once and move between the Catalogue portal and the Federated Catalogue dashboard without repeated logins, while maintaining adherence to the GDDS trust and identity-management principles. The identity, authentication, and trust mechanisms upon which this relies are specified under[ Data Sovereignty & Trust ](../12-data-sovereignty-and-trust/)(Identity & Attestation Management; Trust Framework).&#x20;

{% hint style="warning" %}
_Note: This content was relocated from the Operational Framework (Catalogue and Data Brokerage Services) per the agreed structure, so that the federation-level service description remains in the Operational Framework and the technical architecture resides here. The iSHARE Trust Framework integration was in progress at the time of writing; status to be confirmed.  Per D3.1 (WP3, §3), authenticated, attribute-based filtering of the datasets displayed to a user is not included in the MVP1 minimum feature set; the single sign-on experience described here reflects the target state foreseen for MVP2._
{% endhint %}

{% hint style="warning" %}
_Open governance questions to resolve (raised by a participant): who operates and maintains the catalogue, during the project and in the longer term; and what rules apply to metadata standards, including quality assurance and validation against GDDS-defined schemas. The operator/maintenance question is a governance matter for Registry and discovery governance (Data Sovereignty & Technical Governance, subsection 4); the metadata-standard rules link to Data, Services and Offerings Descriptions. Owner: WP3, with WP4 for the governance rules._&#x20;
{% endhint %}
