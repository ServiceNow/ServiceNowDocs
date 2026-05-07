---
title: Onboard Azure DevOps to DevOps Change Velocity — Workspace
description: Connect to your Azure DevOps instance using the DevOps Change Workspace playbook to collect data for planning, coding, orchestration, artifact, and software quality functions.Connect and configure your Azure DevOps instance directly at your Azure DevOps organization level. All the projects within the organization can be discovered, and you can choose to configure multiple projects within the organization. You can manage the tool at the organization level.Connect and configure your Azure DevOps instance directly at the project level. If you have multiple projects within the organization, you must connect each of them separately.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Azure DevOps to DevOps Change Velocity — Workspace

Connect to your Azure DevOps instance using the DevOps Change Workspace playbook to collect data for planning, coding, orchestration, artifact, and software quality functions.

Connecting Azure DevOps with DevOps Change VelocityModeling an Azure pipeline in DevOps

You can connect to Azure DevOps \(ADO\) at your organization level or at individual project level. If you're connecting at the project level, for each project at your organization, you must repeat the connection process. After connecting to an instance of the tool, you can configure additional settings that enable DevOps to import pipelines, task execution records, and step execution records.

When you configure webhooks in your Azure DevOps instance to send data to DevOps Change Velocity, Azure DevOps uses token authentication for the integration user by default. The DevOps Change Velocity APIs are invoked using token authentication and you don’t have to enter the integration user name and password while configuring. If the devops.system user isn’t available in your ServiceNow instance, you must set the **Switch to this user after token based authentication is successful** property. For more information, see [DevOps Change Velocity properties](dev-ops-administration.md). The step to enter the integration user name and password is required only in the following scenarios:

-   If DevOps Config is installed, as DevOps Config APIs are invoked using basic authentication.
-   If you use the Azure Invoke REST API service connection. You must enable the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property in this case.

**Note:** DevOps Change Velocity uses the term instance to refer to a particular occurrence of a tool. Azure DevOps uses the term project instead.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](azure-devops-integration-dev-ops.md)

## Connect an organization

Connect and configure your Azure DevOps instance directly at your Azure DevOps organization level. All the projects within the organization can be discovered, and you can choose to configure multiple projects within the organization. You can manage the tool at the organization level.

### Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

### Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Azure DevOps.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d41452e230">

Option

</th><th align="left" id="d41452e233">

Steps

</th></tr></thead><tbody><tr><td id="d41452e239">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Azure DevOps from the appropriate category \(Orchestration, Plan, Code, Artifact, or Software quality\).


</td></tr><tr><td id="d41452e263">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](../task/app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Azure DevOps from the appropriate category \(Orchestration, Plan, Code, Artifact, or Software quality\).


</td></tr><tr><td id="d41452e312">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select the appropriate category \(Orchestration, Planning, Coding, Artifact, or Software quality\).
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Azure DevOps**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like pipelines, plans, or repositories while connecting to the tool, you must connect your tool from the Application module.

2.  In the Connect to a tool modal, enter the connection details.

    1.  Select **Connect an organization** from the drop-down list.
    2.  Enter the Azure DevOps URL for the organization.
    3.  In the **Tool name** field, enter a name for the tool.
    4.  Select **Next**.

        ![Connect to organization.](../image/azure-plybk-09.png)

        The DevOps playbook opens to help you complete the onboarding tasks.

3.  In the Enter Azure DevOps instance details section, select one of the following values in the **Credential type** field.

<table id="choicetable_j33_jgk_lcc"><tbody><tr><td id="d41452e419">

**Personal Access Token**

</td><td>

Enter the password or access token to access this instance.For information on creating a PAT, see [Personal access token \(PAT\)](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). ![Connect to a tool - ADO PAT](../image/ado-pat-01.png)

</td></tr><tr><td id="d41452e439">

**OAuth 2.0**

</td><td>

Pre-requisites: -   [Create a tenant in Microsoft Entra](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Add a user to tenant in Microsoft Entra](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create an organization in Azure portal](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create an Azure DevOps app](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Register Azure DevOps as an OAuth provider](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Configure organization and project level settings](../task/set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create credential record and get OAuth token](../task/set-up-azure-devops-oauth-2-0-credential.md#)
**Use an existing OAuth credential record**1.  Select the **Use an existing OAuth credential record** option.
2.  Select a value in the **Credential** field.
**Create a new credential record**1.  Clear the **Use an existing OAuth credential record** option.
2.  Enter the application ID of your Azure application \(available in the Overview section of your Azure application registry in Azure\) in the **Application \(client\) ID** field.
3.  Enter the directory ID of your Azure application \(available in the Overview section of your Azure application registry in Azure\) in the **Directory \(tenant\) ID** field.
4.  Enter the client secret of your Azure application \(available in the Certificates &amp; secrets section of your Azure application registry in Azure\) in the **Client secret** field.![Connect to a tool - ADO OAuth 2.0](../image/ado-oauth-01.png)


</td></tr></tbody>
</table>4.  If your tool instance is attached to a MID Server, select the **MID Server** option and enter its details.

    For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

5.  Select **Connect**.

6.  Permission checks are run on the credentials that you entered.

    Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see Azure DevOps permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    You can choose to continue with the tool connection even if you don't have all the required permissions.

    **Note:** When onboarding an Organization, the **Project Administrators** privilege requires the owner of the PAT to be a member of the organization's **Project Collection Administrators** group.

    You need the Project Administrators privilege only for onboarding the tool. Once the tool is successfully onboarded, you can choose to turn off the Project Administrators privilege from the PAT.

    ![Permissions required for Azure PAT.](../image/azure-plybk-03.png)

7.  Specify the access for the tool.

    1.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field.

        The tasks these users in the groups can perform depends on the role assigned to them.

        -   DevOps Tool Owner role: Can view and edit the tool.
        -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
        -   DevOps Administrator role: Can edit all tools.
        -   Other DevOps roles: Can view the tool.
        **Note:** If you don't select a group and skip this step, all users with the DevOps Tool Owner role will be able to edit the tool.

    2.  If you choose to control access to the tool, the **All DevOps App Owners can view and associate tool objects to applications** option becomes available for selection.

        This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

    3.  Select **Assign**.

        ![Assign access groups.](../image/azure-plybk-11.png)

8.  Install the ServiceNow DevOps extension in your Azure DevOps instance.

    The ServiceNow DevOps extension will automatically create service connections while configuring webhooks. Service connections are required for sending build and release notifications from Azure DevOps. The extension also contains custom tasks to modify the Azure DevOps pipelines for change control, artifacts, and packages.

    For more information on the extension, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](../task/config-dev-ops-extensions-azure.md#).

    **Note:** If you skip this step, to send notifications from Azure DevOps, you must manually create service connections after configuring webhooks.

    After installing the extension, select **Marked as installed**.

    ![Install the ServiceNow DevOps extension.](../image/azure-plybk-01.png)

9.  Configure webhooks automatically in your Azure DevOps instance to send data to DevOps Change Velocity.

    Choose to send data by either nightly polling or configuring webhooks to send real-time data.

    -   Webhooks: Enable real-time notifications for your pipeline executions. Real-time notifications are ideal to maintain the most up-to-date information particularly for automating change requests.

        To use webhooks, select **Configure.**

    -   Nightly polling: If you don’t choose to configure now, you can enable nightly polling later to fetch data for any tracked plans by setting the **Enable Polling** property to **Yes**.
    1.  Enter the DevOps integration user name and password.

        For information about creating the DevOps integration user and password, see [Set up integration user account in DevOps Change Velocity](../task/devops-plybk-set-up-system-accts.md).

        **Note:**

        -   The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is enabled. If this step is not required, webhooks are configured using token-based authentication.
        -   When DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is enabled, you can regenerate token \(auto-configure with new token\) from the workspace UI only, which will update the integration user password. When DevOps Config is not installed, token can be regenerated from both the workspace and classic UI for token based authentication. Re-generate your token periodically for better security.
    2.  Select the projects for which you want to configure webhooks.
    3.  Select **Configure**.

        ![Configure Azure DevOps for organization.](../image/azure-plybk-13.png)

    To configure webhooks manually, select **Configure manually**. See [Configure webhooks in Azure DevOps manually](configure-test-webhooks.md#) for more information.

    Webhook configuration and discovery happen in the background, and you’re taken to the Summary page.

    ![Organization connection summary.](../image/azure-plybk-15.png)

10. From the Summary page, select **View tool record** to review the details of the connected tool.


### Result

You’ve successfully onboarded your Azure DevOps tool to DevOps Change Velocity at the organization level.

### What to do next

From the **Projects** tab on the tool record page, select a project to navigate to the project record page. From here, you can discover project objects, and configure webhooks for the project.

-   Select **Discover** to discover the project objects, including existing plans \(boards\), repositories, and pipelines.
-   If you created the tool directly at the project level, then selecting **Discover projects** from the **Projects** tab of the tool record page will discover all the projects in your organization as well.
-   Select **Configure** and enter the integration user credentials to configure webhooks for the project.
-   If you're on the tool records page, selecting **Configure projects** and entering the integration user credentials gives the list of unconfigured projects in your organization. Select the projects that you want webhooks configured for and select **Configure**.

    **Note:** The step to enter the integration user name and password is required to configure webhooks only when DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is disabled. If this step is not required, webhooks are configured using token-based authentication.

-   To import historical data to the project objects like plans, repositories, or pipelines, associate the objects with an application, and import the data. For more information, see [Associate tool objects to applications - Workspace](../task/apps-associate-objects-wkspc.md).

## Connect a project

Connect and configure your Azure DevOps instance directly at the project level. If you have multiple projects within the organization, you must connect each of them separately.

### Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

### Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Azure DevOps.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d41452e1072">

Option

</th><th align="left" id="d41452e1075">

Steps

</th></tr></thead><tbody><tr><td id="d41452e1081">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Azure DevOps from the appropriate category \(Orchestration, Plan, Code, Artifact, or Software quality\).


</td></tr><tr><td id="d41452e1105">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](../task/app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Azure DevOps from the appropriate category \(Orchestration, Plan, Code, Artifact, or Software quality\).


</td></tr><tr><td id="d41452e1154">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select the appropriate category \(Orchestration, Planning, Coding, Artifact, or Software quality\).
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Azure DevOps**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like pipelines, plans, or repositories while connecting to the tool, you must connect your tool from the Application module.

2.  In the Connect to a tool modal, enter the connection details.

    1.  Select **Connect a project** from the drop-down list.
    2.  Enter the Azure DevOps URL for the project.
    3.  In the **Tool name** field, enter a name for the tool.
    4.  Select **Next**.

        The DevOps playbook opens to help you complete the onboarding tasks.

    ![Connect to project.](../image/azure-plybk-10.png)

3.  Enter the instance details for your tool.

    1.  In the Enter Azure DevOps instance details section, select one of the following values in the **Credential type** field.

        -   **Personal Access Token**: Enter the password or access token to access this instance.

            For information on creating a PAT, see [Personal access token \(PAT\)](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page). ![Connect to a tool - ADO PAT](../image/ado-pat-01.png)

        -   **OAuth 2.0**: Pre-requisites:

            -   [Create a tenant in Microsoft Entra](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Add a user to tenant in Microsoft Entra](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Create an organization in Azure portal](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Create an Azure DevOps app](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Register Azure DevOps as an OAuth provider](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Configure organization and project level settings](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            -   [Create credential record and get OAuth token](../task/set-up-azure-devops-oauth-2-0-credential.md#)
            **Use an existing OAuth credential record**

            1.  Select the **Use an existing OAuth credential record** option.
            2.  Select a value in the **Credential** field.
            **Create a new credential record**

            1.  Clear the **Use an existing OAuth credential record** option.
            2.  Enter the application ID of your Azure application \(available in the Overview section of your Azure application registry in Azure\) in the **Application \(client\) ID** field.
            3.  Enter the directory ID of your Azure application \(available in the Overview section of your Azure application registry in Azure\) in the **Directory \(tenant\) ID** field.
            4.  Enter the client secret of your Azure application \(available in the Certificates &amp; secrets section of your Azure application registry in Azure\) in the **Client secret** field.
            ![Connect to a tool - ADO OAuth](../image/ado-prj-oauth.png)

    2.  If your tool instance is attached to a MID Server, select the **MID Server** option and enter its details.

        For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

    3.  Select **Connect**.

    4.  Permission checks are run on the credentials that you entered.

        Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see Azure DevOps permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

        You can choose to continue with the tool connection even if you don't have all the required permissions.

        **Note:** When onboarding a Project, the **Project Administrators** privilege requires the owner of the PAT to be a member of the project's **Project Administrators** group.

        You need the Project Administrators privilege only for onboarding the tool. Once the tool is successfully onboarded, you can choose to turn off the Project Administrators privilege from the PAT.

        ![Permissions required for Azure PAT.](../image/azure-plybk-03.png)

    5.  Select **Next**.

4.  Specify the access for the tool.

    1.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field.

        The tasks these users in the groups can perform depends on the role assigned to them.

        -   DevOps Tool Owner role: Can view and edit the tool.
        -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
        -   DevOps Administrator role: Can edit all tools.
        -   Other DevOps roles: Can view the tool.
        **Note:** If you don't select a group and skip this step, all users with the DevOps Tool Owner role will be able to edit the tool.

    2.  If you choose to control access to the tool, the **All DevOps App Owners can view and associate tool objects to applications** option becomes available for selection.

        This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

    3.  Select **Assign**.

        ![Assign access groups.](../image/azure-plybk-11.png)

5.  Install the ServiceNow DevOps extension in your Azure DevOps instance.

    The ServiceNow DevOps extension will automatically create service connections while configuring webhooks. Service connections are required for sending build and release notifications from Azure DevOps. The extension also contains custom tasks to modify the Azure DevOps pipelines for change control, artifacts, and packages.

    For more information on the extension, see [Use the ServiceNow DevOps extension for Azure DevOps and Azure DevOps custom actions](../task/config-dev-ops-extensions-azure.md#).

    **Note:** If you skip this step, to send notifications from Azure DevOps, you must manually create service connections after configuring webhooks.

    After installing the extension, select **Marked as installed**.

    ![Install the ServiceNow DevOps extension.](../image/azure-plybk-01.png)

6.  Configure webhooks automatically in your Azure DevOps instance to send data to DevOps Change Velocity.

    Choose to send data by either nightly polling or configuring webhooks to send real-time data.

    -   Webhooks: Enable real-time notifications for your pipeline executions. Real-time notifications are ideal to maintain the most up-to-date information particularly for automating change requests.

        To use webhooks, select **Configure.**

    -   Nightly polling: If you don’t choose to configure now, you can enable nightly polling later to fetch data for any tracked plans by setting the **Enable Polling** property to **Yes**.
    1.  Enter the DevOps integration user name and password.

        For information about creating the DevOps integration user and password, see [Set up integration user account in DevOps Change Velocity](../task/devops-plybk-set-up-system-accts.md).

        **Note:**

        -   The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is enabled. If this step is not required, webhooks are configured using token-based authentication.
        -   When DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is enabled, you can regenerate token \(auto-configure with new token\) from the workspace UI only, which will update integration user password. When DevOps Config is not installed, token can be regenerated from both the workspace and classic UI for token based authentication. Re-generate your token periodically for better security.
    2.  Select **Configure**.

        ![Configure Azure DevOps for a project.](../image/azure-plybk-14.png)

        To configure webhooks manually, select **Configure manually**. See [Configure webhooks in Azure DevOps manually](configure-test-webhooks.md#) for more information.

        **Important:**

        -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
        -   If you're connecting from the Applications module, then plans, repositories, and pipelines available in your project are discovered. You can track and import historical data from them.
7.  Select the plans to track.

    1.  Select the plans for which you want to track updates and associate to the application.
    2.  Select **Next**.

        ![Select plans to track.](../image/azure-plybk-02.png)

    3.  If you want to import plan data, select the date range and select **Submit**.

        You can import up to 90 days of data.

        ![Import plan data.](../image/azure-plybk-04.png)

8.  Select the repositories to track.

    1.  Select the repositories for which you want to track updates and associate to the application.
    2.  Select **Next**.

        ![Select repositories to track.](../image/azure-plybk-05.png)

    3.  If you want to import repository data, select the date range and select **Submit**.

        You can import up to 90 days of data.

        ![Import repository data.](../image/azure-plybk-06.png)

9.  Select the pipelines to track.

    1.  Select the pipelines for which you want to track updates and associate to the application.

    2.  Select **Next**.

        ![Select pipelines to track.](../image/azure-plybk-07.png)

    3.  For each selected pipeline, all steps or stages are imported for the last successful execution. In the Assign services to pipeline steps activity, you can select the following for each pipeline step:
        1.  **Pipeline step type**: Select a step type for which you want to assign a service.

            **Tip:** Specify at least the **Prod deploy** step type for steps that represents the production deployment to enable DevOps to identify successful pipeline executions as production deployments.

        2.  **Service**: Select the CMDB application service that the pipeline step maps to.

            Application service maps approximately to the environment. If you use the same pipeline step to deploy to different environments, leave the field empty. Service information enables DevOps to identify and report on operational metrics such as incidents, outages, and so on.

    4.  Select **Next**.

        ![Assign services to pipeline steps.](../image/azure-plybk-08.png)

    5.  If you want to import pipeline data, select the date range and select **Submit**.

        You can import up to 90 days of data.

        ![Import historical pipeline data.](../image/azure-plybk-17.png)

10. You're taken to the Summary page.

    From the Summary page, select **View tool record** to review the details of the connected tool.

    ![Project connection summary.](../image/azure-plybk-16.png)


### Result

You’ve successfully onboarded your Azure DevOps tool to DevOps Change Velocity at the project level.

### What to do next

From the **Projects** tab on the tool record page, select a project to navigate to the project record page. From here, you can discover project objects, and configure webhooks for the project.

-   Select **Discover projects** to discover the project objects, including existing plans \(boards\), repositories, and pipelines. This will discover all the projects in your organization as well.
-   Select **Configure projects** to configure webhooks for the project.
-   If you're on the tool records page, selecting **Configure projects** and entering the integration user credentials gives the list of unconfigured projects in your organization. Select the projects that you want webhooks configured for and select **Configure**.

    **Note:** The step to enter the integration user name and password is required to configure webhooks only when DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is disabled. If this step is not required, webhooks are configured using token-based authentication.

-   To import historical data to the project objects like plans, repositories, or pipelines, associate the objects with an application, and import the data. For more information, see [Associate tool objects to applications - Workspace](../task/apps-associate-objects-wkspc.md).

**Related topics**  


[Configure webhooks from the tool record](../task/configure-webhooks-from-the-tool-record.md)

