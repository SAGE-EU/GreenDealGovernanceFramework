# Trust Framework

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Trust Framework specifies how verified participants and services are trusted across organisational boundaries: the mechanisms that anchor trust cryptographically and through certified roles, the authorisation patterns by which access rights are represented and conveyed, and the baseline security and data-protection obligations shared by all participants. It follows the authorisation patterns in D3.1 (WP3), Section 2.3 and the policy frameworks in Section 2.4.3 to 2.4.4, extending established frameworks such as iSHARE where appropriate.

***

## Federation, trust and security mechanisms&#x20;

The Trust Framework enables secure collaboration in federated and distributed environments. It supports interoperability between multiple identity federations and infrastructures, allowing users to access services across organisational and national boundaries using a single digital identity (Single Sign-On), and it incorporates trust and security mechanisms such as federated authentication, credential assurance levels, logging, and auditing to ensure compliance with applicable policies and standards.&#x20;

Within the iSHARE Trust Framework as applied in the GDDS, the following trust and security mechanisms are operative:&#x20;

* PKI-based identity validation — each participant's identity is anchored in an eIDAS eSeal certificate (an X.509 certificate) issued by a trusted Certificate Authority and validated at registration. The resulting iSHARE DID serves as the canonical GDDS participant identifier.&#x20;
* Signed JSON Web Tokens (JWTs) — authentication and delegation assertions are expressed as signed JWTs, enabling cryptographically verifiable, stateless trust decisions between participants.&#x20;
* Delegation evidence and the Authorisation Registry (AR) — data access is not implicit; it requires delegation evidence evaluated by an Authorisation Registry or the Entitled Party (data rights holder) at runtime. Delegation can be conditional (for example time-bound, certification-dependent, or use-case scoped) and supports hierarchical delegation chains. The AR is a certified role within the iSHARE framework and subject to conformity assessment.&#x20;
* Certified roles — the iSHARE Trust Framework defines four certified roles (Identity Provider, Identity Broker, Authorisation Registry, Participant Registry); of these, three are applied in the GDDS: the Participant Registry, the Authorisation Registry, and the Identity Provider. Certified roles require formal certification against role-specific assessment criteria, ensuring consistent, auditable trust for participants occupying infrastructure roles in the GDDS ecosystem.

Together, these mechanisms ensure that only verified, active participants can engage in data transactions, and that data sovereignty is technically supported as well as contractually defined. The certification of these roles is governed under the Conformity Framework & Governance Enforcement; the participant-facing trust conditions are governed under Trust & Participation Governance.&#x20;

***

## Authorisation patterns&#x20;

The GDDS supports two complementary authorisation patterns, which may be combined within a single flow (D3.1 (WP3), Section 2.3). &#x20;

1. In the community-based pattern, used for research and education collaborations, authorisation is conveyed through entitlements rather than delegation evidence: it is managed within Virtual Organisations that define collaboration-specific memberships, groups, and roles independently of participants' home organisations, and in an AARC Blueprint Architecture a Proxy combines the identity received from a user's home identity provider with the authorisation information managed by the Virtual Organisation or a community attribute authority. Group membership, roles, and resource capabilities are encoded as structured entitlement values (following AARC-G069 and AARC-G027) and released in the eduPersonEntitlement attribute (SAML) or the entitlements claim (OIDC), which services consume from the assertion or retrieve through token introspection (RFC 7662). This reflects the community authorisation pattern documented in D3.1 (WP3), Section 2.3.1. &#x20;
2. The delegated pattern, adapted from the iSHARE model, is expressed as machine-readable delegation evidence, evaluated at the point of exchange. Delegation evidence carries a validity period, the issuer (policy issuer) and the subject (access subject), a maximum delegation depth, and one or more policies specifying the target resources and identifiers, the permitted actions, the applicable licences, and the conditions under which access is permitted. Two presentation patterns are supported: the consumer fetches the authorisation from the Authorisation Registry as a token and presents it to the provider; or the provider requests the applicable token from the Authorisation Registry for the resource requested by the consumer. Both machine-to-machine (M2M) and human-to-machine (H2M) interaction patterns are supported.&#x20;

_Source: D3.1 GDDS first version report (WP3), §2.2.2. This is the Working Group 3 description of the delegation-evidence structure and authorisation-presentation patterns; the governance rules on delegation reside in Data Sovereignty & Technical Governance (subsection 1)._&#x20;

***

## Baseline security and data-protection obligations&#x20;

Beyond identity assurance, trust in the GDDS depends on a shared security and data-protection baseline. As set out by Working Group 3 in D3.1, participants and the [intermediaries/federated service ](#user-content-fn-1)[^1]providers operating shared services under the GDDS Governance Framework are expected to align with recognised federated-infrastructure baselines: incident response under Sirtfi (maintaining an incident-response capability, publishing security contacts, and collaborating on cross-infrastructure incidents); an Acceptable Use Policy based on the WISE Baseline AUP; and the AARC-G084 Security Operational Baseline, which sets minimum expectations including acceptance of the AUP, Sirtfi compliance, processing of personal data only for operational, administrative, or security purposes, retention of logs for at least 180 days to support incident investigation, secure configuration and timely patching, and equivalent obligations on third-party providers engaged in service delivery. For personal-data processing, service providers are expected to follow a GDPR-aligned baseline consistent with the REFEDS Data Protection Code of Conduct (v2.0), covering purpose limitation, data minimisation, transparency, security, and breach handling.

_Source: D3.1 GDDS first version report (WP3), §2.3.3–2.3.4. These baselines reflect the Working Group 3 technical baseline and are authoritative for the security and data-protection mechanisms; the corresponding participant commitments are reflected as obligations in the Conformity Framework and Trust & Participation Governance._&#x20;

[^1]: TBD
