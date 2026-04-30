---
title: Managing goals in Strategic Planning Workspace
description: Create goals for your portfolio plans, set targets for them, and evaluate the progress of the goals and targets in Strategic Planning Workspace to accomplish your organizational plans and drive business outcomes.
locale: en-US
release: yokohama
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Portfolio Planning in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Managing goals in Strategic Planning Workspace

Create goals for your portfolio plans, set targets for them, and evaluate the progress of the goals and targets in Strategic Planning Workspace to accomplish your organizational plans and drive business outcomes.

Managing goals in Strategic Planning. 

The Goals view in the Strategic Planning Workspace gives you an overview of your goals and their targets with the Dashboard, List, and Hierarchy tabs. The Dashboard tab \(formerly known as the Overview tab\) provides a summary of all your goals in a particular portfolio plan. The List tab helps you view, create, and manage your goals and targets of the particular portfolio level. The Hierarchy tab helps you view the goals and targets of the portfolio plan entities in a hierarchical manner. This tab also helps you view the goals of the parent entities \(of the portfolio plan entities\) along with the goals and targets of the current portfolio plan.

## Roles required for managing goals

<table id="id_cld_xj5_xbc"><thead><tr><th>

Access level

</th><th>

Required roles

</th></tr></thead><tbody><tr><td>

Read access to Goals

</td><td>

-   sn\_align\_core.apw\_user
-   sn\_apw\_advanced.spw\_goal\_user\_read

</td></tr><tr><td>

Edit access to Goals

</td><td>

-   sn\_align\_core.apw\_user
-   sn\_apw\_advanced.spw\_goal\_user

</td></tr></tbody>
</table>## Portfolio plan details section in the Goals view

The portfolio plan details section in the Goals view provides the portfolio plan details along with options to manage the portfolio plan and create goals. The header section is the same for all tabs in the Goals view.

From the Portfolio plan details section, you can:

-   [Create goals](../task/create-goal-egm.md) for your portfolio plan.
-   [Share your portfolio plan](../../alignment-planner-workspace/task/share-portfolio-plan-alignment-planner-workspace.md) with stakeholders and other planning managers so that they have visibility into the progress of the plan and can start collaborating.
-   [Collaborate with stakeholders](../../alignment-planner-workspace/task/collaborate-stakeholders-portfolio-plan-alignment-planner-workspace.md) and drive shared outcomes by adding comments and attachments to your portfolio plan so that users can review and share their feedback.
-   Customize the widgets and cards that you want to view on the Dashboard tab using the Settings icon \(![Settings icon.](../../alignment-planner-workspace/images/personalize-icon.png)\). This setting is available only when the Dashboard tab is selected.

    **Note:** Only users with access to edit the portfolio plan can customize the widgets and cards.


![Header section in the Goals module.](../images/goals-module-header-section.png "Example Header section in the Goals view")

## Dashboard tab in the Goals view

The Dashboard tab has multiple widgets that help you drill down in the goals and targets, see their details, and manage them. The following figure shows a sample goals list and indicates the different features for goals in Strategic Planning Workspace on the Dashboard tab.

-   Goals: A section with multiple widgets that help you view and manage your goals and targets defined for the portfolio plan.

    -   Total progress: Displays the average progress of all the goals from all the entities of the portfolio plan.
    -   Progress by &lt;entity type of the portfolio plan&gt;: Displays the average progress \(in percentage\) of total goals by each entity type of the portfolio plan. For example, if the portfolio plan is of entity type department, the widget shows the average progress of total goals in each department.
    -   Status: Displays your goals based on their status \(example, Red, Green, and Yellow\).
    -   Status by &lt;entity type of the portfolio plan&gt;: Displays your goals status by each entity type of the portfolio plan. For example, if the portfolio plan is of entity type department, the widget shows the goals status in each department.
    -   Total goals: Displays the number of total goals defined for the portfolio plan.
    -   Not aligned to parent goals: Displays the goals that aren’t directly associated with its parent goal or any of the entities of the portfolio plan. Associate such goals with the parent goal or the entities so that the effort is visible.

        **Note:** Associating a goal with the parent goal is optional.

    -   With no targets: Displays the goals that don’t have targets set for them. Set targets for such goals to achieve them.
    -   With no work aligned: Displays the goals that aren’t associated with work. You can associate work items \(Project, Demand, and Epic\) with goals so that the work being done to accomplish goals and meet targets is easily visible.
    The “Not aligned to parent goals,” “With no targets,” and “With no work aligned” cards help you review and define the goals in the system properly from the alignment perspective. After goals are defined and aligned, you can choose to hide these cards.

    ![Example Goals section on the Dashboard tab.](../images/goals-dashboard-goals.png "Example Goals section on the Dashboard tab")

-   Targets: A section with multiple widgets that help you view and manage your targets set for the portfolio plan.
    -   Status: Displays your targets based on their status. The status indicates whether the target is likely to be completed by the planned end date.
    -   State: Displays the state of the targets from all the entities of the portfolio plan.
    -   Due for review: Displays the targets that are due in a week or already overdue from their respective review due date perspective. The **Check-in due date** field on the target form helps you to update your targets periodically based on their check-in frequency.

        ![Example Targets section on the Dashboard tab.](../images/goals-dashboard-targets.png "Example Targets section on the Dashboard tab")

-   Strategic priorities: A section with the By strategic priorities widget that helps you view how your goals are aligned with your organization's long-term strategies and manage them.

    ![Example Strategic priorities section on the Dashboard tab.](../images/goals-dashboard-strategic-priorities.png "Example Strategic priorities section on the Dashboard tab")


-   **Filtering data of the portfolio plan**

    Use the filtering options on the Dashboard tab to filter the data of the goals and targets by their Strategic priority, entity type of the portfolio plan, Time period, Owner, State, and Status, so that you can focus on the particular information.![Filtering data of the portfolio plan.](../images/goals-module-goals-filtering.png)


## List view in the Goals and targets tab

The List view helps you view, create, and manage your goals and targets of the particular portfolio plan. The List tab hides the downstream and upstream goals, enabling you to focus on only the goals and targets of the current portfolio plan. The List tab helps you update the actual values for your target breakdowns directly. However, you can view the downstream and upstream goals and targets from the Hierarchy tab. The following figure shows a sample goals list and indicates the different features for goals in Strategic Planning Workspace on the List tab.

-   The row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) gives you options for managing a goal such as create subgoal, set target, and align work for the selected goal.
-   Assigned entity: Name of the entity to which the goal belongs.
-   Personalize: Helps you customize the columns that you want to view on the List tab. Select the settings icon \(![Settings icon.](../../alignment-planner-workspace/images/personalize-icon.png)\) to enable the columns that you want to view on the List tab.
-   Check-in frequency: Specifies the breakdown interval for the target. Breaking down the target into smaller periods \(example, Quarterly\) helps you set targets for each quarter and focus on the specific breakdown targets.
-   Add remarks icon \(![Add remarks icon.](../images/add-remarks-icon.png)\): Specifies the remarks that were entered by the user for business justification when updating the breakdown actuals. Selecting the Remark icon opens the breakdown side panel with Details and Comments tabs.
-   Target breakdowns: Helps you view the details of target breakdowns in yearly or quarterly intervals. You can also enter or update the actual values in this window.
-   Quarterly / Yearly: Helps to customize the view of target breakdowns quarterly or yearly.

![Example goals and targets view on the List tab](../images/goals-module-list.png "Example goals and targets view on the List tab")

## Hierarchy view in the Goals and targets tab

The Hierarchy view helps you view the goals and targets of the portfolio plan entities in a hierarchical manner. Also, the tab helps you view the goals of the parent entities \(of the portfolio plan entities\) along with the goals and targets of the current portfolio plan. For example, in the following figure, the departments are the portfolio plan entities and business units are their parent entities. Enabling the **Parent entities goals** option shows the goals of the parent entities \(of the portfolio plan entities\) along with the goals and targets of the current portfolio plan. Enabling the **Parent entities goals** option helps you plan and align your portfolio goals with the goals of the parent entities.

-   Parent entities goals: Displays the goals of the parent entities \(of the portfolio plan entities\) that helps you plan and align your portfolio goals with the goals of the parent entities.
-   Personalize: Helps you customize the columns that you want to view on the Hierarchy tab. Select the settings icon \(![Settings icon.](../../alignment-planner-workspace/images/personalize-icon.png)\) to enable the columns that you want to view on the Hierarchy tab.
-   The row context menu icon \(![Row context menu icon.](../../alignment-planner-workspace/images/action-menu-icon.png)\) gives you options for managing a goal such as create subgoal, set target, and align work for the selected goal.
-   Unaligned goals - Not directly associated with parent entities: Lists the goals that aren’t directly associated with the parent goals. You can open these goal records from the side panel and fill in the **Parent goal** field that is based on the goal of the parent entities that your goal belongs to.

![Example goals view on the Hierarchy tab with multiple targets.](../images/goals-module-hierarchy.png "Example goals view on the Hierarchy tab")

