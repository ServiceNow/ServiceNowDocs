---
title: Set up Microsoft Office 365 integration for Walk-up Experience
description: Enable Walk-up Experience Microsoft Office 365 calendar integration. When requesters make an appointment, modify it, or cancel it, the Outlook calendar is sent invites to an appointment and any updates.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integrate Microsoft Office 365 calendar with Walk-up Experience, Configure, Walk-up Experience, IT Service Management]
---

# Set up Microsoft Office 365 integration for Walk-up Experience

Enable Walk-up Experience Microsoft Office 365 calendar integration. When requesters make an appointment, modify it, or cancel it, the Outlook calendar is sent invites to an appointment and any updates.

## Before you begin

Logging into the Microsoft Azure Portal \([https://portal.azure.com](https://portal.azure.com/)\) with your specific customer account is necessary. You will already have a tenant, as logging into the portal requires access to this tenant. For details about setting up a tenant, refer to [Quickstart: Set up a tenant](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-create-new-tenant).

Also required is that you have a Microsoft Office 365 subscription linked to an existing tenant. For details regarding this, refer to [Set up a Microsoft 365 developer subscription](https://docs.microsoft.com/en-us/office/developer-program/microsoft-365-developer-program-get-started).

See the required permissions for Microsoft Azure client setup at [Set up Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) [Set up Microsoft Exchange Online spoke](https://www.servicenow.com/docs/access?context=setup-ms-exch-ol&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

![Video icon](../../itsm-virtual-agent/image/icon-video-link.png) [Virtual Agent Academy: Get service faster with Virtual Agent and Walk-Up Experience](https://www.youtube.com/watch?v=hE5weOQVFe4&list=PLkGSnjw5y2U79gjQuQW-2GBqzEccwFkWH) \(video from the Virtual Agent Academy\)

Role required: admin

## Procedure

1.  Confirm that the Walk-up Experience \(com.snc.walkup\), Microsoft Exchange Online Spoke \(sn\_ex\_online\_spke\), and Microsoft Exchange Server Spoke \(sn\_exchange\_spoke\) plugins are activated on your instance.

2.  Navigate to **System Oauth** &gt; **Application Registry** &gt; **Microsoft Exchange Online** to set up Oauth.

    1.  Insert the client ID \(Application ID\), which you can get from the Microsoft Entra ID application.

    2.  Insert the client secret, which you can get from the Microsoft Entra ID application.

    3.  Copy and paste the following links to access authorization, token, and redirect:

        -   Authorization url: https://login.microsoftonline.com/&lt;tenant-ID&gt;/oauth2/v2.0/authorize
        -   Token url: https://login.microsoftonline.com/&lt;tenant-ID&gt;/oauth2/v2.0/token
        -   Redirect url: https://&lt;instance-name&gt;.service-now.com/oauth\_redirect.do
3.  Navigate to **Connections &amp; Credentials** &gt; **Credentials** to set up credentials.

    1.  Click **New**.

    2.  Choose **OAuth 2.0 Credentials**.

    3.  In the OAuth 2.0 Credentials new record provide a name for the Credential and in the **OAuth Entity Profile** form field, choose **Microsoft Exchange Online default\_profile**.

    4.  Click **Save**.

    5.  Select **Get OAuth Token** in the Related Links section of the form.

    6.  Sign in as a valid user on the Microsoft Exchange Tenant.

4.  Navigate to **Connections and Credentials Aliases** to set up connection.

    1.  Select **Microsoft Exchange Online**.

    2.  In the **Connections** Related Links, click **New**.

    3.  Name the connection `Exchange_Online_Connection` and choose the previously created credential in the **Credential** form field.

    4.  In the Connection URL field, enter: `https://graph.microsoft.com`.

5.  Navigate to **Flow Designer** to enable flows.

    1.  Select **Create Walk-up Appointment Calendar Event**, open in Workflow Studio, and activate.

    2.  Select **Update/Delete Walk-up Appointment Calendar Event**, open in Workflow Studio, and activate.

6.  Schedule an appointment to confirm everything is working properly.

    1.  Create a new test user in the system.

        Refer to [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for details.

        **Note:** Provide a user ID, first name, last name, password and email for the test user.

    2.  Impersonate the test user in your instance.

    3.  Navigate to **Self-Service** &gt; **Service Portal** &gt; **Walk-up Check-in** to schedule an appointment.

        **Note:** The **Walk-up Check-in** icon link must be configured to appear on the Service Portal landing page for you to see and click the link. Refer to [Configure Walk-up Experience online check-in icon to appear on Service Portal](add-walkup-checkin-icon-to-servport.md) if the link is not on the Service Portal landing page.

    4.  Schedule an appointment as the test user.

7.  Verify everything is working correctly by navigating to **Flow Designer** &gt; **Today's Executions**.

8.  Click **Create Walk-up Appointment Calendar Event**.

9.  Check the test user's corporate Microsoft Office 365 calendar to see the emailed calendar event.

    **Note:** It can take a minute or two before the calendar event is created. After you enable this feature, users automatically receive calendar invites, updates, and cancellations on their individual corporate calendars.


-   **[Register an application using the Microsoft Azure portal](register-an-application-using-the-microsoft-azure-portal.md)**  
Grant authorization to the ServiceNow instance by registering an application with Azure AD.
-   **[Register Microsoft Exchange Online as the OAuth provider](register-MS-msexchange-online-as-OAuth-provider.md)**  
Register Microsoft Exchange Online as the OAuth provider so that your Walk-up Experience instance can request OAuth 2.0 tokens.
-   **[Create credential records for the Microsoft Exchange Online spoke](create-credential-records-for-the-microsoft-exchange-online-spoke.md)**  
Authorize the Microsoft Exchange Online spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Exchange Online connection and credential alias uses these credentials to authorize actions.
-   **[Create connection records for the Microsoft Exchange Online spoke](create-connection-records-for-the-microsoft-exchange-online-spoke.md)**  
Perform actions in Microsoft Exchange Online by creating connection records for your Microsoft Exchange Online account. The Microsoft Exchange Online spoke connection and credential alias uses these connections to perform actions.

**Parent Topic:**[Integrate Microsoft Office 365 calendar with Walk-up Experience](../concept/walkup-ms-office-365-integration.md)

