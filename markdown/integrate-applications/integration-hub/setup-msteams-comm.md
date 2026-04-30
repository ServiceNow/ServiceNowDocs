---
title: Set up the Microsoft Teams Communications spoke
description: Integrate the ServiceNow instance and Microsoft Teams Communications account by creating a custom OAuth application in Microsoft Teams Communications to authenticate ServiceNow requests.Create an app to make outbound calls from Microsoft Teams.Assign permissions to users to be able to authenticate successfully and participate in conference calls in Microsoft Teams.Create a service user role to be able to start online meetings on behalf of users in Microsoft Teams.Use the information generated during the application configuration in Microsoft Azure portal to register Microsoft Teams Communications as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.Authorize the Microsoft Teams Communications spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Teams Communications connection and credential alias uses these credentials to authorize actions.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Microsoft Teams Communications Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up the Microsoft Teams Communications spoke

Integrate the ServiceNow instance and Microsoft Teams Communications account by creating a custom OAuth application in Microsoft Teams Communications to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Microsoft Teams Communications spoke.
-   Role required: admin

## Create an app in Microsoft Teams to enable making calls

Create an app to make outbound calls from Microsoft Teams.

### Before you begin

Role required: admin, Microsoft Teams admin, Microsoft Azure admin

### Procedure

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

3.  Create a bot for the new app.

    1.  Navigate to **Configure** &gt; **App features**.

    2.  Select **Bot**.

    3.  Select **Create a new bot**.

    4.  Select **New Bot**.

    5.  Enter a valid name for bot in the Add bot pop-up page and select **Add**.

    6.  Copy to a notepad the Bot ID value of the new bot using one of the following options and this will be your app Client ID.

        -   Copy the ID from the browser URL.
        -   Navigate back to **Bots** &gt; **Tools**, and copy the Bot ID.
    7.  Go to **Channels**, enable **Microsoft Teams**, and select **Save**.

    8.  Select **Client secrets** and enter a client secret for your bot.

        A Client secret is generated.

        **Note:** Ensure you copy the generated Client secret to a notepad because it will not appear again.

4.  Copy the Client ID or Bot ID of the new bot to the Application \(client ID\).

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

    3.  Search and open the new bot created for the spoke by name or by Application \(client\) ID.

    4.  Make a note of client ID/Application \(client\) ID, Object ID, and tenant ID to update these values in your ServiceNow instance in later procedures.

        **Note:** Bot ID created in the Microsoft Teams Developer portal and Application \(client\) ID in the Microsoft Azure portal are the same.


## Manage permissions and authenticate the app and bot in Microsoft Azure portal

Assign permissions to users to be able to authenticate successfully and participate in conference calls in Microsoft Teams.

### Before you begin

Role required: Microsoft Azure admin

### About this task

You can manage the permissions required by the app and bot to perform required actions for conference calls.

### Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/).

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  Search and open the bot created in step 3 in the section [Create an app in Microsoft Teams to enable making calls](setup-msteams-comm.md#) by name or by Application \(client\) ID.

4.  Navigate to **Manage** &gt; **API Permissions** &gt; **Add a permission** &gt; **Microsoft Graph** and select **Application Permissions**.

5.  Search and select the following values using **Select permissions**, and then select **Add permissions** to grant the permission.

    -   **User.Read.All** from User list.
    -   **OnlineMeetings.ReadWrite.All** from OnlineMeetings list.
    -   **Calls.InitiateGroupCall.All**, **Calls.JoinGroupCall.All**, **Calls.JoinGroupCallAsGuest.All** from Calls list.
6.  Grant admins access to the Microsoft Azure applications that require admin approval.

    1.  Select **Grant admin consent for &lt;tenant&gt;** in the API permissions page.

    2.  Select **Yes** in the Grant admin consent confirmation pop-up page.


## Create a Service user to make calls from Microsoft Teams

Create a service user role to be able to start online meetings on behalf of users in Microsoft Teams.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [Microsoft Azure portal](https://portal.azure.com/).

2.  Create a Service user.

    1.  Navigate to **Azure services** &gt; **User**.

    2.  Select **New user**.

    3.  On the form, fill the fields.

        |Field|Description|
        |:----|:----------|
        |User name|Option to provide the user name for the user.|
        |Name|Option to provide the name of the user.|

    4.  Select **Create**.

    5.  Select the created user to view the details.

        **Note:** Ensure that the Service User has the required license/subscription and a valid usage location set to make conference calls from Microsoft Teams.

3.  Run the PowerShell command from Terminal on macOS or from the Command prompt on Windows OS.

    1.  Type the command `pwsh` and press **Enter**.

    2.  Connect your Microsoft tenant with PowerShell.

    3.  Run the following command in PowerShell.

        ```
        connect-microsoftteams
        ```

        ![PowerShell connect Teams command](../image/powershell-connect-teams-command.png)

        Upon successful connection, a confirmation message is displayed in the browser.

        ![Authentication message in browser](../image/authentication-message-browser.png)

        PowerShell will also display the tenant details.

        ![Powershell confirmation](../image/powershell-confirmation.png)

4.  Run the command below to create a new Application Access Policy in PowerShell.

    Use the bot ID created in step 3 in the section [Create an app in Microsoft Teams to enable making calls](https://servicenow.com/docs/bundle/utah-employee-service-management/page/product/notify2/task/create-app-ms-teams.html) as the AppId for the command.

    For more information on the application access policy, see [Configure application access to online meetings](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

    ```
    Syntax:
    
    New-CsApplicationAccessPolicy -Identity "<PolicyName (can be anything)>" -AppIds "<AppIds>" -Description "<Policy Description>"
    
    Example:
    If you have a Self-configured (single tenant) setup, use the application ID from Azure portal.
    
    For Example: New-CsApplicationAccessPolicy -Identity "OnlineMeetingsAccessPolicy" -AppIds "aaaaaaaa-1234-er4r-8dc9-123456789012" -Description "Grant OnlineMeeting Application Permission"
    ```

    ![App access policy in Powershell](../image/app-access-policy.png)

    Upon successfully creating the policy, the details are displayed in PowerShell.

    ![App access policy success message in Powershell](../image/powershell-app-access-success.png)

5.  Run the user permission policy in PowerShell.

    1.  Go to the [Microsoft Azure portal](https://portal.azure.com/).

    2.  Navigate to **Home** &gt; **Users**.

    3.  Select the user created.

    4.  Copy the **Object ID** of the user to notepad.

    5.  Use the policy name created in the previous step as the **PolicyName** of the command and the **Object ID** as the **UserAzureID** respectively in the command to execute in PowerShell.

        ```
        Syntax:
        
        Grant-CsApplicationAccessPolicy -Identity "<UserAzureID>" -PolicyName "<PolicyName>"
        
        Example:
        
        Grant-CsApplicationAccessPolicy -Identity "fdcd9c17-ceae-468f-906f-2er76b4dd0f4" -PolicyName "OnlineMeetingsAccessPolicy"
        
        ```

        ![User permissions](../image/powershell-user-permissions.png)


## Register Microsoft Teams Communications as an OAuth provider

Use the information generated during the application configuration in Microsoft Azure portal to register Microsoft Teams Communications as the OAuth provider so that the ServiceNow instance can request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays this message: `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Client ID|Application ID created during application registration.|
    |Client Secret|Client secret created during application registration.|
    |Active|Option to actively use the application registry.|
    |Authorization URL|OAuth authorization code endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/authorize`.|
    |Token URL|OAuth server token endpoint. Enter `https://login.microsoftonline.com/<Directory-ID>/oauth2/v2.0/token`.|
    |Token Revocation URL|OAuth server token revocation endpoint.|
    |Redirect URL|OAuth callback endpoint. Enter `https://<instance-name>.service-now.com/oauth_redirect.do`.|
    |Default Grant type|Grant type used to establish the token. Select **Client Credentials**.|

5.  Right-click the form header, and click **Save**.

6.  In the **OAuth Entity Scopes** tab, insert a row and fill these values:

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the entity scope record. For example, `MS Teams Comm OAuth Scope`.|
    |OAuth scope|OAuth entity scope. Enter `.default`.|

7.  Right-click the form header, and click **Save**.

8.  In the **OAuth Entity Profiles** tab, open the default profile record.

9.  In the **OAuth Entity Scopes** tab, insert a record.

10. Search and select the OAuth entity scope you had created.

11. Click **Update**.


## Create a credential record for the Microsoft Teams Communications

Authorize the Microsoft Teams Communications spoke actions by creating credential records for the application registered in the Microsoft Azure portal. The Microsoft Teams Communications connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credentials Aliases**.

2.  Open the alias record, **MSTeamsCommunicationsSpoke**.

3.  From the **Credentials** tab, click **New**.

    The system displays this message: `What type of Credentials would you like to create?`

4.  Select **OAuth 2.0 Credentials**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `MS Teams Comm Cred`.|
    |Active|Option to actively use the credential record.|
    |OAuth Entity Profile|OAuth profile created during the registration of Microsoft Teams Communications as an OAuth provider. For example, `MS Teams Comm OAuth Prof`.|

6.  Right-click the form header and click **Submit**.

7.  To generate the OAuth token, click the **Get OAuth Token** related link.


