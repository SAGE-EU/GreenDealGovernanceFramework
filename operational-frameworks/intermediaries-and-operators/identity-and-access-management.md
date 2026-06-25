# Identity and Access Management

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP6, WP7, WP4, and the Techie group, including inputs from T3.1 - GDDS Trust Framework and AAI Federation. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._ &#x20;
{% endhint %}

## **Overview**

Identity and Access Management (IAM) represents a foundational component of the GDDS, providing the mechanisms required to securely identify users and control their access to services, data, and computational resources. IAM covers the full lifecycle of digital identities for both natural persons (e.g. researchers, data stewards) and legal entities (e.g. participating organisations, data providers). This lifecycle ranges from initial registration and onboarding of users and services, through authentication and authorisation, to the management, renewal, and revocation of credentials.

## **IAM Architecture and Components**

The IAM framework relies on a combination of external and internal components to manage identities, authenticate users and services, and control access to resources across the GDDS. Specifically, it leverages existing external trusted identity providers to authenticate users acting on behalf of participant organisations and establish appropriate levels of assurance regarding their identities. In addition, GDDS uses internal or federated data space registries to manage and validate participant metadata, including status, roles, and entitlements within the ecosystem. These registries support trust establishment and authorisation decisions but are not involved in the authentication process itself.

## **Standards and Interoperability**

To ensure technical interoperability, GDDS adopts established standards for authentication and federation (e.g. OAuth 2.0, OpenID Connect, SAML), allowing users to reuse existing credentials where possible and reducing duplication of identities:<br>

* Academic and research users may authenticate via eduGAIN-connected identity providers.
* Business and government participants may rely on corporate identity providers, eIDAS-compliant identities, or other trusted authentication schemes, depending on regulatory and assurance requirements.

## **Access Control and Authorisation**

The IAM framework also includes the management of user attributes, roles, and group memberships, which are used to enforce fine-grained access control policies aligned with organizational, legal, and regulatory requirements. By supporting role-based and attribute-based access control models, IAM enables flexible and scalable permission management across diverse user communities and service providers.

## **Federation, Trust and Security Mechanisms**

In addition, IAM plays a critical role in enabling secure collaboration in federated and distributed environments. It supports interoperability between multiple identity federations and infrastructures, allowing users to access services across organisational and national boundaries using a single digital identity (Single Sign-On). The framework incorporates trust and security mechanisms such as federated authentication, credential assurance levels, logging, and auditing, ensuring compliance with applicable policies and standards.

Within the iSHARE Trust Framework as applied in the GDDS, the following trust and security mechanisms are operative:

* PKI-based identity validation — each participant’s identity is anchored in an X.509 certificate issued by a trusted Certificate Authority and validated at registration. The resulting iSHARE DID serves as the canonical GDDS participant identifier.
* Signed JSON Web Tokens (JWTs) — all authentication and delegation assertions are expressed as signed JWTs, enabling cryptographically verifiable, stateless trust decisions between participants.
* Delegation evidence and the Authorisation Registry (AR) — data access is not implicit; it requires delegation evidence evaluated by an Authorisation Registry or the Entitled Party (data rights holder) at runtime. Delegation can be conditional (e.g. time-bound, certification-dependent, use-case scoped) and supports hierarchical delegation chains. The AR is a certified role within the iSHARE framework and subject to conformity assessment.
* Machine-readable licence policies — the iSHARE licence model defines a set of machine-readable usage conditions (e.g. internal use only, resharing restricted to adhering parties, ISO 27001-linked, country or sector-restricted). These licences connect operational trust to legal compliance and form the basis for GDDS-level data usage policy enforcement. GDDS may define additional licence types or constraints as required by Green Deal use cases.
* Certified roles — certain roles within the iSHARE framework (Participant Registry, Authorisation Registry, Identity Provider) require formal certification against role-specific assessment criteria. This ensures consistent, auditable trust for participants occupying infrastructure roles in the GDDS ecosystem.

These mechanisms collectively ensure that only verified, active participants can engage in data transactions and that data sovereignty is technically enforced, contractually defined.

The Identity and Access Management framework of the GDDS will be developed with a focus on establishing the core IAM architecture, defining governance and trust policies, integrating suitable identity providers, and implementing robust authentication and authorization mechanisms to support secure and interoperable access for all participating stakeholders.

The framework follows an evolutionary approach. GDDS has adopted the Decentralised Claims Protocol (DCP) and Verifiable Credentials (VCs) to support trust, delegation, and authorisation across the data space. These complement existing federation-based approaches (e.g. OAuth 2.0 / OpenID Connect and SAML), which continue to be used for user authentication and service integration. Access decisions are based on the verification of claims issued by trusted authorities and evaluated against trusted registries and policies, enabling fine-grained delegation and interoperability with emerging European frameworks such as eIDAS 2.0.
