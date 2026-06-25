# Trust Framework

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Trust Framework defines the rules, roles, and mechanisms that underpin confidence in all GDDS interactions. It ensures that participants, services, and transactions can be validated against a common rulebook, making trust decisions faster, more transparent, and interoperable across sectors.

The framework serves as the connective tissue between governance requirements and technical enablers, linking identity verification, attestation management, access control, and compliance into one coherent system. By setting clear acceptance criteria for trust anchors, and trust service providers, GDDS can guarantee the authenticity, integrity, and security of both participants and the data they share.

Where possible, GDDS can adopt and extend existing trust frameworks (e.g., Gaia-X, iSHARE, IDSA) to ensure European alignment while tailoring rules to Green Deal–specific use cases.

### **Core Capabilities**

* > Participant & Service Verification – Ensure all participants and services are verifiable against governance requirements and technical standards.
* > Governance Enforcement – Apply the GDDS Rulebook to enforce organisational, technical, and semantic interoperability.
* > Trust Entity Management – Define, accredit, and maintain the registry of Trust Anchors, Trust Service Providers, Conformity Assessment Bodies, and Notaries.
* > Registry Integration – Store the Rulebook, accreditation lists, revoked trust entities, and compliance schemas in the GDDS registry for public reference.
* > Multi-Level Trust – Define different assurance levels based on source reliability, credential type, or attestation scope.

_Further content will be added after co-creation sessions._

***

## Federation, trust and security mechanisms&#x20;

The Trust Framework enables secure collaboration in federated and distributed environments. It supports interoperability between multiple identity federations and infrastructures, allowing users to access services across organisational and national boundaries using a single digital identity (Single Sign-On), and it incorporates trust and security mechanisms such as federated authentication, credential assurance levels, logging, and auditing to ensure compliance with applicable policies and standards.&#x20;

Within the iSHARE Trust Framework as applied in the GDDS, the following trust and security mechanisms are operative:&#x20;

* PKI-based identity validation — each participant's identity is anchored in an X.509 certificate issued by a trusted Certificate Authority and validated at registration. The resulting iSHARE DID serves as the canonical GDDS participant identifier.&#x20;
* Signed JSON Web Tokens (JWTs) — authentication and delegation assertions are expressed as signed JWTs, enabling cryptographically verifiable, stateless trust decisions between participants.&#x20;
* Delegation evidence and the Authorisation Registry (AR) — data access is not implicit; it requires delegation evidence evaluated by an Authorisation Registry or the Entitled Party (data rights holder) at runtime. Delegation can be conditional (for example time-bound, certification-dependent, or use-case scoped) and supports hierarchical delegation chains. The AR is a certified role within the iSHARE framework and subject to conformity assessment.&#x20;
* Certified roles — certain roles within the iSHARE framework (Participant Registry, Authorisation Registry, Identity Provider) require formal certification against role-specific assessment criteria, ensuring consistent, auditable trust for participants occupying infrastructure roles in the GDDS ecosystem.&#x20;

Together these mechanisms ensure that only verified, active participants can engage in data transactions, and that data sovereignty is technically enforced as well as contractually defined. The certification of these roles is governed under the Conformity Framework & Governance Enforcement; the participant-facing trust conditions are governed under Trust & Participation Governance.&#x20;

{% hint style="warning" %}
_Note: The federation, trust and security mechanisms above were relocated from the Operational Framework (IAA Services). Further content might be added in line with the developments within the WP3, WP4 group._&#x20;
{% endhint %}
