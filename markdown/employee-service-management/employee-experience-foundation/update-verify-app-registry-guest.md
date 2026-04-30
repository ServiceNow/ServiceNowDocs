---
title: Enable authentication of guest users
description: Verify and update application registry values to authenticate guest users in the Microsoft Teams application to start and import chats for a self-configured app.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Request-based chat access for a guest user, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Enable authentication of guest users

Verify and update application registry values to authenticate guest users in the Microsoft Teams application to start and import chats for a self-configured app.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select the Microsoft Teams Chat Single Tenant application registry.

3.  On the form, verify and update the fields.

<table id="table_wmt_s3p_g5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the record. For example, Microsoft Teams Chat self-configured app, Microsoft Teams Chat App Permission ST, and so on.

</td></tr><tr><td>

Client ID

</td><td>

Application ID created in the Microsoft Azure portal.

</td></tr><tr><td>

Client Secret

</td><td>

Password generated during the app creation process in ServiceNow for Microsoft Teams.

</td></tr><tr><td>

Authorization URL

</td><td>

Authorization URL that includes the tenant ID that was generated during the creation of your app in ServiceNow for Microsoft Teams in the following format: `https://login.microsoftonline.com/<tenantid>/oauth2/v2.0/authorize`

</td></tr><tr><td>

Token URL

</td><td>

Token URL that includes the tenant ID of your app that was generated during creation in ServiceNow for Microsoft Teams in the following format: `https://login.microsoftonline.com/<tenantid>/oauth2/v2.0/token`

</td></tr><tr><td>

Redirect URL

</td><td>

Redirect the URL that includes your ServiceNow for Microsoft Teams instance URL in the following format: https://&lt;instanceURL&gt;/oauth\_redirect.do

</td></tr></tbody>
</table>4.  Select **Save**.

5.  Navigate to **ServiceNow for Microsoft Teams** &gt; **Properties**.

6.  Select the option **Set this property to true to use integration hub action for Start Chat / Import chat flows**.

7.  Select **Save**.

8.  Repeat this procedure for the Microsoft Teams Chat App Permission ST application registry.


**Parent Topic:**[Request-based chat access for a guest user](../concept/guest-user-chat-access-st.md)

