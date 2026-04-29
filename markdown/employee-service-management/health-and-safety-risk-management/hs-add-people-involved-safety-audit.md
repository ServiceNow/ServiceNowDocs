---
title: Add people involved in a safety audit
description: Add people involved to record all participants in a safety audit — their roles, responsibilities, and the objectives and actions assigned to them.
locale: en-US
release: australia
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create and manage a safety audit, Safety inspections and audits, Use, Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Add people involved in a safety audit

Add people involved to record all participants in a safety audit — their roles, responsibilities, and the objectives and actions assigned to them.

## Before you begin

Role required: sn\_hs\_rm.safety\_audit\_manager or sn\_hs\_rm.safety\_audit\_writer

## About this task

You should add people to this list before assigning objectives, because the **Assigned to** field on an objective is filtered to people already on this list.

## Procedure

1.  Navigate to **Workspaces** &gt; **Health and Safety Workspace**.

2.  Select the risk management icon \(![Risk assessment icon](../image/icon-risk-assessment.png)\).

3.  In the **Audits** list, select **All** and select the audit into which you want to add audit participants.

4.  Select the **People involved** tab and then select **New**.

5.  In the **Name** field, select the user.

    -   Only the employees of the organization \(users in the \[sys\_user\] table\) are listed in this field.
    -   The **Person type**, **Department**, **Phone**, and **Email** fields are auto-populated from the user's profile.
6.  In the **Responsibility** field, select the person's role in the audit.

7.  If this person is needed to approve findings, actions, or the audit itself, select the relevant approver options.

    -   **Findings approver**, **Audit approver**, and **Results approver**: These approver fields are available only when the user has the \[sn\_hs\_rm.safety\_audit\_writer\] role.
    -   **Actions approver**: This field is available only when the user has the \[sn\_ohs\_im.action\_writer\] role.
8.  In the **Description** field, record this person's specific responsibilities.

9.  Select **Save**.

10. Add all people who are needed to participate in this audit.


## Result

-   The person is listed in the **People involved** tab of the audit and is available to select in the **Assigned to** field on any objectives in this audit.
-   Depending on the configured approver option in step 7, the person is automatically added as an approver during the submission of findings, actions, or the audit for approval.

## What to do next

To view a person's objectives and actions, open the person's record and then the **Objectives** and **Actions** tabs in it.

-   The **Objectives** tab lists the objectives assigned to this person on this audit. You can create an objective assigned to this person directly from this list. For more information, see [Define an objective for a safety audit](hs-define-safety-audit-objectives.md).
-   The **Actions** tab lists all actions on this audit assigned to this person. You can create an action directly from this list.

**Parent Topic:**[Create and manage a safety audit](hs-create-manage-safety-audit-workspace.md)

