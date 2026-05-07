---
title: Purchase requisition auto-order
description: Auto-order automates the creation of a purchase order \(PO\) from an approved purchase requisition \(PR\) without requiring manual buyer intervention. Two system properties control whether the feature is active and the maximum PR value that qualifies for automatic processing.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-04-21"
reading_time_minutes: 2
keywords: [auto-order, purchase requisition, purchase order, automatic PO creation, requisition auto-order]
breadcrumb: [Sourcing and Purchasing Automation, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Purchase requisition auto-order

Auto-order automates the creation of a purchase order \(PO\) from an approved purchase requisition \(PR\) without requiring manual buyer intervention. Two system properties control whether the feature is active and the maximum PR value that qualifies for automatic processing.

When a PR reaches the state where all activities are complete, the Requisition State Handler flow evaluates the auto-order configuration. If the conditions are met, the flow creates a PO and links it back to the PR automatically. If the conditions are not met, the PR waits for a buyer to create the PO manually.

## How auto-order works

The Requisition State Handler flow performs the following actions during auto-order processing.

1.  A PR is created and reaches the state where all approval activities are complete.
2.  The Requisition State Handler flow evaluates whether auto-order is active and whether the PR total is at or below the configured threshold.
3.  If the auto-order conditions are met, the flow invokes the `CreatePurchaseOrder` script, which validates the PR and builds the PO header and lines from the approved PR lines.
4.  The PO state is set based on the supplier type:
    -   For standard suppliers, the PO state is set to **Pending submission**.
    -   For punchout suppliers, an integration request is sent to the supplier and the PO state is set to **Pending supplier confirmation**.
5.  The PO is linked to the PR, and the PR state is updated to reflect the PO state.

If PR validation fails during PO creation, any partially created PO records are removed and the PR must be handled manually.

## Auto-order system properties

The system properties that control auto-order behavior are described in the following table.

|Property|Description|Default value|
|--------|-----------|-------------|
|**sn\_shop.spend.requisition.autoorder**|Controls whether auto-order is active. Set to `yes` to turn on automatic PO creation. Any other value, including `no`, turns off auto-order and requires a buyer to create the PO manually. If no value is configured, the system treats it as `yes`.|`no`|
|**sn\_shop.spend.requisition.autoorder.threshold**|Sets the maximum PR total, in reference currency, that qualifies for auto-order. PRs with a total above this value require manual PO creation. Set to `0` to apply auto-order to PRs of any amount. If no value is configured, the system treats it as `0`.|`0`|

**Note:**

The threshold is compared against the PR's reference currency amount. In multi-currency instances, configure the threshold value with the instance reference currency in mind to help avoid unexpected results for PRs entered in other currencies.

## Auto-order requirements

All of the following conditions must be true for auto-order to create a PO:

-   The **sn\_shop.spend.requisition.autoorder** property is set to `yes` or has no configured value.
-   The PR total in reference currency is at or below the configured threshold, or the threshold is set to `0`.
-   The PR has at least one line in an approved state.
-   All approved PR lines have valid cost allocation data, including GL account information.

**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

