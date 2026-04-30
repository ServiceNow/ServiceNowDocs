---
title: Onboard Jenkins to DevOps Change Velocity — Classic
description: Connect your Jenkins instance to discover and track your pipelines, and import your orchestration tasks for end to end traceability and change automation.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Jenkins to DevOps Change Velocity — Classic

Connect your Jenkins instance to discover and track your pipelines, and import your orchestration tasks for end to end traceability and change automation.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

Install and enable the **ServiceNow DevOps** plugin for Jenkins. If you've already installed it, update to the latest version. For instructions, see [Configure Jenkins plugin](configure-jenkins-plugin.md#).

## About this task

Actions:

-   **Connect** to Jenkins and get the webhook URL when you submit a DevOps tool record.
-   **Discover** orchestration tasks and pipelines.
-   **Import** task execution and step execution records.

**Note:** You can authenticate your connection with Jenkins using Jenkins API tokens. For more information, see [Connect to Jenkins using API token authentication](authenticate-jenkins-using-api-token.md).

## Procedure

1.  Create a tool record in DevOps to automatically connect to Jenkins and get the webhook URL.

    1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)** and create a record.

    2.  Enter a **Tool Name** and fill in the tool details.

<table id="table_aqb_5w1_ymb"><tbody><tr><td>

Tool Integration

</td><td>

Jenkins

</td></tr><tr><td>

Tool URL

</td><td>

Jenkins tool URL

 For example:

 `https://jenkins.com`

</td></tr><tr><td>

Tool Username

</td><td>

Jenkins user name

</td></tr><tr><td>

Tool Password / Access Token

</td><td>

Jenkins password, access token or the API token you generate.**Note:** To generate API token, see [Connect to Jenkins using API token authentication](authenticate-jenkins-using-api-token.md).

</td></tr></tbody>
</table>        For a list of all the permissions required on the credentials for connecting to Jenkins, see Jenkins permissions in [Permissions required for DevOps tools](../reference/tool-req-permission.md).

    3.  Select MID Server for an on-premises tool that is attached to a MID Server.

        The Application value is automatically set to DevOps and the Capability value is set to REST.

    4.  Click **Submit**.

        The tool is connected successfully.

2.  On successful tool creation, you're taken to the tool record page.
3.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

4.  Click **Discover** to discover the existing orchestration tasks \(Jenkins stages\) and pipelines.

    **Note:** Orchestration tasks and pipelines are discovered for folders nested to the level specified in the **sn\_devops.discover.folder.depth** property. For more information, see [Properties installed with DevOps](../concept/dev-ops-administration.md).

    Records are added to the corresponding related lists.

5.  Open a discovered record from the Orchestration Tasks related list and click the **Import** related link to import historical data from the orchestration task.

    Imported task execution records and step execution records are added to the corresponding related lists.


**Parent Topic:**[Jenkins integration with DevOps Change Velocity](../concept/jenkins-integration-dev-ops.md)

