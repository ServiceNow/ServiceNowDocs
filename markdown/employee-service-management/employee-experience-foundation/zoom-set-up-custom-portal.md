---
title: Set up a custom portal
description: Configure the ServiceNow Employee Center portal appearance of your organization’s custom portal in Zoom.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Employee Center for Zoom, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Set up a custom portal

Configure the ServiceNow® Employee Center portal appearance of your organization’s custom portal in Zoom.

## Before you begin

Role required: admin

## Procedure

1.  Log in to your ServiceNow instance.

2.  In the navigation filter, enter `sys_properties.list`.

3.  Create the custom portal.

    1.  Select the **Show column search row** icon, enter `sn_ex_ec_zm.portal.suffix` in the **Name** search field, and press **Enter**.

    2.  Select **sn\_ex\_ec\_zm.portal.suffix**.

    3.  On the System Property form, enter your custom portal suffix in the **Value** field.

    4.  Select **Update**.

        **Note:**

        Because the system property is domain separated, different domain admins can create different custom portals.

4.  Create a custom header for the embedded portal.

    1.  In the Navigator pane, type `sys_response_header.list`.

    2.  Select **New**.

    3.  On the form, fill in the fields.

<table id="table_lq5_5ct_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to make the HTTP response header configuration active.

</td></tr><tr><td>

Application

</td><td>

Application scope for the custom portal record.

</td></tr><tr><td>

Applies to

</td><td>

Select **Specify Type**.

</td></tr><tr><td>

Type

</td><td>

Type of record the HTTP response header configuration applies to

 , in this case, Service Portal \(Service Portal \[sp\_portal\]\) records.

</td></tr><tr><td>

Record

</td><td>

The record for your custom portal.

</td></tr><tr><td>

Name

</td><td>

Name for the name-value pair for the HTTP response header for example, Content-Security-Policy.

 `Content-Security-Policy`

</td></tr><tr><td>

Value

</td><td>

Value you want to assign to the name-value pair for the HTTP response header.

 `frame-ancestors ‘self’ https://zoom.us`

</td></tr><tr><td>

Description

</td><td>

Description for the HTTP response header.

</td></tr></tbody>
</table>    4.  Select **Submit**.

        For more information about adding a header, see [Configure HTTP response headers](https://www.servicenow.com/docs/access?context=configure-http-response-header&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).


**Parent Topic:**[Employee Center for Zoom](zoom-ec-create-app.md)

