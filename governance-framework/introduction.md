# Introduction

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering the WP4 Governance working group. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._ &#x20;
{% endhint %}

The Governance Framework defines how the GDDS is governed, by whom, and under which rules. It also serves as a foundation of the GDDS, defining its governance bodies, decision-making processes, and participation lifecycle management mechanisms. Together, these elements provide the structure necessary to ensure accountability, trust, and coordinated collaboration across the data space, yet are able to adapt as the GDDS matures and requirements change.

For this reason, the Governance Framework comprise:&#x20;

1. The Governance Playbook, which describes the governance model, decision-making bodies, and lines of authority,&#x20;
2. The GDDS Rulebook, which operationalises the overall Governance framework, covering Trust & Participant Governance, the Conformity Framework & Governance Enforcement, Data Sovereignty, and Technical Governance.&#x20;
3. [_Rolebook - TBD - see specific page for this_](#user-content-fn-1)[^1]

{% hint style="info" %}
_The current GDDS Governance Framework has been developed through an iterative co-creation process, drawing on insights from the GREAT project, governance models from other European data spaces, and continuous input from SAGE consortium partners and external stakeholders. The GDDS Governance Framework is conceived as an evolving structure, capable of adapting as the data space matures while maintaining clear responsibilities for strategic direction, operational execution, stakeholder participation, and independent oversight._
{% endhint %}

{% hint style="warning" %}
Readers seeking to understand participants’ rights and obligations, the governance bodies, and how the rules are maintained and enforced should consult this section.
{% endhint %}

To further orient readers, this section introduces a layered view of governance, helping readers first understand key governance design principles, based on relevant research, and then synthesising those principles into governance requirements: how it can be structured and what it should enable, before describing the individual governance components in detail. See next section.&#x20;

***

### **LAYER 1 - Governance Design - Principles for the GDDS —  how governance must be designed**&#x20;

This section summarises governance principles derived from research and analysis of existing European data space initiatives, governance frameworks, and reference models. It provides design guidance for the GDDS Governance Framework and informs the evolution of governance structures from the project phase (MVP1) to the operational phase (MVP2).&#x20;

These principles do not prescribe a fixed organisational structure. Instead, they define foundational requirements and constraints that ensure the GDDS governance remains trustworthy, interoperable, inclusive, and sustainable over time.&#x20;

They align with the overall GDDS core Values and Ethical Principles as identified in Deliverable 9.8, and described in the [GDDS Mission, Vision, Values section.](../#core-values) &#x20;

<details>

<summary><strong>Principle 1 – Governance is Foundational Infrastructure</strong></summary>

Research across multiple European data spaces consistently shows that governance is the foundational infrastructure of a data space. Governance and the defined policies outline who is allowed to do what, under what conditions data can be shared, trusted, and reused, who decides and who enforces, what is mandatory and what is optional, and, lastly, enable coordination across legal, technical, business, and operational dimensions. This ensures the long-term sustainability of a data space, the accountability of its participants, as well as inclusivity and accessibility for new stakeholders.&#x20;

Governance therefore:&#x20;

* precedes and enables technical implementation,&#x20;
* provides predictability and trust for participants,&#x20;
* balances innovation with accountability, and
* ensures alignment with European Green Deal objectives.&#x20;

</details>

<details>

<summary><strong>Principle 2 – Multi-Layer Governance is Essential</strong></summary>

All mature data space initiatives adopt a multi-layer governance approach, recognising that no single governance level can address all needs. This is aligned with the principle of Transparency and ultimately contributes to fostering the accountability of the data space and its participants.

The GDDS governance framework is therefore expected to operate across clearly distinguished layers, including:

* a cross-data-space layer to enable interoperability and cross-data-space alignment,
* a data space-wide governance layer to maintain FAIR principles across participants, as well as participant rules and obligations, to preserve accountability,
* domain or use-case-specific governance, to give use cases the ability to adopt specific rules and obligations that allow their own use cases to achieve their objectives
* and participant-level rules and obligations that all must adhere to, which enhances trust and accountability eventually.

Each layer has a distinct purpose and scope. The allocation of decisions across these layers is addressed in Principle 3.

</details>

<details>

<summary><strong>Principle 3 – Subsidiarity by Design</strong></summary>

Building on the layered structure established in Principle 2, subsidiarity determines at which layer a given decision is taken. Decisions should be taken at the lowest competent level, closest to where data is used, and value is created.

Ideally:

* domain- or use-case-specific decisions are handled at domain level,
* data space-level governance intervenes only when cross-cutting impacts exist, such as limits on scalability or extensibility,
* escalation paths, in the event of conflicts or incompatibility, are explicit and predictable.

Subsidiarity supports scalability, respects data sovereignty, and prevents governance bottlenecks (e.g. the delays that arise when too many decisions must be escalated to a single central authority for approval).

</details>

<details>

<summary><strong>Principle 4 – Governance Authority Must Be Clearly Scoped</strong> </summary>

Research highlights the importance of distinguishing between:&#x20;

* legal existence (legal entity),&#x20;
* decision authority (governance authority),&#x20;
* and operational execution (operating entity).&#x20;

Ideally:&#x20;

* governance authority is defined explicitly by mandates and rules, not by legal form alone, to maintain accountability,&#x20;
* multiple governance authorities may coexist with delegated scopes, for example governing separate use cases, while compatible with overarching data space governance,
* operational entities execute decisions but do not define governance (they do not make the rules — law enforcement vs. the justice system).&#x20;

{% hint style="info" %}
_Note: the usual definition of federation, in a political context, is that certain topics are the responsibility of one level of government (e.g. education for German Länder), while other topics are the domain of the federal government (e.g. defence for the Bundesrepublik). There are corresponding sets of enforcement bodies and justice systems._
{% endhint %}

Clear scoping of authority prevents overlap, conflicts of interest, and ambiguity for participants.&#x20;

</details>

<details>

<summary><strong>Principle 5 – Separation of Governance and Operations</strong></summary>

A consistent best practice across data spaces is the separation of governance from operations.&#x20;

Governance bodies:&#x20;

* define rules, roles, and decision rights, &#x20;
* oversee compliance and evolution,&#x20;
* safeguard trust and accountability.&#x20;

Operating entity:&#x20;

* runs technical infrastructure, maintaining, as much as possible, privacy and data protection,&#x20;
* supports onboarding by promoting inclusivity and non-discriminatory service delivery,&#x20;
* implements governance decisions.&#x20;

This separation enables professional operations and avoids concentration of power.&#x20;

</details>

<details>

<summary><strong>Principle 6 – Trust Frameworks Are Non-Negotiable</strong></summary>

Trust is a prerequisite for data sharing at scale. Research confirms that trust must be addressed through both technical and operational mechanisms and governance processes.&#x20;

A data space governance framework must define:&#x20;

* roles and responsibilities related to trust, to maintain accountability &#x20;
* criteria for participant eligibility, fairly and inclusively,&#x20;
* mechanisms for identity, credentials, and verification,&#x20;
* compliance monitoring (in particular, in the area of privacy and data protection) and enforcement procedures (to maintain accountability)&#x20;

Eventually, trust frameworks defined for different data spaces could be aligned to enable a cross-data space trust framework, which would then form the basis for cross-data space data sharing and interoperability.

</details>

<details>

<summary><strong>Principle 7 – Rulebooks Are the Core Governance Instrument</strong></summary>

Across European data spaces, the "Rulebook" has emerged as the key governance artefact.&#x20;

The Rulebook for each data space:&#x20;

* consolidates legal, organisational, and technical rules and components,&#x20;
* defines mandatory versus optional requirements,&#x20;
* assigns rights, obligations, and decision powers,&#x20;
* evolves through formal, transparent change processes.&#x20;

Effective Rulebooks are modular, versioned, and designed to accommodate future evolution without undermining trust.&#x20;

</details>

<details>

<summary><strong>Principle 8 – Inclusivity and Legitimacy Are Governance Requirements</strong></summary>

Research and SAGE's own agreed principles emphasise that governance must enable:&#x20;

* Inclusivity of diverse participant types (public, private, SMEs, research),&#x20;
* Fair and balanced representation in decision-making to avoid dominance by single actors, and as much as possible inclusion of those affected by decision-making in decision-making processes,
* Transparency in decision-making,&#x20;
* Accountability toward broader societal objectives.&#x20;

Governance legitimacy is as important as governance efficiency, especially for public-interest data spaces such as GDDS.&#x20;

</details>

<details>

<summary><strong>Principle 9 – Governance Must Be Evolutionary</strong></summary>

Governance is not static. As the data space matures and its membership, needs and technologies change, its governance evolves through phases:&#x20;

* from formation and experimentation,&#x20;
* to operation and scaling,&#x20;
* to consolidation and long-term sustainability.&#x20;

Research warns against over-engineering governance too early or locking structures prematurely. Instead, governance frameworks should explicitly support:&#x20;

* iterative refinement,&#x20;
* periodic review,&#x20;
* structured transition between lifecycle phases.

</details>

#### Implications of Layer 1 Principles for the GDDS Governance Framework&#x20;

Based on research, the GDDS Governance Framework should:&#x20;

* adopt a multi-layer, subsidiarity-based model,&#x20;
* clearly distinguish governance authority from operations,&#x20;
* embed trust as both a technical and governance concern,&#x20;
* rely on a modular, evolving Rulebook,&#x20;
* ensure inclusive and legitimate decision-making,&#x20;
* explicitly support governance evolution over time&#x20;

These principles provide a research-validated foundation for the GDDS governance model and guide its implementation and evolution.&#x20;

### **LAYER 2 – Governance Capabilities defined in GDDS — what governance should enable**

The GDDS governance framework must enable a defined set of capabilities across its ecosystem. These capabilities reflect the consolidated requirements of the GDDS Use Cases (WP6), GDDS Process Requirements and suggestions from the SIMPL Feasibility study\*. They establish what governance must make possible in practice, spanning authority, participation, roles, trust, data sovereignty, and compliance.&#x20;

{% hint style="info" %}
_\*Note: Reference to these cannot be shared as they are internal sources. IN case they become available publicly, they will be referenced here._&#x20;
{% endhint %}

<details>

<summary><strong>Capability 1 - Organisational Form and Governance Authority</strong></summary>

Governance must enable the GDDS to operate under a dual-entity model, in which a governance authority sets and oversees the rules and an operating entity executes them, together holding the mandate and capability to:

* Define and approve the GDDS Rulebook (governance authority) and enforce it and configure the identity and trust infrastructure (operating entity).
* Manage the full participant lifecycle (onboarding, review, acceptance, compliance, revocation, suspension), including legal agreement to comply with the GDDS Rulebook.&#x20;
* Manage the full lifecycle for credentials (issuance, renewal, revocation, suspension).&#x20;
* Maintain control over accepted data models and vocabularies.&#x20;
* Support interoperability with external data ecosystems (e.g. EOSC, Copernicus, Gaia-X, etc).&#x20;
* Accommodate domain-level governance within the structure, namely the Data Sharing Group Orchestrators (DSGOs) and use-case facilitators that exercise delegated governance for their domain under subsidiarity (see Layer 1, Principle 3), without prejudice to the central governance authority.
* Define and oversee monetisation models, including centralised payment and settlement mechanisms.&#x20;

</details>

<details>

<summary><strong>Capability 2 - Participation Management, Onboarding and Admission</strong></summary>

Governance must enable a structured, trustworthy participation lifecycle, including the ability to:&#x20;

* Gather candidates' evidence of compliance with the rules of participation during onboarding.&#x20;
* Allow candidates to request membership in one or more Data Sharing Groups.&#x20;
* Notify participants upon acceptance and issue the necessary membership credentials (in the GDDS, in any data sharing groups).&#x20;
* Recognise participant identities, enabling controlled data discovery before transactions.&#x20;
* Onboard holders of specialised or sensitive datasets in a way that protects the data and empowers its providers.

</details>

<details>

<summary><strong>Capability 3 - GDDS Roles, Rights and Responsibilities</strong> </summary>

Governance must establish a clear and enforceable taxonomy of roles and associated rights, enabling the GDDS to:

* Allow participants to take multiple roles like Data Provider, Consumer, Service Provider, etc.
* Allow participants to control the visibility of their own presence and their assets in the data space.&#x20;
* Ensure that when a data provider revokes or materially changes access to a resource, affected recipients are reliably informed.
* Enable consumers to access data processing and value-added services offered by Service Providers, under defined access conditions.
* Ensure controlled and timely data access for data consumers based on their agreement to data access and usage policies set by data providers.&#x20;
* Require providers to declare and document the interfaces through which their data is made available, and to favour standardised interfaces where possible.

</details>

<details>

<summary><strong>Capability 4 - Trust, Authentication and Authorisation</strong> </summary>

Governance must establish the conditions under which participants are authenticated, authorised, and trusted, enabling the GDDS to:&#x20;

* Enforce secure authentication and role-based access control (RBAC) across participant types.&#x20;
* Enable data providers to retain control over visibility, access and usage rights for their data products.&#x20;
* Authenticate public organisations through the standard onboarding process.&#x20;
* Facilitate access by financial institutions to ecosystem service and natural capital evaluations.
* Enforce trust conditions established at onboarding throughout the participation lifecycle.&#x20;

</details>

<details>

<summary><strong>Capability 5 - Certification and Conformity Framework</strong> </summary>

Governance must define and oversee a conformity regime, ensuring all participants and data products meet applicable legal, technical, and ethical standards, enabling the GDDS to:&#x20;

* Ensure compliance with EU data governance regulations (DGA, Data Act, GDPR, INSPIRE, Open Data Directive).&#x20;
* Support validation of data products against registered reporting and data standards.  ESG and CSRD reporting (UC9, UC4) are examples of such standards.
* Enforce GDPR compliance for internal data flows, including those involving personal data.&#x20;
* Apply personal data protection requirements to health-sensitive data (GDPR, EHDS).&#x20;

</details>

<details>

<summary><strong>Capability 6 - Data Sovereignty and Technical Governance</strong> </summary>

Governance must align technical mechanisms with governance rules, ensuring the GDDS can:&#x20;

* Apply access policy filters to discovery queries based on data consumer attributes and/or credentials.&#x20;
* Maintain full and auditable, yet securely held, logs of data publication, access, and transaction events.&#x20;
* Support multiple licensing models (e.g. open, research-use, commercial) with enforcement.&#x20;
* Provide GDDS-level licence templates and a reference library for data holders.&#x20;
* [Enable data providers and rights holders to selectively share and to delegate specific access and usage rights to nominated parties. ](#user-content-fn-2)[^2]
* Support granular, tiered access control (RBAC/ABAC) at the data-product level.&#x20;
* Track data usage by participant and, where applicable, by declared purpose.&#x20;
* Ensure licensing and usage rights are clearly defined, accessible, and consistently applied.&#x20;
* Standardise how providers declare data refresh frequency, latency, and timeliness, so that consumers can assess fitness for purpose (handled in the same way as data quality).
* Require providers to declare and document the interfaces through which their data is made available, and to favour standardised interfaces where possible.
* Guide access and usage policies toward common, reusable patterns and templates rather than bespoke rules. Where standard policies are insufficient (for example geofence-based rules), provide a governed process to extend the policy-template library and its corresponding technical implementations, drawing on approaches that link ODRL statements to concrete technical enforcement (for example geo-anonymisation techniques).

</details>

***

### Alignment with the overall GDDS Mission, Vision, and Values&#x20;

The GDDS Governance Framework operates in alignment with the overarching GDDS mission, vision, and values, which define the purpose, ambition, and societal objectives of the Green Deal Data Space as a whole. See more [here ](../#gdds-mission-vision-values)on this topic.&#x20;

While the definition and evolution of the GDDS mission and vision are addressed at the data space level through cross-work-package collaboration (including business, ethical, social and sustainability perspectives), the Governance Framework ensures that governance structures, decision-making processes, and operational practices remain consistent with these shared objectives.&#x20;

[The Governance Authority is responsible for monitoring alignment between governance decisions and the GDDS mission and vision, and for triggering formal review processes when external policy developments (e.g. changes in European Green Deal priorities) require reassessment. ](#user-content-fn-3)[^3]

[^1]: There is the GDDS Rolebook that is considered to be developed. This would be a companion document to the Green Deal Data Space (GDDS) Rulebook. Where the Rulebook establishes the overall governance structure, legal framework, and participation lifecycle, the Rolebook operationalises those rules into role-specific playbooks. _(TBD – not yet final)_

[^2]: Note: Rights are expressed at the offering and catalogue level (for example in ODRL) and, at runtime, are backed by verifiable delegation evidence (for example iSHARE delegation evidence) so that a party acting on another's behalf can prove its authorisation. This complements, and sits above, the access-control mechanisms (RBAC/ABAC) in the bullets below.

[^3]: Is it the DSGA in collaboration with the Ethics Committee?&#x20;
