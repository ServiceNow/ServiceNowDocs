---
title: Create a custom named user type in workspace
description: Create a custom named user type that can be used with your SAP software entitlement in the Software Asset Workspace. Creating a custom named user type allows users to track licenses that are specific to their SAP systems.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License operations view, Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create a custom named user type in workspace

Create a custom named user type that can be used with your SAP software entitlement in the Software Asset Workspace. Creating a custom named user type allows users to track licenses that are specific to their SAP systems.

## Before you begin

Role required: sam\_admin or sam\_user

**Note:** The custom SAP named user types that you create directly on your ServiceNow instance are not reflected in your SAP system. You must make the same changes in your SAP system.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace** &gt; **License operations**.

2.  Select **SAP named user types**.

3.  Select **New** and fill in the details.

    |Field|Description|
    |-----|-----------|
    |Name|Name of custom named user.|
    |Price list|Default price list.|
    |Is developer|Indicates the user has a developer role.|
    |Grant access to|Grant access to a named user type.|
    |Value|Value associated with the named user type. This value can be either numbers or letters.|
    |Rank|Priority of the named user type during reconciliation. Lower rank values take precedence.|
    |Is licensable|Indicates the named user type license status.|
    |Active|Indicates if the named user type is active.|

4.  Select **Save**.

    The named user type is added to the Named User Types list.


