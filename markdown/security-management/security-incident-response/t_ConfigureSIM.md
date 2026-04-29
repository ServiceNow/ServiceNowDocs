---
title: Other additional Security Incident Response setup tasks
description: If you are an administrator in the global domain, you configure how Security Incident Response handles day-to-day operations.To protect investigations and keep security incidents private, you can restrict Security Incident Response access to security-specific roles and ACLs. Non-security administrators can be restricted from access, unless you expressly allow them entry.The Restricted Caller Access \(RCA\) feature enables an administrator to define cross-scope access to an application or application resource and allow or deny access requests. This feature is enabled in Security Incident Response by default so security analysts can protect sensitive security-related information.Validate that Security Incident Response still works after you make any configuration changes, such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Install and configure Security Incident Response, Security Incident Response setup, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Other additional Security Incident Response setup tasks

If you are an administrator in the global domain, you configure how Security Incident Response handles day-to-day operations.

## Before you begin

Role required: sn\_si.admin

**Note:**

These options are standard to many service management applications, and as such, they use service management terminology. For example, Request is used for the main task \(that is, the security incident\) and Task is used for subtasks or Response Tasks.

If you are an administrator in a domain lower than the global domain, you can view the Configurations screen, but cannot modify the settings.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Administration** &gt; **Configuration**.

    The options for configuring the applications are organized under these tabs:

    -   The **Business Process** tab contains options for setting up the request life cycle, creating catalogs and requests, and configuring notifications.
    -   The **Assignment** tab contains options for setting up manual and auto-assignment.
    -   The **Add-ons** tab contains options for enabling the knowledge base, managed documents, and task activities.
2.  Fill in the fields on the **Business process** tab.

<table id="table_kpf_lrk_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

**Lifecycle**

</td></tr><tr><td>

Work notes are required to close or cancel a request or task

</td><td>

Enable this option to require the user to enter work notes before a security incident or response task can be closed or canceled.

</td></tr><tr><td>

Copy task work notes to request

</td><td>

Enable this option to synchronize response task work notes with the work notes on the security incident. So when work notes in the task are added, the same work notes appear in the parent security incident.

</td></tr><tr><td colspan="2">

**Catalog and Request Creation**

</td></tr><tr><td>

Create or update requests by inbound email

</td><td>

Enable this option to create or update security incidents from inbound emails.

</td></tr><tr><td>

Requests are created using

</td><td>

Select **catalog or regular form** to activate the catalog and enable automatic publishing of security incident templates to the catalog.Select **regular form only** to deactivate the catalog and disable automatic publishing of security incident templates to the catalog.

</td></tr><tr><td>

Templates create a dedicated catalog item

</td><td>

Enable this option to activate automatic publishing of catalog items for the application.

</td></tr><tr><td colspan="2">

**Notifications**

</td></tr><tr><td>

For a request or task, when the selected field changes, send notification to recipients

</td><td>

You can configure notifications to be sent to specific recipients when selected fields in security incidents and response tasks change. 1.  From **Table**, select **Request \(security incident** or **Task \(response task\)**.
2.  From **Field**, select the field to use for generating notifications. When a change is made to the selected field, a notification is sent to the identified recipients.
3.  From **Recipients**, select one or more recipients.
4.  If you select **a specific user** or **a specific group**, you are prompted to select a user or group.
5.  To define more notifications using other fields or recipients, repeat the preceding steps for the next set of notification settings.
6.  To remove a notification, click the ![delete notification symbol](../../threat-intelligence/image/DeleteNotification.png) icon to the right of the notification.


</td></tr></tbody>
</table>3.  Click the **Assignment** tab and fill in the fields.

<table id="table_gjj_3vk_ls"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Assignment method for requests

</td><td>

Select the method for assigning security incidents:-   **using auto-assignment**: Security incidents are automatically assigned.
-   **using a workflow**: Security incidents are assigned by the selected workflow.
-   **manually**: Security incidents are manually assigned.


</td></tr><tr><td>

Use this workflow to assign requests

</td><td>

Select the workflow for dispatching security incidents. This field appears when **using a workflow** is selected from the **Assignment method for requests** list.

</td></tr><tr><td>

Assignment method for tasks

</td><td>

Select the method for assigning response tasks:-   **using auto-assignment**: Response tasks are automatically assigned.
-   **using a workflow**: Response tasks are assigned by the selected workflow.
-   **manually**: Response tasks are manually assigned.


</td></tr><tr><td>

Use this workflow to assign tasks

</td><td>

Select the workflow for assigning response tasks. This field appears when **using a workflow** is selected from the **Assignment method for tasks** list.

</td></tr><tr><td>

Assign requests or tasks based on assignment group coverage areas

</td><td>

Enable this option to limit the assignment of security incidents and response tasks to groups that cover the location of the task.

</td></tr><tr><td colspan="2">

**Scheduling**

</td></tr><tr><td>

Auto-selection of agents consider time zone for tasks

</td><td>

Enable this option to consider the time zone of the agent when assigning a task. This field appears when auto-assignment is selected for security incidents or response tasks.

</td></tr><tr><td colspan="2">

**Additional Factors**

</td></tr><tr><td>

Auto-selection of agents consider location of agents

</td><td>

Enable this option to give preference to agents who are closer to the task location, when assigning any tasks. This field appears when auto-assignment is selected for security incidents or response tasks.

</td></tr><tr><td>

Auto-selection of agents for tasks requires them to have skills

</td><td>

Select the degree to which agent skills must be matched to a task when determining auto-assignment. -   Select **all** to require that an assigned agent must have all the skills to perform the task. An agent who lacks even one skill is eliminated.
-   Select **some** if you want agents who have most of the skills required to perform the task.
-   Select **none** if you want to auto-assign agents without taking skills into account. This field appears when auto-assignment is selected for security incidents or response tasks.


</td></tr><tr><td>

Auto-selection attempt to assign the same agent to all tasks in a request

</td><td>

Enable this option to auto-assign all response tasks for a security incident to the same agent.

</td></tr></tbody>
</table>4.  Click the **Add-ons** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Documentation**|
    |Enable a dedicated knowledge base|Enable this option to activate the knowledge base for Security Incident Response.|
    |Enable managed documents|Enable this option to add a related list to managed documents.|
    |Enable task activities|Enable this option to log task interactions and communications, such as phone calls and email messages.|

5.  Click **Save**.


## Lock down security administration

To protect investigations and keep security incidents private, you can restrict Security Incident Response access to security-specific roles and ACLs. Non-security administrators can be restricted from access, unless you expressly allow them entry.

### Before you begin

When the Security Incident Response application is activated, the System Administrator user is granted the sn\_si.admin role by default. The System Administrator is the only administrator who can set up security groups and users.

A security role is required to have access to Security Incident Response features and records.

Role required: sn\_si.admin

### Procedure

1.  After the Security Incident Response plugin has been activated, a user with the admin role assigns the Scoped Admin \(sn\_si.admin\) role to at least one user.

2.  The user with the admin role changes to the Security Incident scope.

3.  Navigate to **All** &gt; **sys\_store\_app.list**.

4.  Type **sn\_si** in the **Scope** field.

    ![System applications.](../image/system-applications.png)

5.  Click **Security Incident Response**.

6.  Scroll down to the **Related Links** and click **Remove from the role contained by admin**.

7.  Log out and log back in.

    The admin user cannot access the Security Incident Response application.


**Related topics**  


[Application administration](https://www.servicenow.com/docs/access?context=application-administration&version=australia&pubname=australia-application-development&ft:locale=en-US)

## Manage Restricted Caller Access

The Restricted Caller Access \(RCA\) feature enables an administrator to define cross-scope access to an application or application resource and allow or deny access requests. This feature is enabled in Security Incident Response by default so security analysts can protect sensitive security-related information.

A field called **Caller access** has been added to all tables and script includes in Security Incident Response, and the field defaults to **Caller Tracking**. This setting means that application scopes are allowed access to Security Incident Response tables and script includes. However, a tracking record is created for each record and stored in the Restricted Caller Access Privilege \[sys\_restricted\_caller\_access\] table.

**Note:** Take care when changing records from **Caller Tracking** to **Caller Restricted**. Records with this status cannot be accessed until an administrator manually allows access to it. The administrator must navigate to **System Applications** &gt; **Application Restricted Caller Access**, locate the table or script include for which access has been requested, and change the **Status** field from **Requested** to **Allowed**.

**Related topics**  


[Restricted caller access privilege settings](https://www.servicenow.com/docs/access?context=restricted-caller-access-privilege&version=australia&pubname=australia-application-development&ft:locale=en-US)

[Set the application scope, application resource, and event access](https://www.servicenow.com/docs/access?context=scope-resource-access&version=australia&pubname=australia-application-development&ft:locale=en-US)

## Run quick start tests for Security Incident Response

Validate that Security Incident Response still works after you make any configuration changes, such as applying an upgrade or developing an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Security Incident Response quick start tests require activating Security Incident Response plugin \(com.snc.security\_incident\) and loading the demo data.

<table id="table_fkf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

SIR: Create Security Incident

</td><td>

Determine whether a user can successfully create a security incident from the security incident form.

</td><td>

Madrid

</td></tr><tr><td>

SIR: Create Security Incident via Security Incident Catalog

</td><td>

Determine whether a user can successfully create a security incident from the catalog.

</td><td>

Madrid

</td></tr><tr><td>

SIR: PIR Assessments OOTB configuration test

</td><td>

Use this test to validate PIR assessments and base system configurations.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: PIR Assessments conditional Configuration tests

</td><td>

Verify that security incidents matching the mandatory conditional rule are not closed without completing the post incident assessment.

 Verify that the security incidents matching the optional conditional rule can be closed without completing the post incident assessment.

 Verify that assessments are not generated for the security incidents that do not match any rule.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: PIR Run Time Experience

</td><td>

Verify that PIR reports are configured and attached to the security incidents as per the new design.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: PIR Design Time Experience

</td><td>

Verify that the security incident is mapped with the report template based on the administrator configuration.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: Link Security Incident to a existing Major Security Incident

</td><td>

Link a Security Incident to an existing Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: Promote Security Incident as Major Security Incident

</td><td>

Promote a Security Incident as Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: Propose Security Incident as Major Security Incident

</td><td>

Propose a Security Incident as Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Tokyo

</td></tr><tr><td>

SIR: Security Incident life cycle

</td><td>

Validate a Security Incident life cycle with the policy violation response tasks workflow.

</td><td>

Yokohama

</td></tr><tr><td>

SIR: Create Security Case

</td><td>

Create a Security Case from the Security Incident form.

</td><td>

Yokohama

</td></tr><tr><td>

Verify that only Allowed Members can access the security incident once Enforce Restriction is ON

</td><td>

Verify that only the allowed members can access the security incident once the Enforce Restriction is enabled.

</td><td>

Yokohama

</td></tr><tr><td>

Verify that security incident enabled with "Enforce Restriction" is not visible for any user

</td><td>

Verify that security incident enabled with "Enforce Restriction" is not visible for any user.

</td><td>

Yokohama

</td></tr><tr><td>

Validate Read Access

</td><td>

Validate the view access.

</td><td>

Yokohama

</td></tr><tr><td>

Validate Write Access

</td><td>

Validate the edit access.

</td><td>

Yokohama

</td></tr><tr><td>

SIR Workspace: Read Access

</td><td>

Verify that Read Access user can view the security incident without having security roles even on workspace.

</td><td>

Yokohama

</td></tr><tr><td>

SIR Workspace: Write Access

</td><td>

Verify that Write Access user can update the security incident without having security roles.

</td><td>

Yokohama

</td></tr><tr><td>

SIR Workspace: Create new Security Incident

</td><td>

Create new security incident from workspace.

</td><td>

Yokohama

</td></tr><tr><td>

SIR Workspace: Create Response Task

</td><td>

Create new response task from an existing security incident.

</td><td>

Yokohama

</td></tr><tr><td>

Now Assist for Security: Active Security Incident Summarization

</td><td>

Summarize an active security incident and validate the displayed sections.

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for Security: Security Incident Summarization\_Share to worknotes

</td><td>

Share the generated summary to worknotes.

</td><td>

Zurich

</td></tr><tr><td>

Now Assist for Security: Closed Security Incident Summarization

</td><td>

Summarize a closed security incident and validate the displayed sections.

</td><td>

Zurich

</td></tr></tbody>
</table>**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)

