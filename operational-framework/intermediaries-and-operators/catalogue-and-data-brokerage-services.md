# Catalogue and Data Brokerage Services

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP6, WP7, WP4, and the Techie group, including inputs from T3.2 on GDDS Catalogue, Marketplace and Registries,_ _Task 3.4 on value-added services. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._ &#x20;
{% endhint %}

The GDDS provides a catalogue portal that supports dataset discovery across the ecosystem. It offers a unified search interface, with advanced filtering and faceted search that let users refine queries across multiple criteria, including restricting results to selected underlying catalogues. By exposing harmonised, standardised metadata and supporting structured navigation across federated resources, the catalogue improves the visibility and accessibility of datasets and reduces fragmentation between catalogue services.&#x20;

Behind the portal, the Federated Catalogue provides the federated view: it gathers the metadata published by participants across the data space into a single, up-to-date catalogue that the portal presents to users, so that data distributed across many participants can be found in one place without being centralised. A companion Participant Discovery service lets a user find and select the participant they belong to, and serves as the entry point to authentication.&#x20;

On selecting a dataset, the user is directed to the relevant dashboard, where the detailed metadata and the applicable usage policies can be reviewed and where access negotiation is initiated in accordance with the GDDS governance frameworks. Access to data found through the catalogue is therefore never automatic: discovery leads to a governed access decision, applying the access and usage conditions set under Data Sovereignty and Technical Governance, after which the data itself is exchanged between the provider's and the consumer's Data Connectors in a sovereignty-preserving manner.&#x20;

Through these capabilities, the catalogue reinforces the role of intermediaries in the GDDS: it facilitates trusted data discovery, supports efficient access brokerage, and promotes interoperability across distributed data services, contributing to a more integrated and user-centric data-sharing environment.&#x20;

The technical architecture of the catalogue, its integration with the Federated Catalogue, and the federated authentication that enables single sign-on across the portal and the catalogue are specified in the Technical Framework (see Data Value Creation Enablers, Publication and Discovery), and their first-version implementation is documented in D3.1 (WP3), Section 3.2. This Operational Framework section describes only the service and the intermediary role it serves.&#x20;
