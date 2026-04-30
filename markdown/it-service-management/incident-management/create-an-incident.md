---
title: Create an incident
description: Create an incident record to document a deviation from an expected standard of operation.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Create an incident

Create an incident record to document a deviation from an expected standard of operation.

## Before you begin

Role required: itil, sn\_incident\_write, or admin

## About this task

This procedure describes how an ITIL agent completes the Incident form. Incidents are also logged when a user fills out a record producer in the service catalog, or sends an email to the instance.

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Create New**.

    You can also click **New** from the Incident list view.

2.  [Use a template](t_UseATemplateFromAForm.md), if one exists for the type of incident that you are logging.

    If the organization uses form templates, then you can apply a template to pre-populate some of the fields for specific types of incidents.

3.  On the form, fill in the fields.

    Your organization has configured the Incident form to adhere to its incident management process. Enter information in the form field is based on the process. The following table describes typical Incident form fields.

<table id="table_wjm_hsv_vy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique system-generated incident number.

</td></tr><tr><td>

Caller

</td><td>

User who contacted you with an issue.

</td></tr><tr><td>

Category and Subcategory

</td><td>

Type of issue. After selecting the category, select the subcategory, if applicable.

</td></tr><tr><td>

Service

</td><td>

Affected business service, if applicable. **Note:**

If you select a business service as the configuration item and if that business service is also listed as the configuration item in any other active task, then the active tasks icon \(![Other active tasks](../../change-management/image/other-active-task.png)\) appears. Click the icon to view the list of all the other active tasks that are affecting the business service.

You can view the BSM map \(dependency view\) of the selected business service by clicking the dependency icon \(![Open dependency view](../image/dependency-icon-r.png)\).

</td></tr><tr><td>

Service Offering

</td><td>

Service offering consists of one or more service commitments that uniquely define the level of service in terms of availability, scope, pricing, and packaging options. This field enables you to receive different features and their levels of performance for a given service.

</td></tr><tr><td>

Configuration item

</td><td>

Affected CI, if applicable.After a CI is selected, you can click the open dependency views icon \(![Open dependency view](../image/dependency-icon-r.png)\) next to the field to see how the CI maps into the infrastructure. The dependency view shows you what is impacted and whether other CIs or services are experiencing issues. To capture information on the affected CIs, refer to [Capture information on affected configuration items in an incident](track-ci.md).

</td></tr><tr><td>

Channel

</td><td>

Communication method that is used by the user to create the incident. Following are the available options:-   Chat
-   Email
-   Phone
-   Monitoring
-   Self-service
-   Virtual agent
-   Walk-in


</td></tr><tr><td>

Origin

</td><td>

Source of the incident. For example, if an incident is created from alert, this field contains the value Alert. This is a auto-populated field and you cannot fill the value manually.

</td></tr><tr><td>

State

</td><td>

State of the incident. The state moves and tracks incidents through several stages of resolution.**Tip:** Use the **State** field, rather than the **Incident State** or **Problem State** fields, as your primary means of tracking the state of an incident because this state progresses through the entire processing cycle. To learn more, see [Life cycle of an Incident](../concept/c_IncidentManagementStateModel.md).

</td></tr><tr><td>

Impact

</td><td>

Impact is a measure of the effect of an incident, problem, or change on business processes.

</td></tr><tr><td>

Urgency

</td><td>

Urgency is a measure of how long the resolution can be delayed until an incident, problem, or change has a significant business impact.

</td></tr><tr><td>

Priority

</td><td>

Priority is based on impact and urgency, and it identifies how quickly the service desk should address the task.

</td></tr><tr><td>

Assignment group

</td><td>

Group who will work on the incident. The business rule **Populate Assignment Group based on CI/SO** populates the **Assignment group** field based on the support group available for the configuration item \(CI\) or the Service offering consecutively.

**Note:** The business rule is triggered when an incident is created or updated, and when the **Assignment group** and the **Assigned to** fields are empty.

 If you want to override the default value, then you need to create new properties and provide the field in the property value that must be used to populate the **Assignment group** field. Create the properties in the following order of preference:

-   **com.snc.incident.ci\_assignment\_group.field\_name**: Identifies which CI field populates the **Assignment group** field.
-   **com.snc.incident.service\_offering\_assignment\_group.field\_name**: Identifies which service offering field populates the **Assignment group** field.
 **Note:**

-   The sys\_user\_group **read** ACL calls the SNCRoleUtil function. The function verifies whether the group that is reviewed contains either the admin role or security\_admin role. The function enables the user to view the group only if the user has the same role. As a result, a user with the itil role cannot assign an incident to a group that has the admin role or security\_admin role, nor to any group whose parent has those roles.
-   Other than using the read ACLs, you can also restrict incidents with specific assignment group\(s\) for visibility only to the group members using before-query business rule. For details, see [How to restrict a specific group incidents to only its group members \[KB0790987\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0790987) article in the Now Support Knowledge Base. You must log in to view the article.


</td></tr><tr><td>

Assigned to

</td><td>

User who works on this incident. If the **Assignment group** changes, the **Assigned to** field is cleared.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the incident.

</td></tr><tr><td>

Description

</td><td>

Detailed explanation on the incident.

</td></tr><tr><td>

Attachments

</td><td>

Attachments related to the incident that helps in incident resolution such as screenshots or pdfs. Select the Attachment \(![Attachment icon](../../vendor-manager-workspace/image/attachments-icon.png)\) to add and manage the attachments.

</td></tr><tr><td class="sub-head" colspan="2">

Notes

</td></tr><tr><td>

Watch list

</td><td>

Users who receive notifications about this incident when comments are added. Click the add me icon \(![Add me icon](../image/add-me.png)\) to add yourself to the watch list.

</td></tr><tr><td>

Work notes list

</td><td>

Users who receive notifications about this incident when work notes are added. Click the add me icon \(![Add me icon](../image/add-me.png)\) to add yourself to the work notes list.**Note:** The administrator must create an email notification for the work notes list.

</td></tr><tr><td>

Additional comments

</td><td>

More information about the issue as needed. All users who can view incidents see additional comments.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve the incident, or steps taken to resolve it, if applicable.

</td></tr><tr><td>

Actions taken

</td><td>

A journal field where you can enter details of the actions taken for a major incident. This field is for only internal users. **Note:** This field is only visible when you activate the Major Incident Management plugin \(com.snc.incident.mim\).

</td></tr><tr><td class="sub-head" colspan="2">

Related Records

</td></tr><tr><td>

Parent Incident

</td><td>

Unique number of the parent incident for this incident record.

</td></tr><tr><td>

Problem

</td><td>

Unique number of any related problem record that is related to the incident.

</td></tr><tr><td>

Change Request

</td><td>

Unique number of any related change request that is related to the incident.

</td></tr><tr><td>

Caused by Change

</td><td>

Unique number of the change request that resulted in the creation of the incident.

</td></tr></tbody>
</table>    **Note:** The **Caller** and **Company** fields are optional for the following situations:

    -   An incident is created from an alert.
    -   An incident is created from a change request. In such case, the change request number is populated in the **Caused by Change** field.
4.  Click **Submit**.


## Result

The incident is created.

## What to do next

-   If you want to mail the incident record, click the more options icon \(![More options icon](../../change-management/image/more-options.png)\) in the title bar and select **Email**.

    The user who requested the incident and the user who is assigned to the incident are automatically populated in the list of recipients.

-   When an incident is created from a case, the Customer Service with Service Management plugin \(com.sn\_cs\_sm\) is installed and you have a customer service agent \(sn\_customerservice\_agent\) role, you can view the **Customer Cases** tab in the Related Links section of the Incident form. This tab contains the list of the customer cases associated with the incident record.
-   When there are one or more interaction records associated with the incident record, you can view the **Interaction** tab in the Related Links section of the Incident form that contains the list of the interaction records.
-   A **Primary device health** link appears on the Related Links section of the Incident form. Select to launch the Digital End-User Experience application and device health page for the selected CI in Service Operations Workspace on a separate browser tab. This tab enables agents to view all the available metrics and the device health for the selected CI, which were collected by DEX. You can also access this feature using the **View device health** option on the classic U16 CI record.

    **Note:**

    -   DEX requires a separate entitlement.
    -   This link is available to the agent only if the following conditions are met:
        -   The selected CI is of type Device, which is also known as Endpoint.
        -   The DEX plugin is installed on the instance. For more information on DEX, see [Digital End-User Experience](../../digital-end-user-experience/concept/dex-landing.md).
        -   The DEX agent is installed on the selected CI.

**Parent Topic:**[Managing incidents](../concept/work-on-incidents.md)

**Related topics**  


[Create a record from incident](t_PromoteAnIncident.md)

[Managing major incidents](../concept/major-incident-management.md)

