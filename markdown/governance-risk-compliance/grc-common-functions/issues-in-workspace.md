---
title: Issues in the Workspace
description: You can track all your issues or one specific issue from the Workspace. Issues are listed under the Issues module in the list view of the Workspace.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage issues, Common GRC features, Governance, Risk, and Compliance]
---

# Issues in the Workspace

You can track all your issues or one specific issue from the Workspace. Issues are listed under the **Issues** module in the list view of the Workspace.

## Issue overview page

The issue form displays the details about your issues. You can see information about an issue's description, state, status, work notes, and what activity has occurred so far. The information about an issue is organized in different tabs such as the **Overview** tab and the **Details** tab as shown in the following example.

![Issue Overview Page.](../image/issue-overview.png "Issue Overview Page")

In the **Details** tab, you can find information about the issue, assignment, schedule, issue grouping, action plan, confidentiality, and activity and settings.

**Note:** The details section has been removed from the **Details** tab.

## Associating objects that are related to an issue

GRC user or business user or business user lite of Issue personas can associate objects, such as the control, risk, risk event, entities, engagements, control objectives, risk statements, policies, authority documents, or processing activities, or remove the existing objects that are related to the issue.

For example, consider an entity that you can select as a related list. You can either add the other related entities or remove the existing entities by using the **Add** or **Remove** UI buttons of the entity form.

The related lists on the issue form display the dependencies that are related to the issues. The following table lists a description of the tabs and sidebar on the Issue form.

|Tab|Description|
|---|-----------|
|Overview|Overview of an issue, such as the description, state, status, work notes, and activity.|
|Details|Details about an issue, such as the assignment, schedule, issue grouping, action plan, confidentiality, activity, settings, and work notes. The Issue grouping section provides grouping information, such as Parent issue and Issue group rule. When advanced Issue grouping is enabled, it shows **Group level** field, indicating whether it’s a parent, child, or standalone issue. It also shows the **Management method** field, indicating whether it’s managed from parent or child issues individually.|
|Highlighted details|Highlighted information, such as the issue source, issue type, issue rating, priority, effects, related to, and hierarchy.|
|Affects|Entities that are affected by this issue.|
|Related to|Count of the different objects that are affected by this issue such as the controls, risks, policies, authority documents, engagements, regulatory change tasks, remediation tasks, and risk events.|
|Hierarchy|Issue hierarchy.|

The following table lists the related lists in the Issues section.

|Related lists|Description|
|-------------|-----------|
|Remediation tasks|Details of the remediation tasks, such as the name, number, state, assigned to, priority, planned end date, and actual date.|
|Task SLAs|Details of the task service level agreements \(SLAs\), such as the SLA definition, type, target, stage, business time left, business-elapsed time, business elapsed percentage, start time, and stop time.|
|Issues|Details of the related issues, such as the name, number, issue source, issue type, state, issue manager, assigned to, priority, and due date.|
|Indicator results|Details of the indicator results, such as the name, result, indicator, and data owner.|
|Control tests|Details of the control tests, such as the name, number, parent, assigned to, state, planned start date, and planned end date.|
|Issue triages|Issue triages details, such as the name, number, source, issue type, state, substate, triage owner, and reviewer.|
|Policy exceptions|Details of the policy exceptions, such as the name, number, requester, reason, policy, control objective, state, substate, valid from, valid to, and risk rating.|
|Evidence|Details of Evidence, such as the name, number, evidence for, request reason, state, substate, requester, assigned to, and due date.|
|Entities|Details of the entities, such as the entity, description, class, and owner.|
|Controls|Details of the controls, such as the name, number, entity, function, state, status, exempt, owner, and description.|
|Risks|Details of the risks, such as the name, number, entity, risk statement, owning group, owner, state, and risk assessment methodology.|
|Engagements|Details of the engagements, such as the name, number, type, engagement lead, state, engagement planned start date, and engagement planned end.|
|Control objectives|Details of the control objectives, such as the name, source ID, source, parent, category, classification, type, and compliance.|
|Risk Statements|Details of the risk statements, such as the name, framework, category, description, and appetite status.|
|Policies|Details of the policies, such as the name, type, owner, state, valid from, valid to, and compliance score.|
|Authority documents|Details of the authority documents, such as the name, common name, type, and compliance score.|
|Risk events|Details of the risk events, such as the risk event,primary entity, event type, subtype, state, date of discovery, net loss, expected loss, and non-financial impact.|
|Processing activities|Details of the processing activities, such as the processing activity, processing activity category, owner, and privacy analyst.|

The following example shows a 360-degree view of the entire relationship for a selected issue, such as the upstream issues, downstream issues, controls, and remediation tasks that are associated with the Issue.

![360-degree relationship of issue.](../image/360-degree-relationship-overview.png "360-degree relationship of an issue")

## Recommended actions

Recommended actions are system-generated suggestions that can help you quickly select a remediation task or assign an issue to the correct person.

![Remediation tasks recommended actions](../image/recommended-actions.png "Remediation tasks recommended actions")

As shown in the figure, recommended actions for remediation tasks are shown in the right side pane. You can see the list of recommended actions and perform the following:

-   **Use**: When you select a **Use** button, a form is shown with pre-populated data. You can assign to any user using the **Assigned to** field and select **Save**. You can see this record in the **Remediation tasks** tab.
-   **Dismiss**: If you don't want to use the recommended action, select **Dismiss**.

**Important:** Recommendations are shown only to the users with the following roles:

1.  Users with minimum roles of `sn_grc.business_user`, `sn_grc.business_user_lite`. You must add the `sn_nb_action.next_best_action_use` role to the `sn_grc.business_user` and `sn_grc.business_user_lite`.
2.  Users who have minimum role of `sn_grc.user` though they are not part of the issue persona.
3.  Users with minimum role of `sn_grc.business_user` and `sn_grc.business_user_lite` must be part of the issue persona.

![Recommended actions for assigned to field](../image/recommended-action-assigned.png "Recommended actions for the Assigned to field")

As shown in the figure, system-generated recommendations are shown for the **Assigned to** field. You can see the top three predictions \(John Retak, James Vittolo, and Jerrod Bennett\) above the list of alphabetized users.

-   **[Configuring an issue relationship](issue-relationship-configuration.md)**  
If an issue isn't reusable and you know that multiple similar issues were created for different controls, risk statements, or control objectives, you can still configure the issue relationship to reuse the issue in the GRC application.

**Parent Topic:**[Manage issues](manage-issues-common-core.md)

