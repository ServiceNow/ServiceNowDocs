---
title: Create an Employee Relations case in Core UI
description: You create ER cases for employees that wish to report misconduct, discrimination or a disciplinary issue.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Using HR Service Delivery Employee Relations, Employee Relations, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create an Employee Relations case in Core UI

You create ER cases for employees that wish to report misconduct, discrimination or a disciplinary issue.

## Before you begin

Role required: sn\_hr\_er.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Create New Case**.

2.  From **Search for Employee or case number**, enter an employee name or click **Skip verification**.

    ![HR Employee Relations - Skip verification](../image/hr-er-case-creation-skip.png)

    **Note:** Skipping verification enables you to create an ER case without identifying an Opened for person and takes you directly to case details.

<table id="table_j3t_5tx_llb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

The **Center of Excellence** associated with the HR case you are creating. Currently, Employee Relations Case is the only COE available for ER cases.

 Selecting a COE filters the choices for HR service. See [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).

 **Note:** You can also select an HR service first and the associated COE automatically populates.

</td></tr><tr><td>

HR service

</td><td>

The HR service depends on the COE selected or what you select based on communication with the employee request. Select:

-   Accommodation Request
-   Report Discrimination
-   Report Misconduct
-   Performance improvement plan\(PIP\)
 HR services available to an employee filter by:

-   COE selected.
-   HR criteria for the **Subject person** based on the HR service configuration.

Limit services filter on the **Case Creation Configuration** form. If the HR service field is empty, ensure that you did not remove the Opened for field.

 **Note:** **Bulk Parent Case** does not appear as a selection because it only appears when creating a parent case for child bulk cases. Refer to [Add or modify bulk HR cases](t_CreateBulkCases.md).

</td></tr><tr><td>

Opened for

</td><td>

The person the HR service request is for. **Note:** This field does not appear if you selected the **Skip verification** link.

 Click the **Lookup using list** icon to find a user.

 Use the choice list to search and select another employee.

 Click the **Reference field** icon to view or edit **HR profile** information.

**Note:** Selecting the **Do Not Default Subject Person** HR Service Option for an HR service, prevents the **Subject Person** from automatically filling in when creating an HR case. For more information, see [Configure an HR service](configure-hr-service.md).

</td></tr><tr><td>

Work notes

</td><td>

Information specific to the case that can help other HR agents. **Work Notes** are not visible to the **Opened for** subject.The sn\_hr\_core.restrict\_guest\_email system property allows a user to send an email from a personal email account referencing an HR case. When the property has a value of false \(default\), the text from the email appears in the Work notes field. To access system properties, enter `sys_properties.list` in the navigation filter.

 **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see Dynamic translation.

</td></tr></tbody>
</table>3.  Click **Create Case** and the **Employee Relations Case** form appears with additional information about the case.

    The **COE** and **HR service** selected for the HR case determines the fields that appear.

<table id="table_jyd_rgy_llb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An HR case number is assigned and is a unique identifier, cannot be changed, and has an HRC prefix.

</td></tr><tr><td>

External opened for

</td><td>

The ER case was reported by somebody outside of your company.Checking this box removes the following fields:

-   Opened for
-   Preferred contact method


</td></tr><tr><td>

Opened for

</td><td>

The person who is responsible for the HR service request. **Note:** Select **Skip verification** to create a case without verifying the employee or case number.

 -   The person requesting the HR service. When you make an HR service request for yourself, the **Subject person** and **Opened for** person are the same.
-   The person requesting the HR service on behalf of an employee. For example, a manager requesting an HR service for a direct report. In this example, the manager \(**Opened for**\) made an HR request on behalf of an employee \(**Subject person**\).
 Use the choice list to search and select another employee.

 Click the **Reference field** icon to view or edit **HR profile** information.

</td></tr><tr><td>

Preferred contact method

</td><td>

The communication method the **Opened for** person \(if applicable\) prefers to be contacted. Select:-   Not Specified
-   Personal Phone
-   Work Phone
-   Personal Email
-   Work Email


</td></tr><tr><td>

HR service

</td><td>

The HR service selected in the Case creation form.

</td></tr><tr><td>

Incident date

</td><td>

The date of the incident. If there are multiple incidents, select the date of the most recent incident.

</td></tr><tr><td>

Skills

</td><td>

The required skills of the person assigned to this category of HR case. Skills can auto-populate based on the HR case template associated with the HR service.

</td></tr><tr><td>

State

</td><td>

Status of the case. The state can auto-populate based on the HR case or task template associated with the HR service.-   Draft: The default state for a case when it is first opened.

**Note:** Can only be changed to Ready, Closed Complete, Closed Incomplete, Cancelled, or Suspended.

-   Ready: The case is ready to be worked on.
-   Closed Complete
-   Closed Incomplete
-   Cancelled
-   Suspended: Use to temporarily prevent violation of a service level agreement \(SLA\). Refer to [Suspend and resume an HR case](t_SuspendAndResumeAnHRCase.md).


</td></tr><tr><td>

Priority

</td><td>

The priority that the incident needs resolution. Use impact and urgency to determine the priority.

</td></tr><tr><td>

Source

</td><td>

The reporting method the incident

</td></tr><tr><td>

Opened

</td><td>

The date and time the ER case was created.

</td></tr><tr><td>

Opened by

</td><td>

The person who created the ER case.

</td></tr><tr><td>

Assignment group

</td><td>

The group the ER case is assigned to. If the group is not set automatically, assign an HR group to provide a selection of HR users in the **Assigned to** field. For automatic assignment, refer to [Employee Relations assignment rules](../concept/hr-er-assign-rules.md).

</td></tr><tr><td>

Assigned to

</td><td>

The user assigned to work on this case. When a group is automatically assigned, a user from the group is automatically assigned when the case is created. If the user is not auto-assigned, click the **Lookup using list** icon to select a user who is a member of the selected assignment group.To change the **Assigned to** HR agent, the agent must be a member of the Assignment group.

</td></tr><tr><td>

Collaborators

</td><td>

Agents or interested parties you want to associate with the case. Collaborators can track and stay up-to-date on the progress of the ER case.If an ER case transfers from the assigned to agent to another agent, the original assigned to agent can add themselves as a collaborator and still monitor the case.

 By having visibility to the case, collaborators can also help the assigned to agent with the case.

 Other factors:

-   Collaborators can remove themselves from the case.
-   The Assigned to agent can add or remove collaborators.
-   Collaborators cannot add or remove collaborators.
-   Notifications are sent to the collaborators when added to the ER case.
 Collaborators and the COE for the HR case can conflict. The basic rules are:

-   For all HR cases, collaborators override any security on a COE. For more information, see [Create COE security](../concept/configure-hr-coe-security.md).
-   Employee Relations \(ER\) cases can override collaborators when restrictions apply. For more information, see [Configure an employee relations case restriction](hr-er-create-case-restriction.md).
**Note:** Agents must have the ER case writer \[sn\_hr\_er.case\_writer\] role in order to be a collaborator.

</td></tr><tr><td>

Watch list

</td><td>

Interested parties that can view all updates and receive notifications for the ER case.

</td></tr><tr><td>

Short description

</td><td>

Populates from the HR service. After the case is created, you can modify the description.

</td></tr><tr><td>

Description

</td><td>

A longer, detailed description after the ER case is created. Use the Rich Text Format \(RTF\) tools to format your text.Rich text formatting also appears for a case or task description on the Employee Center or service portal.

</td></tr></tbody>
</table>    The following buttons appear:

    -   **Discuss**

        Option to begin a sidebar discussion on the case by adding the required participants.

    -   **Follow**

        Option to get notified of any comments or work notes on the case, according to your notification settings.

    -   **Update**

        Option to update the case.

    -   **Ready for work**

        Option to change the status of case to Ready for work.

    -   **Cancel**

        Option to cancel the case.

    -   **Delete**

        Option to delete the case.

    The following embedded lists appear:

    -   **Fulfillment Instructions**

        Information on how to complete the case. This information is defined in the HR Service configuration.

        A checklist outlining the exact steps to complete appears when configured by the HR service. See [Configure an HR service](configure-hr-service.md).

    -   **Comments and Work Notes**

        Comments or work notes that provide details about the case. **Work notes** are not visible to the **Subject person**.

        **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see Dynamic translation.

    -   **Related Links**

        The following appear dependent on the type of case and roles associated with the user:

        -   Add Task: Task you want to add to the case. Refer to [Add an HR task to an HR case](t_ViewAnHRTask.md).
        -   Show SLA Timeline: The SLA in timeline format that shows elapsed time.
        -   Repair SLAs: Click to repair any service level agreements associated with the case.
    -   **Involved Parties**

        People associated with the ER case. Involved parties can be the complainant, subject of the allegation, a witness, or other \(undefined\). For more information, see [Create an involved parties record](hr-er-involved-parties.md).

    -   **Allegations**

        Information that further defines an employee relations case. For more information, see [Create an allegation record](hr-er-create-allegation.md).

    -   **Interviews**

        Interview record for an involved party. For more information, see [Schedule an interview in Employee Relations using the legacy UI](hr-er-interview.md).

    -   **Evidence**

        Evidence to support the ER case. For more information, see [Evidence Management for Employee Relations](../concept/hr-er-evidence-mgmt.md#).

    -   **Corrective Actions**

        Information about the resolution and any associated corrective actions after an investigation related to the ER case. For more information, see [Create a corrective action](hr-er-corrective-actions.md).

    -   **Attached Knowledge**

        List of knowledge articles attached to the HR service type. For more information, see [HR Knowledge Management](../concept/hr-knowledge-management.md).

    -   **Approvers**

        Lists employees that can approve changed information or the case, state of approval, comments, and associated dates. For more information, see [Resubmit an HR case for approval](t_ApproveAnHRCase.md).

        **Note:** To reject an approval, users should have the HR case writer \[sn\_hr\_core\_case.writer\] role.

    -   **Child Cases**

        Lists child cases for the current case.

    -   **ER Cases for Involved Parties**

        Lists other ER cases for the involved parties of the ER case.


