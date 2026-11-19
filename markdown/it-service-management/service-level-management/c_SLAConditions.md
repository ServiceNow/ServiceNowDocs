---
title: SLA conditions
description: SLA conditions determine when a task SLA record is attached, paused, resumed, reset, canceled, and completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-level-management/c\_SLAConditions.html
release: brazil
product: Service Level Management
classification: service-level-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# SLA conditions

SLA conditions determine when a task SLA record is attached, paused, resumed, reset, canceled, and completed.

On the SLA definition, you specify up to six conditions that are evaluated each time a task record is created or updated. For example, for an SLA to attach to a task, the start conditions must match and stop conditions must not match.

SLA conditions work in the following ways:

-   SLA conditions
-   SLA condition evaluation

## SLA conditions

You can set up to six SLA conditions: start, cancel, pause, resume, stop, reset.

-   **Start condition**

    Enables you to define the conditions under which the SLA is attached.

    You can choose the conditions from the **When to cancel** list under which the SLA is canceled.

    -   **Start conditions aren't met**: If one or more of the specified start conditions change, the SLA is canceled. Selected by default.
    -   **Cancel conditions are met**: The start condition must be met only once. After that, the SLA cancels only when the cancel condition is met.
    -   **Never**: The SLA isn't canceled.
    Select **Retroactive start** to choose a date and time field from the task that will provide the start time of the task SLA. If you select the **Retroactive start** check box, the **Set start to** field appears offering the date and time fields available on the task type that this SLA definition applies to. For example if you select **Retroactive start** on a Priority 1 SLA definition and then choose **Created** in the **Set start to** field, then the SLA is attached with the start time being the date and time from the **Created** field on the Incident.

-   **Cancel condition**

    Enables you to define the conditions under which the SLA cancels. You can specify the cancel conditions at the same time when you specify the start conditions.

-   **Pause condition**

    Enables you to define the conditions under which the SLA suspends increasing elapsed time.

    You can choose the conditions from the **When to resume** list under which the SLA resumes increasing elapsed time.

    -   **Pause conditions are not met** option: If one or more of the specified pause conditions no longer match, then the elapsed time continues to increase.
    -   **Resume conditions are met** option: If one or more of the specified resume conditions match, then the elapsed time continues to increase. The **Resume conditions are met** option is selected by default.
-   **Resume condition**

    Enables you to define the conditions under which the SLA resumes increasing elapsed time. You can specify the resume conditions at the same time when you specify the pause conditions.

-   **Stop condition**

    Enables you to define the conditions under which the SLA completes. If all of the specified stop conditions match, then the task SLA completes regardless of whether it is breached.

-   **Reset condition**

    Enables you to define the conditions under which the running SLA is completed and a new SLA is attached. For a new SLA to be attached, the start condition must match.

    Reset condition also helps to configure SLAs when the value of any specific field on the task record changes, changes to or changes from a specific value in the record. For example, the value of the **Location** field in the task record is 101 Broadway East, Seattle, WA. If you set the SLA reset condition as **Location** **changes from** 101 Broadway East, Seattle, WA, any change in the value of the **Location** field resets the SLA of the task record.


## SLA condition evaluation

Every task in the system is evaluated in the following order:

-   Process new SLAs: determine if a new SLA record must be attached to a task
-   Process existing SLA records attached to a task.

SLA conditions are evaluated in the following ways:

-   Attach if start condition matches and both the stop and cancel conditions don't match.
-   Complete if the stop condition matches.
-   Pause if the pause condition matches.
-   Resume if the pause condition doesn't match or resume condition matches.
-   Reattach if both the reset and the start conditions match.
-   Cancel if the start condition doesn't match or cancel conditions matches.

Consider this evaluation order when you create conditions. For example, if your Start condition is a subset of your Stop condition, the Stop condition matches when the Start condition matches and the SLA does not attach. This includes processing any new SLAs that were just created.

If your Pause condition is a subset of your Start condition, the SLA attaches but remains permanently in Paused state. As soon as the Pause condition does not match, the equivalent Start condition also does not match and that task SLA record is canceled.

If you create an SLA definition with a Start condition and a Pause condition that are mutually exclusive, your SLA does not pause and is canceled first. For example, for an SLA definition where the Start condition is **State is one of "New, Active"** and the Pause condition is **State is "On Hold"**, when the Task is updated to state **On Hold**, the start condition no longer matches and the task SLA is canceled.

**Parent Topic:**[Service Level Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/service-level-management/service-level-management-reference.md)

