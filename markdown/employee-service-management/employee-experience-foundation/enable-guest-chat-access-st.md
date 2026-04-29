---
title: Enable chat access for guest users
description: Enable chat access for a guest user while configuring ServiceNow for Microsoft Teams settings for a self-configured app.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request-based chat access for a guest user, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Enable chat access for guest users

Enable chat access for a guest user while configuring ServiceNow® for Microsoft Teams settings for a self-configured app.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

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

Directory \(tenant\) ID from the application overview page in the Microsoft Azure portal.

 Use the ID value to update details in the ServiceNow instance.

</td></tr><tr><td>

Tenant full name

</td><td>

Full domain name of the tenant or host. For example, account1.onmicrosoft.com.

</td></tr><tr><td>

Enable Guest access

</td><td>

Option to enable the Client Credentials token to fetch user type details that were set during the process of [Enable authentication of guest users](update-verify-app-registry-guest.md).

 If you do not select this option, an error occurs when the guest tries to start or import a Microsoft Teams chat.

 **Note:** When the guest access is enabled, the sn\_tcm\_collab\_hook.MS\_Teams\_Chat\_App\_Credentials value in the sys\_alias table configured in Connection &amp; Credential Aliases fetches the Azure user details. When the guest access is inactive, the sn\_tcm\_collab\_hook.MS\_Teams\_Chat\_Credentials value in the sys\_alias table configured in Connection &amp; Credential Aliases fetches the Azure user details.

</td></tr><tr><td>

Allowed Guest domains

</td><td>

The guest user domains where invited guests can start or import a chat. Only the tenants in these domains can start or import a chat.

 List multiple guest domain names as comma-separated values.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Result

Guests belonging to the selected guest domains can start or import chats.

**Parent Topic:**[Request-based chat access for a guest user](../concept/guest-user-chat-access-st.md)

