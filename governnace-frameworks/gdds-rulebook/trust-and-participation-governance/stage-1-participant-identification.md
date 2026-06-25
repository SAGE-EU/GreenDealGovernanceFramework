# Stage 1 — Participant identification

## Rule&#x20;

Every participant must be identified before admission, using a verifiable identifier appropriate to its participant type, and must meet the minimum level of identity assurance required for its intended role. Identification establishes the participant as a trusted actor in the data space; access rights follow from, and are proportionate to, the assurance level achieved.&#x20;

The GDDS recognises three categories of identifier, which differ in their verifiability and governance weight:&#x20;

* Authoritative identifiers — nationally or internationally registered identifiers that are unique, persistent, and verifiable against official registries (for example national business registry numbers, VAT numbers, LEI codes, EORI numbers). These are the primary identifiers for Institutional Participants.&#x20;
* Communal data space identifiers — ecosystem-specific identifiers issued within or recognised by the GDDS trust framework. The primary example is the iSHARE DID, which packages an existing legal identity derived from a PKI certificate and serves as the canonical GDDS participant identifier, particularly for machine-to-machine interactions. Other recognised identifiers include ADS 1.1-compliant digital IDs and EGI Check-In credentials for research and academic communities.&#x20;
* Non-authoritative identifiers — changeable identifiers such as email addresses that cannot be verified against official registries. These are not accepted as primary onboarding identifiers and may be used only for contact and notification purposes.&#x20;

## Procedure&#x20;

To accommodate different participant types and existing identity infrastructures, the GDDS defines three identity pathways. A participant's type and its identity pathway are separate dimensions: the type determines its governance status, while the pathway determines how it proves its identity and at what assurance level.&#x20;

* Organisational pathway — for Institutional Participants using their own identity infrastructure (corporate identity provider, PKI, or eIDAS Organisation ID). The organisation first registers itself as a participant using a recognised authoritative identifier, and then determines which individuals may represent it and what roles and credentials those individuals receive. Minimum assurance: Substantial (eIDAS).&#x20;
* Academic pathway — for Institutional Participants whose institution provides identity assurance through eduGAIN or an equivalent national academic federation. Academic participants are Institutional Participants for governance purposes; "Academic" is a credential pathway, not a separate participant type. Where an institution cannot provide the assurance level a participant requires, that participant may proceed via the Individual pathway.&#x20;
* Individual pathway — for Individual Participants. Anonymous access is limited to open resources; low-assurance credentials permit limited access where allowed; and eIDAS-compliant digital identities enable verifiable participation. High or Substantial assurance is required for full access to restricted data and services. Support for eIDAS 2.0 wallet-based identities will be added as it becomes available.&#x20;

The table below provides a reference overview of accepted identifiers and minimum assurance levels per identity pathway:&#x20;

| Organisational pathway                                                                                                    | Academic pathway                                                                                                                                                                                                                                                                                                    | Individual pathway                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>Organisation registers, then delegates internal users. Internal role assignments under org governance. </li></ul> | <ul><li>Accepted IDs: eduGAIN-connected institutional login, National academic federation ID </li><li>Min. assurance: Depends on institution. Higher access may require Individual pathway. </li><li>If institution cannot provide required assurance level, participant upgrades to Individual pathway. </li></ul> | <ul><li>Accepted IDs: eIDAS 1.0-compliant digital ID (Substantial+), Low LoA (Google/LinkedIn) for open resources only, eIDAS 2.0 wallet (future), Role-specific attestation where applicable </li><li>Min. assurance: High / Substantial required for full access </li><li>Anonymous access limited to open resources. Credential enrichment enables finer-grained permissions. </li></ul> |

{% hint style="info" %}
See more details about the detailed pathways and assurance levels in Technical Framework. [Data Sovereignty section. ](../../../12-data-sovereignty-and-trust/)
{% endhint %}

{% hint style="warning" %}
_Open decision: The minimum eIDAS assurance level required per role has not yet been formally decided. The open question is: must a Data Provider always use Substantial or High LoA, while a Data Recipient may use Low LoA? How does eIDAS status (mandatory / optional / one of several accepted schemes) apply per role? This must be resolved and documented here before Rulebook v0.4 is finalised. Owner: WP4 / WP3._&#x20;
{% endhint %}

Beyond initial identification, participants may enrich their credentials by adding verifiable attributes (for example, region of residence, professional role, or sector certifications) to support finer-grained, attribute-based access.&#x20;

The GDDS maintains a credential ontology and a list of trusted credential issuers for this purpose; Data Providers define which credentials are required for their datasets and ensure these rules are operational before data is onboarded. The verifiable-credential mechanisms, the supported protocols, and machine-to-machine credential exchange between system components are specified in the Technical Framework (see [Data Sovereignty & Trust](../../../12-data-sovereignty-and-trust/identity-and-attestation-management.md)); this section governs which identifiers and assurance levels are required and who is accountable for them, rather than how they are technically implemented.&#x20;

Two further provisions support participant mobility and group-based access:&#x20;

* Upgrade from Individual to Institutional participation. An Individual Participant may migrate to Institutional participation once their institution formally joins the data space — for example, a researcher who initially participates individually and whose institution later completes Institutional onboarding. On upgrade, the individual's credentials are re-linked under the institutional umbrella, and their roles and access rights are re-evaluated under the institution's governance. Until the upgrade is complete, the individual retains Individual-level access only.&#x20;
* Group-based membership. The GDDS may operate Data User Groups (thematic circles or virtual organisations) for which organisations or individuals may apply, with membership evaluated automatically or through human validation. This supports flexible access schemes, such as a group of certified consultants.&#x20;

{% hint style="info" %}
_See more in the sections of technical - Data sovereignty - Identity and Attestation management_ [_here_](../../../12-data-sovereignty-and-trust/identity-and-attestation-management.md)_._&#x20;
{% endhint %}

## Responsible body&#x20;

The GDDS Operator performs identity verification under the oversight of the Data Space Governance Authority (DSGA). Authoritative identifiers are validated against official registries at registration; the resulting iSHARE DID serves as the canonical participant identifier thereafter.&#x20;

{% hint style="warning" %}
_Open decision: The minimum eIDAS assurance level required per role has not yet been formally decided — in particular, whether a Data Provider must always use Substantial or High assurance while a Data Recipient may use Low, and how eIDAS status (mandatory, optional, or one of several accepted schemes) applies per role. To be resolved and documented here before Rulebook v0.4 is finalised. Owner: WP4 / WP3._&#x20;
{% endhint %}

{% hint style="warning" %}
_Note: European identification standards are prioritised across all pathways. Country-specific variations in accepted identifiers will be documented as confirmed, in coordination with WP3 and GRNET. Participants from countries with non-standard identifier schemes should contact the GDDS Operator for guidance._&#x20;
{% endhint %}

{% hint style="warning" %}
_Note: The detailed procedural steps and technical implementation of the Individual-to-Institutional upgrade pathway are to be defined in a dedicated follow-up session. Human-in-the-loop manual approvals may serve as a transition path where automated attribute-based access rules are not yet established, with GDDS support for evolving toward automated access control. Further content to be added after co-creation sessions by WP4 and WP3._&#x20;
{% endhint %}
