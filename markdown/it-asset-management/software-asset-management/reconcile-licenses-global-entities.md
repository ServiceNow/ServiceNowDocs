---
title: Reconciliation of licenses across global entities
description: Share entitlements across different entities within your organization by creating consumption rules for entitlements.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Reconciliation of licenses across global entities

Share entitlements across different entities within your organization by creating consumption rules for entitlements.

Limit consumption of entitlements to specific set of entities during the reconciliation process. This allows a cost center to purchase licenses and provide it as a service to other cost centers to license software running on their devices without requiring allocations.

## Overview of consumption rules

Create consumption rules for entitlements to restrict all entities from using that entitlement. If a consumption rule isn't defined for an entitlement and when the reconciliation process runs, any entity can use that entitlement regardless of who owns that entitlement.

Consumption rules can be created for the following reconciliation groups:

-   Company
-   Department
-   Region
-   Cost center
-   Country

A single consumption rule can be used across multiple entitlements that helps in reuse of consumption rules.

After you create consumption rules in the License operations view, you must link a consumption rule to one or more entitlements in the **Entitlement Consumption Rules** related list in the entitlement page. After you link a consumption rule to an entitlement, consumption is limited to the users or devices belonging to at least one of the specified entities specified in the consumption rule.

If no active consumption rules exist in the **Entitlement Consumption Rules** related list, anyone in your organization can use the entitlement.

**Note:** Consumption rules aren’t supported for the following license metrics: IBM RVUs, IBM UVUs, and Workday.

Irrespective of grouping, consumption rules apply and licensing is restricted. After you link consumption rules with an entitlement and run the reconciliation process, the following actions take place:

-   with grouping: The reconciliation result appears in the form of product results, software model results, and licenses metric results; all generated individually for each group.
-   without grouping: The reconciliation result appears in the form of product results, software model results, and license metric results, all under a single heading.

The License Consumption Breakdown \[samp\_lmr\_consumption\_result\] table reports the allocated and unallocated rights used per license metric results per consumption rule.

Further reporting can be done through the consumption rule column in the Licenses Required By \[samp\_licenses\_required\_by\] table. The consumption rule column stamps the consumption rule satisfied by that entity.

## Use case for consumption rules

Let's say that you've created three separate consumption rules for three departments, namely Sales, HR, and Marketing.

You now link all these three consumption rules to an entitlement, titled ENT A. After you run reconciliation, ENT A can be used by the Sales, HR, and Marketing departments. No allocations need to be created for ENT A.

## Parent and child hierarchy

Consumption rules also support parent or child hierarchy for groups. If you have a consumption rule for parent company A, you can choose to include child company B and child company C without creating separate rules.

The Create New Consumption Rulepage in the Enterprise Asset Workspace lets you include the children of the company, department, and cost center in the consumption rule. This reduces the effort required to create individual consumption rules for each entity and to update consumption rules when new entities are added, update, or deleted.

## License pools

Consumption rules allow you to define license pools for entities. A license pool is a reservation of rights for a group entity defined on a consumption rule. License pools are specific to an entity per entitlement. If no license pool is defined, the entity can consume rights, but none will be set aside as a guarantee.

For example, an entitlement with 100 available rights can have an HR consumption rule with a license pool of 50. This sets aside 50 rights for HR consumers, and the remaining 50 rights can be used by HR or other entities defined in the consumption rules.

You can view the consumption rules and associated license pools in the **Entitlement Consumption Rules** related list in the entitlement page.

If you don't want license consumption to be limited to entities in the consumption rules, you can use the **Unrestricted consumption** check box on the entitlement page. Once this check box is selected, any entity can consume rights, but the entities in the consumption rules have a reservation of rights set aside.

**Note:** While both allocations and the **Unrestricted consumption** check box allow other groups to access the entitlement; only allocations provide priority.

## Allocations

Allocations take precedence over consumption rules. You don't need to create consumption rules for allocations to work. For example, let's say you have a consumption rule that states that only HR devices can use this entitlement. This entitlement can still include allocations outside of HR such as Sales or Marketing.

Allocations are automatically counted towards license pools when the first applicable consumption rule is satisfied. This is the default setting, but allocations will still be honored even if there is no defined consumption rule or license pool.

Any new allocations that exceed the license pool count will be honored. Any allocations that do not satisfy a consumption rule will also be honored.

## Upgrading from Pre Utah releases

If you're upgrading from a Pre Australia release and based on what you have selected in the **com.snc.samp.recon.group** and **com.snc.samp.recon.subgroup** properties \(in the Software Asset Management Properties page\), the following upgrade actions take place:

-   Grouping: **Company**, **Cost Center**, **Region**, **Department**, or **Country** is selected. A consumption rule is automatically created for the grouping entity selected if the entitlement is in use. For example, if **Department** is selected, and **Company** is selected as the subgroup, then one combined consumption rule is created for both the group, Department and the subgroup, Company. When reconciliation is run, the entitlement usage is restricted to only the Department group and the Company subgroup.

    **Note:** An entitlement is considered to be in use, if in the Entitlement table, the Install status column has the value 1.

-   Non-grouping: **None** is selected. No consumption rule is created as reconciliation runs without grouping. The entitlements can be used by any group.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

