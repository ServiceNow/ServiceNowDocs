---
title: Create a custom SAP named user type
description: Create a custom SAP named user type so that you can track and manage your SAP licenses based on the named user type that is specific to your SAP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-named-user.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create a custom SAP named user type

Create a custom SAP named user type so that you can track and manage your SAP licenses based on the named user type that is specific to your SAP system.

## Before you begin

Role required: sam\_admin

**Important:** You can create custom SAP named user types in both the Software Asset Management classic application and the Software Asset Workspace. Use the following steps to create custom named SAP user types in the Software Asset Management classic application. For details on how to create custom named user types in the Software Asset Workspace, see [Create a custom named user type in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-named-usertypes-workspace.md).

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

**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create entitlements for SAP]()

[Create software models for SAP]()

[Map a role to a named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

