---
title: Data flow, planning, and execution in an event
description: When the configuration item data is available on the ServiceNow AI Platform the same items can be used to assess dependencies in business impact analysis \(BIA\). The dependencies from the BIA can then be used in the planning and events. The configuration items \(CIs\) can be added manually to the plans and events as well.
locale: en-US
release: xanadu
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Structured workflows for Exercise and Crisis Management, Using BCM Classic Workspace, Business Continuity Management, Governance, Risk, and Compliance]
---

# Data flow, planning, and execution in an event

When the configuration item data is available on the ServiceNow AI Platform the same items can be used to assess dependencies in business impact analysis \(BIA\). The dependencies from the BIA can then be used in the planning and events. The configuration items \(CIs\) can be added manually to the plans and events as well.

You can also add new plans with assets to be recovered in a sequence.

The advantages of automatic data flow are:

-   You can reuse the configuration item \(CI\) data that is created in CMDB in BIA, and from the BIA the dependencies are used in the plans and events.
-   You have the capability to branch off to a related referred plan within the task of the main plan before executing the rest of the tasks in the main plan, especially when the referred plans are managed by planners of other departments or teams to recover their respective assets.
-   The flow of execution is sequenced as per the Task ID and no event task is skipped in between.

## Automatic data flow from CMDB to BIA and BIA to plans

When a record in created in ServiceNow AI Platform as a configuration item in CMDB, the record with all its related items are available for you to leverage as assets to assess dependencies in BIA.

-   **CMDB**

    Data is created as a CI and the record is stored in CMDB. In CMDB, this CI is related to other items by a relationship either that depends on or used by the other related items. For example, if it's a Data Center NYC, then it can depend on SAP on-premise application and other web servers, business processes, locations, and others.

-   **BIA**

    When you assess a BIA based on CMDB dependencies, the CMDB CI and its related items are automatically available as items for assessment in BIA. You can add these dependencies and the source of these items are tracked as CMDB. Therefore, the data created in CMDB is available as dependencies in BIA. In addition, you can also manually create other dependencies in BIA. For example, the Data Center NYC and its dependent SAP on-premise application are available in BIA to be added as dependencies. In addition, you can also add dependencies manually such as a Facility: New York.

-   **Plan**

    When you are in the planning stage, if you have scoped the BIA-dependent item and added it as the scope, then the dependencies of the scoped item are available as Related Assets. Also, the plans existing for these assets are available as Related Plans. In addition, you can add new plans also. For example, a plan is created for Data Center: NYC, along with which the related plans of the related assets such as SAP on-premise application and Facility: New York \(created in BIA\) also move in to the planning phase automatically. In addition to the items that came from the BIA, you can also add new assets manually to the plan.

    In the **Recovery Tasks** tab of a plan, you can also [refer to a different plan](../task/bcp-recovery-tasks-grid.md#refer-related-plan-bcp) and select the plan from the list of related plans.

-   **Exercise**

    In the event, the impacted assets and the activated plans are pulled into the **Impacts** tab automatically based on the dependencies in the BIA. Along with the primary scope of exercise and related impacts, you can also add assets and plans manually, which are all pulled into the exercise for recovery.


## Planning phase

In this planning phase, as a planner you can identify the related assets, add the related plans, and set a sequence and dependencies for execution of recovery.

![Recovery tasks to activate related plans.](../image/RecoveryTaskPlanningBCP.png "Recovery tasks to activate related plans")

If you must recover assets in Data center A before recovering assets in Data center B, then you can refer to a different plan that follows the recovery process of Data Center A. In this case, use the **Refer a different plan** option in the **Recovery Tasks** tab of the main plan, and select the relevant plan from the related plans to recover Data center A. The referred plan has its own set of tasks that the application executes when it comes to this particular task. You can also set a sequence for the execution of the referred plan within the event tasks of the main plan.

![Refer a different plan option.](../image/ReferDifferentPlanBCP.png "Refer a different plan option")

## Tracking and execution phase

In the tracking and execution phase, you can activate relevant plans during an event recovery. When you add an impacted asset in the **Impacts** tab of an exercise, then all the related assets and related plans are pulled in. Similarly, if you add a plan, then all its sub-plans are also added.

![Related plan execution sequence.](../image/RelatedPlanTaskExec.png "Related plan execution sequence")

Navigate to the **Event Tasks** tab to track the execution of the event tasks of the selected main plan. When you click the **Start Event** button for an event, the tasks are triggered for execution. When you select the main activated plan in the **Plans** section of the left pane, you can view all the event tasks of the selected plan listed on the right pane as event tasks. In the **Plans** section on the left, below the main plan are the **Related plans**. The event tasks of the main plan are executed in the order of Task ID sequentially but when a particular task in the sequence has a referred or a related plan, then the application branches off to that plan and executes all the tasks listed in that plan thereof and completes the sequence before coming back to the original main plan from where it branched off to complete the rest of the tasks in the sequence. Therefore, there's a main list of recovery tasks under a main plan, within which there are sub-plans with their own set of recovery sub-tasks. The application executes all the tasks sequentially within the referred plan before it continues to execute the rest of the recovery tasks sequentially in the main plan.

**Note:**

For a primary main plan, if there are related referred plans within, then the application executes only the referred sub-plan but does not execute any other related plan that the sub-plan might have. The hierarchy of execution stops with the first level only if there are sub-plans.

**Parent Topic:**[Structured workflows for Exercise and Crisis Management](bcm-recovery-exercise-management.md)

