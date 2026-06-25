---
title: Onboard Bitbucket to DevOps Change Velocity — Workspace
description: Create, connect, discover, and configure your Bitbucket instance using the DevOps Change Velocity workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/devops-wkspc-bitbucket-tool-conn.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Bitbucket, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Bitbucket to DevOps Change Velocity — Workspace

Create, connect, discover, and configure your Bitbucket instance using the DevOps Change Velocity workspace.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Bitbucket.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d413187e96">

Option

</th><th align="left" id="d413187e99">

Steps

</th></tr></thead><tbody><tr><td id="d413187e105">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Bitbucket from the **Code** category.


</td></tr><tr><td id="d413187e132">

**Applications module**

</td><td>

1.  Select **Applications** \(\[Omitted image "applications-icon.png"\] Alt text: Applications icon.\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Bitbucket from the **Code** category.


</td></tr><tr><td id="d413187e184">

**Tools module**

</td><td>

1.  Select **Tools** \(\[Omitted image "tools-icon-wkspc.png"\] Alt text: Tools icon.\) from the primary navigation.
2.  From the Capability list, select **Coding**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select Bitbucket.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like repositories while connecting to the tool, you must connect your tool from the Application module.

2.  Select **Bitbucket Cloud** or **BitBucket Server** from the Platform drop-down, enter a name for the tool in the **Tool name** field, and select **Next**.

    \[Omitted image "bitbucket-workspace-connect-1.png"\] Alt text: Connect to the Bitbucket tool screen

3.  On the Bitbucket instance details playbook activity, enter the following details.

<table id="choicetable_krv_ykg_42c"><thead><tr><th align="left" id="d413187e272">

Tool

</th><th align="left" id="d413187e275">

Steps

</th></tr></thead><tbody><tr><td id="d413187e281">

**Bitbucket Server**

</td><td>

1.  Enter the URL of your Bitbucket instance.
2.  Enter the login credentials of the global admin for the Bitbucket instance.
3.  If your Bitbucket instance is attached to a MID Server, select the MID Server option and enter its details. A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_MIDServerSelector.md).
\[Omitted image "bitbucket-connect-server.png"\] Alt text: Enter Bitbucket instance details page for Bitbucket Server

</td></tr><tr><td id="d413187e318">

**Bitbucket Cloud**

</td><td>

1.  Select the credential type as one of the following:
    -   Basic Auth
    -   Access Token
    -   OAuth 2.0 - Authorization Code
    -   Oauth 2.0 - Client Credentials
2.  Perform the following steps based on the credential type you selected,

For Basic Auth,

    1.  Enter the email address associated with your Bitbucket Cloud account in the **Bitbucket Cloud email** field.
    2.  Enter the Bitbucket API token with scopes in the **Password** field.

**Note:** For more information on creating basic auth credentials, see [Bitbucket integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/bitbucket-integration-dev-ops.md).

\[Omitted image "bitbucket-connect-cloud-basicauth.png"\] Alt text: Enter Bitbucket instance details page for Bitbucket Cloud - Basic Auth

For Access Token,

    1.  Enter a value in the **Access Token** field.
    2.  Enter the Unique identifier of your Bitbucket Cloud workspace in the **Workspace ID** field.
\[Omitted image "bitbucket-connect-cloud-accesstoken.png"\] Alt text: Enter Bitbucket instance details page for Bitbucket Cloud - Access Token

For Oauth 2.0 - Authorization Code,

    1.  If you have an existing credential record, enter a value in the **Credentials** field.
    2.  If not, create a credential by performing the steps specified in the [Set up OAuth 2.0 Authorization Code for Bitbucket Cloud](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/set-up-oauth-2-0-authorization-code.md) topic.
\[Omitted image "bitbucket-connect-cloud-oauth-auth.png"\] Alt text: Enter Bitbucket instance details page for Bitbucket Cloud - OAuth 2.0 - Authorization Code

For Oauth 2.0 - Client Credentials,

    1.  If you already have an OAuth credential record created, select the **Use an existing OAuth credential record** option, and select the required credential record in the **Credential** field. If not, proceed to the next step.
    2.  Enter a value in the **Client Id** and **Client secret** fields.

**Note:** You can get the Client Id and Client secret values from your Bitbucket account. Client ID of your Bitbucket tool is available in the OAuth consumers section of your workspace settings in the **Key** field of Bitbucket cloud. Client secret of your Bitbucket tool is available in the OAuth consumers section of your workspace settings in the **Secret** field of Bitbucket cloud. For more information, see [Bitbucket integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/bitbucket-integration-dev-ops.md).

\[Omitted image "bitbucket-connect-cloud-oauth-client.png"\] Alt text: Enter Bitbucket instance details page for Bitbucket Cloud - OAuth 2.0 - Client Credentials

3.  If your Bitbucket instance is attached to a MID Server, select the MID Server option and enter its details. A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_MIDServerSelector.md).


</td></tr></tbody>
</table>4.  Select **Connect**.

5.  Permission checks are run on the credentials that you entered.

    Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see Bitbucket permissions in [Permissions required for DevOps tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/tool-req-permission.md).

    You can choose to continue with the tool connection even if you don't have all the required permissions.

6.  Select **Next**.

7.  Specify the access for the tool.

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
    \[Omitted image "bitbucket-workspace-connect-6.png"\] Alt text: Specify tool access.

8.  Select the repositories for which you want to configure webhooks automatically.

    Real-time notifications are ideal to maintain the most up-to-date information particularly for automating change requests.

    You can also set up webhook by configuring it manually. Alternatively, you can choose to enable nightly polling to fetch data system for any tracked repositories by setting the **Enable Polling** property to **Yes**.

9.  Select **Configure**.

    \[Omitted image "bitbucket-workspace-connect-4.png"\] Alt text: Connect to the Bitbucket tool - select items to configure screen

    To configure manually, select **Configure manually**. See [Configure webhooks in Bitbucket manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/config-webhooks-bitbucket-manually.md) for more information.

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then repositories available in your instance are discovered. You can track and import historical data from them.
10. Select the repositories you want to associate to the application, and select **Associate repositories**.

11. In the Import historical data step, select the date range in the **Start date** and **End date** fields and select **Import data**.

    **Note:** You can import up to 90 days of data.

    Imported commits, branches, and pull request records from the repository are added to the corresponding related lists.

12. Select **Next**.

13. From the **Summary** page, review the details of the successfully connected Bitbucket tool.

    Select **View tool record** to review the details of the connected instance and the repositories discovered from it.

    \[Omitted image "bitbucket-workspace-connect-7.png"\] Alt text: Connection summary


## Result

You’ve successfully onboarded your Bitbucket tool to DevOps Change Velocity.

**Note:** If your tool credential changes, you must also update the credentials in DevOps Change. For more information, see [Update third-party tool credentials in DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/update-third-party-tool-credentials-in-devops-change-velocity.md).

**Parent Topic:**[Bitbucket integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/bitbucket-integration-dev-ops.md)

**Related topics**  


[Configure webhooks from the tool record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/configure-webhooks-from-the-tool-record.md)

