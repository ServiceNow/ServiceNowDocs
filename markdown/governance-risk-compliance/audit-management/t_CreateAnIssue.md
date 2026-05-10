---
title: Manually create GRC issues
description: As a GRC user, you can manually create issues to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Audit Issues &amp; Remediation, Audit Management Overview, Audit Management, Governance, Risk, and Compliance]
---

# Manually create GRC issues

As a GRC user, you can manually create issues to document policy, risk, or audit observations, or to accept any GRC problems. You can also identify the source of the issue to help analyze and classify the issues.

## Before you begin

Role required: \(per product\)

-   In Policy and Compliance Management: sn\_grc.business\_user, sn\_grc.business\_user\_lite
-   In Risk Management: sn\_grc.business\_user
-   In Audit Management: sn\_grc.business\_usersn\_grc.business\_user\_lite

**Note:** Starting with Version 12.0.1 of the products mentioned above, the minimum role for the **Assigned to** user on the Issues form is GRC Business User \[sn\_grc.business\_user\]. The minimum role for the **Issue manager** is GRC User \[sn\_grc.\_user\].

For more information on the access control limitations to issues, see [GRC business user role to control access and track usage of compliance tables](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#acls-issue-busin-user).

## Procedure

1.  Navigate to one of the following locations:

    -   **All** &gt; **Policy and Compliance** &gt; **Issues** &gt; **Create New**.
    -   **Risk** &gt; **Issues** &gt; **Create New**.
    -   **Audit** &gt; **Issues** &gt; **Create New**.
    **Note:** Starting with Version 12.0.1 of the products mentioned above, the minimum role for the **Assigned to** user on the Issues form is GRC Business User \[sn\_grc.business\_user\]. The minimum role for the **Issue manager** is GRC User \[sn\_grc.\_user\].

2.  On the [Issue form](../reference/issue-form.md), fill in the fields.

    The due date under the **Dates** tab is automatically calculated based on the issue rating. You can manually override the calculated due date. The Task SLAs related list creates and displays SLAs based on the **Due date**.

3.  Save the issue record.

    The tabs at the bottom of the screen enable you to perform various tasks for remediating the issue. You can add policy exceptions and create remediation tasks. Additionally, you can view other issues, indicator results, and task SLAs related to the issue.

    **Note:** Starting with Version 12.0.1, the **Task SLA** tab creates and displays SLAs based on the **Due date**. Notifications are sent to the issue owner and issue manager when the issue **Due date** reaches 50%, then 75%, then when it breaches. If the **Assigned to** and **Due date** fields are not empty and the issue is not in the **New** state, an SLA is created for the issue.

    If the due date for the SLA changes, a new SLA is created. The SLA is completed when the issue transitions to **Closed Complete** or **Closed Incomplete**. Also, the SLA is cancelled if the **Due date** or **Assigned to** fields are empty, or the state is New.

    Also starting with Version 12.0.1, remediation tasks can be created with the Assigned to user and issue manager user roles, as well as any user with the [GRC Business User role](../../grc-policy-compliance-implementation/task/assign-user-roles.md).


-   **[Group similar issues under a new parent issue](../../grc-policy-and-compliance/task/group-similar-issues.md)**  
When you are creating an issue, you have the option of grouping the issue with other similar issues.
-   **[Group similar issues under an existing parent issue](../../grc-policy-and-compliance/task/group-similar-issues-existing-parent.md)**  
When you are creating an issue, you have the option of grouping the issue with other similar issues as part of an existing parent issue group.
-   **[User hierarchy access control](../../grc-policy-and-compliance/concept/user-hierarchy-risk-remed-task.md)**  
If a user is assigned to an issue or a remediation task, then the manager of the user and the manager above in the hierarchy also get access to the issue or remediation task record.
-   **[Report issues from the Service Portal](../../grc-risk/task/report-issues-from-serviceportal.md)**  
When you identify any deficiencies in the controls or improvements that can be made in the organization policies, report an issue from the ServiceNow, Inc. Service Portal.
-   **[Issue assignment using the Governance, Risk, and Compliance Predictive Intelligence plugin](../../grc-risk/concept/issue-assignment-using-predictive-intelli.md)**  
Train a similarity solution model that uses machine learning so that the system can automatically suggest how to route issues to the correct assignee. Automatic routing suggestion reduces the time spent on deciding who should own the issue.

**Parent Topic:**[Manage issues in Policy and Compliance Management](../../grc-policy-and-compliance/concept/manage-issues.md)

**Parent Topic:**[Using Risk Management](../../grc-risk/concept/using-risk-mgmt.md)

