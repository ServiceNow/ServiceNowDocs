---
title: View control tests in grid view
description: View and edit control tests and assessment procedures in a hierarchical data grid.
locale: en-US
release: australia
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Implementing controls and assessment objectives in CAM, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# View control tests in grid view

View and edit control tests and assessment procedures in a hierarchical data grid.

## Before you begin

Role required: sn\_grc\_cam.sca or sn\_grc\_cam.isso

## About this task

The Control Tests tab includes a grid view that displays control tests as parent rows with assessment procedures as expandable child rows. The grid view enables bulk editing of test results and automatic cascading of effectiveness ratings.

## Procedure

1.  Navigate to **All** &gt; **CAM Workspace** and select the **List** icon.

2.  From the **Assessments** list, select **All engagements**.

3.  Select an engagement.

4.  Select the **Control tests** tab.

5.  Select **Switch View** to toggle to the data grid view.

    The grid displays control tests as parent rows and assessment procedures as child rows in the right pane. Drag the panel divider to resize column groups.

6.  To expand a control test and view its assessment procedures, select the expand icon.

7.  To open a control test record, select the control test number link in the Number column.

8.  To open an assessment procedure record, select the assessment procedure identifier in the Identifier column.


## What to do next

**Edit assigned to:**

-   Double-click the **Assigned To** cell
-   Select from engagement lead or auditors list
-   Editable only when the control test state is Open or Work in Progress.

**Edit operating effectiveness:**

-   Select the **Operating Effectiveness** cell for a control test
-   Select Effective, Ineffective, or None.
-   Changes automatically cascade to parent control test effectiveness
-   Requires engagement lead role
-   Editable only when control test state is Open or Work in Progress and engagement state is not Closed

**Edit objective effectiveness:**

-   Select the **Objective Effectiveness** cell for an assessment procedure
-   Select Effective, Ineffective, or None.
-   Changes automatically cascade to parent control test effectiveness
-   If any assessment procedure is Ineffective, the control test becomes Ineffective

**Customize columns:**

-   Select the three-dot menu icon
-   Select **Personalize Columns**
-   Show or hide columns \(Notes and Attachments fields are hidden by default\)

