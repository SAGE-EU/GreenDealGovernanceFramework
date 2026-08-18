# Access & Usage Policies Enforcement

{% hint style="warning" %}
_This section might be updated based on the latest developments in the SAGE consortium, specifically considering WP2, WP3, WP4, and WP5 working groups. Since the project runs till 2028, the final GDDS deliverable is expected to have additional information on these sections._
{% endhint %}

Access and Usage Policies Enforcement specifies how agreed access and usage conditions become machine-readable policies applied at runtime. It is the operational layer of data sovereignty, linking identity, trust, and legal agreements into enforceable rules, and it covers the policy types, the enforcement points, and the licence model evaluated by the Authorisation Registry.

## Policy Types & Mechanisms

1. **Access Control Policies**&#x20;

* Define who can access which data and under what circumstances (role-, attribute-, or context-based).&#x20;
* Enforce pre-access checks through Policy Enforcement Points (PEP) and Policy Decision Points (PDP).&#x20;

2. **Usage Control Policies**&#x20;

* Define what actions (e.g., analyse, share, modify) are permitted once access is granted.&#x20;
* Apply continuous usage checks where obligations or prohibitions change over time.&#x20;

3. **Consent Management Policies**&#x20;

* Manage data subject consent and legal permissions.&#x20;
* Support opt-in/opt-out and revocation workflows.&#x20;
* Maintain audit trails for compliance proof.&#x20;

4. **Policy Transformation & Interoperability**&#x20;

* Translate agreements into machine-readable formats &#x20;
* Ensure semantic interoperability between participants’ systems.&#x20;

5. **Compliance Tracking & Enforcement Proof**&#x20;

* Log and audit every access and usage event.&#x20;
* Provide verifiable enforcement evidence for trust and dispute resolution.&#x20;

{% hint style="warning" %}
_Note (Clarify and discuss with WP3, Phase 2): clarify which usage conditions can realistically be enforced once the data has been transferred to another participant? Some conditions may be technically controlled, while others may still rely on contracts, monitoring or audits._ &#x20;

_Note (WP5 scope item, for September onwards): some propose extending access and usage policies to linked resources as well as datasets and services, aligning with GS1 standards. 'For product, asset, party, location and traceability data, GDDS should also align with relevant GS1 standards, complementing data-space trust frameworks such as Gaia-X, iSHARE and IDSA.'_&#x20;

_Additionally, to consider ‘Delegation policies may need resource-level granularity. Public product information, DPP resources, certification evidence and event traceability may require different access rules.’_
{% endhint %}

***

## Machine-readable licence policies&#x20;

The iSHARE licence model defines a set of machine-readable usage conditions (for example: internal use only, resharing restricted to adhering parties, certification-linked such as ISO 27001, or country- or sector-restricted). These licences connect operational trust to legal compliance and form the basis for GDDS-level data usage policy enforcement. The GDDS may define additional licence types or constraints as required by Green Deal use cases.&#x20;

Access control operates through role-based and attribute-based models, using the management of user attributes, roles, and group memberships to enforce fine-grained access control policies aligned with organisational, legal, and regulatory requirements. This supports flexible and scalable permission management across diverse user communities and service providers. Pre-access checks are enforced through Policy Enforcement Points (PEP) and Policy Decision Points (PDP),  and agreements are expressed as machine-readable policies, following, for the time being, the iSHARE delegation-evidence and licence model documented in D3.1 (WP3, Section 2.3.2). According to the iSHARE Trust Framework, the Authorisation Registry performs the policy-decision function: it holds the delegation evidence and policies that the Policy Decision Point (PDP) consults, while the Service Provider acts as the Policy Enforcement Point (PEP) at the point of exchange.&#x20;

Machine-readable licence policies take legal effect through the participants' signed [Terms of Use](#user-content-fn-1)[^1] and the corresponding contractual terms. A machine-readable condition and its human-readable contractual expression must correspond, so that enforcement is valid in both technical and legal terms (see Legal Framework, Contractual Framework).

{% hint style="warning" %}
_Note (open): The machine-readable policy language for expressing agreements at GDDS level has not yet been decided. The iSHARE Trust Framework enforcement stack natively uses the XACML-JSON-inspired delegation-evidence format evaluated by the Authorisation Registry (see D3.1, §2.2.2), while ODRL has been discussed as a candidate open format for policy expression. Full ODRL implementation does not yet exist in current connectors; for the time being, therefore, policy requirements are derived from the specific use cases rather than from a full ODRL integration, and this document follows the iSHARE model as documented in D3.1._&#x20;

_Related open topics for co-creation: the licence catalogue and any additional GDDS licence types, the overall policy taxonomy, and the role of the Authorisation Registry in enforcement. Owner: WP4, with WP3._
{% endhint %}

{% hint style="warning" %}
_Note (alignment check, open): A possible overlap or conflict with the Trusted Data Transaction standard (associated with the Gaia-X framework and the Data Transfer Agent) has been flagged for the enforcement approach described here. The current governance and enforcement drafts are to be checked against that standard to confirm compatibility. Owner: WP4, in coordination with the standard's working group._
{% endhint %}

This capability is the technical home for the enforcement mechanisms referenced by the governance rules in Data Sovereignty & Technical Governance (subsection 1, Data access and usage policy governance). The governance rules who sets conditions, which licensing models are offered, and how custom and conditional policies are approved reside there; the policy languages, evaluation points, and runtime enforcement reside here.&#x20;

[^1]: TBD
