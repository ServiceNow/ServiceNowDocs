---
title: Onboard GitHub to DevOps Change Velocity — Workspace
description: Connect to your GitHub instance using the DevOps Change Workspace playbook to discover, configure, and import repositories, plans, and pipelines.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard GitHub to DevOps Change Velocity — Workspace

Connect to your GitHub instance using the DevOps Change Workspace playbook to discover, configure, and import repositories, plans, and pipelines.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard GitHub.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d355496e97">

Option

</th><th align="left" id="d355496e100">

Steps

</th></tr></thead><tbody><tr><td id="d355496e106">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  From the Connect to a tool modal, select the tool from the appropriate category \(Orchestration, Code, Plan, or Software quality\). For example, if you want to connect to GitHub as coding tool, you'd select the **Coding tools** category.


</td></tr><tr><td id="d355496e133">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to GitHub as coding tool, select GitHub under the **Code** category.


</td></tr><tr><td id="d355496e188">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select the appropriate category. For example, if you want to connect to GitHub as coding tool, you'd select the **Coding** category.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select GitHub.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like pipelines, plans, or repositories while connecting to the tool, you must connect your tool from the Application module.

2.  In the **Tool name** field, enter a name for the tool.

    ![Connect to GitHub](../image/github-plybk-04.png)

3.  Select **Next**.

    The DevOps playbook opens to help you complete the onboarding tasks.

4.  Complete the connection and configuration using the playbook.

    1.  In the **Credential type** field, select one of the following credential type.

        -   Basic Auth
        -   OAuth 2.0 with Authorization Code
        -   OAuth 2.0 with JSON Web Token \(JWT\)
    2.  Enter the credentials.

<table id="table_uxp_shk_ybc"><tbody><tr><td>

Basic Auth

</td><td>

Enter the username and password/access token of your GitHub instance.

 ![GitHub basic auth credential type.](../image/github-basic-auth.png)

</td></tr><tr><td>

OAuth 2.0 with Authorization Code

</td><td>

Select an existing OAuth 2.0 with Authorization Code credential record or create an OAuth 2.0 with Authorization Code credential record. For more information, see [Create a credential record for GitHub App provider \(Authorization Code\)](../concept/dev-ops-github-apps-oauth-auth.md#).

 ![GitHub Oauth 2.0 with Authorization Code credential type](../image/github-oauth-auth.png)

</td></tr><tr><td>

OAuth 2.0 with JSON Web Token \(JWT\)

</td><td>

To connect using OAuth 2.0 with a JWT, you must first perform the following:

-   [Create and configure a GitHub App](../concept/dev-ops-github-apps-oath-jwt.md#)
-   [Generate the Java KeyStore certificate for GitHub](../concept/dev-ops-github-apps-oath-jwt.md#)
-   [Attach the GitHub Java KeyStore certificate to your instance](../concept/dev-ops-github-apps-oath-jwt.md#)
 After completing the prerequisites, you can continue with the DevOps Change Velocity Connect playbook activity:

1.  Select the **Use an existing JWT credential record** option if you want to use an already existing JWT credential record. If this option is not selected, the fields to create a new JWT credential record are displayed. Proceed to the next step.
2.  In the **JKS certificate** field, select an existing JKS certificate. This is the name you entered to uniquely identify the JWT provider. JKS certificates are created using shell commands to create a sys\_certificate record.

For more information, see [Create a JWT signing key for the GitHub JKS certificate](../concept/dev-ops-github-apps-oath-jwt.md#).

3.  In the **Signing key** field, enter the signing key to be assigned to your JKS certificate. This is the export password entered while [generating the JKS certificate](../concept/dev-ops-github-apps-oath-jwt.md#).
4.  In the **GitHub App ID** field, select the app ID of your GitHub App \(available in the About section of your GitHub App configuration in GitHub\). The following image displays an example of the About section of a GitHub App configuration from where you can access the GitHub App ID, Client ID, and Client secret.

![About page of GitHub App.](../image/github-jwt-about-screen.png)

5.  In the **Client ID** field, select the client ID of your GitHub App \(available in the About section of your GitHub App configuration in GitHub\).
6.  In the **Client secret** field, select the client secret of your GitHub App \(available in the About section of your GitHub App configuration in GitHub\).
7.  In the **Token URL** field, select the location of the token endpoint that the instance uses to retrieve and refresh tokens.

For cloud version, enter: `https://api.github.com/app/installations/<installation_id>/access_tokens`.

For enterprise version, enter: `https://<HOST_URL>/api/v3/app/installations/<installation_id>/access_tokens`.

For the installation id, go to Install App section in your GitHub App configuration in GitHub and select the gear icon to configure your app. The installation id will be in the webpage URL. For example, https://github.com/settings/installations/&lt;installation\_id&gt;.

![GitHub Oauth 2.0 with JWT credential type.](../image/github-oauth-jwt.png)

 If the OAuth credential is created using GitHub Apps - JWT, the **Configure with GitHub App** option will be available on the tool record page.

</td></tr></tbody>
</table>        For more information on OAuth2.0 credentials, see [Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity](../concept/setting-up-github-oauth-dev-ops.md).

    3.  Enter a value in the **GitHub app slug name** field to check the permission requirements of the tool before connecting if you have created your Oauth 2.0 credentials using GitHub Apps.

        You can find the app slug name on the settings page of your app.

    4.  If your GitHub instance is attached to a MID Server, select the **MID Server** option and enter its details.

        For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

        **Note:** The OAuth Authorization Code &amp; JWT grant types are supported for GitHub &amp; GitHub Enterprise with MID server.

    5.  Select **Connect**.

        ![Connect GitHub to DevOps Change Velocity.](../image/github-plybk-01.png)

    6.  Permission checks are run on the credentials that you entered.

        Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see GitHub permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

        For OAuth 2.0, if you haven’t entered the GitHub app slug name, the tool is connected without checking permission requirements.

    7.  Select **Next**.

        ![Permission checks](../image/github-plybk-05.png)

5.  Specify the access for the tool.

    1.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field.

        The tasks these users in the groups can perform depends on the role assigned to them.

        -   DevOps Tool Owner role: Can view and edit the tool.
        -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
        -   DevOps Administrator role: Can edit all tools.
        -   Other DevOps roles: Can view the tool.
        **Note:** If you don't select a group and skip this step, all users with the DevOps Tool Owner role will be able to edit the tool.

    2.  If you choose to control access to the tool, the **All App Owners can view and associate tool objects to applications** option becomes available for selection.

        This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

    3.  Select **Assign**.
    ![Specify tool access](../image/github-plybk-06.png)

6.  Configure webhooks automatically in your GitHub instance to send data to DevOps Change Velocity.

    This action configures the following webhooks:

    -   **push**: To gather repository commits, branches, and tags
    -   **workflow\_job**: To gather pipeline data
    -   **issues**: To gather issues \(work item\) data
    **Note:** Completing the configuration as part of this task is recommended as real-time notifications are ideal to maintain current information, particularly for automating change requests. Otherwise, you can set up the webhook by configuring it manually later by enabling nightly polling to fetch data system for any tracked repositories or pipelines by setting the **Enable Polling** property to **Yes**.

    Select the repositories for which you want to configure webhooks and select **Configure**.

    ![Select repositories to configure from GitHub.](../image/github-plybk-02.png)

    To configure manually, select **Configure manually**. See [Configure webhooks in GitHub manually](config-webhooks-github-manually.md) for more information.

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then repositories and pipelines available are discovered. You can track and import historical data from them.
7.  Select the plans to track.

    1.  Select the plans for which you want to track updates and associate to the application.

        After the tool onboarding is complete, the work items only for these selected plans are automatically imported.

    2.  Select **Next**.

        ![Track plans playbook step](../image/github-issues-plan-playbook.png)

8.  Select the repositories to track.

    1.  Select the repositories for which you want to track updates and associate to the application.
    2.  Select **Next**.

        ![Select repositories for tracking.](../image/github-plybk-08.png)

    3.  If you want to import repository data, select the date range and select **Submit**.

        You can import up to 90 days of data. Workflows associated with the repositories will also be imported.

9.  Select the pipelines to track.

    1.  Select the pipelines for which you want to track updates and associate to the application.

    2.  Select **Next**.

    3.  For each selected pipeline, all steps or stages are imported for the last successful execution. In the Assign services to pipeline steps activity, you can select the following for each pipeline step:
        1.  **Pipeline step type**: Select a step type for which you want to assign a service.

            **Tip:** Specify at least the **Prod deploy** step type for steps that represents the production deployment to enable DevOps to identify successful pipeline executions as production deployments.

        2.  **Service**: Select the CMDB application service that the pipeline step maps to.

            Application service maps approximately to the environment. If you use the same pipeline step to deploy to different environments, leave the field empty. Service information enables DevOps to identify and report on operational metrics such as incidents, outages, and so on.

    4.  Select **Next**.

        ![Assign services to pipelines from GitHub.](../image/github-plybk-03.png)

10. From the **Summary** page, select **View tool record** to review the details of the connected GitHub tool.

    ![Connection summary](../image/github-plybk-07.png)

    For GitHub Actions pipelines, you must perform some additional steps like creating secrets, defining the workflow configuration in GitHub, and so on. For more information, see [GitHub Actions configurations](../concept/github-actions-integration-with-devops.md#).


## Result

You’ve successfully onboarded your GitHub tool to DevOps Change Velocity.

## What to do next

You can manually discover plans after your GitHub tool is onboarded as well. As there is no plan entity in GitHub, the repositories will be considered to discover corresponding plan records in ServiceNow.

1.  From the tool record page, select **Discover** to discover plans.
2.  Select **Configure**. Plans are tracked and a webhook called **issues** is created to send real-time notifications for work items.

The following information is updated for a work item in ServiceNow when the corresponding issue is updated in GitHub.

-   Change in issue title
-   Assignees update
-   Transfer issue

    **Note:** When an issue is transferred, the same will be marked as transferred in the repository from which it is being transferred and opened in the repository to which it is being transferred.

-   Delete issue

    **Note:** When an issue is deleted in GitHub, the corresponding work item is not deleted in ServiceNow but the state of the work item will be marked as deleted.


If you are an upgrading customer, plans will be discovered for your repositories through the scheduled job to discover periodically or through manual discovery. After your plans are discovered, you can enable the **sn\_devops.track.github.issues** property to re-configure all the previously configured repositories at once so that all plans are tracked and the issues webhook is created for work items.

**Note:** Historical import of plans is not supported.

**Parent Topic:**[GitHub integration with DevOps Change Velocity](../concept/github-integration-dev-ops.md)

**Related topics**  


[Configure webhooks from the tool record](configure-webhooks-from-the-tool-record.md)

