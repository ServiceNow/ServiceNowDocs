---
title: Onboard Jira to DevOps Change Velocity — Workspace
description: Connect to your Jira Server or Jira Cloud instance from the DevOps Change Workspace to discover available plans and register webhooks to track projects, stories, features, and epics.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Jira, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Jira to DevOps Change Velocity — Workspace

Connect to your Jira Server or Jira Cloud instance from the DevOps Change Workspace to discover available plans and register webhooks to track projects, stories, features, and epics.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Jira.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d359128e100">

Option

</th><th align="left" id="d359128e103">

Steps

</th></tr></thead><tbody><tr><td id="d359128e109">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Jira from the **Plan** category.


</td></tr><tr><td id="d359128e136">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Jira from the **Plan** category.


</td></tr><tr><td id="d359128e188">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select **Planning**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Jira**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like plans while connecting to the tool, you must connect your tool from the Application module.

2.  Connect to your Jira Server or Jira Cloud instance.

<table id="table_h2d_2lv_kbc"><tbody><tr><td>

Jira Server

</td><td>

1.  From the **Platform** list, select **Jira Server**.
2.  In the **Tool name** field, enter a name for the tool.

This name is used to identify your Jira instance from the list of tools connected to DevOps Change Velocity.

 ![Connect to Jira server.](../image/jira-plybk-02.png)

</td></tr><tr><td>

Jira Cloud

</td><td>

1.  From the **Platform** list, select **Jira Cloud**.
2.  In the **Tool name** field, enter a name for the tool.

This name is used to identify your Jira instance from the list of tools connected to DevOps Change Velocity.

 ![Connect to Jira cloud.](../image/jira-plybk-08.png)

</td></tr></tbody>
</table>3.  Select **Next**.

    The DevOps playbook page opens to help you complete the onboarding tasks.

4.  Complete the connection to your Jira tool using the playbook.

    1.  Enter the connection details.

<table id="table_zld_3lv_kbc"><tbody><tr><td>

Jira Server

</td><td>

1.  Enter your Jira server instance URL.
2.  From the **Credential type** list, select the authentication type you want to use to connect with your Jira server.
    -   **Basic Auth**

        1.  Enter your Jira server username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

        2.  Enter the password or access token to access this instance.
![Enter Jira server basic auth details.](../image/jira-plybk-01.png)

    -   **API Key**

Enter the API token to access the instance.

![Enter Jira server API token.](../image/jira-plybk-11.png)

3.  If your Jira instance is attached to a MID Server, select the **MID Server** option and enter its details.

For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

Jira Cloud

</td><td>

1.  Enter your Jira Cloud instance URL.

**Note:** If you select the credential type as **OAuth 2.0 with 3LO** in the next step, you must enter your Jira instance URL in the following format:

    ```
https://api.atlassian.com/ex/jira/<Cloud-ID>
    ```

For information on obtaining the value of Cloud ID, see [Obtain the value of Cloud ID](https://www.servicenow.com/docs/access?context=setup-jira-serv-mgmt&version=australia&pubname=australia-integrate-applications&section=jira-cloud-id&ft:locale=en-US).

2.  Select the credential type as **Basic Auth** or **OAuth 2.0 with 3LO**.

**Basic Auth**

    1.  Enter your Jira Cloud username.

**Note:** The Jira user that you use here must have the Jira Administrators permissions.

    2.  Enter the password or access token to access this instance. ![Enter Jira Cloud instance details for basic authentication](../image/jira-plybk-12.png)
**OAuth 2.0 with 3LO**

Pre-requisites:

    -   
    -   
    -   Create a credential record for Jira Cloud
Select an existing OAuth 2.0 credential record in the **Credential** field, or select **Create OAuth 2.0 credential record** to create a new record. For instructions on creating a new credential record, see Create a credential record for Jira Cloud.

**Note:**

    -   The option to create a new OAuth 2.0 will only be available if you have the connection &amp; OAuth admin role.
    -   Only records that are not in use and configured for Jira Cloud can be selected as an existing credential record.
![Enter Jira Cloud instance details for OAuth 2.0 authentication](../image/jira-plybk-10.png)

3.  If your Jira instance is attached to a MID Server, select the **MID Server** option and enter its details.

For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

</td></tr></tbody>
</table>    2.  Select **Connect**.

        If the connection is successful, the tool is created in the DevOps Change Velocity and connected to your Jira instance.

    3.  Permission checks are run on the credentials that you entered.

        Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see Jira permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

        You can choose to continue with the tool connection even if you don't have all the required permissions.

        ![Permission checks for connecting to Jira.](../image/jira-plybk-07.png)

    4.  Select **Next**.

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

        ![Specify tool access.](../image/jira-plybk-04.png)

6.  To send data in real time between DevOps and your Jira instance, select **Configure**.

    This action does the following:

    -   Registers a webhook between your Jira and ServiceNow instances, and enables real-time data transfer between the two.
    -   If you have connected your Jira tool using OAuth 2.0 based authentication, the webhooks are created for the OAuth 2.0 integration app in Jira when you configure automatically, whereas if you have connected using basic authentication, the webhooks are created for all your projects in Jira. If you choose to configure the webhooks manually for a Jira tool created using OAuth 2.0 based authentication, a duplicate webhook may get created.
    All the discovered Jira projects are listed as Plans.

    If you don’t choose to configure now, you can enable nightly polling later to fetch data for any tracked plans by setting the **Enable Polling** system property to **Yes**.

    ![Configure Jira instance.](../image/jira-plybk-05.png)

    To configure manually, select **Configure manually**. See [Configure webhooks in Jira manually](config-webhooks-jira-manually.md) for more information.

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then plans available in your Jira instance are discovered. You can track and import historical data from them.
7.  Select the plans to track.

    1.  Select the plans for which you want to track updates and associate to the application.

        After the tool onboarding is complete, the work items only for these selected plans are automatically imported.

    2.  Select **Next**.

        ![Select Plans from Jira to track.](../image/jira-plybk-03.png)

    3.  If you want to import plan data, select the date range and select **Submit**.

        You can import up to 90 days of data.

        ![Import plan data.](../image/jira-plybk-09.png)

8.  From the **Summary** page, select **View tool record** to review the details of the connected instance and the plans discovered from it.

    ![Connection summary.](../image/jira-plybk-06.png)


## Result

You’ve successfully onboarded your Jira tool to DevOps Change Velocity.

## What to do next

From the tool record page, you can:

-   See the details and status of the tool.
-   **Discover** plans and **Configure** webhooks.

    **Note:**

    -   By default, projects are discovered in a set of 50 for Jira Cloud. 50 is the maximum pagination limit supported by Jira. If you want to reduce this value, then you should edit the respective constant in DevOpsCommonConstants script.
    -   Project and version data that are discovered aren't updated or tracked in real time.
-   Assign groups to control access to the tool using the **Maintained by** field.
-   Check credential permissions and update credentials for the tool. For more details, see [Check permissions and update credentials for tools — Workspace](../reference/update-credentials-check-permissions.md).
-   From the **Plans** tab, select a plan to view its details such as imported work items, features, and others.
-   To import historical data from the plans, associate the plans with an application, and import the data. For more information, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).

**Note:** It is recommended not to update the project key for projects in Jira. If the project key is updated, the updated object names will not reflect in DevOps Change Velocity. Only when the object is updated in Jira, the new name will reflect in DevOps Change Velocity.

**Parent Topic:**[Jira integration with DevOps Change Velocity](../concept/jira-integration-dev-ops.md)

**Related topics**  


[Configure webhooks from the tool record](configure-webhooks-from-the-tool-record.md)

