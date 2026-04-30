---
title: Manage engagements
description: The audit engagement process involves creating, planning, scoping, and conducting engagements as well as reporting on engagement findings.
locale: en-US
release: zurich
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Audit Management, Governance, Risk, and Compliance]
---

# Manage engagements

The audit engagement process involves creating, planning, scoping, and conducting engagements as well as reporting on engagement findings.

## Engagement process

The base system audit engagement process includes steps for scoping, validating, conducting, and approving engagement results. It also contains steps for following up on open audit tasks and issues, and finally closing out the audit engagement.

<table id="table_pzj_vyr_pw"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Scope

</td><td>

During the **Scope** state, audit managers define which entities are involved in the audit engagement. For example, for a financial audit, one may include all business services that the finance department relies on and the finance department itself.

 See [Add entities to an engagement scope](../task/add-profiles-to-engagement-scope.md).

</td></tr><tr><td>

Validate

</td><td>

After an engagement has moved to the **Validate** state, all the risks, controls, and test plans associated with the entities in the engagement's scope will be associated with the audit. Indicator results that were collected during the audit period of the engagement will also be associated with the audit. Audit managers can review the risks, controls, test plans, and indicator results, and update the scope of the engagement, if necessary. Audit managers can also begin creating and planning audit tasks for the engagement.

 To move an engagement into the **Validate** state, click **Validate** on any engagement currently in the **Scope** state.

</td></tr><tr><td>

Fieldwork

</td><td>

Auditors complete their assigned audit tasks during the **Fieldwork** state. These tasks include control testing, interviews, walkthroughs, and other activities. Issues that are found during control testing are associated with the engagement. Auditors can also create general issues associated with the engagement. Audit managers can create additional audit tasks as needed. When the audit is done, audit managers specify the result of the engagement, whether it's satisfactory, adequate or inadequate, and provide details on their opinion.

 To move an engagement into the **Fieldwork** state, click **Advance to Fieldwork** on any engagement currently in the **Validate** state.

 See [Audit task management](c_AuditTasks.md).

</td></tr><tr><td>

Awaiting Approval

</td><td>

During the "Awaiting Approval" state, the approvers specified in the **Approvers** field of the engagement review the results of the audit tasks conducted and the issues that were created. After reviewing the results of the engagements, approvers approve or reject the engagement.

 To move an engagement into the **Awaiting Approval** state, click **Request approval** on any engagement currently in the **Fieldwork** state.

 See [Approve or reject an engagement](../task/approve-reject-engagement.md).

</td></tr><tr><td>

Follow Up

</td><td>

After an engagement has been approved, if there are any remaining open tasks, issues or milestones, in case of GRC Advanced Audit, associated with the engagement, the engagement automatically goes into the **Follow Up** state. During this stage, auditors must close out all remaining issues, tasks, and milestones before the engagement are marked as complete.

</td></tr><tr><td>

Closed

</td><td>

Engagements move into the "Closed" state under one of three conditions:

-   The engagement is closed as incomplete during the **Scope**, **Validate**, or **Fieldwork** states.
-   There are no open audit tasks, issues, and milestones after the engagement is approved. In this case, the engagement automatically moves from the **Awaiting Approval** state to the **Closed** state.
-   All follow-up tasks, issues, and milestones are closed out. In this case, the engagement automatically moves from the **Follow Up** state to the **Closed** state.

</td></tr></tbody>
</table>-   **[Audit task management](c_AuditTasks.md)**  
Audit tasks are completed throughout an engagement and provide documented evidence that the organization is complying with external regulations and internal policies.
-   **[Create an engagement](../task/t_CreateEngagement.md)**  
Audit managers create engagements to manage audit information and collect entities, controls, and control tests that are relevant to the audit.
-   **[Generate an audit report from an engagement](../task/generate-an-audit-report.md)**  
Generate an audit report and maintain different versions of audit reports from an engagement in Follow up state.
-   **[Create an engagement from a previous engagement](../task/create-engagement-from-previous.md)**  
Audit managers can create engagements from previous engagements to reduce the need to redefine the scope, auditors, and approvers for similar engagements that are conducted throughout the year.
-   **[Create a control test from an engagement](../task/t_CreateControlTest.md)**  
After defining a control, audit managers create control tests that run periodically and provide documented evidence of whether the associated control is operating correctly.
-   **[Create an audit task activity](../task/t_CreateAnActivity.md)**  
After defining a control, audit managers create activities that explore and provide documented evidence of whether the associated control is operating correctly.
-   **[Create an interview](../task/t_CreateAnInterview.md)**  
After defining a control, audit managers create interviews with control owners to discuss and provide documented evidence of whether the associated control is operating correctly.
-   **[Create a walkthrough](../task/t_CreateAWalkthrough.md)**  
After defining a control, audit managers create walk throughs that will be conducted to observe and provide documented evidence of whether the associated control is operating correctly.
-   **[Generate a KB article from an engagement](../task/generate-kb-from-engage.md)**  
Audit managers can generate a KB article that summarizes the findings of an engagement so report findings can be communicated to executives.
-   **[Approve or reject an engagement](../task/approve-reject-engagement.md)**  
Audit users that are assigned as approvers for an engagement can approve or reject engagements in the **Awaiting Approval** state.
-   **[Add entities to an engagement scope](../task/add-profiles-to-engagement-scope.md)**  
Audit managers can define which entities are involved in the audit engagement. When you add an entity to an engagement, the corresponding risks, controls, test plans, and indicator results of the entity are also added to the engagement.
-   **[Manage Audit Engagements](c_AuditEngagementWorkbench.md)**  
The Engagement Workbench provides a timeline view from which you can select an audit engagement to view details or create a new engagement.

**Parent Topic:**[Using Audit Management](using-audit-management.md)

