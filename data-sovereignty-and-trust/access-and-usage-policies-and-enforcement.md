# Access & usage policies and enforcement

The iSHARE Framework provides a comprehensive set of tools to ensure proper access and usage policies and enforcement. Most notably:

* The framework defines [the role of an Authorisation Registry](https://framework.ishare.eu/is/framework-and-roles)
* Entitled Parties are enabled in exercising data sovereignty by providing delegations (as described in the [generic use cases](https://framework.ishare.eu/is/use-cases)) to parties to use their data
* [Licenses](https://framework.ishare.eu/is/licenses) further specify to legal boundaries of the data usages
* The [structure of delegation evidence](https://framework.ishare.eu/is/structure-of-delegation-evidence) is well defined in the framework and on the [dev portal](https://dev.ishare.eu)

{% hint style="info" %}
iSHARE provides a generic approach for delegations, including generic licenses. The data space can decide to provide better guidance or standards on the semantics of delegations (specifically for policy->target) and to allow more detailed licenses.
{% endhint %}

{% hint style="info" %}
**DSSC Description**

This building block aims to specify how to define and enforce access and usage policies within a data space and how participants define their policies in data spaces. It is of significant importance for every business operation and actual data transaction (sharing, processing) within a data space, and it is essential for enabling data sovereignty in data spaces.

The primary aspect of this building block is a policy, either an offer from the data provider or an agreement between the data provider and the data recipient. A policy is comprised of rules that specify the rights and duties of the parties concerning the policy. These rules can have different forms that indicate how these should be enforced during a data transaction:

Access Rules: define whether access to a resource is allowed or not.

Usage Rules: define how a resource might or may not be used.

Consent Rules: define whether usage of a resource, for which consent might be required from third parties, is allowed or not.

Access control policies control the authorisation to access specific data while the data rights owner retains direct control over the data. Usage policies, including consent, regulate the permissible actions and behaviours related to the utilisation of the accessed data, which means keeping control of data even after the items have left the trust boundaries of the data owner. Both types of policies are the units of business transactions within a data space as part of a data product offering. In Figure 1, we show an overview, as introduced by the International Data Spaces Association (IDSA), of how various types of policies play a role at different levels in data spaces.

These policies can be developed at the data space level as part of the rulebook, which all participants should adhere to. Still, every participant should also be able to exercise their data sovereignty, defining their own data access and usage policies. In this context, there are three primary considerations:

Policy negotiation constitutes the agreement on the compatibility between two policies.

The authorisation registry helps to enforce the organisation's policies.

Some domains may be affected by concrete regulations for the enforcement of policies. As part of this building block, we will also address the unique challenges of policy enforcement in the context of personal data, which usually involves the application of consent.

In summary, the purpose of a data space is to control data sharing, which cannot be realised without policy enforcement.

The complete description is available [here](https://dssc.eu/space/BVE2/1071256095/Access+&+Usage+Policies+Enforcement).
{% endhint %}
