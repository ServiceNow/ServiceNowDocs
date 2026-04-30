---
title: Grouping and consumption rules in reconciliation
description: Grouping and consumption rules can work in tandem during the reconciliation process in the Software Asset Management application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-20"
reading_time_minutes: 1
breadcrumb: [Software reconciliation for compliance, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Grouping and consumption rules in reconciliation

Grouping and consumption rules can work in tandem during the reconciliation process in the Software Asset Management application.

Grouping is a reconciliation configuration that controls how reconciliation results are displayed. Results are broken down by the entitlement owner, determined by the group and the subgroup set. For example, if you choose to group by company during reconciliation, the results display only the entitlements associated with the products and owned by that specific company. However, this doesn’t imply that these entitlements are exclusively used by the selected company; other companies may also use them.

Consumption rule is a methodology to restrict entitlement consumption to a particular group or combination of groups. For details on consumption rules, see [Reconciliation of licenses across global entities](reconcile-licenses-global-entities.md).

You can create a consumption rule by specifying any combination, such as company, department, and country. Only installations that match these criteria are eligible to use that entitlement. However, it's not restricted solely to the group with which you perform reconciliation.

**Note:** Consumption rules aren’t automatically added to new entitlements.

Grouping doesn't affect licensing. Licensing remains the same whether you run reconciliation with or without grouping.

Licensing rules can only be altered if you employ both grouping and consumption rules simultaneously or use just consumption rules. Using grouping by itself doesn’t change the licensing rules.

-   **[Use cases for grouping and consumption rules](usecases-grouping-consumptionrules.md)**  
Learn how grouping and consumption rules are used during the reconciliation process through some use cases.

**Parent Topic:**[Software reconciliation for compliance](c_SAMReconciliation.md)

**Related topics**  


[Use cases for grouping and consumption rules](usecases-grouping-consumptionrules.md)

