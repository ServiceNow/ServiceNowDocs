---
title: Create custom SAP price lists
description: Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create custom SAP price lists

Create custom SAP price lists so that you can track and manage SAP licenses based on the contracts that are specific to your SAP system.

## Before you begin

Role required: sam\_admin

**Note:** The custom SAP named user types that you create directly on your ServiceNow instance aren’t reflected in your SAP system. You must make the same changes in your SAP system.

**Important:** You can create custom SAP price lists in both the Software Asset Management classic application and the Software Asset Workspace. Use the following steps to create custom SAP price lists in the Software Asset Management classic application. For details on how to create custom SAP price lists in the Software Asset Workspace, see [Create custom SAP price lists in workspace](sap-prcielists-workspace.md).

## Procedure

1.  On the page header of your ServiceNow instance, select **All**.

2.  In the menu navigation filter, enter `samp_price_list_list.do`.

    The Price Lists \[samp\_price\_list\] table opens.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the price list.|
    |Id|Unique identifier for the price list.|
    |Default named user type|Default named user type for the price list.|
    |Active|Option that indicates if the price list is active.|

5.  Select **Submit**.

    You automatically return to the Price Lists \[samp\_price\_list\] table.

6.  Associate SAP named user types with the custom SAP price list.

    1.  From the Price Lists \[samp\_price\_list\] table, select the custom SAP price list that you created.

        The Custom Price List record opens.

    2.  In the **Named User Types** related list, select **New**.

    3.  On the form, fill in the fields.

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

    4.  Select **Submit**.

    5.  Repeat steps a to c for each custom named user type that you want to add.


**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

