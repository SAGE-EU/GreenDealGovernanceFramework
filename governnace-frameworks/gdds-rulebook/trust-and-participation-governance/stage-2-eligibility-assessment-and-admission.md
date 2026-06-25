# Stage 2 — Eligibility assessment and admission

Admission depends on meeting the GDDS eligibility criteria. The eligibility model operates on two layers:&#x20;

* GDDS baseline layer: a lightweight set of minimum criteria applied uniformly to all applicants at the GDDS levlow-frictionlow friction at the point of first entry. Focuses on verifiable legal identity and the signing of legal and governance agreements. This baseline does not include sector-specific or Green Deal relevance criteria as mandatory entry requirements — these were assessed and rejected as too restrictive for the initial phase.&#x20;
* Data Sharing Group (DSG) layer: additional or stricter eligibility requirements may be applied at the level of individual Data Sharing Groups, set by the relevant DSG orchestrator. These are not GDDS-wide requirements; they reflect domain-specific contexts and use case needs. [(Current UCs to become DSGs](#user-content-fn-1)[^1])

The following design principles govern the eligibility model:&#x20;

* Criteria must be objective, assessable, and — where possible — automated.&#x20;
* The applicable EU regulations (DGA, Data Act, GDPR) do not directly mandate a fixed list of onboarding requirements for data space participants. The eligibility requirements defined here are governance choices made by the GDDS consortium.&#x20;
* A phase-based approach applies: the initial phase is inclusive, with graduated quality and compliance checks added as the ecosystem matures.&#x20;

Stricter verification at the GDDS baseline level may be legally required in the following scenarios, regardless of DSG-level rules:&#x20;

* Sharing of personal data&#x20;
* Financial transactions&#x20;
* AI training scenarios&#x20;
* Official policy monitoring or reporting with legally binding obligations&#x20;

{% hint style="info" %}
Green Deal alignment criteria were explicitly assessed and rejected as a mandatory entry requirement for the GDDS baseline. They may be applied at DSG level where relevant to a specific domain.&#x20;
{% endhint %}

***

## 2.1  Eligibility criteria (Initial proposal)&#x20;

Application requirements are classified into two tiers to minimise friction at initial entry while ensuring all necessary information is collected before admission is confirmed:&#x20;

* &#x20;
* Primary requirements — collected at initial submission, sufficient to classify and begin assessing the candidate.&#x20;
* Secondary requirements — collected later, triggered by role selection or specific onboarding steps, with applicants informed of them upfront.&#x20;

The following design principles are suggested to be applied to the application process:&#x20;

* Infrastructure readiness questions (connector deployment readiness, cloud provider setup, technical implementation details) must be presented early in the application form — not at the end — to prevent applicants discovering blockers only after completing all other fields.&#x20;
* Applicants must be provided with upfront guidance material (a checklist or FAQ page, analogous to government guidance pages) listing all documents and information that will be required at each stage of the process. This avoids bottlenecks at advanced stages.&#x20;
* A lightweight initial application is the default. Stricter checks are applied progressively as the applicant advances through the admission workflow.&#x20;
* The feasibility of automating information retrieval via registration numbers and tax codes is to be investigated to reduce manual data entry burden for applicants.&#x20;

The table below sets out the proposed application form field structure, organised by category. Fields are a mix of primary and secondary requirements; the exact primary/secondary classification is subject to finalisation.&#x20;

| Legal                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | Governance                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Technical                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>Name of entity </li><li>Legal status &#x26; legal form </li><li>Registration number(s) </li><li>Jurisdiction of incorporation </li><li>Ownership structure, including relevant subsidiaries (where applicable) </li><li>Publicly accessible website </li><li>Designated contact person(s), email &#x26; address </li><li>Technical &#x26; organisational measures (e.g.data security safeguards, access control mechanisms, tools for granting and withdrawing consent or permissions) </li><li>Estimated commencement date where different from admission date </li><li>▸  Self-declaration on integrity &#x26; past sanctions </li><li>GDPR compliance statement / legal transfer mechanism </li><li>For natural persons: role-specific attestation &#x26; legal basis </li></ul><p> </p><p> </p> | <ul><li>Intended GDDS role(s): Data Provider / Recipient / Rights Holder / Intermediary / Service Provider </li><li>Description of GDDS activities intended </li><li>Nature &#x26; categories of data (incl. personal data)  </li><li>Data Sharing Group(s) to join (and eligibility for those DSGs) (TBD — confirm scope with WP6) </li><li>Mandate/proxy if applying on behalf of another entity </li><li>Confirmation of authority to enter binding agreements </li></ul><p> </p><p> </p> | <ul><li>Organisation identifier: LEI · EORI · VAT · eIDAS Org ID  </li><li>Identity pathway: Org / Academic (eduGAIN) / Individual (eIDAS) </li><li>Minimum assurance level achieved (Low / Substantial / High) </li><li>PKI certificate / X.509 CSR (for M2M participants) </li><li>Conformance testing result (Intermediaries &#x26; Service Providers) (TBD — confirm scope with WP2/WP3) </li><li>Digital certificate from accredited CA (for certified roles) </li><li>Sector certifications (ISO 27001, CSRD, etc. — optional) </li></ul><p> </p><p> </p> |

### 2.1.1 Eligibility Criteria per Role&#x20;

The previously listed criteria per category are also suggested to be divided by role. So there is a clear distinction in the onboarding flows, and on who needs to fulfil what requirement. The table below represents a working proposal developed in Co-Creation Sessions 8 and 9 (28th of May, 2026), following the initial list of requirements that is showcased above per legal, governance and technical requirements.&#x20;

| Criterion                                                                              | Data Provider  | Data Recipient  | Data Rights Holder  | Intermediary   | Service Provider  |
| -------------------------------------------------------------------------------------- | -------------- | --------------- | ------------------- | -------------- | ----------------- |
| EU/EEA establishment OR legally authorised EU representative                           | ✓ Required     | ✓ Required      | ✓ Required          | ✓ Required     | ✓ Required        |
| Legal capacity to enter binding agreements                                             | ✓ Required     | ✓ Required      | ✓ Required          | ✓ Required     | ✓ Required        |
| Verifiable legal identity — LEI · VAT · eIDAS Org ID · iSHARE DID                      | ✓ Required     | ✓ Required      | ✓ Required          | ✓ Required     | ✓ Required        |
| Self-declaration: past sanctions, investigations, prior exclusions                     | ✓ Required     | ✓ Required      | ✓ Required          | ✓ Required     | ✓ Required        |
| GDPR compliance statement (non-EEA: adequacy decision / SCCs / BCRs)                   | ✓ Required     | ✓ Required      | ✓ Required          | ✓ Required     | ✓ Required        |
| Eligibility for requested Data Sharing Group(s) — per DSG-specific rules               | Per DSG rules  | Per DSG rules   | Per DSG rules       | Per DSG rules  | Per DSG rules     |
| PKI certificate / X.509 eSeal — M2M connector participants                             | ✓ Required     | ✓ Required      | N/A                 | ✓ Required     | ✓ Required        |
| Conformance testing + digital cert from accredited CA (certified roles — TBC WP2/WP3)  | Optional       | Optional        | N/A                 | ✓ Required     | ✓ Required        |
| Sector certification (ISO 27001, CSRD, domain accreditation) — optional / per DSG      | Optional       | Optional        | Optional            | Recommended    | Recommended       |

{% hint style="warning" %}
_Note: The eligibility-criteria table is a working proposal from Co-Creation Sessions 8 and 9 (28 May 2026), subject to review and formal approval by WP4 and UNIBO. Conformance-testing scope for Intermediaries and Service Providers is to be confirmed with WP2 and WP3. Personal data collected via the application form requires an explicit lawful basis, and the GDDS Privacy Policy must cover data received from identity providers — coordinate with UNIBO for legal review. The primary/secondary classification of application fields is subject to finalisation._&#x20;
{% endhint %}

***

## 2.2 Admission and Governance oversight&#x20;

The admission workflow operates under the oversight of the GDDS governance structure. The following bodies are involved in the admission process:&#x20;

* Council of Participants sets the eligibility rules, policies, and frameworks within which the admission process operates. Admission criteria changes require Council approval.&#x20;
* Data Space Governance Authority (DSGA): manages the admission process and conducts compliance review. Holds the accept/reject authority.&#x20;
* Supervisory Board: provides independent oversight of the admission process and may review systemic issues or complaints.&#x20;
* Compliance and Ethics Committee: ensures ethical and compliance standards are met in admission decisions, particularly in cases involving sensitive data categories or high-risk roles.&#x20;
* GDDS Operator: handles  identity verification (Step 1.2) and technical onboarding (Step 5) under DSGA oversight.&#x20;

<figure><img src="../../../.gitbook/assets/Rulebook_Diagrams.png" alt=""><figcaption></figcaption></figure>

Overarching design principle: despite the multi-body governance structure, the applicant-facing admission process must be lightweight and as frictionless as possible. Governance complexity is managed in the back end; it must not create unnecessary barriers for applicants.&#x20;

***

## 2.3 Rejection and Appeal Procedure&#x20;

This subsection defines what happens when an application for admission is not accepted, and the applicant’s right to contest that decision. It complements the onboarding and admission procedures and ensures that rejections are reasoned, consistent, and reviewable.&#x20;

### Grounds for rejection (hybrid model)&#x20;

Rejection follows a hybrid model that combines a closed list of hard disqualifiers with a principle-based assessment for borderline cases:&#x20;

* Hard disqualifiers (exhaustive) — for example, failure to pass identity verification; a legal or sanctions bar to participation; or refusal to sign the Rulebook, or DPA.&#x20;
* Principle-based assessment (soft cases) — eligibility judgements decided by the designated admission authority against documented criteria, with the reasons recorded.&#x20;

### The rejection decision&#x20;

A rejection must be issued in writing, stating the reasons and the basis for the decision (the specific disqualifier or criterion relied upon).&#x20;

Responsible: Data Space Governance Authority (DSGA) on Data Space Level. &#x20;

{% hint style="warning" %}
_Note: Based on the cocreation session on 11th of June 2026, the WP4 group suggested to preserve independence, the appeal should be heard by a body other than the one that issued the rejection — proposed: the Supervisory Board (strategic oversight) or the Compliance & Ethics Committee (independent oversight). Open points remaining: Confirm also any re-application waiting period._&#x20;
{% endhint %}

### Right of appeal&#x20;

An applicant may appeal a rejection. Therefore, the contest mechanism is as follows:&#x20;

1. The rejection is issued with written reasons and its legal or criteria basis.&#x20;
2. The applicant may contest the decision within 5 working days.&#x20;
3. The reviewing body must respond within 5 working days.&#x20;
4. The final decision is recorded, and any terms for re-application are stated.&#x20;

<figure><img src="../../../.gitbook/assets/Rulebook_Diagrams (1).png" alt=""><figcaption></figcaption></figure>

### Outcome&#x20;

If the appeal succeeds, the application proceeds through the normal admission procedure. If it is rejected, the applicant is informed of the final decision and of any conditions or waiting period before re-application. &#x20;

***

## 2.4 Final admission procedures&#x20;

In this step, the applicant should complete the final application steps to be admitted. &#x20;

The DSGA must notify the participant of the decision of the eligibility review. Upon Admission, the DSGA must request the participant to sign the Data Space Participant Agreement, to adhere to the GDDS Rulebook and accept the service level agreements depending on the role chosen. &#x20;

These agreements can be found in the Section of [Contractual Frameworks](../../../contractual-frameworks.md).

{% hint style="warning" %}
Note: There might be additions in this section, or in the Contractual framework section about some rules on how long they have to sign, descrption of the suggested process, automated etc.  &#x20;
{% endhint %}

[^1]: TBD
