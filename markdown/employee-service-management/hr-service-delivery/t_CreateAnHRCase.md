---
title: Work an HR case
description: After initial creation of an HR case, the next steps are to change the state, provide additional information, and ensure that any outstanding tasks are completed.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Work an HR case

After initial creation of an HR case, the next steps are to change the state, provide additional information, and ensure that any outstanding tasks are completed.

## Before you begin

Role required: sn\_hr\_core.case\_writer

HR case creation and completion require different information depending on the Center of Excellence \(COE\) and HR service selected. The HR service an employee is requesting determines the type of HR case.

## Procedure

1.  After employee verification, click **Create Case**.

    The following fields appear:

<table id="table_udl_fb4_sbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An HR case number is assigned and is a unique identifier, cannot be changed, and has an HRC prefix.

</td></tr><tr><td>

Parent

</td><td>

Populates the parent case when the displayed case is a child.For example, a **Request onboarding** case has multiple child cases and tasks under it.

</td></tr><tr><td>

Skills

</td><td>

The required skills of the person assigned to this category of HR case. Skills can auto-populate based on the HR case template associated with the HR service.

</td></tr><tr><td>

Company

</td><td>

Company account to which the remote case is associated.

</td></tr><tr><td>

Remote case

</td><td>

Option indicating that the HR case is created due to a provider task from a consumer instance.**Note:** This option appears only when the HR Multi Instance Integration for Provider \(sn\_hr\_mii\_provider\) plugin is installed.

</td></tr><tr><td>

State

</td><td>

The state of the case. The state can auto-populate based on the HR case or task template associated with the HR service.-   Draft: The default state for a case when it is first opened.

**Note:** Can only be changed to Ready, Closed Complete, Closed Incomplete, Cancelled, or Suspended.

-   Ready: The case is ready to be worked on.
-   Awaiting Approval: Requires approval before it can move to the next state.

**Note:** Can only be changed to Ready, Closed Complete, Closed Incomplete, Cancelled, or Suspended.

-   Work in Progress: The case is assigned and being worked on.
-   Closed Complete
-   Closed Incomplete
-   Cancelled
-   Awaiting Acceptance: The **Opened for** person must accept the HR case before it can proceed. For example, a **Request for Onboarding** case was opened for a hiring manager. The hiring manager must accept the case before it can move to the next state.
-   Suspended: Use to temporarily prevent violation of a service level agreement \(SLA\). Refer to [Suspend and resume an HR case](t_SuspendAndResumeAnHRCase.md).

**Note:** The **State** cannot be edited in List view.

</td></tr><tr><td>

Priority

</td><td>

The precedence of the case, based on the **HR service**. The priority automatically overrides the template and changes to **2 - High** for users flagged as VIP. Configured in HR Properties \(sys\_property\).

</td></tr><tr><td>

Source

</td><td>

From where the case originated. Sources are:-   Not selected
-   Self Service
-   Phone
-   Chat / Connect / Live Feed
-   In Person
-   Email
-   Other
-   Virtual Agent

**Note:** Cases created through email or self-service are automatically moved to **Ready** state and assigned to a group or user.

</td></tr><tr><td>

Opened by

</td><td>

The user who created the case.

</td></tr><tr><td>

Assignment group

</td><td>

The group the record is assigned to. If the group is not set automatically, assign an HR group to provide a selection of HR users in the **Assigned to** field. Assignment groups are restricted to those groups with a type of human\_resources.To change the **Assignment group**, the **Assigned to** agent must be a member of the new group and the **State** must be **Ready**.

 **Note:** To automatically assign a group to an HR case, see [Assignment and matching rules in HR](../concept/c_UseAssignmentRules-1.md) and [Configure an HR case template](configure-hr-case-template.md).

</td></tr><tr><td>

Assigned to

</td><td>

The user assigned to work on this case. When a group is automatically assigned, a user from the group is automatically assigned when the case is created. If the user is not auto-assigned, click the **Lookup using list** icon to select a user who is a member of the selected assignment group.To change the **Assigned to** HR agent, the agent must be a member of the **Assignment group** and the **State** must be **Ready**.

 If **Assigned to** is left blank, some features are not available from the Employee Center ticket page. For example, the **Ask a Question** link to chat directly about an HR case cannot assign an agent. Comments or work notes do not appear on a case until an agent is assigned.

</td></tr><tr><td>

Collaborators

</td><td>

Add collaborators or other HR agents to the case.Only HR agents can be added as collaborators. This action permits the original agent to still track the case. Or, an HR agent can add another HR agent as a collaborator to request help. Adding a collaborator populates the case on the collaborations list.

 Other factors related to adding collaborators:

 -   Collaborators can remove themselves from the case. To remove yourself, highlight your name in the **Collaborators** list and click the **X**.
-   Collaborators are not required to be part of the assignment group.
-   Assigned to person can add or remove collaborators.
-   Collaborators cannot add or remove collaborators.
-   Notifications are sent to collaborators when added to the HR case.
 Adding collaborators can alleviate the amount of emails requesting help on an HR case by consolidating communication.

 Collaborators and the COE for the HR case can conflict. The basic rules are:

-   For all HR cases, collaborators override any security on a COE. For more information, see [Create COE security](../concept/hr-service-categorization.md#).
-   Employee Relations \(ER\) cases can override collaborators when restrictions apply. For more information, see [Configure an employee relations case restriction](hr-er-create-case-restriction.md).
 **Note:** Agents must have the ER case writer \[sn\_hr\_er.case\_writer\] role in order to be a collaborator.

</td></tr><tr><td>

Case support team

</td><td>

Employees assigned to answer questions about onboarding a new hire. Only appears for Lifecycle Events cases.You can add users or define a group that can support the **Subject person** for a Lifecycle Event case. The **Subject person** can communicate with the case support team while the case progresses.

</td></tr><tr><td>

Watch list

</td><td>

The list of users who receive notifications regarding this case. Anyone in the company can be added to the **Watch list**. For example, an employee requests a travel visa. Add the manager of the employee to ensure that updates are communicated.

Click the **Edit Watch List** icon to add users. Click the **Add me** icon to include yourself.

</td></tr><tr><td>

Min ETTR

</td><td>

Indicates the minimum estimated resolution time in days for case completion. Estimate is based on the historical data taken for resolving similar HR cases.**Note:** Available after activating Predictive Intelligence ETTR capability

</td></tr><tr><td>

Max ETTR

</td><td>

Indicates the maximum estimated resolution time in days for case completion. Estimate is based on the historical data time taken for resolving similar HR cases. **Note:** Available after activating Predictive Intelligence ETTR capability

</td></tr><tr><td>

Short description

</td><td>

Populates from the HR service. After the case is created, you can modify the description.

</td></tr><tr><td>

Description

</td><td>

You can add a longer, detailed description after the HR case is created. Use the Rich Text Format \(RTF\) tools to format your text.Rich text formatting also appears for a case or task description on the Employee Center.

</td></tr></tbody>
</table>    The following embedded lists appear:

    -   **Special Handling Notes List**

        Shows notes of messages specific to an HR case or conditions. For more information, see [Add special handling notes for an HR Service Delivery case](hr-add-special-handling-notes.md).

    -   **Knowledge results**

        Shows knowledge results based on the short description of the HR case. There are two tabs. One showing articles that you have access to, and one showing articles that the **Opened for** employee can access. Click **Attach** to make the article visible to the person that the HR case was opened for in the **Additional comments** section. See [Attach knowledge articles to an HR case](t_AttachKnowledgeArticleToHRCase.md) for more information.

    -   **Tasks**

        Appears when there are tasks associated with the case. Click a task to view or update it.

        **Note:** When you close the parent case, all child tasks are assigned the Closed Incomplete state.

    -   **Fulfillment Instructions**

        View information on how to complete the case. This information is defined in the HR Service configuration.

        A checklist outlining the exact steps to complete appears when configured by the HR service. See [Configure an HR service](configure-hr-service.md).

    -   **Comments and Work Notes**

        You can add comments or work notes to the case to provide details about the case. **Work notes** are not visible to the **Subject person**.

        **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

        If your company uses templated snippets and depending on the conditions defined, the **Responses** button appears in the form header:

        1.  Click the **Responses** button.
        2.  Select a response template.
        3.  Click **Copy to clipboard**.

            **Note:** This button copies all text in the message field. To copy partial text, highlight the text, and use the copy command. You can also edit the text after pasting it.

        4.  You can paste the text into the **Work Notes**, **Comments**, or any text field.
    -   **Parental Leave Details**

        Appears for Parental Leave of Absence Request cases. Provides details about the leave request.

<table id="table_g1l_mhb_qhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Leave subtype

</td><td>

Identifies the role of the Subject person for parental leave of absence or the type of parental leave. Select:-   Birthing parent
-   Partner of birthing parent
-   Adoption
-   Surrogacy
-   Foster placement


</td></tr><tr><td>

Leave status

</td><td>

Indicates the status of the parental leave. Select:-   Requested
-   Approved
-   On Leave
-   Rejected
-   Completed
-   Cancelled


</td></tr><tr><td>

Child arrival date

</td><td>

The date the child is expected to arrive.**Note:** Use this field for Adoption or Foster placement.

</td></tr><tr><td>

First day of leave

</td><td>

The date the employee is requesting to start parental leave.

</td></tr><tr><td>

Estimated last day of leave

</td><td>

The estimated date the employee is expected to end parental leave.

</td></tr><tr><td>

Due date

</td><td>

The birth date of the child.**Note:** Use this field when Birthing parent, Partner of birthing parent, or Surrogacy is selected from **Leave subtype**.

</td></tr></tbody>
</table>    The following sections appear dependent on the type of task or case:

    -   **Reimbursement**

        Appears when a **Tuition Reimbursement Request** case is selected. Complete the fields related to the school or program name, justification, refund amount, and course dates.

    -   **Activities**

        Shows a list of all changes or updates to the HR case with the most current at the top.

    -   **Related Links**

        The following appear dependent on the type of case and roles associated with the user:

        -   Add Task: Click to add a task to the case. Refer to [add a task](t_ViewAnHRTask.md).
        -   Show SLA Timeline: The SLA in timeline format that shows elapsed time.
        -   Show Workflow: The workflow that is associated with the case.
        -   Escalate Case: Click to escalate the case and provide a reason.
        -   Activity Set Execution: Populates for Lifecycle event cases. Click to view the Activity Set Contexts and each activity set.
        -   Repair SLAs: Click to repair any service level agreements associated with the case.
        -   Assign to Me: Appears when **Assignment group** is empty or if you belong to the Assignment group. Click to assign the HR case to you. A button also appears in the header form.
    The related lists appear dependent on type of case or task:

    -   **Emergency Contacts**

        List of emergency contacts for the **Subject person**

    -   **Cases for Subject Person**

        List of cases associated with the **Subject person**.

    -   **Cases Opened for User**

        List of cases associated with the **Opened for** person.

    -   **Attached Knowledge**

        List of knowledge articles attached to the HR service type.

    -   **Approvers**

        Lists employees that can approve changed information or the case, state of approval, comments, and associated dates.

        **Note:** To reject an approval, users should have the HR case writer \[sn\_hr\_core\_case.writer\] role.

    -   **Requested Item**

        List items like laptops, software, or furniture requested for the Subject person.

    -   **Requested Items**

        List of items requested for the case. Requested items are created from tasks, but do not appear under HR Tasks.

    -   **Similar Cases**

        List of related cases by type of request.

    -   **KB Articles Read by User**

        List of Knowledge Base articles read by the **Subject person**.

    -   **Direct Deposit for Subject Person**

        List of direct deposit information for the

    -   **Health Benefits for Subject Person**

        List of health benefits the subject person is enrolled. This tab only appears for health benefit cases.

    -   **Retirement Benefits for Subject Person**

        List of retirement benefits the subject person is enrolled. This tab only appears for retirement benefit cases.

    -   **HR Cases**

        All HR cases for the **Subject person**.

    -   **Child Cases**

        Lists child cases associated with this case. Click **New** to create a child case under the case you are working on.

        **Note:** When you close the parent case, all child cases are cancelled.

    -   **Beneficiaries**

        Only appears for Total Rewards cases with an HR service type of Beneficiaries Add/Modify or Inquiry.

        List of beneficiaries for **Opened for** and **Subject person**.


-   **[View HR case information](t_ViewHRCaseInformation.md)**  
There are multiple ways to find a specific HR case.
-   **[HR document generation](../concept/DocumentGeneration.md)**  
There are multiple ways to generate documents in HR Service Delivery.
-   **[Secure HR case attachments](secure-doc-ckm.md)**  
Add an extra layer of security on attachments that are linked to a case. Grant access to attachments with sensitive or private data to groups, users, user criteria or roles.
-   **[Sending an email from a case](send-email-cm.md)**  
Send any communication related to HR Workforce Administration cases using the Send email feature. Minimise typing errors by auto-populating the email address of the subject person \(of the case\) in the email.
-   **[Checklists in HR cases](../concept/c_ChecklistsInHRCasesAndTasks.md)**  
A feature of HR services is the ability to automatically add a checklist to an HR case. A checklist can serve as a reminder to the HR agent to ensure that the procedure is followed.
-   **[Adding an HR task to an HR case](t_ViewAnHRTask.md)**  
You can add, view, or work on HR tasks assigned to HR cases.
-   **[View HR task information](ViewHRTaskInformation.md)**  
There are multiple ways to find a specific HR task.
-   **[Add adhoc approvers to a case](add-approvers-cm.md)**  
Provide your agents with the flexibility to add adhoc approvers to a case that is part of an HR service.

**Parent Topic:**[Use HR Case Management](../concept/c_HRCaseManagement.md)

