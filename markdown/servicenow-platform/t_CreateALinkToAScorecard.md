---
title: Create a link to a scorecard
description: Users with the admin role can create UI actions that allow users to view scorecards from tables.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [View an assessment scorecard, Assessment administrator tasks, Using assessments, Assessments, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a link to a scorecard

Users with the admin role can create UI actions that allow users to view scorecards from tables.

## Before you begin

Role required: assessment\_admin or admin

## Procedure

1.  Generate [assessable records](../concept/c_MetricTypesAndAssessableRecords.md) you want to evaluate.

    For example, you might create a metric type called **Project** to assess project management records.

2.  Navigate to **System Definition** &gt; **UI Actions**.

3.  Open the View Scorecard record.

4.  Right-click the header bar and select **Insert and Stay** from the context menu to create a duplicate record.

5.  Change the **Table** name to the table on which you want the UI action to appear.

    For example, you might select Project \[pm\_project\].

    ![UI action table name](../images/UIActionTableName.png)

6.  Do not edit the **Action name** field or the **Condition** script.

7.  Save the record.

8.  Navigate to the table on which you created the UI action and open an assessable record.

    1.  In this example, navigate to **Project** &gt; **Projects** &gt; **All**.

    2.  Open any record in the list.

    3.  Click **View Scorecard** under **Related Links** to open the scorecard for that assessable record.

    The scorecard appears with the title in the form of `**&lt;table display name&gt;**` **Scorecard**. For example, a scorecard for an assessable record in the Project `[pm_project]` table is named **Project Scorecard**.

    **Note:** Content does not appear in the scorecard unless the associated assessable record has assessment results or related Live Feed conversations.

9.  Insert a new **View Scorecard** UI action record for each table where you want the related link to appear.


**Parent Topic:**[View an assessment scorecard](t_ViewAnAssessmentScorecard.md)

**Related topics**  


[Assessment scorecard averages](../reference/r_Averages.md)

[Assessment scorecard categories](../reference/r_Categories.md)

[Assessment scorecard category metrics](../reference/r_CategoryMetrics.md)

[Assessment scorecard head-to-head compare view](../reference/r_HeadToHeadCompare.md)

[Assessment scorecard history](../reference/r_History.md)

[Live feed view of assessable records](../reference/r_LiveFeed.md)

[Assessment scorecard ratings](../reference/r_Ratings.md)

