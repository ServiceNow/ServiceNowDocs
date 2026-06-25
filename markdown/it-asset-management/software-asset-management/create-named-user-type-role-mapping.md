---
title: Map a role to a named user type
description: You can optimize your SAP licenses by mapping roles to a named user type. During reconciliation, discovered user roles and their assigned named user types are compared against these roles to identify user that can be given a lower named user type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/create-named-user-type-role-mapping.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
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

6.  Select the Add icon \[Omitted image "add-icon.png"\] to move the selected role to the SAP Roles List.

7.  Repeat steps 5 and 6 for each role that you want to map to the named user type.

8.  Select **Save**.


**Parent Topic:**[Software Asset Management publisher pack for SAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/sap-publisher-pack.md)

**Related topics**  


[Tables installed with the SAP publisher pack]()

[Set up SAP integration to establish a connection with SAP]()

[Establish an SAP connection using basic authentication]()

[Establish an SAP connection using OAuth 2.0]()

[Create entitlements for SAP]()

[Create software models for SAP]()

[Create a custom SAP named user type]()

[Create custom SAP price lists]()

[Import custom SAP named user types]()

[Import custom SAP price lists]()

[SAP USMM-based optimization]()

[User transaction activity for named user types]()

[Self-declaring SAP engine license usage]()

[Software Publisher Analytics dashboard for SAP in Software Asset Management classic]()

[Publisher overview for SAP in the Software Asset Workspace]()

