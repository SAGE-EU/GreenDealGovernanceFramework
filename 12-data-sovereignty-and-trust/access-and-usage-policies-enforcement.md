# Access & Usage Policies Enforcement

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

The Access & Usage Policies Enforcement capability defines the rules, processes, and technical mechanisms that govern how data can be accessed, used, and shared within the GDDS ecosystem. It ensures that:

* > Access is granted only to authorised parties.
* > Data usage follows explicitly agreed purposes and obligations.
* > Consent is managed transparently and revocably.
* > Compliance is verifiable and enforceable in both organisational and technical terms.

It acts as the operational layer of data sovereignty, linking identity management, trust rules, and legal agreements into actionable, machine-readable policies.

### **Core Capabilities**

1. > Access Control Policies
   * > Define who can access which data and under what circumstances (role-, attribute-, or context-based).
   * > Enforce pre-access checks through Policy Enforcement Points (PEP) and Policy Decision Points (PDP).
2. > Usage Control Policies
   * > Define what actions (e.g., analyse, share, modify) are permitted once access is granted.
   * > Apply continuous usage checks where obligations or prohibitions change over time.
3. > Consent Management Policies
   * > Manage data subject consent and legal permissions.
   * > Support opt-in/opt-out and revocation workflows.
   * > Maintain audit trails for compliance proof.
4. > Policy Transformation & Interoperability
   * > Translate agreements into machine-readable formats (e.g., ODRL[^1]).
   * > Ensure semantic interoperability between participants’ systems.
5. > Compliance Tracking & Enforcement Proof
   * > Log and audit every access and usage event.
   * > Provide verifiable enforcement evidence for trust and dispute resolution.

***

## Machine-readable licence policies&#x20;

The iSHARE licence model defines a set of machine-readable usage conditions (for example: internal use only, resharing restricted to adhering parties, certification-linked such as ISO 27001, or country- or sector-restricted). These licences connect operational trust to legal compliance and form the basis for GDDS-level data usage policy enforcement. The GDDS may define additional licence types or constraints as required by Green Deal use cases.&#x20;

Access control operates through role-based and attribute-based models, using the management of user attributes, roles, and group memberships to enforce fine-grained access control policies aligned with organisational, legal, and regulatory requirements. This supports flexible and scalable permission management across diverse user communities and service providers. Pre-access checks are enforced through Policy Enforcement Points (PEP) and Policy Decision Points (PDP),  and agreements are expressed as machine-readable policies, following, for the time being, the iSHARE delegation-evidence and licence model documented in D3.1 (WP3, §2.2.2).&#x20;

Machine-readable licence policies take legal effect through the participants' signed [Terms of Use](#user-content-fn-1)[^1] and the corresponding contractual terms. A machine-readable condition and its human-readable contractual expression must correspond, so that enforcement is valid in both technical and legal terms (see Legal Framework, Contractual Framework).

{% hint style="warning" %}
_Note (open): The machine-readable policy language for expressing agreements at GDDS level has not yet been decided. The iSHARE Trust Framework enforcement stack natively uses the XACML-JSON-inspired delegation-evidence format evaluated by the Authorisation Registry (see D3.1, §2.2.2), while ODRL has been discussed as a candidate open format for policy expression. Full ODRL implementation does not yet exist in current connectors; for the time being, therefore, policy requirements are derived from the specific use cases rather than from a full ODRL integration, and this document follows the iSHARE model as documented in D3.1._&#x20;

_Related open topics for co-creation: the licence catalogue and any additional GDDS licence types, the overall policy taxonomy, and the role of the Authorisation Registry in enforcement. Owner: WP4, with WP3._
{% endhint %}

{% hint style="warning" %}
_Note (alignment check, open): A possible overlap or conflict with the Trusted Data Transaction standard (associated with the Gaia-X framework and the Data Transfer Agent) has been flagged for the enforcement approach described here. The current governance and enforcement drafts are to be checked against that standard to confirm compatibility. Owner: WP4, in coordination with the standard's working group._
{% endhint %}

This capability is the technical home for the enforcement mechanisms referenced by the governance rules in Data Sovereignty & Technical Governance (subsection 1, Data access and usage policy governance). The governance rules who sets conditions, which licensing models are offered, and how custom and conditional policies are approved reside there; the policy languages, evaluation points, and runtime enforcement reside here.&#x20;

{% hint style="warning" %}
_Note: The machine-readable licence model and access-control details were relocated from the Operational Framework (IAA Services). Further content (consent-management workflows, usage-control continuity, and compliance/enforcement proof) is to be added in line with the developments within the WP3, WP4 group._&#x20;
{% endhint %}

[^1]: TBD
