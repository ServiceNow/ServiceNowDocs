---
title: Onboard Argo CD to DevOps Change Velocity – Workspace
description: Connect to your Argo CD instance using the DevOps Change Workspace playbook to automate the deployment of applications from GitHub repositories.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Argo CD, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Argo CD to DevOps Change Velocity – Workspace

Connect to your Argo CD instance using the DevOps Change Workspace playbook to automate the deployment of applications from GitHub repositories.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard Argo CD.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d435019e80">

Option

</th><th align="left" id="d435019e83">

Steps

</th></tr></thead><tbody><tr><td id="d435019e89">

**Homepage**

</td><td>

1.  Select the **Connect tool** widget
2.  On the  Connect to a tool  modal, select Argo CD from the **Orchestration** category.


</td></tr><tr><td id="d435019e113">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\).
2.  Select an existing application, or create one. To create an application, see [Create an application - Classic](app-create-all.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select Argo CD from the **Orchestration** category.


</td></tr><tr><td id="d435019e159">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\).
2.  From the Capability list, select **Orchestration**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select Argo CD.


</td></tr></tbody>
</table>2.  Specify a name for the tool in the **Tool name** field, and select **Next**.

    ![Connect to Argo CD tool screen](../image/argocd-5.png)

3.  On the Argo CD instance details playbook activity:

    1.  Enter the URL of your Argo CD instance.

    2.  Enter the login credentials of the Argo CD instance.

        **Note:** To generate a token for the user in Argo CD, go to **Accounts**. Ensure that the user has the capability: apiKey. For more information, see [Argo CD documentation](https://argo-cd.readthedocs.io/en/stable/operator-manual/user-management/#create-new-user).

    3.  Select the MID Server option and enter its details if your Argo CD instance is attached to a MID Server.

        A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    ![Enter Argo CD instance details playbook activity](../image/argocd-6.png)

4.  Select **Connect**.

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
    ![Specify Argo CD tool access playbook activity](../image/argocd-7.png)

6.  From the **Summary** page, select **View tool record** to review the details of the connected instance.

    ![Connection summary page](../image/argocd-8.png)


## Result

You’ve successfully onboarded your Argo CD tool to DevOps Change Velocity.

**Parent Topic:**[Argo CD integration with DevOps Change Velocity](../concept/argo-cd-integration-with-devops-change-velocity.md)

