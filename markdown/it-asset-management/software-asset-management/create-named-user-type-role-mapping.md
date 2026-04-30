---
title: Map a role to a named user type
description: You can optimize your SAP licenses by mapping roles to a named user type. During reconciliation, discovered user roles and their assigned named user types are compared against these roles to identify user that can be given a lower named user type.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for SAP, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Map a role to a named user type

You can optimize your SAP licenses by mapping roles to a named user type. During reconciliation, discovered user roles and their assigned named user types are compared against these roles to identify user that can be given a lower named user type.

## Before you begin

Role required: sam\_admin

## About this task

## Procedure

1.  On the page header of your ServiceNow® instance, select **All**.

2.  In the menu navigation filter, enter `samp_named_user_type_list.do`.

    The Named User Types \[samp\_named\_user\_type\] table opens.

3.  Select the named user type that you want to map a role to.

4.  In the **SAP Roles** related list, select **Edit...**.

5.  In the Collection list on the Edit Members form, search for and select the role that you want to map to the named user type.

6.  Select the Add icon \(![Add icon.](../image/add-icon.png)\) to move the selected role to the SAP Roles List.

7.  Repeat steps 5 and 6 for each role that you want to map to the named user type.

8.  Select **Save**.


**Parent Topic:**[Software Asset Management publisher pack for SAP](../concept/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack](../concept/component-installed-sap-plugin.md)

[Deploy the ABAP program for SAP](import-abap-program-sap.md)

[Establish an SAP connection](add-sap-connection.md)

[Create entitlements for SAP](create-entitlement-sap.md)

[Create software models for SAP](add-software-model-sap.md)

[Create a custom SAP named user type](create-named-user.md)

[Create custom SAP price lists](create-sap-pricelist.md)

[Import custom SAP named user types](import-custom-sap-named-user-type.md)

[Import custom SAP price lists](import-custom-sap-price-list.md)

[SAP USMM-based optimization](../concept/usmm-optimization.md)

[User transaction activity for named user types](../concept/sap-named-user-transaction-activity.md)

[Self-declaring SAP engine license usage](../concept/self-declaring-sap-engine-usage.md)

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic](../reference/dashboard-sap.md)

[Publisher overview for SAP in the Software Asset Workspace](../reference/publisher-overview-sap.md)

