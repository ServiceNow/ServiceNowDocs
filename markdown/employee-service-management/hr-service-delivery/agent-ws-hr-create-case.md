---
title: Create case in Classic HR Service Delivery Agent Workspace
description: Creating a new HR case in HR Service Delivery Agent Workspace is easy and all the information you need is on one page.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# Create case in Classic HR Service Delivery Agent Workspace

Creating a new HR case in HR Service Delivery Agent Workspace is easy and all the information you need is on one page.

## Before you begin

Role required: sn\_hr\_core.case\_writer

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

    The landing page appears.

2.  To create an HR case, select the **Add** icon.

3.  Select **HR Case**.

    For information on **Interactions**, see [Using interactions in HR Service Delivery Agent Workspace](../concept/agent-ws-hr-interactions.md#). For Employee Relations \(ER\) cases you can skip adding the Opened for person by selecting the **Skip verification** link. For more information on ER cases, see [Create an HR Service Delivery Employee Relations case using the legacy UI](create-hr-employee-relations.md).

    ![HR Agent WS search for employee or case](../image/agent-ws-hr-search-no.png)

4.  Enter an employee name.

    If an employee is flagged as a VIP in their HR profile, VIP appears when you enter their name. ![HR Agent WS verify employee](../image/agent-ws-hr-verify-empl.png)

5.  Verify that the employee is the correct person the case is for.

    **Note:** Advanced reference qualifiers on a reference field is not supported in the case creation configuration page. When the limit user search filter is applied to the employee search, it will not be applied to **Opened for** and **Subject person**.

6.  Select the HR service for the HR case.

7.  In the Case Details section, fill in the fields.

<table id="table_l2g_h51_w4b"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

COE

</td><td>

Select the **Center of Excellence** associated with the HR case you are creating. Selecting a COE filters the choices for HR service. For more information, see [HR Centers of Excellence data model](../concept/hr-centers-of-excellence-coes.md).**Note:** You can also select an HR service first and the associated COE automatically populates.

</td></tr><tr><td>

HR service

</td><td>

The HR service based on the COE selected or what you select based on communication with the employee request. What HR services are available to an employee filter by:-   COE selected.
-   HR criteria for the **Subject person** based on the HR service configuration.

Limit services filter on the **Case Creation Configuration** form. If the HR service field is empty, ensure that you did not remove the Opened for field.

 **Note:** **Bulk Parent Case** does not appear as a selection because it only appears when creating a parent case for child bulk cases. For more information, see [Add or modify bulk HR cases](t_CreateBulkCases.md).

</td></tr><tr><td>

Work notes

</td><td>

Information specific to the case that can help other HR agents. **Work Notes** are not visible to the **Subject person**.The sn\_hr\_core.restrict\_guest\_email system property allows a user to send an email from a personal email account referencing an HR case. When the property has a value of false \(default\), the text from the email appears in the Work notes field. To access system properties, enter `sys_properties.list` in the navigation filter.

 **Note:** Translate the text in your preferred language using the **Translate** option. For configuring the dynamic translation framework, see [Dynamic translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>8.  Select **Create Case**.

    If the duplicate case warning appears, verify that you are creating a unique case. When there are no similar cases, an HR case number is assigned and the State is **Draft**. If there is a similar case for the subject person, HR service, and if the case was created within three days \(configurable from HR Administration/Properties\), a warning appears. ![HR Agent WS duplicate case warning](../image/agent-ws-hr-dup-case.png)

9.  Select **Create new case**.

    The following fields appear:

<table id="table_mhw_xpb_w4b"><thead><tr><th>

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

Opened

</td><td>

The date and time the HR case was opened.

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

Add collaborators or other HR agents to the case.Only HR agents can be added as collaborators. For example, an HR agent can add them self as a collaborator after transferring a case to a different agent or group. This action permits the original agent to still track the case. Or, an HR agent can add another HR agent as a collaborator to request help. Adding a collaborator populates the case on the collaborations list.

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

Short description

</td><td>

Populates from the HR service. After the case is created, you can modify the description.

</td></tr><tr><td>

Description

</td><td>

You can add a longer, detailed description after the HR case is created. Use the Rich Text Format \(RTF\) tools to format your text.Rich text formatting also appears for a case or task description on the Employee Center.

</td></tr></tbody>
</table>10. Check the contextual side panel for information that can help you work this case.

    You can choose from Agent Assist, Response Templates, or Fulfillment Instructions depending on what information you need. ![HR Agent WS contextual side panel](../image/contextual-sidebar-1.png)

11. Select **Ready for Work** to change the **State** to **Ready** and assign an HR agent and assignment group.

    If your company requires approvals or signed agreements, you must resolve these requirements before you can close the case.


