# Identity, Authentication and Authorisation (IAA) Services

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP6, WP7, WP4, and the Techie group, including inputs from T3.1 - GDDS Trust Framework and AAI Federation. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._ &#x20;
{% endhint %}

{% hint style="info" %}
_The terms 'Intermediaries', 'Intermediary ', and 'Operator(s)' are currently being re-evaluated within the Consortium after multiple feedback items were received from stakeholders on the ambiguity of these terms._ \
\
_After the evaluation, definitions will be added to the Glossary, and the Framework sections will reflect those._&#x20;
{% endhint %}

**Identity, Authentication and Authorisation** are delivered in the GDDS as a shared, operational function of the data space. They enable participants to be identified, authenticated, and authorised across organisational and national boundaries without each participant having to establish bilateral trust with every other: a participant admitted once is recognised throughout the data space, and access and usage decisions are made enforceable at the point of data exchange. This is what makes federated, sovereignty-preserving data sharing possible at scale.&#x20;

The service covers the full lifecycle of digital identities for both natural persons (for example researchers, citizen scientists, and data stewards) and legal entities (for example participating organisations and data providers), from registration and onboarding, through authentication and authorisation, to the renewal and revocation of credentials.&#x20;

Operationally, the function is delivered through four services, provided by the intermediaries and operators that sustain the trust fabric of the GDDS:&#x20;

* the Onboarding Portal, the participant-facing service that guides registration, collects the information required for admission, and, once a participant is approved, registers it in the Participant Registry;&#x20;
* the Participant Registry, the authoritative record of participants, their roles, and their status, which lets any two parties validate each other's legitimacy before a transaction and which serves as the trust-anchor component of the data space;&#x20;
* the Authorisation Registry, which holds the access rights that data providers set over their resources and evaluates, at the point of exchange, whether an authenticated participant may perform the requested action; and&#x20;
* authentication through trusted identity providers, which verifies the identity of participants and users.&#x20;

A defining feature of the model, adopted from the iSHARE Trust Framework, is that identification and authentication are handled separately from authorisation: identity is established once, while access rights are managed and evaluated separately at the point of exchange. It is useful to distinguish three authentication contexts: the admission of a participant, which is an organisational verification carried out at onboarding; human-to-machine authentication, where a person acts through a browser or application; and machine-to-machine authentication, where systems interact without human involvement.&#x20;

The Identity Providers, Authorisation Registries, and Participant Registries that provide these services are defined as functional roles, some of which are certified roles, under Trust and Participation Governance and the Conformity Framework and Governance Enforcement. The participant-facing lifecycle that the service supports, that is identification, onboarding, credential issuance, and revocation, is governed under Trust and Participation Governance.&#x20;

The technical architecture and trust mechanisms that underpin this service, namely identity and attestation management, authentication and federation standards, access-control and authorisation models, and the federation, trust, and security mechanisms, are specified in the Technical Framework (see Data Sovereignty and Trust), and their first-version implementation is documented in D3.1 (WP3), Section 3.1. This Operational Framework section describes only the service and the roles that provide it.&#x20;
