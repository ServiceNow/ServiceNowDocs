---
title: SLA timeline
description: The SLA timeline is a feature of the Service Level Management application. The SLA timeline detail helps you understand the progress of an SLA. The timeline provides detailed insight to the task updates which triggered stage changes during the life cycle of a task SLA.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, Service Level Management, IT Service Management]
---

# SLA timeline

The SLA timeline is a feature of the Service Level Management application. The SLA timeline detail helps you understand the progress of an SLA. The timeline provides detailed insight to the task updates which triggered stage changes during the life cycle of a task SLA.

The SLA timeline detail helps you to:

-   View the progress of SLAs, OLAs, and underpinning contracts.
-   View related task updates.
-   Identify the reason a task update triggered a specific stage in the task SLA.
-   Debug and verify a task SLA and the SLA definition.

**Note:** This feature is available only on the SLA Engine 2011 version.

Role required: itil, sla\_admin, sla\_manager

![SLA Timeline](../image/SLATimeline.png "SLA Timeline")

<table id="table_a4l_zcr_xy"><thead><tr><th>

Levels

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

Name

</td><td>

Specifies the SLA definition name and lists the task SLAs that result from the SLA definition. This field also displays, in the form of symbols, the last known stage, and the completion or the cancellation status, if any, of the task SLA.

</td></tr><tr><td>

2

</td><td>

Preference to see **Business elapsed time** or **Business time left** on timeline row

</td><td>

**Business elapsed time:** Specifies the business time that has accumulated from the beginning of the SLA to its end.

 **Business time left:**

Specifies the business time that is remaining by which the SLA task must be completed.**Note:** The selected option from the choice list is saved as a user preference and is selected by default when you navigate to the SLA timeline in the future. Whether you set the system property **Always populate business fields on a Task SLA** to true or false, the SLA timeline always populates the **Business fields for representation**.

</td></tr><tr><td>

3

</td><td>

![SLA filter icon](../image/SLAFilter.png)

</td><td>

Enables filtering of the data displayed by the SLA timeline . You can filter data by selecting the following options:-   **Show only breached**: When selected, displays the task SLAs that are breached. This check box appears only when the SLA engine property **Enable compatibility with 2010 ‘breached’ stage for SLAs** is set to false.
-   **SLA Stage**: Select to view the task SLA records that match the final stage of a specific task SLA.

**Note:** If the SLA engine property **Enable compatibility with 2010 ‘breached’ stage for SLAs** is set to true, the **Completed** stage appears as **Achieved** and the **Breached** check box appears under the SLA stage.

-   **SLA Definitions**: Select to view the task SLA records for a specific SLA definition.

</td></tr><tr><td>

4

</td><td>

![Task Record Picker](../image/SLATaskRecordPicker.png)

</td><td>

Lets you view detailed information about the task when you click the information icon.

</td></tr><tr><td>

5

</td><td>

![Zoom In/Out](../image/SLAZoom.png)

</td><td>

Provides several zoom in/out levels to control SLA timeline zoom resolution.**Note:** If the duration of any task SLA is more than 1 year, then the 5-minutes view is disabled because of performance issues and browser limitations. The condition is applicable for all the browsers.

For IE and EDGE:

-   The 5-minutes view is not available for any task SLA that has a duration of more than 35 days.
-   The 8-hours view is not available for any task SLA that has a duration of more than 10 months, and the default view is set to 16 hours.
-   The 16-hours view is not available for any task SLA that has a duration of more than 21 months, and the default view is set to 24 hours.

</td></tr><tr><td>

6

</td><td>

![SLA Legend List](../image/SLALegendList.png)

</td><td>

The legend provides the following categories.-   **Shapes**
    -   **Completed**: Symbolizes a task update which completed the task SLA.
    -   **Canceled**: Symbolizes a task update which canceled the task SLA.
    -   **Task update**: Symbolizes an update of the task.
    -   **Task update with stage change**: Symbolizes an update of the task which also led to the change in SLA stage.
    -   **Breach time \(Estimated\)**: Symbolizes estimated Breach time of an in-progress task SLA that is not yet breached or paused.
    -   **Expected start**: Symbolizes estimated Start time of a task SLA. This scenario is encountered for a retroactive task SLA starting in the future.
-   **Bar color \(SLA Duration\)**
    -   **Below 50%**: Green represents a task SLA stage below 50% of the defined SLA duration.
    -   **In-between 50% and 75%**: Yellow represents a task SLA stage between 50% and 75% of the defined SLA duration.
    -   **In-between 75% and 100%**: Orange represents a task SLA stage between 75% and 100% of the defined SLA duration.
    -   **Above 100%**: Red represents a task SLA stage after the SLA is breached.
    -   **Paused**: Gray represents a task SLA stage when it is paused.
-   **Modifiers**
    -   **Retroactive \(in lighter shade\)**: Represents the stages, updates, and out-of-schedules that are in the retroactive time.
    -   **Out of schedule \(with center stripe\)**: Represents the time period that the task SLA was outside of the schedule time defined in the SLA definition.

</td></tr><tr><td>

7

</td><td>

![SLA Configuration Toggle Button](../image/SLAConfigurationToggle.png)

</td><td>

Provides a toggle to show and hide task updates that did not cause an SLA stage. Task updates that are not responsible for an SLA stage change can help debug SLA definition conditions.

</td></tr><tr><td>

8

</td><td>

![Refresh](../image/SLARefresh.png)

</td><td>

Refreshes the information on the SLA timeline.

</td></tr><tr><td>

9

</td><td>

Task SLA Details

</td><td>

Displays the details of a task SLA, depending on where you click the timeline. **Stage details**: When you click the update on the task SLA timeline, the stage details section appears with the following information:

-   Summary of the changes or useful information relevant to the selected stage.
-   Information on stage start and stage end such as the start and the end time, actual elapsed time and percentage, actual time left, pause duration. The stage information also displays any breach of the SLA.

**Note:** If no schedule is attached to the SLA definition, then business values are hidden and actual values are displayed. If any schedule is attached to the SLA definition, both the business and the actual values are displayed.


 **Task update details**: When you click the task update, the **Task update details** section appears with the following information:

-   **SLA definition conditions**: Displays the respective conditions of the task SLA and the values for the related columns at that point for the task. A blue check mark appears for the conditions that affect the SLA stage change.
-   **Time**: Displays the date and the time when an update takes place in the task SLA. It also displays the delta changes that occurred in the task for that update.

 **Out of schedule details**: When you click the out of business schedule on the task SLA timeline, the outside business period details section appears with the following information:-   **Start date**: Displays the start date of the selected task SLA.
-   **End date**: Displays the end date of the selected task SLA.
-   **Duration**: Displays the duration of the current out of schedule selection.
-   **Total out of schedule duration**: Displays the total out-ofschedule hours until the end of the current selection.

 **Note:** Click ![Left Carousel in SLA Timeline](../image/SLALeftCarousel.png) and ![Right Carousel in SLA Timeline](../image/SLARightCarousel.png) to navigate to the left and right task update in the details section.

</td></tr></tbody>
</table>**Note:**

The SLA timeline receives information about the task from the audit history and refers to the current SLA definition to pull data for the SLA timeline. The SLA timeline displays task SLA information as though the SLA repair is already executed, irrespective of whether it is executed or not.

-   **[Understand why an SLA did not trigger as expected](why-sla-did-not-trigger.md)**  
Describes the conditions when an SLA might not trigger as expected.
-   **[Use SLA timeline to determine business schedule](sla-timeline-determines-bus-schedule.md)**  
This example demonstrates how to use the SLA timeline to determine the business schedules and business percentage time related to a task SLA.
-   **[Use SLA timeline to understand SLA stage change](understand-sla-stage-change.md)**  
Describes how you can understand SLA stage changes using SLA timeline.
-   **[Use SLA Timeline to validate a new SLA definition](validate-new-sla-definition.md)**  
When a new SLA Definition is created the SLA Timeline can be used to see how the SLA will behave against existing task records.

**Parent Topic:**[Service Level Management reference](service-level-management-reference.md)

**Related topics**  


[Use SLA timeline to determine business schedule](sla-timeline-determines-bus-schedule.md)

[Use SLA timeline to understand SLA stage change](understand-sla-stage-change.md)

[Use SLA Timeline to validate a new SLA definition](validate-new-sla-definition.md)

[Understand why an SLA did not trigger as expected](why-sla-did-not-trigger.md)

