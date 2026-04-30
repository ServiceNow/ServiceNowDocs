---
title: Setting up Azure DevOps OAuth 2.0 credential
description: Create Azure DevOps OAuth 2.0 credential and use them to connect your Azure DevOps instance.Create a tenant in Microsoft Entra and set up the required permissions to create an Azure DevOps \(ADO\) app.Add a user who contains the admin role, to the tenant created in the previous procedure.Create an organization in the new tenant, which has access to create an app.Create and configure an Azure DevOps \(ADO\) app and copy the required values to enable OAuth 2.0 authentication with your ServiceNow instance.Use the information generated during Azure DevOps \(ADO\) app account configuration to register Azure DevOps as an OAuth provider and enable the instance to request OAuth 2.0 tokens.Configure organization and project level settings for your app.Create credential record and get OAuth token.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Setting up Azure DevOps OAuth 2.0 credential

Create Azure DevOps OAuth 2.0 credential and use them to connect your Azure DevOps instance.

If you want to use Basic Authentication credentials instead of OAuth 2.0, skip this section and proceed to onboarding Azure DevOps using one of the following options:

-   [Onboard Azure DevOps to DevOps Change Velocity — Workspace](../concept/devops-wkspc-azuredevops-tool-conn.md#)
-   [Onboard Azure DevOps to DevOps Change Velocity — Service Catalog](onboard-azure-devops-service-catalog.md)
-   [Onboard Azure DevOps to DevOps Change Velocity — Classic](create-azure-tool-dev-ops.md)

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

## Create a tenant in Microsoft Entra

Create a tenant in Microsoft Entra and set up the required permissions to create an Azure DevOps \(ADO\) app.

### Before you begin

Role required: Tenant Creator in Azure DevOps.

### About this task

Your tenant represents your organization and helps you to manage a specific instance of Microsoft Cloud services for your internal and external users.

If you have an existing tenant, which has access to create an ADO app, you do not need to perform this procedure. If you don’t have a tenant, you must create a tenant in Microsoft Entra, which will have access to create an ADO app.

### Procedure

1.  In the [Microsoft Entra](http://entra.microsoft.com) portal, navigate to **Overview &gt; Manage tenants**.

2.  Select **Create**.

3.  Select the **Workforce** configuration, and select **Continue**.

4.  Enter the following information:

    -   Your desired Organization name into the **Organization name** box.
    -   Your desired Initial domain name into the **Initial domain name** box.
5.  Select **Next: Review + Create**.

6.  Review the information that you entered and if the information is correct, select **Create** in the lower left corner.

    For more information, see the [Microsoft](https://learn.microsoft.com/en-us/entra/fundamentals/create-new-tenant) documentation.


## Add a user to tenant in Microsoft Entra

Add a user who contains the admin role, to the tenant created in the previous procedure.

### Before you begin

Role required: User Administrator in Azure DevOps

### Procedure

1.  In the Microsoft Entra ID tenant page, select the number of users link in the Tenant details section. ![Users in Tenant details section](../image/tenant-users.png)

2.  Select **New user &gt; Create new user**.

3.  In the Basics tab, enter the following details.

    |Field|Value|
    |-----|-----|
    |User principal name|Enter a unique user name and select a domain from the menu after the @ symbol.|
    |Mail nickname|If you need to enter an email nickname that is different from the user principal name you entered, clear the **Derive from user principal name** option, then enter the mail nickname.|
    |Display name|Enter the user's name.|
    |Password|Provide a password for the user to use during their initial sign-in. Clear the Auto-generate password option to enter a different password|
    |Account enabled|This option is checked by default. Clear to prevent the new user from being able to sign in. You can change this setting after the user is created. This setting was called **Block sign in** in the legacy create user process.|

4.  Select **Next: Properties** to complete the next section.

    |Field|Value|
    |-----|-----|
    |Identity|Enter the user's first and last name. Set the User type as either Member or Guest.|
    |Job information|Add any job-related information, such as the user's job title, department, or manager.|
    |Contact information|Add any relevant contact information for the user.|
    |Parental controls|For organizations like K-12 school districts, the user's age group may need to be provided. Minors are 12 and under, Not adult are 13-18 years old, and Adults are 18 and over. The combination of age group and consent provided by parent options determine the Legal age group classification. The Legal age group classification may limit the user's access and authority.|
    |Settings|Specify the user's global location.|

5.  Select **Next: Assignments** to complete the next section.

6.  In the Assignments section, select **+ Add** role.

7.  From the menu that appears, select the **Global Administrator** role from the list and select the **Select** button.

8.  Select the **Review + create** button.

    For more information, see the [Microsoft](https://learn.microsoft.com/en-us/entra/fundamentals/how-to-create-delete-users) documentation.


## Create an organization in Azure portal

Create an organization in the new tenant, which has access to create an app.

### Before you begin

Role required: Global Administrator in Azure DevOps

### Procedure

1.  Log in to [Azure](http://portal.azure.com) portal with the user created in the previous procedure.

2.  Navigate to **Azure DevOps Organizations &gt; My Azure DevOps Organizations**.

3.  Select **Create new organization**.

4.  Enter the name of your ADO organization and location, and then select **Continue**. ![Create ADO org page](../image/create-ado-org.png)

    This newly created org will be connected with the tenant created in the [Create a tenant in Microsoft Entra](set-up-azure-devops-oauth-2-0-credential.md#) topic.


## Create an Azure DevOps app

Create and configure an Azure DevOps \(ADO\) app and copy the required values to enable OAuth 2.0 authentication with your ServiceNow instance.

### Before you begin

Role required: Global Administrator in Azure DevOps

### Procedure

1.  In the [Azure](http://portal.azure.com) portal, navigate to **App registrations**.

2.  Select **+ New registration**.

3.  On the App registrations page, enter your application's registration information as described in the table.

    |Field|Value|
    |-----|-----|
    |Name|Enter a meaningful application name that is displayed to users.|
    |Supported account types|Select Accounts in this Organizational directory only \(Single tenant\)|
    |Redirect URL|Enter your ServiceNow instance URL.|

4.  Select **Register**.

5.  In the newly created application, from the Overview page in the left navigation pane and copy the following details:

    -   Application \(client\) ID
    -   Directory \(tenant\) ID
    ![Overview page for an ADO app](../image/ado-app-creation-overview.png)

6.  Add a client secret by selecting the **Manage &gt; Certificates &amp; secrets** link in the left navigation pane.

    For more information, see the [Add a client secret](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate#add-a-client-secret) and [Register an application](https://learn.microsoft.com/en-us/entra/identity-platform/quickstart-register-app?tabs=certificate) topics in Microsoft documentation.

7.  Copy the client secret value. ![Certificates & secrets section for an ADO app](../image/ado-app-client-secret.png)

8.  Navigate to **Manage &gt; API permissions**.

9.  Select **+ Add a permission**, and select the Microsoft APIs tab on the right.

10. Search and select Azure DevOps and add the **vso.project** permission.

11. Select the vso.project permission, and copy the **Resource App ID** value. ![Resource App ID in the API Permissions screen](../image/vso-resource-id.png)

    **Note:** The resource app ID value copied here will be added in the OAuth Entity Scopes for the Application Registry.


## Register Azure DevOps as an OAuth provider

Use the information generated during Azure DevOps \(ADO\) app account configuration to register Azure DevOps as an OAuth provider and enable the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin

### Procedure

1.  In ServiceNow DevOps Change Velocity, navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The **What kind of OAuth application?** message is displayed.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_fd2_2xr_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `My ADO App Provider`.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your ADO app \(hint: available in the **Overview** section of your ADO app\).

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your ADO app \(hint: available in the **Certificates &amp; secrets** section of your ADO app\).

</td></tr><tr><td>

Default Grant type

</td><td>

Type of grant associated with application registry. Select **Client Credentials**.

</td></tr><tr><td>

Authorization URL

</td><td>

Enter:https://login.microsoftonline.com/&lt;Directory \(tenant\) ID&gt;/oauth2/v2.0/authorize

Where, Directory \(tenant\) ID is the alphanumeric value found in the Overview section of your ADO app.

</td></tr><tr><td>

Token URL

</td><td>

Enter:https://login.microsoftonline.com/&lt;Directory \(tenant\) ID&gt;/oauth2/v2.0/token

Where, Directory \(tenant\) ID is the alphanumeric value found in the Overview section of your ADO app.

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as is.

    ![ADO OAuth app registry page](../image/ado-oauth-app-registry.png)

6.  Select and hold \(or right-click\) the form header, and select **Save**.

    The system validates the OAuth credentials and populates the **Redirect URL** \(Hint: It should match the redirect URL previously provided in your ADO app creation\).

7.  Select the **OAuth Entity Scopes** related tab.

8.  Add the OAuth scope value as **&lt;Resource App ID value copied in step 11 of the previous procedure&gt;/.default**. ![OAuth Entity Scope related tab](../image/oauth-entity-scope.png)


## Configure organization and project level settings

Configure organization and project level settings for your app.

### Before you begin

Role required: Member of the [**Project Collection Administrators** group](https://learn.microsoft.com/en-us/azure/devops/organizations/security/change-organization-collection-level-permissions?view=azure-devops) or organization's owner.

### Procedure

1.  Navigate to **Organizational Settings** of your organization in the Azure DevOps portal.

2.  Select **Users**.

3.  In the **Users or Service Principals** field, select the app you created in the previous procedure to the list. ![Add app user to organization](../image/add-user-org.png)

4.  Navigate back to the users list, and select the app user.

5.  Select the **Actions** menu, and select **Manage Access**.

6.  Add the project that you want to enable the app to access, and assign the **Project Administrator** role to that project.

    **Note:** If you aren’t seeing your release or classic pipelines, ensure that the **Disable creation of classic release pipelines** setting is switched off for your organization.

    ![Pipeline Settings for your organization](../image/organization-pipeline-settings.png)

7.  Navigate to **Project Settings** of your project.

8.  Select **Permissions**.

    There will be one project team created under permissions by default. ![Project level permissions](../image/project-level-team-permission.png)

9.  Select the default project team, and navigate to the Members tab.

10. Add your app user. ![Add app user to default project](../image/project-level-app-user.png)


## Create credential record and get OAuth token

Create credential record and get OAuth token.

### Before you begin

Role required: admin, sn\_devops.admin

### About this task

For ADO OAuth 2.0, you must create separate credential records for build, release, and feeds in ServiceNow.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The **What type of Credentials would you like to create?** message is displayed.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `My ADO APP Build Credential`.|
    |Active|Option to enable the record.|
    |OAuth Entity Profile|Default OAuth Entity profile created in the Application Registry.|

5.  Save the record.

6.  Select the **Get OAuth Token** related link to generate the OAuth token.

7.  Repeat the procedure to create release and feeds credentials.


