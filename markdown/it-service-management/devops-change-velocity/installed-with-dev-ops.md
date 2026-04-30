---
title: Components installed with DevOps Change Velocity
description: Several types of components are installed with DevOps Change Velocity, including tables, users, roles, and scheduled jobs.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# Components installed with DevOps Change Velocity

Several types of components are installed with DevOps Change Velocity, including tables, users, roles, and scheduled jobs.

Demo data is available for this application.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Users installed

<table id="table_cvk_4ps_jjb"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

devops.integration.user

</td><td>

DevOps Integration User

 **Note:** You must configure the password before the DevOps Integration User can configure a tool.

</td></tr><tr><td>

devops.system

</td><td>

DevOps System user

</td></tr></tbody>
</table>## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

DevOps Administrator

 \[sn\_devops.admin\]

</td><td>

Sets up and configures the DevOps application.Only the DevOps Administrator has access to the Administration module.

**Note:** To ensure that the devops.system user has correct access, add the sn\_devops.admin role to the field-level ACL \(sys\_connection.\*\) if a field-level ACL exists on the sys\_connection table or include the connection\_admin role in the sn\_devops.admin role.

</td><td>

-   sn\_devops.app\_owner
-   sn\_devops.integration
-   sn\_devops.tool\_owner
-   action\_designer

 If the DevOps Change Health Scan Content Pack application is installed, the following roles are also added to DevOps Administrator to access the health scan feature.

-   sn\_cicd.sys\_ci\_automation
-   scan\_user

</td></tr><tr><td>

DevOps Integration

 \[sn\_devops.integration\]

</td><td>

Has inbound access to the tools in your environment to allow integration with the DevOps application.

</td><td>

-   flow\_operator
-   cmdb\_read

</td></tr><tr><td>

DevOps App Owner

 \[sn\_devops.app\_owner\]

</td><td>

Oversees the operation of the DevOps application and monitors performance in your DevOps environment.The app owner can:

-   Create, update, and delete applications only.
-   Associate or dissociate objects to applications \(pipelines, repos, plans, artifact repository\)
-   Perform change automation and modify pipeline steps.
-   Access to see all the tools but not modify them.
-   Can click discover from tool records to find new plans, repos, or pipelines from already connected tools.
-   Has the viewer role.

</td><td>

-   sn\_devops.viewer
-   cmdb\_read

</td></tr><tr><td>

DevOps Tool Owner

 \[sn\_devops.tool\_owner\]

</td><td>

The tool owners can:-   Create new tools.
-   Perform the following actions on the tool:
    -   Discover \(classic UI and workspace\)
    -   Enter Manual Configuration Mode \(classic UI and workspace\)
    -   Configure \(classic UI and workspace\)
    -   Configure Guidance \(Jenkins only, workspace\)
    -   Update Credentials \(workspace\)
    -   Check Permissions \(workspace\)
    -   Delete tool \(classic UI and workspace\)
-   View System health and Troubleshooting sections of the Administration module and view Insights dashboards.
-   On the tool record page, the Related Links tabs will show Tool connections and Tool connectivity history.
-   If users have both Tool Owner and App Owner roles, they can also create apps and change request automations.

Tool owners can update credentials only for tools in which they are a member of the access groups, or for tools without access restrictions.

</td><td>

sn\_devops.viewer**Note:**

-   The sn\_vul.app\_sec\_manager role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the DevOps Vulnerability Integrations plugin \(sn\_devops\_vul\_ints\) is installed.
-   The sn\_vul\_veracode.configure\_integration role is added to the DevOps Tool Owner \[sn\_devops.tool\_owner\] role when the Vulnerability Response Integration with Veracode plugin \(sn\_vul\_veracode\) is installed.

</td></tr><tr><td>

DevOps Viewer

 \[sn\_devops.viewer\]

</td><td>

Has access to the DevOps application to use in their environment.

</td><td>

-   sn\_devops\_ws.workspace\_user
-   cmdb\_read
-   sn\_devops.report\_viewer

**Note:** The sn\_devops.report\_viewer role enables users to view reports that are created for DevOps tables. Users cannot view DevOps reports without this role.


</td></tr></tbody>
</table>**Warning:** When you uninstall DevOps Config, there could be empty rows in the **Contains Roles** related list \(table: sys\_user\_role\_contains\) for the roles installed with DevOps Change Velocity. You must delete these empty rows before discovering tool objects.

## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[DevOps\] Historical Data Collection

</td><td>

Collects data from DevOps tools on demand.

 **Note:** You must run this scheduled job to see historical DevOps data after installation of the DevOps Insights application.

</td></tr><tr><td>

\[DevOps\] Daily Data Collection

</td><td>

Collects data from DevOps tools daily.

</td></tr><tr><td>

DevOps auto discover tool associations

</td><td>

Automatically discovers new pipelines, plans, and repositories for all the tools that are in connected state and for all the capabilities. This job is scheduled to run once daily.

 You can deactivate or change the frequency of the schedule:

1.  Navigate to **System Definition** &gt; **Scheduled Jobs** and select **DevOps auto discover tool associations**.
2.  To deactivate the job, deselect the **Active** check box.
3.  To change the frequency, update the **Repeat Interval**.

</td></tr><tr><td>

Tool connectivity history

</td><td>

For all the tools, the scheduled job does the following:

-   Checks the connectivity of the tool and updates the **Connection state** field in the tool record page.
-   Checks the inbound events received in the given interval and updates the **Last webhook activity** field in the tool record page with the latest date and time.

 This job is scheduled to run every hour. You can update the frequency if required.

1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.
2.  Search for and select **Tool connectivity history**.
3.  Update the **Repeat Interval** fields based on your requirement.

**Note:** This job is scheduled at the product level and cannot be scheduled for an individual tool.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Name

</th><th>

Table

</th></tr></thead><tbody><tr><td>

API Schema Definition

</td><td>

\[sn\_devops\_api\_schema\_definition\]

</td></tr><tr><td>

App

</td><td>

\[sn\_devops\_app\]

</td></tr><tr><td>

Artifact

</td><td>

\[sn\_devops\_artifact\]

</td></tr><tr><td>

Artifact Repository

</td><td>

\[sn\_devops\_artifact\_repository\]

</td></tr><tr><td>

Artifact Staged Request

</td><td>

\[sn\_devops\_artifact\_staging\]

</td></tr><tr><td>

Artifact Version

</td><td>

\[sn\_devops\_artifact\_version\]

</td></tr><tr><td>

Base Planning Item

</td><td>

\[sn\_devops\_base\_planning\_item\]

</td></tr><tr><td>

Branch

</td><td>

\[sn\_devops\_branch\]

</td></tr><tr><td>

Build Test Result

</td><td>

\[sn\_devops\_build\_test\_result\]

</td></tr><tr><td>

Build Test Summary

</td><td>

\[sn\_devops\_build\_test\_summary\]

</td></tr><tr><td>

Callback

</td><td>

\[sn\_devops\_callback\]

</td></tr><tr><td>

Commit

</td><td>

\[sn\_devops\_commit\]

</td></tr><tr><td>

Committer

</td><td>

\[sn\_devops\_committer\]

</td></tr><tr><td>

Commit Details

</td><td>

\[sn\_devops\_commit\_details\]

</td></tr><tr><td>

Contributor Score Change Factor

</td><td>

\[sn\_devops\_contributor\_score\_chg\_factor\]

</td></tr><tr><td>

Environment

</td><td>

\[sn\_devops\_environment\]

</td></tr><tr><td>

Event

</td><td>

\[sn\_devops\_event\]

</td></tr><tr><td>

Event Processor

</td><td>

\[sn\_devops\_event\_processor\]

</td></tr><tr><td>

Import Filter

</td><td>

\[sn\_devops\_import\_filter\]

</td></tr><tr><td>

Import Request

</td><td>

\[sn\_devops\_import\_request\]

</td></tr><tr><td>

Import Request Page

</td><td>

\[sn\_devops\_import\_request\_page\]

</td></tr><tr><td>

Inbound Event

</td><td>

\[sn\_devops\_inbound\_event\]

</td></tr><tr><td>

Integration Capability

</td><td>

\[sn\_devops\_integration\_capability\]

 Extends table Application File.

</td></tr><tr><td>

App to Plan

</td><td>

\[sn\_devops\_m2m\_app\_plan\]

</td></tr><tr><td>

Deployed Artifact to TaskExecution

</td><td>

\[sn\_devops\_m2m\_artifact\_execution\]

</td></tr><tr><td>

Artifact Version to Commit

</td><td>

\[sb\_devops\_m2m\_artifact\_version\_commit\]

</td></tr><tr><td>

Artifact Version to Package

</td><td>

\[sn\_devops\_m2m\_artifact\_version\_package\]

</td></tr><tr><td>

Branch To Commit

</td><td>

\[sn\_devops\_m2m\_branch\_commit\]

</td></tr><tr><td>

Run Commit

</td><td>

\[sn\_devops\_m2m\_commit\_execution\]

</td></tr><tr><td>

Work Item To Plan Version

</td><td>

\[sn\_devops\_m2m\_work\_item\_plan\_version\]

</td></tr><tr><td>

Orchestration Task

</td><td>

\[sn\_devops\_orchestration\_task\]

</td></tr><tr><td>

Orchestration Task Definition

</td><td>

\[sn\_devops\_orchestration\_task\_definition\]

</td></tr><tr><td>

Package

</td><td>

\[sn\_devops\_package\]

 Extends table Configuration Item.

</td></tr><tr><td>

Participant

</td><td>

\[sn\_devops\_participant\]

</td></tr><tr><td>

Pipeline

</td><td>

\[sn\_devops\_pipeline\]

</td></tr><tr><td>

Pipeline Execution

</td><td>

\[sn\_devops\_pipeline\_execution\]

</td></tr><tr><td>

Plan

</td><td>

\[sn\_devops\_plan\]

 Extends table Base Planning Item.

</td></tr><tr><td>

Plan Version

</td><td>

\[sn\_devops\_plan\_version\]

 Extends table Base Planning Item.

</td></tr><tr><td>

Repository

</td><td>

\[sn\_devops\_repository\]

</td></tr><tr><td>

Step

</td><td>

\[sn\_devops\_step\]

</td></tr><tr><td>

Step Execution

</td><td>

\[sn\_devops\_step\_execution\]

</td></tr><tr><td>

Tag

</td><td>

\[sn\_devops\_tag\]

</td></tr><tr><td>

Task Execution

</td><td>

\[sn\_devops\_task\_execution\]

</td></tr><tr><td>

Test Execution

</td><td>

\[sn\_devops\_test\_execution\]

</td></tr><tr><td>

Test Result

</td><td>

\[sn\_devops\_test\_result\]

</td></tr><tr><td>

Test Type

</td><td>

\[sn\_devops\_test\_type\]

</td></tr><tr><td>

DevOps Tool

</td><td>

\[sn\_devops\_tool\]

</td></tr><tr><td>

Tool Action

</td><td>

\[sn\_devops\_tool\_action\]

</td></tr><tr><td>

Tool Capability Mapping

</td><td>

\[sn\_devops\_tool\_capability\_mapping\]

</td></tr><tr><td>

DevOps Tool Integration

</td><td>

\[sn\_devops\_tool\_integration\]

 Extends table Application File.

</td></tr><tr><td>

Tool Type Capability

</td><td>

\[sn\_devops\_tool\_type\_capability\]

</td></tr><tr><td>

Work Item

</td><td>

\[sn\_devops\_work\_item\]

 Extends table Base Planning Item.

</td></tr></tbody>
</table>**Parent Topic:**[DevOps Change Velocity reference](devops-change-velocity-reference.md)

