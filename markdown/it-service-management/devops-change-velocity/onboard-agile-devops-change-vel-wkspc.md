---
title: Onboard Agile Development 2.0 to DevOps Change Velocity — Workspace
description: Connect to your Agile Development 2.0 instance using the DevOps Change Workspace playbook to enable tracking of stories and epics.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Agile Development 2.0, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Agile Development 2.0 to DevOps Change Velocity — Workspace

Connect to your Agile Development 2.0 instance using the DevOps Change Workspace playbook to enable tracking of stories and epics.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Activate the Agile Development 2.0 plugin. For more information, see [Activate Agile Development 2.0](https://www.servicenow.com/docs/access?context=activate-agile-development&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US).

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Agile Development 2.0.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d427182e107">

Option

</th><th align="left" id="d427182e110">

Steps

</th></tr></thead><tbody><tr><td id="d427182e116">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Agile Development 2.0 from the **Plan** category.


</td></tr><tr><td id="d427182e143">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Agile Development 2.0 from the **Plan** category.


</td></tr><tr><td id="d427182e195">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select **Planning**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Agile Development 2.0**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like plans while connecting to the tool, you must connect your tool from the Application module.

2.  In the **Tool name** field, enter a name for the tool.

    ![Connect to Agile Development 2.0](../image/agile2-plybk-03.png)

3.  Select **Next**.

    The DevOps playbook opens to help you complete the onboarding tasks.

4.  Select **Connect**.

    ![Connect Agile Development 2.0.](../image/agile2-plybk-01.png)

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
    ![Specify the tool access](../image/agile2-plybk-04.png)

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then plans available in your project are discovered. You can track and import historical data from them.
6.  Select the plans for which you want to track updates and associate to the application, and select **Next**.

    If you don’t choose to select plans now, you can enable nightly polling later to fetch the data for any tracked plans by setting the **Enable Polling** system property to **Yes**.

    ![Track work items from Agile Development 2.0.](../image/agile2-plybk-02.png)

7.  If you want to import plan data, select the date range and select **Submit**.

    You can import up to 90 days of data.

8.  From the **Summary** page, select **View tool record** to review the details of the connected instance and the plans discovered from it.

    ![Connection summary](../image/agile2-plybk-05.png)


## Result

You’ve successfully onboarded your Agile Development 2.0 tool to DevOps Change Velocity.

**Parent Topic:**[Agile Development 2.0 integration with DevOps Change Velocity](../concept/agile-integration-dev-ops.md)

