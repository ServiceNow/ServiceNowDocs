---
title: Configure Application Registry on the ServiceNow instance
description: Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment.Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment by editing existing Microsoft Teams Chat self-configured app application registry.Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment by creating a Microsoft Teams Chat self-configured app application registry.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Request-based chat on the Microsoft Azure portal, Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure Application Registry on the ServiceNow instance

Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment.

You can register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment using one of the following methods.

-   [Edit existing Microsoft Teams Chat self-configured app application registry](app-registry-chat-single-tenant.md#) \(Recommended\)
-   [Create an application registry for Microsoft Teams chat self-configured app](app-registry-chat-single-tenant.md#)

**Parent Topic:**[Register and configure the Request-based chat application on the Microsoft Azure portal](register-app-req-based-chats.md)

## Edit existing Microsoft Teams Chat self-configured app application registry

Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment by editing existing Microsoft Teams Chat self-configured app application registry.

### Before you begin

Role required: oauth\_admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Search and select **Microsoft Teams Chat Single Tenant** application registry.

3.  Fill in the details **Client ID** and **Client Secret** on the form.

4.  Select **Save**.

5.  **All** &gt; **ServiceNow for Microsoft 365 ** &gt; **Properties**

6.  Enable the option **Set this property to true to use integration hub action for Start Chat / Import chat flows** on the ServiceNow for Microsoft Teams properties form

    The OAuth profile property **Sys ID of OAuth profile for single tenant setup** is set to default \(OOB\) when shipped with application registry.

7.  Select **Save**.


## Create an application registry for Microsoft Teams chat self-configured app

Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment by creating a Microsoft Teams Chat self-configured app application registry.

### Before you begin

**Note:** Use this procedure only if it is absolutely required.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  Select  **Connect to a third party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_yqx_1h3_wqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter: Microsoft Teams chat self-configured app

</td></tr><tr><td>

Client ID

</td><td>

Client ID created in Azure portal. Provide the value of the Azure application ID in this field.

</td></tr><tr><td>

Client Secret

</td><td>

The password you generated when creating the app in Microsoft Teams. For more information, see [Register and configure the Request-based chat application on the Microsoft Azure portal](register-app-req-based-chats.md).

</td></tr><tr><td>

Authorization URL

</td><td>

Authorization URL that includes the tenant ID of your app with the format https://login.microsoftonline.com/\{tenantid\}/oauth2/v2.0/authorize

 where is the tenant ID created during the app creation in Microsoft Teams.

</td></tr><tr><td>

Token URL

</td><td>

Token URL that includes the tenant ID of your app with the format https://login.microsoftonline.com/\{tenantid\}/oauth2/v2.0/token

 where is the tenant ID created during the app creation in Microsoft Teams.

</td></tr><tr><td>

Redirect URL

</td><td>

Redirect URL that includes the instance URL with the format https://&lt;instanceURL&gt;/oauth\_redirect.do

 Update the &lt;instanceURL&gt; value with your instance URL.

</td></tr></tbody>
</table>    ![Microsoft Teams Chat Single Tenant form](../images/chat-single-tenant-oauth-entity.png)

5.  Select **OAuth Entity Scopes** related list.

6.  Add the following scopes.

    -   Enter `Default` in **Name** and enter `.default` in **OAuthscope**.
    -   Enter `Offline Access` in **Name** and enter `offline_access` in **OAuthscope**.
7.  Select **Save**.

    System generates an OAuth Entity profile.

8.  See OAuth Entity Profile details in the related list **OAuth Entity Profiles**.

9.  Open the OAuth Entity Profile record and copy the Sys ID.

10. Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Properties**.

11. Enable the option **Set this property to true to use integration hub action for Start Chat / Import chat flows** on the ServiceNow for Microsoft Teams properties form.

12. Enter the copied OAuth Entity Profile value in the field **Sys ID of OAuth profile for single tenant setup. This needs to be setup if you are setting "sn\_tcm\_collab\_hook.teams\_use\_ih\_actions\_for\_single\_tenant" to true**.

13. Select **Save**.


