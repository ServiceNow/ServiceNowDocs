---
title: Enable chat access for a guest user
description: Enable chat access for a guest user while configuring ServiceNow for Microsoft Teams settings for a pre-published app.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Request-based chat access for a guest user, Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Enable chat access for a guest user

Enable chat access for a guest user while configuring ServiceNow® for Microsoft Teams settings for a pre-published app.

## Before you begin

In an upgrade scenario for a pre-published app, after the upgrade process, you must reauthorize the Request-based chat and SSO and Activity Notifications applications. Reauthorization permits your ServiceNow instance to make API calls to Microsoft Azure. As a result, ServiceNow for the Microsoft Teams application workflow is enabled and your consent for the new API permissions is ensured. For more information, see [Grant permissions to required Microsoft Azure apps](authorize-multi-tenant-apps-mt.md).

Role required: admin

## About this task

Connecting the ServiceNow instance to your Microsoft Teams pre-published app automatically populates the fields tenant id, tenant full name, and source on the Teams Guest User Chat Configuration form. If you want to grant guest user access, enable the guest access in the Teams Guest User Chat Configuration form.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Teams Guest User Chat Configuration**.

2.  On the form, fill in the fields.

<table id="table_udz_vc4_f5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tenant ID

</td><td>

Auto-populated during the pre-published app installation.

 Directory \(tenant\) ID from the application overview page in the Microsoft Azure portal updates details in the ServiceNow instance.

</td></tr><tr><td>

Tenant full name

</td><td>

Auto-populated during the pre-published app installation.

 Full domain name of the tenant or host. For example, account1.onmicrosoft.com.

</td></tr><tr><td>

Enable Guest access

</td><td>

Option to enable the Client Credentials token to fetch user type details.

 If you do not select this check box, then an error occurs when the guest tries to start or import a Microsoft Teams chat.

 **Note:** When the guest access is enabled, the sn\_tcm\_collab\_hook.MS\_Teams\_Chat\_App\_Credentials value in the sys\_alias table configured in Connection &amp; Credential Aliases fetches the Azure user details. When the guest access is inactive, the sn\_tcm\_collab\_hook.MS\_Teams\_Chat\_Credentials value in the sys\_alias table configured in Connection &amp; Credential Aliases fetches the Azure user details.

</td></tr><tr><td>

Allowed Guest domains

</td><td>

The guest user domains where invited guests can start or import a chat. Only the tenants in these domains can start or import a chat.

 List multiple guest domain names as comma-separated values.

</td></tr><tr><td>

Source

</td><td>

Auto-populated during the pre-published app installation.

 This field is associated with the Tenant Connections module.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

Guests belonging to the selected guest domains can now start or import chats.

**Parent Topic:**[Request-based chat access for a guest user](../concept/guest-user-chat-access-mt.md)

