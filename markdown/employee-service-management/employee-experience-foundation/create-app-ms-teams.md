---
title: Create an app in Microsoft Teams to enable making calls
description: Create an app to make outbound calls from Microsoft Teams.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrating Notify connector self-configured app with Microsoft Teams, Integration for Agent Experience, Setup for integrating self-configured apps, Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Create an app in Microsoft Teams to enable making calls

Create an app to make outbound calls from Microsoft Teams.

## Before you begin

Ensure you have installed Notify connector and other required plugins on your ServiceNow® instance. For more information, see [Install Notify connector for Microsoft Teams](setup-notify-ms-teams.md).

Role required: Microsoft Teams admin, Microsoft Azure admin

## Procedure

1.  Log in to [Microsoft Teams developer portal](https://dev.teams.microsoft.com).

    **Note:**

    The Developer Portal for the Government Community Cloud \(GCC\) is accessible only through an application within Microsoft Teams. It is not available as a separate, standalone website. For more information, see [Developer Portal for Teams](https://learn.microsoft.com/en-us/microsoftteams/platform/concepts/build-and-test/teams-developer-portal). To create an app for GCC, you must create the app from Microsoft Teams.

2.  Create an app.

    1.  Navigate to **Apps** &gt; **New app**.

    2.  Enter a valid name for the app in the Add app pop-up page and select **Add**.

    3.  On the App details page, fill in the fields.

<table id="table_opf_nw5_rwb"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Short name

</td><td>

Name of your application. For example, ServiceNow for Notify Microsoft Teams.

</td></tr><tr><td>

Full name

</td><td>

Full name of your application.

</td></tr><tr><td>

App ID

</td><td>

Unique identification number for the app.**Note:** This App ID is different from the Bot ID/App ID that will be generated in further steps.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the app.

</td></tr><tr><td>

Long description

</td><td>

Detailed description of the app.

</td></tr><tr><td>

Version

</td><td>

Version for the app.

 For example, 1.0.

</td></tr><tr><td>

Developer or company Name

</td><td>

Name of your company.

</td></tr><tr><td>

Website

</td><td>

Link to your company website.

</td></tr><tr><td>

Privacy policy

</td><td>

Link to the privacy statement for your app.

</td></tr><tr><td>

Terms of use

</td><td>

Link to the terms and conditions for your app.

</td></tr></tbody>
</table>    4.  Select **Save**.

        An app is created in Microsoft Teams.

3.  Create a bot \(Notify connector\) for the new app.

    1.  Navigate to **Configure** &gt; **App features**.

    2.  Select **Bot**.

    3.  Select **Create a new bot**.

    4.  Select **New Bot**.

    5.  Enter a valid name for bot in the Add bot pop-up page and select **Add**.

    6.  Copy to a notepad the Bot ID value of the new Notify connector using one of the following options and this will be your app Client ID.

        -   Copy the ID from the browser URL.
        -   Navigate back to **Bots** &gt; **Tools**, and copy the Bot ID.
    7.  Go to **Channels**, enable **Microsoft Teams**, and select **Save**.

    8.  Select **Client secrets** and enter a client secret for your bot.

        A Client secret is generated.

        **Note:** Ensure you copy the generated Client secret to a notepad because it will not appear again.

4.  Copy the Client ID/Bot ID of Notify Connector to the Application \(client ID\).

    1.  Go to **Apps** and select the app you created.

    2.  Navigate to **Configure** &gt; **Basic information**.

    3.  Paste the Client ID/Bot ID that you copied during step 3f in the **Application \(client\) ID** field and select **Save**.

5.  Configure additional app features for new bot.

    1.  Go to **Apps** and select the app you created.

    2.  Navigate to **Configure** &gt; **App features** &gt; **Bot** &gt; **Select an existing bot** and select the bot you created.

    3.  Select **Support audio calls** and **Support video calls** from 'What can your bot do?'.

    4.  Select **Personal**, **Team**, and **Group chat** from 'Select the scopes in which people can use this command'.

6.  Copy the new app attributes.

    1.  Log in to [Microsoft Azure portal](https://portal.azure.com/) as Microsoft Azure admin.

    2.  Navigate to **Azure services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

    3.  Search and open the new bot created for Notify Connector by name or by Application \(client\) ID.

    4.  Make a note of client ID/Application \(client\) ID, Object ID, and tenant ID to update these values in your ServiceNow instance in later procedures.

        **Note:** Bot ID created in the Microsoft Teams Developer portal and Application \(client\) ID in the Microsoft Azure portal are the same.


## What to do next

Assign permissions to users to access the new bot. For more information, see [Manage permissions and authenticate the Notify connector app/bot in Microsoft Azure portal](manage-permissions-notify.md).

**Parent Topic:**[Integrating Notify connector self-configured app with Microsoft Teams](../concept/setup-notify-ms-teams-single-tenant.md)

