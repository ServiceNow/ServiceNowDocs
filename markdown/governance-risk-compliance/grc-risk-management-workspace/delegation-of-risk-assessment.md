---
title: Delegation of risk assessment
description: If a risk assessor is unavailable to perform a risk assessment, the assessor can appoint a delegate to perform the risk assessment for a specified time period. The ServiceNow AI Platform enables you to appoint your delegates.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Risk Assessment, Explore, Risk Management, Governance, Risk, and Compliance]
---

# Delegation of risk assessment

If a risk assessor is unavailable to perform a risk assessment, the assessor can appoint a delegate to perform the risk assessment for a specified time period. The ServiceNow AI Platform enables you to appoint your delegates.

Delegation is the assignment of authority to another person to perform specific activities. It is a process of entrusting work to another person. In the context of risk assessments, at times, it may happen that the assigned assessor for a risk assessment is unavailable to perform their risk assessments. In such a scenario, the assessor can assign another user as a delegate and the delegate can perform the risk assessment on behalf of the original assessor for a specified time period. A delegate can perform the risk assessment from the Risk Workspace and the Risk Portal. A delegate also receives a copy of all the system notifications that are sent to the original assessor. Once the delegate starts performing the assessment, the delegate's name is visible on the assessment instance. ![Delegate on the risk assessment instance.](../image/delegate-feature.png)

As a risk assessor, to understand how you can assign a delegate, refer to Configure a delegate for your tasks.

To delegate tasks to another user, configure your user profile form to display the Delegates related list. For details, refer to Add the Delegates related list.

It is important to note the following points when you assign a delegate.

-   The ability to assign a delegate is only available to perform an assessment. You cannot assign a delegate for approving a risk assessment.
-   After a delegate is assigned an assessment, the assessment shows the names of the original assessor as well as the delegate.
-   You can only assign an individual user as a delegate and not a group.
-   A delegate must have the sn\_risk\_advanced.ara\_assessor role to perform risk-based assessment.
-   A delegate must have the sn\_risk\_advanced.ara\_assessor to perform any object assessment.
-   All delegates are considered licensed users and are tracked for their GRC usage.
-   When the delegate logs in to perform the risk assessment on behalf of the assessor, the original assessor's name remains in the **Assessor** field. The new field **Assessor's delegates** displays the name of the delegate.
-   The delegate can reassign the task to another user.
-   The delegate can view the on-going assessments for the original assessor under **Tasks** in the Workspace.
-   The delegate can create issues.
-   The delegate can create risk response tasks and request approval.
-   All activity performed by the delegate is captured in the activity stream.

**Parent Topic:**[Advanced Risk Assessment](../../grc-risk/concept/advanced-risk-assessment.md)

