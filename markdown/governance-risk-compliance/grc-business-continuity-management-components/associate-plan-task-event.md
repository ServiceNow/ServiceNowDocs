---
title: Add impacted assets and plans to an event
description: Quantify the performance of your continuity and recovery plans through event-based testing. Measure success by tracking the completion of tasks associated with each plan.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Monitor event task completion, Structured workflows for Exercise and Crisis Management, Using BCM Classic Workspace, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Add impacted assets and plans to an event

Quantify the performance of your continuity and recovery plans through event-based testing. Measure success by tracking the completion of tasks associated with each plan.

## Before you begin

Role required: sn\_bcm.planner, sn\_bcm.program\_manager

## About this task

A good business continuity plan is a result of thoughtful assessment of business impact analysis and the risks involved in a disruptive situation. However, the plan becomes viable only after it is tested in an event.

## Procedure

1.  Navigate to **Business Continuity** &gt; **Business Continuity Workspace**.

2.  To update an active exercise or crisis event from the Home page of the Business continuity workspace, click the link to the event record in the **Event** column of the **My exercises** section.

3.  To update the event from the lists view of the workspace, click the lists icon \(![Lists icon](../../grc-workspace-audit/image/ListsIcon.jpg)\).

4.  If the record is an exercise event and is in pending state, Click **Pending** link in the Exercises list.

5.  Click the link to the event record in the **Number** column.

6.  Click the **Impacts** tab to view the list of impacted items.

    You can add assets, activated plans for the recovery of the assets, and an ad hoc plan for an event asset.

7.  Click the **Impacts** tab to view the list of impacted items.

    Impacts grid displays impacted assets and activated plans. You can:

    -   add the assets that are impacted and the plans that are related to the assets
    -   view the plans related to the assets under the respective assets in the grid
    -   add an ad hoc plan that does not have a plan reference
    -   view the details of asset recovery and the activated plan by clicking the information icon \(![Information icon](../image/InformationIcon.png)\)
    For information on the logic behind the calculation of recovery task entities, see [Calculation of actual duration and total effort to recover an event asset](view-exercise-crisis-event-details.md#ref-calc-actual-dur).

    If the impacted assets are CMDB CI data that came into the BIA automatically based on CMDB dependencies and when these assets are scoped in the plan, then at the time of recovery of the asset, the related assets and the related plans are automatically pulled into the exercise event as impacted assets and activated plans in the **Impacts** tab.

    For more information on the planning and execution of a recovery event, see [Data flow, planning, execution, and recovery of related plan assets in event](../concept/planning-execution-event-bcm.md).

8.  Click the **Add assets** button to recover assets in the event.

    1.  Select the impacted item type or the primary element to recover in the Add Assets pop-up.

    2.  Click **Next**.

    3.  Select the impacted items or assets in the Add Assets pop-up.

    4.  Click **Save**.

        The grid displays the assets in the **Short description** column. As these assets are added to the event, they are now event assets. The grid also displays the state of assets whether they are recovered or not, and the actual time taken for recovery.

9.  Click **Add plans** button.

    The assets can be part of an approved plan or without a plan.

    Use the grouped button to add as many plans as you need to an event. However, you can add only one ad hoc plan to the event. **Add ad hoc plan** button appears when an ad hoc plan is created for an event. This ad hoc plan is the one that appears in the Ad hoc plan pop-up when you select assets.

    Add ad hoc plan button is shown after an adhoc plan is created for an event. The same is mapped to the selected assets in the ad hoc plan modal.

    -   To select a plan that the impacted asset is part of, select **Show plan for impacted assets**.
        1.  Select the asset that is impacted in the **Select Impacted Asset** field.
        2.  Click **Next**.
        3.  Select the plans for the impacted asset in the Select Plans to Add pop-up.

            This action creates the activated plan if it does not already exist and then maps the impacted asset with the activated plan in the Impacted Asset to Activated Plan \[sn\_recovery\_impacted\_asset\_to\_activated\_plan\] table.

    -   To display all plans and select assets from the plans, select **Show all plans**.
        1.  Click **Next**.
        2.  Select plans from the list in the Select Plans to Add modal.
        3.  Click **Next**.
        4.  Select impacted assets for the selected plans from the Choose Assets of Selected Plans modal.

            This action adds impacted assets, activated plans, and maps the impacted assets with the activated plans in the Impacted Asset to Activated Plan \[sn\_recovery\_impacted\_asset\_to\_activated\_plan\] table.

            As the plan is being activated for the event that is active, the plans or the assets cannot be removed once the event is **In Progress** state.

        5.  Click **Confirm** to proceed with the activation of the selected plans. This message pops up for the events that are **In Progress** state.
    **Note:** The impacted items or event assets, the activated plans, and their status are displayed in the grid.

10. Click the **Add ad hoc plan** button.

    After you add assets to the event, you can click the **Add ad hoc plan** button to add an ad hoc plan for the selected assets of the event.

    **Note:** This action adds an ad hoc plan if it does not already exist for the event. After an ad hoc plan is added to the event, subsequently whenever you click the add ad hoc plan button, all the impacted assets that you select are added to this existing ad hoc plan.

    There can be only one ad hoc plan per event.

    -   You can delete the impact of an event that is its assets, activated plans, and tasks until the event begins or is in **Pending** state.
    -   If the exercise or the crisis event is in **Work in Progress** state, then you cannot delete the associated impacts.
    -   You cannot add event assets, activated plans, or event tasks when the event is in **Closed Complete** or **Closed Incomplete** states.
    You can view the selected assets and plans in a hierarchy on the grid in the **Short description** column.

    ![Impacts grid.](../image/AdhocEventTask.png "Impacts grid")

11. To update the impact details, click ![Information icon](../image/InformationIcon.png) of the respective record to launch the event asset and activated plan in the form view.

    1.  To view the plan details of an activated plan, click ![Information icon](../image/InformationIcon.png) for the respective plan record in the impact grid.

        You can view the activated plan number, the plan name, its short description, state of the plan, priority, and description details.

    2.  Click the **Open Record** link next to the plan name.

        ![Plan details from impact grid.](../image/PlanDetailsImpactGrid.png "Plan details from impact grid")

        The action opens the plan in a separate tab, where you can view its complete details.

    -   **Editable details in an Impacted Asset**

        In the impacted asset details, you can only edit the **State** of the asset if it has been recovered or not, and the **Actual time taken** to recover the asset. However, the rest of the impacted asset details are view only.

    -   **Editable details in an Activated Plan**

        You can edit the state of the plan, its priority, and description. However, you cannot edit the activated plan number or its short description.

    -   **Editable details in an impacted Event Task**

        You can only edit the **Assignment group**, **Assigned to**, and **Additional assignee list** fields. The rest of the fields are read only.

12. Click **Save**.

13. Click the refresh icon \(![Refresh icon.](../image/RefreshAlertsIcon.png)\) to display the updated state of the asset or plan, and the actual time taken to recover the asset.


