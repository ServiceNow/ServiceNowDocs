---
title: View the general details of a business continuity plan
description: Use the Details tab of the plan to view the general information about the template that is used for the plan, its type, and other details.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Structured workflows for Business Continuity Planning, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# View the general details of a business continuity plan

Use the **Details** tab of the plan to view the general information about the template that is used for the plan, its type, and other details.

## Before you begin

Role required: sn\_bcm.admin, sn\_bcm.program\_manager, or sn\_bcm.planner

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  Click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

3.  Click **In Draft** state in the Planning list.

4.  Click the link to the plan record in the **Name** column.

5.  Click the **Details** tab of the business continuity plan \(BCP\).

    This tab gives you a summary of the plan details. You can edit the information if required.

6.  Click **Save** after updating the plan details.

7.  To generate a PDF and download a copy of the BCP to your local hard drive, click **Generate PDF**.

    A message appears with a downloadable link to the BCP PDF.

    **Note:** After the plan is approved, the PDF is generated and attached to the plan.

8.  To move a plan from **Approved** to **Draft** state, select the **Edit** button.

9.  To create a copy of the plan, click the **Copy** button.

    If you have the permission to edit a BIA, then you can also copy the BIA. A BCM planner and program manager can delete a plan and its related table records when the plan is in Draft, In Review, and Returned states. BCM admin can delete a plan irrespective of its state.

    1.  Enter the name of the new plan in the Copy plan pop-up.

    2.  Click **Confirm**.

        -   The copy action creates an exact replica of the plan with the name that you enter in the Copy plan pop-up. The copied plan is moved to **Draft** state.
        -   The action copies the plan assets, plan documentation sections, recovery teams, loss scenarios, its related asset dependencies and recovery strategies, and recovery tasks of the original plan to the copied plan.
        -   The documentation sections of the copied plan are in **Pending** state. Edit each section, if required, and move it to **Complete** state.
        -   Dependencies are populated when the plan is copied.

