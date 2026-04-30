---
title: Create custom SAP price lists in workspace
description: Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Create custom SAP price lists in workspace

Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.

## Before you begin

Role required: sam\_admin

**Note:** The custom SAP prices lists that you create directly on your ServiceNow instance are not reflected in your SAP system. You must make the same changes in your SAP system.

## Procedure

1.  From the Software Asset Workspace, open the License operations view.

2.  From the left navigation menu of the License operations view, select **Discovery** &gt; **SAP price lists**.

3.  Select **New**.

4.  On the Create New Custom Price List form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the price list.|
    |Id|Unique identifier for the price list.|
    |Default named user type|Default named user type for the price list.|
    |Active|Option that indicates if the price list is active.|

5.  Select **Save**.

    You are automatically redirected to the SAP price list record.

6.  Associate SAP named user types with the custom SAP price list.

    1.  On the **Named User Types** tab of the SAP price list record, select **New**.

    2.  On the Create New Custom Named User Type form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the named user type.|
        |Price List|Price list that you want to associate the named user type with. This field populates automatically.|
        |Is developer|Option that indicates if users with this named user type have a developer role.|
        |Grants access to|Applications that the named user type has access to.|
        |Value|Alphanumerical value that identifies the named user type.|
        |Rank|Priority of the named user type during reconciliation. Lower rank values correlate with a higher priority during reconciliation.|
        |Is licensable|Option that indicates if the named user type can be licensed.|
        |Active|Option that indicates if the named user type is active.|

    3.  Select **Save**.

    4.  Repeat steps a to c for each custom named user type that you want to add.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

