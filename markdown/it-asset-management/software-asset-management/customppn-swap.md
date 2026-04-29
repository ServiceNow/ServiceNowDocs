---
title: Custom publisher part numbers \(PPN\)
description: Propagate changes to entitlements and software models by replacing your custom PPNs and custom discovery maps \(DMAPs\) with the Software Asset Management Content Service PPNs and DMAPs.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software models and Software entitlements, Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Custom publisher part numbers \(PPN\)

Propagate changes to entitlements and software models by replacing your custom PPNs and custom discovery maps \(DMAPs\) with the Software Asset Management Content Service PPNs and DMAPs.

**Note:** Custom PPNs that use a part number that is not a valid SKU from the publisher can't be replaced.

Once the Content Service updates are downloaded to your instance, the scheduled job, **SAM - Find Product Definition Suggestions**, runs. The scheduled job checks all custom PPN and DMAP records to find corresponding PPN and DMAP matches on the Content Service. If a match for the custom PPN and DMAP is found, then a suggestion record is created in the Part number suggestions \[samp\_sw\_part\_number\_suggestion\] table. You can view the suggestions record by navigating to the **Part number suggestions** option.

**Note:** If you have excluded custom PPNs from the Content Service by selecting the **Exclude from content service** option in the Custom Part Number form, then suggestions aren't shown for those custom PPNs.

**Note:** For details on viewing the suggestion records, see [View publisher part number \(PPN\) suggestions in workspace](../task/view-customppn-workspace.md) or [View publisher part number \(PPN\) suggestions in Software Asset Management classic](../task/View-customppn-classic.md).

You can accept or reject the suggestions. If you accept the suggestion, the custom PPN and DMAP are replaced with the Content Service PPN and DMAP. All changes to entitlements and software models are propagated automatically.

The propagation of the content service PPN results in the following changes:

-   All impacted entitlements are updated with the new PPN.
-   Downgrade rights associated with the content service DMAP gets copied to the entitlement.
-   Downgrade rights that are copied overwrite any existing entries made by you.
-   Values for license type and license metric get modified based on the PPN \(where needed\).
-   Entitlement remains in the **In use**state.

The propagation of the Content Service DMAP results in the following changes:

-   Associated software model is updated with the new DMAP.
-   Fields get impacted on the software model:
    -   Short description, Asset tracking strategy/unit, next version.
    -   Suite components/parents get overwritten with the Content Service DMAP values.
    -   Any custom components that were added are deleted, as stated in a warning.
    -   Life cycles get overwritten \(with a warning message\).

**Parent Topic:**[Software models and Software entitlements](software-models-and-entitlements.md)

