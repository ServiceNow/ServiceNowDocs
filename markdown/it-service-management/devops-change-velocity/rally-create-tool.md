---
title: Onboard Rally to DevOps Change Velocity — Classic
description: With this integration, you can configure and expose data like projects, user stories, and defects from the Rally. You can then associate these planning objects to application for end-to-end traceability.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Rally, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Rally to DevOps Change Velocity — Classic

With this integration, you can configure and expose data like projects, user stories, and defects from the Rally. You can then associate these planning objects to application for end-to-end traceability.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner

## Procedure

1.  Navigate to **All** &gt; **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)**.

2.  In the Create DevOps tool form, enter the tool details:

<table id="table_lfh_tr1_fwb"><tbody><tr><td>

Tool name

</td><td>

Name for the tool you're integrating.

</td></tr><tr><td>

Tool integration

</td><td>

Tool to integrate. Select Rally.

</td></tr><tr><td>

Tool URL

</td><td>

URL of your Rally instance to integrate.

</td></tr><tr><td>

Tool password / Access token

</td><td>

Enter the API key for Rally.

</td></tr><tr><td>

Use MID Server

</td><td>

MID Server is optional. Select MID Server for an on-premises tool that is attached to a MID Server. The Application value is automatically set to DevOps and the Capability value is set to REST. For more information, see [MID Server selection](https://www.servicenow.com/docs/access?context=c_MIDServerSelector&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr></tbody>
</table>3.  Click **Submit** to connect to your Rally instance.

4.  On successful tool creation, you’re taken to the tool record page.
5.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

6.  Click **Discover** to import existing projects associated with Rally.

    Plan records are added to the **Plans** related links.

7.  To configure webhooks for Rally projects:

    1.  Click **Configure**.
    2.  Select the projects for which you want to configure webhooks and click **Continue**.
8.  To import historical data, select a plan and click **Import**.

    Select the dates to import historical data from the Rally project. You can see the imported data under **Work Items**. Select a work item to see details including commits made.

    **Note:** Scheduledstate in Rally is used when mapping object state to internal ServiceNow work item state.

    Formatted id is used for the work item NativeID, for associating work items and commits.


**Parent Topic:**[Rally integration with DevOps Change Velocity](../concept/rally-devops-integration.md)

