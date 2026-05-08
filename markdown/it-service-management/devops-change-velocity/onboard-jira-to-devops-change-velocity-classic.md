---
title: Onboard Jira to DevOps Change Velocity — Classic
description: Connect your Jira Server or Jira Cloud instance to discover, configure, and import projects and work items such as stories, epics, and features.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Jira, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Jira to DevOps Change Velocity — Classic

Connect your Jira Server or Jira Cloud instance to discover, configure, and import projects and work items such as stories, epics, and features.

## Before you begin

Complete the tasks in [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md).

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Connect to your Jira Server or Jira Cloud instance.

    1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

    2.  Enter the details for connecting to your Jira instance.

<table id="table_yz2_qlv_kbc"><tbody><tr><td>

Jira Server

</td><td>

1.  In the **Tool name** field, enter a name for the tool.
2.  In the **Tool integration** field, search for and select Jira.
3.  Enter your Jira server instance URL.
4.  From the **Credential type** list, select the authentication type you want to use to connect with your Jira server.
    -   **Basic Auth**

        1.  Enter your Jira server username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

        2.  Enter the password or access token to access this instance.
    -   **API Key**

Enter the API token to access the instance.

</td></tr><tr><td>

Jira Cloud

</td><td>

1.  In the **Tool name** field, enter a name for the tool.
2.  In the **Tool integration** field, search for and select Jira Cloud.
3.  in the **Tool URL** field, enter your Jira Cloud instance URL.
4.  In the **Credential type** field, select **Basic Auth** or **OAuth 2.0**.

**Basic Auth**

    1.  Enter your Jira Cloud username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

    2.  Enter the password or access token to access this instance.
**OAuth 2.0**

Pre-requisites:

    -   
    -   Obtain the value of Cloud ID
    -   
    -   Create credential record for Jira Cloud
In the **Tool credential** field, select an existing OAuth 2.0 tool credential record.

**Note:** Only records that are not in use and configured for Jira Cloud can be selected as an existing credential record.

</td></tr></tbody>
</table>        For a list of all the permissions required on the credentials for connecting to Jira, see Jira permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    3.  If your Jira instance is attached to a MID Server, select the **MID Server** option and enter its details.

        For more information about MID server, see MID Server selection

    4.  Select **Submit**.

    The tool is automatically connected using a connection alias and HTTP tool connection \(Basic Auth credential\).

2.  On successful tool creation, you're taken to the tool record page.
3.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    |Role|Description|
    |----|-----------|
    |DevOps Tool Owner role|Can view and edit the tool.|
    |DevOps App Owner role|Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).|
    |DevOps Administrator role|Can edit all tools.|
    |Other DevOps roles|Can view the tool.|

    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

4.  Select **Discover**  to discover all existing projects from Jira.

    **Note:** By default, projects are discovered in a set of 50 for Jira Cloud. 50 is the maximum pagination limit supported by Jira. If you want to reduce this value, then you should edit the respective constant in DevOpsCommonConstants script.

5.  Select **Configure** to configure webhooks.

    This action does the following:

    -   Registers a webhook between your Jira and ServiceNow instances, and enables real-time data transfer between the two.
    -   If you have connected your Jira tool using OAuth 2.0 based authentication, the webhooks are created for the OAuth 2.0 integration app in Jira when you configure automatically, whereas if you have connected using basic authentication, the webhooks are created for all your projects in Jira.
    All the discovered Jira projects are listed as Plans.

    If you don’t choose to configure now, you can enable nightly polling later to fetch data for any tracked plans by setting the **Enable Polling** system property to **Yes**.

    **Note:** If you don’t have admin privileges for Jira to allow automatic configuration of the webhook URL, request your Jira admin to configure it for you. This action would require creating and configuring the webhook URL manually in your tool instance. After the webhook is configured in the tool, select **Enter Manual Configuration Mode** to connect to Jira manually, then exit the manual configuration mode.

6.  Select the  **Import**  related link to import historical data from Jira projects.

    Imported work items are added to the corresponding related lists.

    **Note:** If the project key for a project is updated in Jira, the updated object names will not reflect in DevOps Change Velocity. Only when the object is updated in Jira, the new name will reflect in DevOps Change Velocity.


**Parent Topic:**[Jira integration with DevOps Change Velocity](../concept/jira-integration-dev-ops.md)

