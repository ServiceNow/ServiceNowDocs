---
title: Software reclamation rules
description: Reclamation rules aggregate usage over time and specify a minimum number of hours or the latest date that a software unit must be used before the software is flagged for reclamation.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software reclamation rules

Reclamation rules aggregate usage over time and specify a minimum number of hours or the latest date that a software unit must be used before the software is flagged for reclamation.

## Overview of software reclamation rules

You can avoid purchasing more software rights for products by knowing which rights have already been allocated but are being used infrequently, haven't been used recently enough, or aren't being used at all. Reclamation rules reclaim those software rights so that these rights can be freed up and allocated elsewhere. Reclamation rules are configured to specify a period of time, amount of time, or most recent date that a software unit must be used before the software is flagged for reclamation.

When a reclamation rule is created for a suite parent, the usage for the suite parent as well as that of the suite components are automatically pulled into the rule.

When you create a reclamation rule, you can add software products associated to the reclamation rule. When you add a product, which is a suite parent, all the suite components automatically get added and appear in the Software Products related list in the Reclamation rule form. Similarly, the product processes for all the added software suite products and component products also get added and appear in the Product Processes related list.

**Note:** The products in the Software Products related list are updated based on the content updates in the Software Asset Management Content Service. For example, if a suite component has been added or removed from a suite parent, the change is reflected in the Software Products related list.

After a suite parent is added to a reclamation rule, you can't edit or delete any suite components, but you can edit or delete the suite parent. If you delete the suite parent, the suite components are also automatically deleted along with the product processes. If you edit a suite parent, then the changes of the edit are reflected for the suite components and the associated product processes. For example, if you change the suite parent from Microsoft Office 365 to Microsoft Word, all the suite components and product processes for Microsoft Office 365 get deleted. Microsoft Word becomes the new parent and all suite components and product processes for Microsoft Word are automatically added.

## Filter conditions

You can add a filter condition on a suite parent record. The filter condition that you specify for a suite parent is automatically applied to all the suite components of the parent and the filter condition field on the suite component record is no longer editable. You can, however, edit the filter condition on the suite parent record. You can open a suite parent record from the Software Products related list and specify your filter condition in the record.

You can also specify a filter condition at the reclamation rule level. The filter condition that you specify applies to all the products that belong to the reclamation rule. The filter condition can only be applied when the **Applies to** field in the Reclamation rule form has the value **Installed Software** or **Subscription Software**. For details, see [Add a software reclamation rule](../task/t_AddAReclamationRule.md).

## Reclamation rules for SaaS and SSO applications

When you create a direct integration profile for a SaaS application or connect an SSO application, a reclamation rule is automatically created for the software product. It's important that you review the reclamation rule to verify that it meets your specifications. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

For more information about the reclamation rules for each application, see [Reclamation rules](../reference/reclamation-rules.md).

## Upgrading to Yokohama

If you’re upgrading to Yokohama from any past release, your existing reclamation rules do not automatically take bulk reclamation into account. You must manually set up your existing reclamation rules for bulk reclamation to take effect. For example, in an existing reclamation rule, you have Microsoft Office 365 listed in the Software Installations related list. When you upgrade to Yokohama, you must delete Microsoft Office 365 from the Software Product related list and re-add it to the same reclamation rule to trigger the automatic addition of suite components and their product processes.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

