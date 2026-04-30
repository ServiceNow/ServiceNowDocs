---
title: Link consumption rules to entitlements
description: After you've created a consumption rule, you must link the rule to one or more entitlements.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Link consumption rules to entitlements

After you've created a consumption rule, you must link the rule to one or more entitlements.

## Before you begin

Consumption rules aren't supported for the following license metrics:

-   IBM RVUs
-   IBM UVUs
-   Workday
-   Employee

The Entitlement Consumption Rules related list on the entitlement form doesn’t appear for these license metrics.

Role required: sam\_user

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.

2.  Open the entitlement to which you want to link the consumption rule.

3.  Select the Entitlement Consumption Rules related list.

4.  Select **New**.

    The Create New Entitlement Consumption Rule page opens.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Software entitlement**|The software entitlement to which you’re linking the consumption rule.|
    |**Consumption rule**|The consumption rule that you want to link this entitlement to.|
    |**License pool**|License pool associated to the consumption rule. A license pool is a reservation of rights for a group entity defined on a consumption rule.|

6.  Select **Save**,

    The consumption rule appears in the Entitlement Consumption Rules related list.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

