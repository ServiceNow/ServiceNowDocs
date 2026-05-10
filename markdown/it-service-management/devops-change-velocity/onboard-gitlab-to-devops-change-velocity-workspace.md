---
title: Onboard GitLab to DevOps Change Velocity — Workspace
description: Connect to your GitLab instance using the DevOps Change Workspace playbook to discover plans, repositories, and pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard GitLab to DevOps Change Velocity — Workspace

Connect to your GitLab instance using the DevOps Change Workspace playbook to discover plans, repositories, and pipelines.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard GitLab.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d332120e97">

Option

</th><th align="left" id="d332120e100">

Steps

</th></tr></thead><tbody><tr><td id="d332120e106">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to GitLab as coding tool, you'd select GitLab under the **Code** category.


</td></tr><tr><td id="d332120e136">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to GitLab as coding tool, you'd select GitLab under the **Code** category.


</td></tr><tr><td id="d332120e191">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select the appropriate category. For example, if you want to connect to GitLab as coding tool, you'd select the **Coding** category.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **GitLab**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like plans, pipelines, or repositories while connecting to the tool, you must connect your tool from the Application module.

2.  In the **Tool name** field, enter a name for the tool.

    ![Connect to GitLab tool screen](../image/gitlab-connect-workspace-1.png)

3.  Select **Next**.

    The DevOps playbook opens to help you complete the onboarding tasks.

4.  Enter your GitLab instance details.

    1.  Enter your GitLab instance URL.

    2.  In the **Credential type** field, select one.

        -   Basic Auth
        -   OAuth 2.0
    3.  Enter the credentials.

        -   Basic Auth: Enter the username and password/access token of your GitLab instance.

            **Note:** Only personal access token is supported. When you generate the token, select the scope API and grant read/write access including all the groups and projects, container registry, and package registry.

        -   OAuth 2.0: Enter your OAuth credential.

            For more information on OAuth2.0 credentials, see [Setting up GitLab OAuth 2.0 credentials for DevOps](../concept/setting-up-gitlab-oauth.md#).

    4.  If your GitLab instance is attached to a MID Server, select the **MID Server** option and enter its details.

        For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md)

    5.  Select **Connect**.

        ![Connect to Gitlab tool - Enter instance details screen](../image/gitlab-connect-workspace-2.png)

5.  Permission checks are run on the credentials that you entered.

    Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. For detailed information on all the required permissions, see GitLab permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    You can choose to continue with the tool connection even if you don't have all the required permissions.

    ![Connect to Gitlab tool - permission checks screen](../image/gitlab-connect-workspace-3.png)

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
    ![Specify tool access](../image/gitlab-connect-workspace-6.png)

8.  Select the projects for which you want to configure webhooks automatically.

    You can also choose to enable nightly polling to retrieve data for any tracked pipelines by selecting the **Enable Polling** property option in the **Administration** module. See [DevOps Change Velocity properties](../concept/dev-ops-administration.md).

9.  Select **Configure**.

    ![Connect to the Gitlab tool - configure screen](../image/gitlab-connect-workspace-4.png)

    To configure manually, select **Configure manually**. See [Configure webhooks in GitLab manually](configure-webhooks-in-gitlab.md) for more information.

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then plans, repositories, and pipelines available in your project are discovered. You can track and import historical data from them.
10. Select the pipelines that you want to associate to the application, and select **Associate pipelines**.

    For each selected pipeline, all steps are imported for the last successful execution.

11. In the Assign services to pipeline steps activity, specify **Step type** and **Service** for each pipeline step.

    Completing this step as part of tool onboarding enables the DevOps Insights dashboards to show more meaningful data immediately.

12. Select the plans you want to associate to the application, and select **Associate plans**.

13. Select the repositories you want to associate to the application, and select **Associate repositories**.

14. In the Import historical data step, select the date range in the **Start date** and **End date** fields and select **Import data**.

    **Note:** You can import up to 90 days of data.

15. Select **Next**.

16. From the **Summary** page, review the details of the successfully connected GitLab tool.

    Select **View tool record** to review the details of the connected instance.


## Result

You’ve successfully onboarded your GitLab tool to DevOps Change Velocity.

**Note:** If your tool credential changes, you must also update the credentials in DevOps Change. For more information, see [Update third-party tool credentials in DevOps Change Velocity](update-third-party-tool-credentials-in-devops-change-velocity.md).

**Parent Topic:**[GitLab integration with DevOps Change Velocity](../concept/gitlab-integration-dev-ops.md)

**Related topics**  


[Configure webhooks from the tool record](configure-webhooks-from-the-tool-record.md)

