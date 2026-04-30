---
title: Onboard Azure DevOps to DevOps Change Velocity — Service Catalog
description: Create, connect, discover, and configure your Azure DevOps instance using the ServiceNow Service Catalog.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Azure DevOps, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Azure DevOps to DevOps Change Velocity — Service Catalog

Create, connect, discover, and configure your Azure DevOps instance using the ServiceNow Service Catalog.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items** and search for DevOps.

    **Note:** You can also access the service catalog from Employee Center or Service portal.

2.  From the DevOps catalog items, select and activate **DevOps App Onboarding** and **DevOps Tool Onboarding**.

3.  After activating, select **DevOps Tool Onboarding** and select **Try it**.

4.  In the DevOps Tool Onboarding form, enter the tool details:

<table id="table_ubw_p1p_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tool name

</td><td>

Name for your Azure DevOps integration.

</td></tr><tr><td>

Tool integration

</td><td>

Select Azure DevOps.

</td></tr><tr><td>

Connect to an organization or project

</td><td>

Select from the list.-   **Connect an organization**: Connect directly at your Azure DevOps organization level. All the projects within the organization will be discovered, and you can choose to configure multiple projects within the organization.
-   **Connect a project**: Connect directly at the project level.


</td></tr><tr><td>

Tool URL

</td><td>

Azure DevOps organization URL \(for example, `https://dev.azure.com/<your organization>`\) or the Azure DevOps project URL \(for example, `https://dev.azure.com/<your organization>/<your project>`\).

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

</td></tr><tr><td>

Do you wish to configure webhook for this tool?

</td><td>

Option to enable configuring webhooks automatically for Azure DevOps. Select to enable.**Note:** This option isn’t available if you're connecting at the organization level. You can configure webhooks from the tool records page.

</td></tr><tr><td>

Integration username

</td><td>

This field is available only when the option to configure webhook is selected.Enter the username for the DevOps Integration User account.

**Note:**

-   The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is enabled. If this step is not required, webhooks are configured using token-based authentication.
-   When DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is enabled, you can regenerate token \(auto-configure with new token\) from the workspace UI only, which will update integration user password. When DevOps Config is not installed, token can be regenerated from both the workspace and classic UI for token based authentication. Re-generate your token periodically for better security.
.

</td></tr><tr><td>

Integration user password

</td><td>

This field is available only when the option to configure webhook is selected.Enter the password for the DevOps Integration User account.

**Note:**

-   The step to enter the integration user name and password is required to configure only when DevOps Config is installed or the **This property decides whether to create a Generic Connection on configure operation for Azure DevOps** property is enabled. If this step is not required, webhooks are configured using token-based authentication.
-   When DevOps Config is installed or the Generic Connection on configure operation for Azure DevOps property is enabled, you can regenerate token \(auto-configure with new token\) from the workspace UI only, which will update integration user password. When DevOps Config is not installed, token can be regenerated from both the workspace and classic UI for token based authentication. Re-generate your token periodically for better security.


</td></tr><tr><td>

Use MID Server

</td><td>

Optional. Select  MID Server for an on-premises tool that is attached to a  MID Server. Application is automatically set to  DevOps and capability is set to REST.

</td></tr></tbody>
</table>    For a list of all the permissions required on the credentials for connecting to Azure DevOps, see Azure DevOps permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

5.  Select **Order Now**.

    A request is created. When the request is approved:

    -   If connecting to an organization, the tool is created.
    -   If connecting to a project, the tool is created, connected, and project objects like plans, repositories, and pipelines are discovered.
6.  When connecting to a project, for the discovered objects, you can import historical data from the tool and also associate an application with it.
7.  From the DevOps catalog items, select **DevOps App Onboarding**.

8.  Select **Try It**.

9.  In the DevOps App Onboarding form, enter the details:

<table id="table_vb5_s3p_gwb"><tbody><tr><td>

Are you creating a new app or adding to an existing one?

</td><td>

Select from the options whether to create a new app or use an existing app.

</td></tr><tr><td>

App

</td><td>

Enter the name for the app that you're creating or using.

</td></tr><tr><td>

Onboarding pipelines

</td><td>

Enter the connected Azure DevOps tool name.

</td></tr><tr><td>

Pipelines

</td><td>

Select the pipelines for which you want to import historical data.

</td></tr><tr><td>

Artifact repositories

</td><td>

Select the artifacts for which you want to import historical data.

</td></tr><tr><td>

Onboarding repositories

</td><td>

Enter the connected Azure DevOps tool name.

</td></tr><tr><td>

Import from and Import to

</td><td>

Select the dates for which you want to import the pipeline and artifact data. By default, the last 30 days are selected. You can choose to import data for a maximum of 90 days.

</td></tr><tr><td>

Repositories

</td><td>

Select the repositories for which you want to import historical data.

</td></tr><tr><td>

Import from and Import to

</td><td>

Select the dates for which you want to import the Repositories data. By default, the last 30 days are selected. You can choose to import data for a maximum of 90 days.

</td></tr><tr><td>

Onboarding plans

</td><td>

Enter the connected Azure DevOps tool name.

</td></tr><tr><td>

Plans

</td><td>

Select the plans for which you want to import historical data.

</td></tr><tr><td>

Import from and Import to

</td><td>

Select the dates for which you want to import the Plans data. By default, the last 30 days are selected. You can choose to import data for a maximum of 90 days.

</td></tr></tbody>
</table>10. Select **Order Now**.

    A request is created. When the request is approved, the plans, repositories, artifacts, and pipeline objects are associated to the app record and webhooks are configured for real-time tracking. Historical data is imported for the selected items. The **Track** field is automatically enabled for imported plans, repositories, and pipelines.


**Parent Topic:**[Azure DevOps integration with DevOps Change Velocity](../concept/azure-devops-integration-dev-ops.md)

