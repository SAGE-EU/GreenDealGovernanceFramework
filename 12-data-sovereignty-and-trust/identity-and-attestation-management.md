# Identity & Attestation Management

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Identity & Attestation Management building block provides a trusted foundation for onboarding, verifying, and maintaining participants’ credentials within the GDDS ecosystem.

It ensures that every actor and asset is uniquely identifiable, authenticated, and authorized before engaging in data transactions, while preserving sovereignty over identity data.

By combining machine-readable rulebooks, standardized credential formats, and secure exchange protocols, GDDS enables participants to present and verify attestations, such as membership, compliance, or sector-specific qualifications, across multiple domains and jurisdictions.

This capability is essential for:

* > Trust & Compliance – Verifying that participants meet the GDDS baseline requirements and any sector-specific rules.
* > Interoperability – Enabling credential federation across other recognised data spaces and trust frameworks.
* > Efficiency – Reducing onboarding time and transaction costs through reusable, portable credentials.

### **Core Capabilities**

* > Trusted Legal & Natural Person Identification – Support for both organisational and human identities, aligned with EU-recognised schemes (eIDAS, Qualified Trust Service Providers).
* > Secure Credential Lifecycle Management – Issuance, renewal, revocation, and validation of credentials in compliance with GDDS governance.
* > Conformity Assessment Integration – Alignment with the GDDS Rulebook and automated compliance checks.
* > Credential Portability & Federation – Interoperable with other ecosystems through open standards (W3C Verifiable Credentials, DIDs, OIDC4VC).
* > Attestation Diversity – Support for multiple attestation types, including identity, membership, and compliance attestations.

### **Design Principles**

* > Self-Sovereign Identity (SSI) – Allow participants to control their identity attributes while meeting governance requirements.
* > Standards-First Approach – Prioritise open, widely adopted technical and governance standards.
* > Federation over Centralisation – Enable multiple trust domains to coexist with GDDS as the trust anchor.
* > Policy-Linked Identity – Ensure access and usage rights are tied to verified identities.
* > Credential Reuse – Encourage interoperability with existing compliance certifications to minimise duplication.

***

## Technical architecture and components&#x20;

The IAM framework relies on a combination of external and internal components to manage identities, authenticate users and services, and control access to resources across the GDDS. It leverages existing external trusted identity providers to authenticate users acting on behalf of participant organisations and to establish appropriate levels of assurance regarding their identities. In addition, the GDDS uses internal or federated data space registries to manage and validate participant metadata, including status, roles, and entitlements within the ecosystem. These registries support trust establishment and authorisation decisions but are not themselves involved in the authentication process.&#x20;

## Authentication and federation standards&#x20;

To ensure technical interoperability, the GDDS adopts established standards for authentication and federation (for example OAuth 2.0, OpenID Connect, and SAML), allowing users to reuse existing credentials where possible and reducing the duplication of identities:&#x20;

* academic and research users may authenticate via eduGAIN-connected identity providers;&#x20;
* business and government participants may rely on corporate identity providers, eIDAS-compliant identities, or other trusted authentication schemes, depending on regulatory and assurance requirements.&#x20;

The framework follows an evolutionary approach. The GDDS has adopted the Decentralised Claims Protocol (DCP) and Verifiable Credentials (VCs) to support trust, delegation, and authorisation across the data space. These complement the federation-based approaches above, which continue to be used for user authentication and service integration. Access decisions are based on the verification of claims issued by trusted authorities and evaluated against trusted registries and policies, enabling fine-grained delegation and interoperability with emerging European frameworks such as eIDAS 2.0.&#x20;

{% hint style="warning" %}
_Note: This content was relocated from the Operational Framework (IAA Services) per the agreed structure, so that the federation-level service description remains in the Operational Framework and the technical architecture resides here. Further content might be added in line with the developments within the WP3, WP4 group._&#x20;
{% endhint %}

***

## 1.Identity Paths and Credential Enrichment in GDDS&#x20;

### 1.1. Organisational Participants with Their Own Identity Systems&#x20;

Organisations such as municipalities, real estate companies, consultancies, or research labs may wish to participate using their existing identity infrastructure.&#x20;

* These organisations must first register themselves as official participants of GDDS using a recognised organisational identifier (e.g., LEI or other trusted digital IDs).\[Accepted identifiers include: LEI (Legal Entity Identifier), EORI (Economic Operators Registration and Identification), KVK/CoC (Chamber of Commerce registration numbers), national business registry IDs, eIDAS Org ID (Organization Identifier)&#x20;
* \[Minimum assurance level: Substantial (eIDAS), as the primary assurance standard for organisational participants.]&#x20;
* Upon successful registration, the organisation determines which individuals may represent it within GDDS and defines the roles and credentials these individuals will receive.&#x20;
* Organisational representatives may then act on behalf of their entity to:&#x20;
* Manage datasets&#x20;
* Input or extract data&#x20;
* Administer services (e.g. onboarding of sub-participants)&#x20;
* Role-based credentials are assigned internally and can be enriched further via GDDS processes (see Section 4).&#x20;

### 1.2. Academic Participants&#x20;

Individuals working within academic institutions (e.g. universities, applied research centres) may participate via their existing academic credentials, such as institutional logins compliant with eduGAIN or national federation protocols.&#x20;

* \[Note on participant type: Academic participants are classified as Institutional participants for governance purposes. The Academic pathway is an identity/credential pathway available to Institutional participants whose institution provides authentication via eduGAIN or an equivalent national academic federation. 'Academic' is not a separate participant type; the distinction is retained solely at the identity and credential level.]&#x20;
* The level of access will depend on the authentication assurances provided by the institution.&#x20;
* If an academic participant requires higher assurance or greater access rights than their institution offers, they may proceed via the individual pathway (see below).&#x20;

### 1.3. Individual Participants&#x20;

Individuals (e.g. freelancers, private consultants, independent researchers) may:&#x20;

* Access GDDS anonymously — but only to view open resources visible to unauthenticated users.&#x20;
* Use low-assurance digital IDs (e.g. Google, LinkedIn) for limited access, where permitted.&#x20;
* Register using eIDAS 1.0 -compliant digital identities from trusted EU providers. These identities can enable secure and verifiable participation in the data space. \[In future: eIDAS 2.0 wallet-based identities will be supported as they become available. Role-specific attestations (e.g. professional certifications, researcher accreditation) may be required for certain roles and will be accepted where applicable.]&#x20;
* \[Minimum assurance level: High or Substantial assurance is required for full access to restricted data and services. Low assurance limits access to open resources only. Credential enrichment (adding verifiable credentials over time) enables finer-grained permissions as the participant's assurance level increases.]&#x20;

#### 1.3.1 Individual to Institutional Participants&#x20;

An individual participant may begin participation in GDDS under the Individual pathway and subsequently migrate to Institutional participation once their institution is ready to formally join the data space. This upgrade path is relevant, for example, for an academic researcher who initially participates as an individual but whose institution later completes Institutional onboarding.&#x20;

The upgrade process involves the following general steps:&#x20;

1. The institution completes the Institutional onboarding process (see §2 — Onboarding and Admission Procedures), including identity verification under the Organisational or Academic pathway, eligibility assessment, and execution of the participation agreement.&#x20;
2. Once the institution is an admitted Institutional participant, the individual's existing credentials are re-linked under the institutional umbrella, subject to the institution's internal authorisation.&#x20;
3. The individual's roles and access rights are re-evaluated and re-assigned in line with the institution's governance framework and the roles selected by the institution at onboarding.&#x20;
4. Until the upgrade is complete, the individual retains Individual-level access only.&#x20;

{% hint style="warning" %}
_Note: The detailed procedural steps and technical implementation of the upgrade pathway are to be defined in a dedicated follow-up session._
{% endhint %}

### 1.4. Credential Enrichment & Attribute-Based Access&#x20;

To enable finer-grained access control, participants may enrich their identity by adding verifiable credentials to their digital identity wallet. These could include:&#x20;

* Nationality or region of residence (e.g. Bavarian residency for access to regional health data)&#x20;
* Employment or professional role&#x20;
* Diploma or educational attainment&#x20;
* Property ownership or professional certifications&#x20;
* eIDAS 2.0-aligned verified attributes&#x20;

GDDS will define a credential ontology and maintain a list of trusted credential issuers for access-related attributes. Data providers must:&#x20;

* Define the access rules for their datasets/services&#x20;
* Work with GDDS to identify which credentials are required and from which issuers&#x20;
* Ensure that these mechanisms are operational before the data is onboarded into GDDS&#x20;

In addition to user-level identity enrichment, GDDS supports the exchange of verifiable credentials between system components (e.g. connectors) using protocols such as DCP. This occurs during data exchange interactions, enabling secure machine-to-machine communication and enforcement of data access and usage policies.&#x20;

### 1.5. Group-Based Membership Systems&#x20;

GDDS may implement Data User Groups (similar to virtual organisations or thematic circles), where:&#x20;

* Organisations or individuals may apply for membership&#x20;
* Rules for group membership may be evaluated automatically or through human validation&#x20;
* This model supports flexible data access schemes (e.g. a group of certified consultants)&#x20;

### 6. Human-in-the-Loop (HITL) Approvals&#x20;

Initially, some access requests may rely on manual validation by data providers — especially where no automated attribute-based access rules have yet been established.&#x20;

* This non-scalable model can serve as a practical transition path&#x20;
* GDDS will provide technical and governance support to help data providers evolve toward automated access control systems&#x20;
