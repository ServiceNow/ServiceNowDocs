---
title: Approve the business impact analysis
description: Approve the business impact analysis in BCM UI Builder Workspace in the BCM application. If you’re the business impact analysis owner or the BCM lead for the business impact analysis, you can approve the business impact analysis.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Approve the business impact analysis

Approve the business impact analysis in BCM UI Builder Workspace in the BCM application. If you’re the business impact analysis owner or the BCM lead for the business impact analysis, you can approve the business impact analysis.

## Before you begin

Role required: sn\_bia.bia\_admin, sn\_bia.bia\_manager, sn\_bcm.program\_manager, sn\_bcm.planner

## Procedure

1.  Navigate to **Workspaces** &gt; **Business Continuity Workspace**.

2.  Verify that you have completed the required steps listed in the workflow.

3.  To approve the business impact analysis \(BIA\), navigate to the BIA record in the **Name** column.

4.  Select **Approve** in the BIA form.

    If you’re the business impact analysis owner or the BCM lead for the business impact analysis, you can approve the business impact analysis.

    **Note:** If an approval record is created for the BIA, the **Approve** or **Reject** actions aren’t displayed on the BIA form. To view the **Approve** or **Reject** actions, these conditions must be fulfilled:

    -   As a user, you should have the sn\_bia.bia\_manager role.
    -   As a prerequisite, the BIA should be in the **Pending approval** state.
    -   As a condition, the BIA shouldn’t have any approval records created.
    When you approve the business impact analysis, its state is updated to **Approved**.


**Parent Topic:**[Structured workflows for BIAs](../concept/bia-tasks-performed-by-bia-owner.md)

