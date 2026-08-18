# Identity & Attestation Management

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

Identity and Attestation Management specifies how participants are identified, authenticated, and assured, and how their attestations are issued and verified. It covers the identity architecture and components, the authentication and federation standards, the levels of assurance and multi-factor authentication, and the identity pathways by which each participant type obtains and, where needed, enriches its credentials. It follows the GDDS identity and trust architecture in D3.1 (WP3), Section 3.1 and the assurance framework in Section 2.4.1 to Section 2.4.2, and applies the principles of self-sovereign identity, a standards-first approach, policy-linked identity, and the reuse of existing credentials and certifications.&#x20;

The section distinguishes three identity layers: the participant's identity, established once at onboarding, which identifies the organisation or person; the credential and attribute layer, which carries assurance levels, entitlements, and verifiable credentials; and runtime delegation evidence, through which authorisation is represented and evaluated at the point of exchange (see [Trust Framework below](trust-framework.md), and D3.1 (WP3), Section 2.3 and Section 3.1).&#x20;

{% hint style="warning" %}
_Note (open items carried over from consortium comments on the previous draft, for the co-creation sessions from September onwards): decide whether trusted identification should extend beyond the organisations to data, locations, products, logistic units, parties, and assets, aligning with GS1 standards._&#x20;
{% endhint %}

***

## Technical architecture and components&#x20;

The Identity and Attestation Management framework combines shared/distributed services with components operated by [Federated Service Providers/Intermediaries ](#user-content-fn-1)[^1]\(under the GDDS Governance Framework), in line with the GDDS identity and trust architecture documented in D3.1 (WP3), Section 3.1, and the architecture diagram in D2.1.&#x20;

The distributed services are:&#x20;

1. the **Onboarding Portal,** which registers and admits participants and serves as the front end to the Participant Registry;
2. the **Participant Registry,** which holds the authoritative record of participants and their status and against which parties validate each other's legitimacy;
3. **the Authorisation Registry,** which stores and evaluates delegation evidence and access policies at the point of exchange;&#x20;
4. and authentication provided through trusted **Identity Providers.**&#x20;

On the participant side, each organisation connects through its **Data Connector** and may use its own identity infrastructure to authenticate its users. The registries manage and validate participant metadata (status, roles, entitlements) and support trust establishment and authorisation decisions without being involved in the authentication event itself. Consistent with the iSHARE Trust Framework, identification and authentication are handled separately from authorisation.

<img src="../.gitbook/assets/unknown (2).jpeg" alt="Figure 14: Overview of GDDS Core (Source D3.1)" height="369" width="639">

## Authentication and federation standards&#x20;

To ensure technical interoperability, the GDDS adopts established standards for authentication and federation (for example, OpenID Connect v1.0 and SAML), allowing users to reuse existing credentials where possible and reducing the duplication of identities:&#x20;

* academic and research users may authenticate via eduGAIN-connected identity providers;&#x20;
* business and government participants may rely on corporate identity providers, eIDAS-compliant identities, or other trusted authentication schemes, depending on regulatory and assurance requirements.&#x20;

Additionally, the GDDS has adopted the Decentralised Claims Protocol (DCP v1.0.0) and Verifiable Credentials (OID4VCI v1.0 and OID4VP v1.0) to support trust, delegation, and authorisation across the data space (Source: D3.1, Section 3, 1). These complement the federation-based approaches above, which continue to be used for user authentication and service integration. Access decisions are based on the verification of claims issued by trusted authorities and evaluated against trusted registries and policies, enabling fine-grained delegation and interoperability with emerging European frameworks such as eIDAS 2.0.&#x20;

{% hint style="warning" %}
_Note (open – to confirm with WP3): the baseline standard versions in force (the Decentralised Claims Protocol, OpenID Connect, and, for verifiable-credential exchange, OID4VCI and OID4VP), should be specified/ confirmed/ listed in specific section or tab._&#x20;

_Another suggestion to consider: Credentials should be able to describe claims about organisations, facilities, products, assets and linked resources, not only people or systems._
{% endhint %}

## Levels of assurance and multi-factor authentication&#x20;

Assurance in the GDDS is expressed through Levels of Assurance (LoA) that qualify the strength of identity proofing, credential issuance, and authenticator binding. For research and education participants authenticating through eduGAIN-connected providers, assurance is conveyed using the REFEDS Assurance Framework (RAF); for organisational and eIDAS-based identities it is expressed against the eIDAS Levels of Assurance (Low, Substantial, High).&#x20;

As documented by Working Group 3 in D3.1, RAF Identity Assurance Profiles map to eIDAS as follows: RAF IAP “low” and “medium” map to eIDAS Low, while RAF IAP “high” can align with eIDAS Substantial where the RAF v2.0 criteria for strong authenticator binding and controlled remote proofing are met. Because most academic identity providers assert lower profiles, participants requiring higher assurance for restricted data may need to raise it through the individual pathway or through credential enrichment. RAF assurance is carried in the eduPersonAssurance attribute (SAML) or the eduperson\_assurance claim (OIDC). Identity assurance, which concerns how an identity was proofed and bound to credentials, is distinct from authentication assurance, which concerns the strength of the authentication event itself.

Where a role or data product requires stronger authentication, multi-factor authentication is signalled and enforced in line with the REFEDS MFA Profile, with interoperable proxy behaviour following AARC-G029. A home identity provider signals multi-factor authentication by asserting the REFEDS MFA Profile value in the SAML authentication-context class reference or the OpenID Connect acr claim, and a proxy relies on multi-factor authentication performed at the home identity provider where available, enforcing it itself only where the home provider cannot. Where MFA is required but cannot be performed, access is denied rather than silently downgraded.

_Source: D3.1 GDDS first version report (WP3), §2.4.1–2.4.2. The RAF-to-eIDAS mapping and MFA handling reflect the Working Group 3 technical baseline and are authoritative for the assurance mechanisms; the governance rules that consume these levels reside in the Conformity Framework and Trust & Participation Governance._&#x20;

{% hint style="warning" %}
_Note (to Clarify with WP3): the difference between improving the assurance of a person's identity and adding additional credentials about that person? For example, adding a diploma or professional certification provides more information about the participant, but may not necessarily increase the assurance level of the original identity._
{% endhint %}

***

## Identity Paths and Credential Enrichment in GDDS&#x20;

The identity paths below describe how each participant profile obtains and enriches credentials in practice, applying the architecture, standards, and assurance levels set out above. They were developed through WP3 and define the practical entry points into the GDDS.

### 1. Organisational Participants with Their Own Identity Systems&#x20;

Organisations such as municipalities, real estate companies, consultancies, or research labs may wish to participate using their existing identity infrastructure.&#x20;

These organisations must first register themselves as official participants of GDDS using a recognised organisational identifier (e.g., LEI or other trusted digital IDs).

* Accepted identifiers include: LEI (Legal Entity Identifier), EORI (Economic Operators Registration and Identification), KVK/CoC (Chamber of Commerce registration numbers), national business registry IDs, eIDAS Org ID (Organisation Identifier).&#x20;
* Minimum assurance level: Substantial (eIDAS), as the primary assurance standard for organisational participants.&#x20;

Upon successful registration, the organisation determines which individuals may represent it within GDDS and defines the roles and credentials these individuals will receive.&#x20;

Organisational representatives may then act on behalf of their entity to:&#x20;

* Manage datasets&#x20;
* Input or extract data&#x20;
* Administer services (e.g. onboarding of sub-participants)&#x20;

Role-based credentials are assigned internally and can be enriched further via GDDS processes (see Section 4 ['Credential Enrichment & Attribute-Based Access '](identity-and-attestation-management.md#id-4.-credential-enrichment-and-attribute-based-access)).&#x20;

{% hint style="warning" %}
_Note (Open Decisions and Suggestions):  clarify when each identifier can be used, as LEI, EORI and national business registry identifiers have different purposes and geographical coverage._  \
_Suggestion to also add GLN as an operational identifier option for parties and locations where already used by participants._&#x20;
{% endhint %}

### 2. Academic Participants&#x20;

Individuals working within academic institutions (e.g. universities, applied research centres) may participate via their existing academic credentials, such as institutional logins compliant with eduGAIN or national federation protocols.&#x20;

The level of access will depend on the authentication assurances provided by the institution.&#x20;

If an academic participant requires higher assurance or greater access rights than their institution offers, they may proceed via the individual pathway (see below).&#x20;

{% hint style="info" %}
_Note on participant type: Academic participants are classified as Institutional participants for governance purposes. The Academic pathway is an identity/credential pathway available to Institutional participants whose institution provides authentication via eduGAIN or an equivalent national academic federation. 'Academic' is not a separate participant type; the distinction is retained solely at the identity and credential level._
{% endhint %}

{% hint style="warning" %}
_Note (To clarify): Does the academic institution need to be formally admitted as an Institutional Participant before one of its users can follow this pathway? Authenticating through eduGAIN confirms the user's relationship with an academic institution, but may not by itself confirm that the institution has joined GDDS or authorised that user to represent it. --> In principle, the academic institution is admitted as the Institutional Participant and its users follow under that umbrella. The exact admission sequencing for the academic pathway (whether the institution must be fully admitted before a user proceeds) is part of the onboarding detail to be specified in Phase 2. Owner: WP4, WP3._&#x20;
{% endhint %}

### 3. Individual Participants&#x20;

Individuals (e.g. freelancers, private consultants, independent researchers) may:&#x20;

* Access GDDS anonymously — but only to view open resources visible to unauthenticated users.&#x20;
* Use low-assurance digital IDs (e.g. Google, LinkedIn) for limited access, where permitted.&#x20;
* Register using eIDAS 1.0 -compliant digital identities from trusted EU providers. These identities can enable secure and verifiable participation in the data space. _\[In future: eIDAS 2.0 wallet-based identities will be supported as they become available. Role-specific attestations (e.g. professional certifications, researcher accreditation) may be required for certain roles and will be accepted where applicable.]_&#x20;

Minimum assurance level: High or Substantial assurance is required for full access to restricted data and services. Low assurance limits access to open resources only. Credential enrichment (adding verifiable credentials over time) enables finer-grained permissions as the participant's assurance level increases.

#### 3.1 Individual to Institutional Participants&#x20;

An individual participant may begin participation in GDDS under the Individual pathway and subsequently migrate to Institutional participation once their institution is ready to formally join the data space. This upgrade path is relevant, for example, for an academic researcher who initially participates as an individual but whose institution later completes Institutional onboarding.&#x20;

The upgrade process involves the following general steps:&#x20;

1. The institution completes the Institutional onboarding process (see [Trust & Participation Governance, Stage 2 — Eligibility assessment and admission](../governance-framework/gdds-rulebook/trust-and-participation-governance/stage-2-eligibility-assessment-and-admission.md), and [Stage 3 — Onboarding and assignment of roles and access rights](../governance-framework/gdds-rulebook/trust-and-participation-governance/stage-3-onboarding-and-assignment-of-roles-and-access-rights.md)), including identity verification under the Organisational or Academic pathway, eligibility assessment, and execution of the participation agreement.
2. Once the institution is an admitted Institutional participant, the individual's existing credentials are [re-linked under the institutional umbrella, ](#user-content-fn-2)[^2]subject to the institution's internal authorisation.&#x20;
3. The individual's roles and access rights are re-evaluated and re-assigned in line with the institution's governance framework and the roles selected by the institution at onboarding.&#x20;
4. Until the upgrade is complete, the individual retains Individual-level access only.&#x20;

{% hint style="warning" %}
_Note: The detailed procedural steps and technical implementation of the upgrade pathway are to be defined in a dedicated follow-up session. Additionally to clarify which credentials carry over if any. Owner: WP3, WP4._&#x20;
{% endhint %}

### 4. Credential Enrichment & Attribute-Based Access&#x20;

To enable finer-grained access control, participants may enrich their identity by adding verifiable credentials to their digital identity wallet. These could include:&#x20;

* Nationality or region of residence (e.g. Bavarian residency for access to regional health data)&#x20;
* Employment or professional role&#x20;
* Diploma or educational attainment&#x20;
* Property ownership or professional certifications&#x20;
* eIDAS 2.0-aligned verified attributes&#x20;

Where credentials relate to product, location, certification, DPP, sustainability or traceability information, the credential ontology should support mappings to GS1 identifiers, GS1 Digital Link resource types and relevant GS1 vocabularies.

GDDS will define a credential ontology and maintain a list of trusted credential issuers for access-related attributes. Data providers must:&#x20;

* Define the access rules for their datasets/services&#x20;
* Work with GDDS to identify which credentials are required and from which issuers&#x20;
* Ensure that these mechanisms are operational before the data is onboarded into GDDS&#x20;

In addition to user-level identity enrichment, GDDS supports the exchange of verifiable credentials between system components (e.g. connectors) using protocols such as DCP. This occurs during data exchange interactions, enabling secure machine-to-machine communication and enforcement of data access and usage policies.&#x20;

{% hint style="warning" %}
_Note (Clarify with WP3):  Some of the proposed attributes, such as nationality, residence or property ownership, could be sensitive. Could we mention that only the minimum information required for an access decision should be requested? For example, confirming that a person meets a regional eligibility condition may be preferable to disclosing their full address or nationality. --> Only the minimum attributes necessary for the is intended purpose should be requested and shared, consistent with GDPR data minimisation; sensitive attributes such as nationality, residence, or property ownership should be requested only where strictly necessary and proportionate.  Owner: WP4, WP3._&#x20;

_Additional Note (To define further with WP3): how an issuer becomes trusted by GDDS and who is responsible for maintaining the trusted issuer list? It would also be useful to clarify what happens when an issuer or credential is no longer considered valid. --> for now it is assumed that for the operational GDDS that an issuer becomes trusted through the Trust Framework and gov procedures of GDDS, following the certification steps to be onboarded - with that the trusted issuer list is maintained by the DSGA/ Operator of the GDDS whoever that would be._
{% endhint %}

### 5. Group-Based Membership Systems&#x20;

GDDS may implement Data User Groups, where:&#x20;

* Organisations or individuals may apply for membership&#x20;
* Rules for group membership may be evaluated automatically or through human validation&#x20;
* This model supports flexible data access schemes (e.g. a group of certified consultants)&#x20;

Group-based membership may be complemented by human-in-the-loop approval: where no automated attribute-based rule has yet been established, a data provider may validate access requests manually as a practical transition path, with GDDS providing support to evolve toward automated access control.

[^1]: TBD

[^2]: Re-linked under the institutional umbrella means that when an individual later joins an institution, their existing individual credential is associated with that Institutional Participant, which then becomes the accountable entity, subject to the institution's admission and internal authorisation.
