---
title: Onboard Harness to DevOps Change Velocity - Workspace
description: Connect to your Harness instance using the DevOps Change Workspace playbook to discover pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Harness, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Harness to DevOps Change Velocity - Workspace

Connect to your Harness instance using the DevOps Change Workspace playbook to discover pipelines.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Harness.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d193329e86">

Option

</th><th align="left" id="d193329e89">

Steps

</th></tr></thead><tbody><tr><td id="d193329e95">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to Harness as orchestration tool, you'd select Harness under the **Orchestration** category.


</td></tr><tr><td id="d193329e119">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  From the Connect to a tool modal, select the tool from the appropriate category. For example, if you want to connect to Harness as orchestration tool, you'd select Harness under the **Orchestration** category.


</td></tr><tr><td id="d193329e168">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select the appropriate category. For example, if you want to connect to Harness as orchestration tool, you'd select the **Orchestration** category.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Harness**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like pipelines while connecting to the tool, you must connect your tool from the Application module. The steps for associating tool objects in this procedure are only applicable when you connect your tool from the Application module.

2.  In the **Tool name** field, enter a name for the tool.

    ![Connect to Harness tool screen](../image/harness-workspace-01.png)

3.  Select **Next**.

    The DevOps playbook opens to help you complete the onboarding tasks.

4.  Enter your Harness instance details.

    1.  Enter your password or access token for Harness.

    2.  Enter a value in the **Account Identifier** field.

        **Note:** Account Identifier is the unique identifier for your account in the Harness platform. Copy it from Account Settings of your Harness account.

    3.  If your Harness instance is attached to a MID Server, select the **MID Server** option and enter its details.

        For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

    4.  Select **Connect**.

        ![Connect to a tool - Enter instance details page](../image/harness-workspace-2.png)

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
6.  In the Configure webhooks manually screen, copy the ServiceNow instance connection details for Harness.

    ![Configure webhooks manually screen](../image/harness-workspace-3.png)See [Configure webhooks in Harness manually](configure-webhooks-in-harness-manually.md) for more information.

7.  Select the pipelines that you want to track and associate to the application, and select **Associate pipelines**.

    For each selected pipeline, all steps are imported for the last successful execution.

8.  In the Assign services to pipeline steps activity, specify **Step type** and **Service** for each pipeline step.

    Completing this step as part of tool onboarding enables the DevOps Insights dashboards to show more meaningful data immediately.

9.  In the Import historical data step, select the date range in the **Start date** and **End date** fields and select **Import data**.

    **Note:** You can import up to 90 days of data.

10. Select **Next**.

11. From the **Summary** page, review the details of the successfully connected Harness tool.

    Select **View tool record** to review the details of the connected instance.


## Result

You’ve successfully onboarded your Harness tool to DevOps Change Velocity.

**Note:** If your tool credential changes, you must also update the credentials in DevOps Change. For more information, see [Update third-party tool credentials in DevOps Change Velocity](update-third-party-tool-credentials-in-devops-change-velocity.md).

**Parent Topic:**[Harness integration with DevOps Change Velocity](../concept/harness-integration-with-devops-change-velocity.md)

