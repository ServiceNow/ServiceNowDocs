---
title: Create a custom SAP named user type
description: Create a custom SAP named user type so that you can track and manage your SAP licenses based on the named user type that is specific to your SAP system.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a custom SAP named user type

Create a custom SAP named user type so that you can track and manage your SAP licenses based on the named user type that is specific to your SAP system.

## Before you begin

Role required: sam\_admin

**Important:** You can create custom SAP named user types in both the Software Asset Management classic application and the Software Asset Workspace. Use the following steps to create custom named SAP user types in the Software Asset Management classic application. For details on how to create custom named user types in the Software Asset Workspace, see [Create a custom named user type in workspace](sap-named-usertypes-workspace.md).

## About this task

**Note:** The custom SAP named user types that you create directly on your ServiceNow instance are not reflected in your SAP system. You must make the same changes in your SAP system.

## Procedure

1.  On the page header of your ServiceNow® instance, select **All**.

2.  In the menu navigation filter, enter `samp_named_user_type_list.do`.

    The Named User Types \[samp\_named\_user\_type\] table opens.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of custom named user.|
    |Price list|Default price list.|
    |Is developer|Option that indicates the user has a developer role.|
    |Grants access to|Grant access to a named user type.|
    |Value|Value associated with the named user type. This value can be either numbers or letters.|
    |Rank|Priority of the named user type during reconciliation. Lower rank values take precedence.|
    |Is licensable|Option that indicates the named user type license status.|
    |Active|Option that indicates if the named user type is active.|

5.  Select **Submit**.


## Result

The named user type is added to the Named User Types \[samp\_named\_user\_type\] table.

## What to do next

After you have added the custom named user, create a software model designating the custom named user in the form.

**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Map a role to a named user type](create-named-user-type-role-mapping.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

