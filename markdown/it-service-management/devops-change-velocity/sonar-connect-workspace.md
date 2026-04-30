---
title: Onboard SonarQube to DevOps Change Velocity — Workspace
description: Connect to your Sonar instance using the DevOps Change Workspace playbook.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [SonarQube, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard SonarQube to DevOps Change Velocity — Workspace

Connect to your Sonar instance using the DevOps Change Workspace playbook.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard SonarQube.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d392920e90">

Option

</th><th align="left" id="d392920e93">

Steps

</th></tr></thead><tbody><tr><td id="d392920e99">

**Homepage**

</td><td>

1.  Select the **Connect tool** widget
2.  On the  Connect to a tool  modal, select SonarQube from the **Software quality** category.


</td></tr><tr><td id="d392920e126">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\).
2.  Select an existing application, or create one. To create an application, see [Create an application - Classic](app-create-all.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select SonarQube from the **Software quality** category.


</td></tr><tr><td id="d392920e175">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\).
2.  From the Capability list, select **Software quality**.
3.  Select **Connect a tool**.
4.  On the  **Connect to a tool ** modal, select **SonarQube**.


</td></tr></tbody>
</table>2.  Enter a name to identify your tool and click **Next**.

3.  On the Enter Sonar instance details playbook activity section, enter the following details:

    1.  In the **URL of the SonarQube instance** field, enter the SonarQube or SonarCloud instance URL.

        For example, https://sonarcloud.io.

    2.  In the **SonarQube username** field, enter the user name for your Sonar account.
    3.  In the **Password or access token** field, enter the token generated in Sonar.
    4.  If your Sonar instance is attached to a MID Server, select the **Use MID Server** option and enter its details.

        A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

4.  Click **Connect** and review the details of the successfully connected Sonar instance.

    ![Connect to SonarQube instance in DevOps Change workspace.](../image/sonar-plybk-01.png)

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
    ![Specify tool access](../image/sonar-plybk-03.png)

6.  From the **Summary** page, select **View tool record** to review the details of the connected instance.

    ![Connection summary](../image/sonar-plybk-04.png)


## Result

You’ve successfully onboarded your SonarQube tool to DevOps Change Velocity.

**Parent Topic:**[SonarQube integration with DevOps Change Velocity](../concept/sonarqube-devops-integration-devops.md)

