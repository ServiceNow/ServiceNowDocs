---
title: Register and configure the Request-based chat application on the Microsoft Azure portal
description: Create a Microsoft Azure application in Microsoft Azure portal to enable agents to import the conversations from Microsoft Teams to ServiceNow.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration for Employee Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, Microsoft Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Register and configure the Request-based chat application on the Microsoft Azure portal

Create a Microsoft Azure application in Microsoft Azure portal to enable agents to import the conversations from Microsoft Teams to ServiceNow.

## Before you begin

Role required: admin

**Note:** You can use one Microsoft Azure application if you use both **IT Service Management integration with Microsoft Teams**, and **HR Service Delivery integration with Microsoft Teams** applications.

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Select **New registration**.

    The **New registration** page displays.

4.  On the **New registration** form, perform the following actions:

    1.  Name: Enter the name of your application. `Example: Request based chat app.`
    2.  Redirect URI: Enter `https://<instance-name>/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance.
    3.  If you're prompted to select a supported account type, select **Accounts in any organizational directory**
5.  Select **Register**.

6.  Select **Redirect URIs**.

    ![App registration in azure portal](../images/register-app-req-based-chat.png)

7.  Select the **Access tokens** check box.

8.  Select **Configure**.

9.  Navigate to **Manage** &gt; **Certificates &amp; secrets**.

    ![Certificates and secrets screen](../images/certificates-secrets.png)

10. Select **New client secret**.

    ![Add client secret](../images/add-client-secret.png)

11. On the Add a client secret form, fill the fields.

    1.  Description: Provide the description for the client secret.

    2.  Expires: Select the expiry date for the client secret using the drop-down menu.

    3.  Select **Add**.

    4.  Copy and save the client secret in a notepad.

        ![Client secret value](../images/client-secret-value.png)


-   **[Add permissions to the Microsoft Azure application](authenticate-users-req-based-chat.md)**  
Assign permissions to users to enable them to start chat and import chat conversations with employees from Microsoft Teams to ServiceNow® instance.
-   **[Configure Application Registry on the ServiceNow instance](app-registry-chat-single-tenant.md#)**  
Register the Request-based chat app in your instance to use Microsoft Teams chat for self-configured app environment.

**Parent Topic:**[Setup for integrating self-configured apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_s_tnt.md)

