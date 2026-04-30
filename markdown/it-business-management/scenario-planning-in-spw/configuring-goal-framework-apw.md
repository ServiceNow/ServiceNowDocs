---
title: Configuring goals in Strategic Planning
description: To define and manage goals in Strategic Planning, you must perform some initial administrative tasks for the workspace to be fully functional. The data displayed in the goals view in Strategic Planning is stored in the Goal Framework tables.
locale: en-US
release: xanadu
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configuring goals in Strategic Planning

To define and manage goals in Strategic Planning, you must perform some initial administrative tasks for the workspace to be fully functional. The data displayed in the goals view in Strategic Planning is stored in the Goal Framework tables.

-   With the admin role, you can migrate the existing goals data to the Goal Framework tables.
-   With the sn\_gf.goal\_admin role, you can set the goal preferences.

Post migration of your existing goals \(if any\) and configuring the goal preferences, use the Goals view in Strategic Planning to define your goals. For more information, see [Managing goals in Strategic Planning Workspace](managing-goals-in-alignment-planner-workspace.md).

-   **[Migrate existing goals data to Goal Framework tables](../task/migrate-existing-goals-data-apw.md)**  
With the admin role, you can migrate the existing goals data to the Goal Framework tables by running the scheduled job.
-   **[Configure goal preferences](../task/configure-goal-preferences-apw.md)**  
Configure goal preferences to manage goals such as the calendar type used for goal setting, weighted average calculation for goal progress, and deletion of goals and targets.
-   **[Customize label for Goal and Target tables](../task/customize-labels-for-goal-and-target-tables.md)**  
Customize the label for Goal \[sn\_gf\_goal\] and Target \[sn\_gf\_goal\_target\] tables according to your organization’s requirement.
-   **[Configure a table for an assigned entity](../task/configure-assigned-entity-egm.md)**  
Configure a table for an assigned entity type, so that the goal user can associate goals with the required assigned entity.
-   **[Create goals demo data with target breakdowns](../task/create-goals-demo-data-with-target-breakdowns.md)**  
Run the **Create Goals Demo Data with Target Breakdowns** schedule job to create goals demo data with target breakdowns, so that you can view the target breakdowns section on the Goals page.
-   **[Import goals and targets data from a spreadsheet](../task/import-goals-and-targets-data-from-a-spreadsheet-apw.md)**  
With the admin role, you can import your existing goals and targets data from a spreadsheet to the Goal Framework tables.
-   **[Update a schedule job to automate Actual value of the targets](../task/schedule-a-job-to-automate-actual-value-of-the-targets-apw.md)**  
Use the Goal Framework for SPM application to modify the run time for the scheduled job according to your preference to auto-update the actual value of the targets for which a target source has been configured.
-   **[Migrate target breakdowns](../task/migrate-target-breakdowns-spw.md)**  
After upgrading to Strategic Planning v4.3.2 or later, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job to migrate the existing values from the **Review frequency** field to the **Check-in frequency** field in the target records.
-   **[Migrate goal relationships for assigned entities](../task/migrate-goal-relationships-for-assigned-entities-egm.md)**  
Migrate the existing goal relationship data from the Goal Relationship \[sn\_gf\_goal\_m2m\_relationship\] table by running the scheduled job.
-   **[Configuring target source for target automation](setting-targets-for-a-goal-and-automating-the-actual-value-using-agf-apw.md)**  
Configure target sources for target automation so that the goal user can define a target source when setting a target for the goal. Defining a target source for a target updates the actual value of the target automatically.
-   **[Defining a custom unit of measure](defining-a-custom-unit-of-measure.md)**  
Defining a custom unit of measure helps the goal users to set the unit of measure for targets as per their choice. Unit of measures are two types, quantitative and qualitative.

**Parent Topic:**[Configuring Strategic Planning Workspace](../../alignment-planner-workspace/concept/setting-up-alignment-planner-workspace.md)

