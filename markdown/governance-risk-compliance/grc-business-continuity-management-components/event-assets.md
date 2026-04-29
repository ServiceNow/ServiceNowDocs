---
title: Event assets
description: When an event is initiated, event assets are managed by using different recovery management methods.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Event assets

When an event is initiated, event assets are managed by using different recovery management methods.

Beginning with the Xanadu release, you can use the time fields from an activated plan and the event asset, calculated from the dependent event tasks. When plans linked to an exercise are activated, they are now displayed in an **Open** state instead of a **Work in Progress** state. Even if a plan has recovery tasks without any tagged assets, you can still initiate an event task. When at least one of the tasks linked to an activated plan is updated to the **Work in Progress** state, the status of the activated plan is changed to **Work in Progress**.

The time needed to complete the tasks is aggregated at these levels:

-   Plans
-   Assets

These fields and columns are instrumental in calculating the time for plans:

-   When a plan transitions to the **Work in progress** state, the start date is recorded. The completion date and time of the final task are captured as the End date.
-   The Total Effort column is calculated by adding up the durations of all tasks of the plan.
-   The Total effort and Total time taken columns are left blank if any tasks remain in the **Open** state \(The tasks are not in the **Closed** state\).
-   If new ad-hoc tasks are initiated, the Total effort, Total time taken, and Status columns are reset.
-   Once all tasks in a plan are completed, the Total Effort, Total Time Taken, and Status columns are updated to reflect that the plan is Closed complete.
-   If no tasks are listed in the plan, the Actual start date time and Actual end date time should be manually adjusted.
-   Confirm to check the boxes for the mandatory **Start Date Time** and **End Date Time** fields in the list view when the tasks are marked as Closed.


These fields and columns are used to calculate time for the assets:

-   For an asset, the start date and end time are populated based on its tasks. For example, if an asset is part of two tasks, the start date of the first task is recorded in the **Start date** field, and the end date of the final task is noted in the **End time** field.
-   The Total effort column is calculated by adding up the duration of all tasks where the asset is tagged.
-   If any tasks within the plan are not in the **Closed** state, the Total Effort and Total Time Taken columns remain blank.
-   If new ad-hoc tasks are initiated, the Total effort, Total time taken, and Status columns are reset.
-   If the status of any task where the asset is tagged is marked as Closed failed, then the status of the asset is not updated as Recovered. When all the tasks for an asset are closed, the status of the asset is updated as Recovered.

## Recovery of event assets

-   **Enhanced event asset management**

    BCM version 9.x.x introduces a significant improvement in event asset management by establishing a direct link between event assets and their corresponding Business Impact Analysis \(BIA\) records. This integration enables the system to automatically import Recovery Time Objective \(RTO\) and Recovery Point Objective \(RPO\) values from the BIA into recovery events. As a result, continuity managers can now directly compare actual recovery times with target recovery times, gaining a transparent and reliable metric to evaluate recovery performance and assess organizational resilience maturity.

    This enhancement streamlines the process of assessing recovery performance, allowing organizations to make more informed decisions about their business continuity strategies. By providing a clear and accurate measure of how well recovery operations align with predefined objectives, BCM 9.x.x helps organizations refine their resilience capabilities.

-   **Time measurement for recovery events**

    As you can exclude irrelevant task from calculation such as "Preparation" tasks, time management is enhanced.

-   **Event asset tracking**

    The latest enhancements to event asset management introduce more granular recovery tracking capabilities, including support for partial recovery scenarios and automated state updates for event assets. Key features of these updates include:

    -   A new **Partially recovered** state for event assets, along with the existing **Not recovered** and **Recovered** states, has been added allowing for better tracking of recovery progress.
    -   By completing specific event tasks, you can update the corresponding event asset state \(for example, from Not Recovered → Partially Recovered → Recovered\). These updates driven by the event tasks provide an accurate and timely reflection of the recovery milestones.

## Refining the recovery status as Partially recovered

When an asset is largely recovered but still requires minor tasks to be fully operational, it can be marked as **Partially recovered**. This status allows teams to perform these tasks:

-   Proceed with critical tasks without delay.
-   Address smaller, ad-hoc tasks later.
-   Update the asset status to **Recovered** once all tasks are complete.

By introducing this intermediate status, you can better manage your recovery processes, prioritize tasks more effectively, and maintain a clear overview of the asset recovery progress.

These improvements provide several benefits:

-   Real-time visibility into the operational status of assets during recovery
-   Clearer coordination signals for the recovery of dependent assets
-   Enhanced alignment between technical recovery progress and overall business continuity outcomes

By providing more detailed and accurate tracking of recovery efforts, these updates enable organizations to better manage their recovery processes and improve their overall resilience.

**Parent Topic:**[Structured workflows for exercises](performing-tasks-to-manage-exercise-events.md)

