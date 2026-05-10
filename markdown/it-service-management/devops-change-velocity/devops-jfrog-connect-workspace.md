---
title: Onboard JFrog to DevOps Change Velocity — Workspace
description: Connect to your JFrog instance using the DevOps Change Workspace playbook to track artifact repositories published to JFrog.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [JFrog, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard JFrog to DevOps Change Velocity — Workspace

Connect to your JFrog instance using the DevOps Change Workspace playbook to track artifact repositories published to JFrog.

## Before you begin

Complete the tasks specified in the [Getting started with DevOps Change Velocity](../concept/setting-up-devops-change-velocity.md) topic.

Install the JFrog plugin \(x\_snc\_jfrog\) from the ServiceNow® Store to enable bearer token authentication and integration with JFrog AppTrust application. For more information, see [Integration with JFrog AppTrust application](../concept/integration-with-jfrog-apptrust-application.md).

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **Workspaces** &gt; **DevOps Change Workspace** and use one of the following options to open the Playbook to onboard JFrog.

<table id="choicetable_m3t_ky1_fwb"><thead><tr><th align="left" id="d386213e121">

Option

</th><th align="left" id="d386213e124">

Steps

</th></tr></thead><tbody><tr><td id="d386213e130">

**Homepage**

</td><td>

1.  Select the **Connect tool** widget
2.  On the  Connect to a tool  modal, select JFrog from the **Artifact** category.


</td></tr><tr><td id="d386213e157">

**Applications module**

</td><td>

1.  Select **Applications** \(![Applications icon.](../image/applications-icon.png)\).
2.  Select an existing application, or create one. To create an application, see [Create an application - Classic](app-create-all.md).
3.  From the  Recommended actions  pane, select the  **Connect a tool ** card.
4.  On the  Connect to a tool  modal, select JFrog from the **Artifact** category.


</td></tr><tr><td id="d386213e206">

**Tools module**

</td><td>

1.  Select **Tools** \(![Tools icon.](../image/tools-icon-wkspc.png)\).
2.  From the Capability list, select **Artifact**.
3.  Select **Connect a tool**.
4.  On the  Connect to a tool  modal, select JFrog.


</td></tr></tbody>
</table>2.  Specify a name for the tool in the **Tool name** field, and select **Next**.

    ![Connect to the JFrog tool screen](../image/jfrog-workspace-1.png)

3.  On the JFrog instance details playbook activity:

    1.  Enter the URL of your JFrog instance.

    2.  Select the credentials type as **Basic Auth** or **Bearer Token**.

    3.  Based on the credential type, do one of the following:

        -   For Basic Auth, select the login credentials of the primary user.
        -   For Bearer Token, select the bearer token associated with the project.

            **Note:** Bearer token can be generated from the AppTrust Integrations page of your JFrog tool. For more information, see [Integration with JFrog AppTrust application](../concept/integration-with-jfrog-apptrust-application.md).

    4.  Select the MID Server option and enter its details if your JFrog instance is attached to a MID Server.

        A MID server is required if your tool instance is hosted on-prem. For more information about MID server, see [MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/c_MIDServerSelector.md).

    ![Connect to the JFrog tool - Enter instance details screen](../image/jfrog-workspace-connect-2.png)

4.  Select **Connect**.

5.  Permission checks are run based on the credential type and credentials that you entered.

    Permissions required and permissions that are available are displayed. If you want to enter credentials with better permissions, select **Re-enter credentials**. The credentials that you specified must have the Administer Platform role in JFrog for seamless discovery and import of tool objects. This is a limitation from JFrog. For detailed information on all the required permissions, see Jira permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    You can choose to continue with the tool connection even if you don't have all the required permissions.

    **Note:** If your tool credential has changed, you must update the credentials in your ServiceNow instance. For more information, see [Update third-party tool credentials in DevOps Change Velocity](update-third-party-tool-credentials-in-devops-change-velocity.md).

    ![Connect to JFrog tool - Permission checks screen](../image/jfrog-workspace-connect-3.png)

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
8.  From the **Summary** page, select **View tool record** to review the details of the connected instance.


## Result

You’ve successfully onboarded your JFrog tool to DevOps Change Velocity.

**Parent Topic:**[JFrog integration with DevOps Change Velocity](../concept/devops-jfrog-integration.md)

