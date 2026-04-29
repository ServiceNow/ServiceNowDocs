---
title: BIA states and UI actions
description: When you create a business impact analysis \(BIA\), certain UI actions are associated with each state.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Structured workflows for BIAs, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# BIA states and UI actions

When you create a business impact analysis \(BIA\), certain UI actions are associated with each state.

## States and associated UI actions in BIA

The states and their UI associated actions in a business impact analysis are described in the table.

<table id="table_amh_4kb_cv"><thead><tr><th>

State of the business impact analysis

</th><th>

UI action

</th><th>

Description of the action

</th></tr></thead><tbody><tr><td>

**Draft**

</td><td>

In the Business Impact Analysis record Lists view, select **New**.

 **Note:** You can also navigate to the Business Impact Analysis section of the Home page and select **Create BIA**.

</td><td>

When you select **New** in the Create New Impact analysis form or **Create BIA** in the Home page, a record is created in the **Draft** state by default.

 On the **Details** tab, you can add details of the business impact analysis \(BIA\). On the **Assessments** tab, you can respond to the Recovery point objective assessment, Recovery time objective assessment, and Dependency assessment.

</td></tr><tr><td>

**In review**

</td><td>

Select **Submit for review**.

</td><td>

When you select **Submit for review** in the Create New Impact analysis form, the state of the business impact analysis is updated to **In review**.

</td></tr><tr><td>

**Pending approval**

</td><td>

Select **Submit for approval**.

</td><td>

When you select **Submit for approval** in the Create New Impact analysis form, the state of the business impact analysis is updated to **Pending approval**.

</td></tr><tr><td>

**Approved**

</td><td>

Select **Approve**.

</td><td>

When you select **Approve** in the Create New Impact analysis form, the state of the business impact analysis is updated to **Approved**. The **Overview** tab displays the progression of the states as shown in the example.

 ![BIA in the Approved state.](../image/bia-analysis-approved-overview-tab-states-progression.png)

 When the business impact analysis is in the **Approved** state, it is in the read-only format. You can only view the Recovery point objective assessment, Recovery time objective assessment, and Dependency assessment in the **Approved** state.

</td></tr><tr><td>

**Archived**

</td><td>

In the Create New Impact analysis form, select **Archive**.

</td><td>

When you select **Archive** in the Create New Impact analysis form, the state of the business impact analysis is updated to **Archived** as shown in the example.

 ![Archived BIA.](../image/bia-archived.png)

 Starting with BCM release 9.0.x, you can revert an archived business impact analysis \(BIA\) to the **Draft** state by selecting the **Edit** button on the form.

 You can perform additional UI actions in the Create New Impact analysis form:

-   **Generate PDF**

Download the PDF of the business impact analysis for reference. The PDF attachment is available in the **Activity** panel on the **Details** tab.

For information on generating the PDF of a business impact analysis, see [Generate BIA reports in PDF or Microsoft Word formats](../task/generate-pdf-for-bia.md).

-   **Copy**

Save a copy of the PDF of the business impact analysis for future reference as a template.

-   **360º view**

Visualize 360º representation of the business impact analysis such as its name, template used, dependencies, and BIA result.

For information on how to view 360º relationships of a business impact analysis, see [Visualize 360° relationships for BIAs](../task/visualize-360-degree-view-for-bia.md).

-   **Delete**

Delete the business impact analysis if you don't need to refer to it anymore.

-   **Edit**

Edit the business impact analysis in the application.

-   **Save**

Save the business impact analysis in the application.


</td></tr><tr><td>

**Returned**

</td><td>

Select **Reject**.

</td><td>

If you select **Reject** in the Create New Impact analysis form, the state of the business impact analysis is set to **Returned**. You can edit the business impact analysis in the **Returned** state. You can update and submit it for review again.

</td></tr></tbody>
</table>**Note:** A scheduled job runs weekly to move the expired business impact analyses to the **Archived** state.

**Parent Topic:**[Structured workflows for BIAs](bia-tasks-performed-by-bia-owner.md)

