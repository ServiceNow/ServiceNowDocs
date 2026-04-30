---
title: Onboard Rally to DevOps Change Velocity — Workspace
description: Connect to your Rally instance using the DevOps Change Workspace playbook to configure webhooks and discover plans.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Rally, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Rally to DevOps Change Velocity — Workspace

Connect to your Rally instance using the DevOps Change Workspace playbook to configure webhooks and discover plans.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Rally.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d420373e95">

Option

</th><th align="left" id="d420373e98">

Steps

</th></tr></thead><tbody><tr><td id="d420373e104">

**Homepage**

</td><td>

1.  Select **Connect a tool**.
2.  On the  Connect to a tool  modal, select Rally from the Plan category.


</td></tr><tr><td id="d420373e128">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\) from the primary navigation.
2.  Select an existing application, or create one. To create an application, see [Create an application - Workspace](app-create-workspace.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Rally from the Plan category.


</td></tr><tr><td id="d420373e177">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\) from the primary navigation.
2.  From the Capability list, select **Planning**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select **Rally**.


</td></tr></tbody>
</table>    **Important:** If you want to discover and track tool objects like plans while connecting to the tool, you must connect your tool from the Application module.

2.  Enter a tool name to identify your tool and select **Next**.

3.  On the Enter Rally instance details playbook activity, enter the following details:

    1.  In the **URL of the Rally project** field, enter your Rally project URL.
    2.  In the **Password or access token** field, enter the API token for your Rally instance.
    3.  \(Optional\) If your Rally instance is attached to a MID Server, select the **Use MID Server** option and enter its details.

        A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

4.  Select **Connect**.

    On successful connection, the tool is created in ServiceNow and connected to your Rally instance.

    ![Connect Rally to DevOps Change Velocity.](../image/rally-plybk-01.png)

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

    ![Specify tool access.](../image/rally-plybk-04.png)

6.  Configure webhooks automatically in Rally to send real-time notifications.

    **Note:** If you prefer not to configure webhooks, you can enable nightly polling to fetch data for all tracked plans by selecting the **Enable import polling** check box in [DevOps properties](../concept/dev-ops-administration.md).

    1.  Select the plans that you want to track.

    2.  Select **Configure**.

    ![Connect Rally to DevOps Change Velocity.](../image/rally-plybk-03.png)

    **Important:**

    -   If you're connecting from the Home page or Tools module, the connection is complete and you're taken to the Summary page.
    -   If you're connecting from the Applications module, then plans available in your instance are discovered. You can track and import historical data from them.
7.  If you want to import plan data, select the date range and select **Submit**.

    You can import up to 90 days of data.

    ![Import plan data.](../image/rally-plybk-06.png)

8.  From the **Summary** tab, select **View tool record** to review the details of the connected instance and the plans discovered from it.

    ![Connection summary.](../image/rally-plybk-05.png)


## Result

You’ve successfully onboarded your Rally tool to DevOps Change Velocity.

## What to do next

From the tool record page, you can do the following:

-   See the details and status of the tool.
-   Discover plans and configure webhooks.
-   Assign groups to control access to the tool using the **Maintained by** field.
-   From the **Plans** tab, select a plan to view its details such as imported work items, features, and others.
-   To import historical data from the plans, associate the plans with an application, and import the data. For more information, see [Associate tool objects to applications - Workspace](apps-associate-objects-wkspc.md).

**Parent Topic:**[Rally integration with DevOps Change Velocity](../concept/rally-devops-integration.md)

**Related topics**  


[Configure webhooks from the tool record](configure-webhooks-from-the-tool-record.md)

