---
title: States and UI actions for a BCP
description: When you create a business continuity plan \(BCP\), certain UI actions are associated with each state.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Structured workflows for BCPs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# States and UI actions for a BCP

When you create a business continuity plan \(BCP\), certain UI actions are associated with each state.

## States and UI actions that are associated with a business continuity plan

The states and UI actions that are associated with a business continuity plan are described in the following table.

<table id="table_amh_4kb_cv"><thead><tr><th>

Updated state of the BCP

</th><th>

UI action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Draft**

</td><td>

In business continuity plan record Lists view, select **New**.

 **Note:** You can also navigate to the **Planning** section of the Home page and select **Create BIA**.

</td><td>

When you select **New** in the Create New Plan form or **Create BIA** in the Home page, a record is created in the **Draft** state by default.

 On the **Details** tab, add details of the business continuity plan. Add details on the following tabs:

-   Scope
-   Documentation
-   Related plans
-   Recovery teams
-   Loss scenarios
-   Recovery tasks

</td></tr><tr><td>

**In review**

</td><td>

Select **Submit for review**.

</td><td>

When you select **Submit for review** in the Create New Plan form, the state of the business continuity plan is updated to **In review**.

</td></tr><tr><td>

**Pending approval**

</td><td>

Select **Submit for approval**.

</td><td>

When you select **Submit for approval** in the Create New Plan form, the state of the business continuity plan is updated to **Pending approval**.

</td></tr><tr><td>

**Approved**

</td><td>

Select **Approve**.

</td><td>

When you select **Approve** in the Create New Plan form, the state of the business continuity plan is updated to **Approved**. The **Overview** tab displays the progression of the states for the business continuity plan.

 When the business continuity plan is in the **Approved** state, you cannot edit it further.

</td></tr><tr><td>

**Archived**

</td><td>

In the Create New Plan form, select **Archive**.

</td><td>

When you select **Archive** in the **Create New Plan** form, the state of the business continuity plan is updated to **Archived**.

 Starting with BCM release 9.0.x, you can revert an archived business continuity plan \(BCP\) to the **Draft** state by selecting the **Edit** button on the form.

 You can perform the following additional UI actions in the Create New Plan form:

-   **Generate PDF**

Download the PDF of the business continuity plan for reference. The PDF attachment is available in the **Activity** panel of the **Details** tab.

For information on generating the PDF of a business impact analysis, see [Generate BCP reports in PDF or Microsoft Word format](../task/generate-pdf-for-bcp.md).

-   **Copy**

Save a copy of the PDF of the business impact analysis for future reference as a template.

-   **360º view**

Visualize the 360º representation of the business continuity plan such as its name, scope, related plans, and related tasks. To view 360º relationships of a business continuity plan, see [Visualize 360° relationships for the BCP](../task/relationship-view-bcp.md).

-   **Delete**

Delete the continuity plan.

-   **Edit**

Edit the business continuity plan.

-   **Save**

Save the business continuity plan.


</td></tr><tr><td>

**Returned**

</td><td>

Select **Reject**.

</td><td>

When the BCP is rejected, it is set to **Returned**. You can edit the business continuity plan in the **Returned** state.

</td></tr></tbody>
</table>**Parent Topic:**[Structured workflows for BCPs](bcp-tasks-performed-by-bcp-owner.md)

