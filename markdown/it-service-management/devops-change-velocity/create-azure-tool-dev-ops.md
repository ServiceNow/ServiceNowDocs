---
title: Onboard Azure DevOps to DevOps Change Velocity — Classic
description: Create an Azure DevOps tool record in DevOps Change Velocity to connect, discover, and import Azure DevOps tool data.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Azure DevOps to DevOps Change Velocity — Classic

Create an Azure DevOps tool record in DevOps Change Velocity to connect, discover, and import Azure DevOps tool data.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## About this task

Actions:

-   **Connect** to Azure DevOps organization or project.
-   **Discover** plans, repositories, orchestration tasks, and pipelines.
-   **Configure** webhooks in Azure DevOps.
-   **Import** work item, plan version, and feature records, branch and commit records, and task execution and step execution records.

To [customize Azure Boards import](../reference/dev-ops-azure-work-item-import.md) of work item states or types, use the **DevOpsAzureDevOpsWorkItemHelper** script include.

## Procedure

1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  On the Create DevOps tool form, fill in the fields.

<table id="table_kz1_ply_xmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool name

</td><td>

Name of your choice to identify this tool.

</td></tr><tr><td>

Tool Integration

</td><td>

Select **Azure DevOps**.

</td></tr><tr><td>

Connect to an organization or project

</td><td>

Select from the list.-   **Connect an organization**: Connect directly at your Azure DevOps organization level. All the projects within the organization can be discovered, and you can choose to configure multiple projects within the organization.
-   **Connect a project**: Connect directly at the project level.


</td></tr><tr><td>

Tool URL

</td><td>

Azure DevOps organization URL \(for example, `https://dev.azure.com/<your organization>`\) or the Azure DevOps project URL \(for example, `https://dev.azure.com/<your organization>/<your project>`\), depending on your earlier selection.

</td></tr><tr><td>

Credential type

</td><td>

Type of credential, **Basic Auth** or **OAuth 2.0**.**Basic Auth**

1.  Enter your ADO instance username.
2.  Enter the [Personal access token \(PAT\)](https://docs.microsoft.com/en-us/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate?view=azure-devops&tabs=preview-page) or password for your Azure DevOps instance.

**Note:**

When you generate a Personal access token \(PAT\) for Azure DevOps, you must select the scopes to authorize if you aren’t granting complete access. See [Azure DevOps PAT scopes for DevOps](../reference/dev-ops-pat-scopes-azure.md).

**OAuth 2.0**

Pre-requisites:

-   [Create a tenant in Microsoft Entra](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Add a user to tenant in Microsoft Entra](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create an organization in Azure portal](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create an Azure DevOps app](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Register Azure DevOps as an OAuth provider](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Configure organization and project level settings](set-up-azure-devops-oauth-2-0-credential.md#)
-   [Create credential record and get OAuth token](set-up-azure-devops-oauth-2-0-credential.md#)
In the **Tool credential** field, select an OAuth 2.0 tool credential record.**Note:** Only records that are not in use and configured for ADO can be selected as an existing credential record.

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to Azure DevOps, see Azure DevOps permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

3.  If your Azure DevOps instance is attached to a MID Server, select the **Use MID Server** option and enter its details.

    For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md)

4.  Select **Submit**.

    The tool is automatically connected using a connection alias and HTTP tool connection \(Basic Auth credential\) and the tool record details are shown in a form.

    **Note:** If you do not have global admin privileges for your tool \(to allow automatic configuration of the webhook URL\), you might need to have the tool admin user configure it for you \(cut and paste the webhook URL into the tool configuration\). Once the webhook is configured in the tool, **Enter Manual Configuration Mode** to connect to the tool manually, then exit.

5.  On successful tool creation, you're taken to the tool record page.
6.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

7.  Discover tool objects, including existing application plans \(projects associated with the tool\), repositories, orchestration tasks, and pipelines.

    -   Connected to organization: Select **Discover projects** to discover the projects from the organization. After discovery, the projects from your organization are available under the **Projects** related list.
    -   Connected to a project: The project is discovered during connection creation and is available under the **Projects** related list. Selecting **Discover projects** from the **Projects** tab of the tool record page discovers all the projects in your organization.
    Select a project from the **Projects** related list to navigate to the project record page. Select **Discover** to discover the project objects, including existing plans \(boards\), repositories, and pipelines.

8.  Configure webhook URLs in Azure DevOps.

    1.  You can configure directly from the tool records page, or from the project record page for each product.

        -   To configure from the tool records page, select **Configure projects**. Select the projects that you want to configure and select **Continue.**.
        -   To configure from the project records page, first select the project from the tool records page and select **Configure**.
    2.  Enter the DevOps integration user and password and select **Send**.

        On send, webhooks and service connections are automatically created in Azure DevOps. This sends the notifications from Azure DevOps tools to DevOps Change Velocity using the DevOps Integration user. For information on setting up Integration user account, see [Set up integration user account in DevOps Change Velocity](devops-plybk-set-up-system-accts.md).

        **Note:**

        -   The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is enabled. If this step is not required, webhooks are configured using token-based authentication.
        -   When DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is enabled, you can regenerate token \(auto-configure with new token\) from the workspace UI only, which will update integration user password. When DevOps Config is not installed, token can be regenerated from both the workspace and classic UI for token based authentication. Re-generate your token periodically for better security.
    **Note:** For plans, the **Track** field is automatically set to **True**.

9.  For the discovered plans, you can import historical data from the tool and also associate an application with it.

    1.  Open a plan record from the Plans related list.

    2.  Select the **Import** related link.

        Records are created for the plan in the Work Items, Plan Versions, and Features related lists.

        -   Work items related list shows tasks, bugs, and stories.

            **Native State** and **Native Type** fields of the work item contain the original state and type values from the source tool.

        -   Plan Versions related list shows releases.
        -   Features related list shows epics and features.
        **Note:** Historical import of Azure DevOps work items isn’t supported for Agile Boards CMMI process.

    3.  In the Apps related list, select **Edit...** to select an App to associate with the plan \(project\), or select **New** to create one.

        A plan must have an associated App record to complete the planning tool setup.

10. For the discovered repositories, import historical data for the tool, and associate the repository with an app.

    1.  Open the repository record from the Repositories related list.

    2.  Select **Import**.

        Imported branch records and commit records from the repository are added to the corresponding related lists.

    3.  In the **App** field, select the lookup list and select an App record to associate with the repository, or click **New** to create one.

    Imported historical data records are added to the corresponding related lists.


## What to do next

For Azure pipelines, [Model an Azure pipeline in DevOps](model-azure-pipeline-dev-ops.md) to complete the configuration in DevOps Change Velocity.

-   Map each pipeline to a specific app.
-   Create pipeline steps and map each step to an Azure pipeline job.
-   Configure change control.

**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

