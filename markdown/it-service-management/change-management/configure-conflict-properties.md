---
title: Configure conflict analysis properties
description: Configure Change Management conflict analysis properties to detect change conflicts. Use the relevant information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.Conflict detection includes properties that determine how the conflict detection capability is executed. Identify conflicts based on the selected properties and the roles that have access to the feature.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Configure conflict analysis properties

Configure Change Management conflict analysis properties to detect change conflicts. Use the relevant information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.

## Before you begin

Role required: admin

## About this task

By default, not all properties are selected in the Change Management Conflict Analysis Properties page. Modify or customize conflict detection capabilities to meet the needs of your organization.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Conflict Properties**.

2.  In the Change Management Conflict Analysis Properties page, enter the roles that have access to the conflict detection feature.

3.  Configure the remaining customization properties as required.

4.  Click **Save**.


**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Create blackout and maintenance schedules in Change Management](t_CreateBlkoutMaintSched.md)

[Configure a change request to monitor outside maintenance schedule conflicts](monitor-maintenance-schedule.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md)

[Detect conflicts manually and review conflict details](t_RunManualConflictDetection.md#)

[Conflict analysis properties](configure-conflict-properties.md#)

## Conflict analysis properties

Conflict detection includes properties that determine how the conflict detection capability is executed. Identify conflicts based on the selected properties and the roles that have access to the feature.

These properties are available by navigating to **Change** &gt; **Administration** &gt; **Conflict Properties**.

<table id="table_pdf_gy2_3fb"><thead><tr><th>

Property

</th><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

A comma separated list of roles which have access to the conflict detection feature. Roles included here should have access to the underlying change\_request record

</td><td>

**change.conflict.role**

</td><td>

The roles are entered exactly as they appear in **User Administration** &gt; **Roles**. For example, enter `itil`.

</td></tr><tr><td>

When checking for change request conflicts, check against blackout windows

</td><td>

**change.conflict.blackout**

</td><td>

To check if the change request falls within the blackout window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within the child CIs' blackout window

</td><td>

**change.conflict.relatedchildblackout**

</td><td>

To check if the change request of any of the child configuration items \(CIs\) falls within the blackout window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within the parent CIs' blackout window

</td><td>

**change.conflict.relatedparentblackout**

</td><td>

To check if the change request of the parent CI falls within the blackout window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check against changes already schedules for the same CI

</td><td>

**change.conflict.currentci**

</td><td>

To check if the change request is already scheduled against the given CI, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within the CIs' maintenance window

</td><td>

**change.conflict.currentwindow**

</td><td>

To check if the change request of the CI falls within the maintenance window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within child CIs' maintenance window

</td><td>

**change.conflict.relatedchildwindow**

</td><td>

To check if the change request of any of the child CIs falls within the maintenance window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within parent CIs' maintenance window

</td><td>

**change.conflict.relatedparentwindow**

</td><td>

To check if the change request of the parent CI falls within the maintenance window, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within the schedule defined in the maintenance schedule reference field on the CI

</td><td>

**change.conflict.ci\_maint\_sched**

</td><td>

To check if the change request falls within the scheduled maintenance defined for the CI in the maintenance schedule reference field, select **Yes**.

</td></tr><tr><td>

When checking change request conflicts, check whether the change falls within maintenance or blackout windows affecting related Application Services

</td><td>

**change.conflict.relatedservices**

</td><td>

To check if the change request that falls within the maintenance or blackout windows affects other related application services, such as the services created that include the CI scheduled for change or any other CI within that service, select **Yes**.**Note:** This action requires any business services identified to be converted to an application service. For more information, see [Convert business services to application services](https://www.servicenow.com/docs/access?context=convert-bus-to-app-svc-intro&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US). For information about application services, see [Application services](https://www.servicenow.com/docs/access?context=application-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) [Application services](https://www.servicenow.com/docs/access?context=application-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

When checking change request conflicts, check whether other change requests are already scheduled for the same assigned to user

</td><td>

**change.conflict.assigned\_to**

</td><td>

To check if any other change request is assigned to the same change request assigned to a user. For example, if you assign a change request to a user who is already scheduled to implement another change request at that date and time, a conflict error is displayed, select **Yes**.

</td></tr><tr><td>

CI conflict check mode. Basic mode only checks the change requests CI. Advanced mode checks the entire Affected CIs related list \(the change's CI will be automatically added to the related list\)

</td><td>

**change.conflict.mode**

</td><td>

To check the conflict mode for a CI, select the appropriate CI conflict mode.-   **Basic**: When selected, checks only change requests of the CI against the change request for the CI and all affected CIs.
-   **Advanced**: When enabled, checks both the CI for the current change request and affected CIs against other change requests for the CI and affected CIs.

</td></tr><tr><td>

Run conflict detection automatically after changes to Configuration item, Planned start date, Planned end date or State when a change request is updated

</td><td>

**change.conflict.refresh.conflicts**

</td><td>

To refresh and run conflict detection automatically when any of the following field values are changed, select **Yes**.-   **Configuration item**
-   **Planned start date**
-   **Planned end date**

</td></tr><tr><td>

Enable the scheduled change conflict checker

</td><td>

**change.conflict.refresh.scheduled**

</td><td>

To enable the schedule change conflict checker, select **Yes**.

</td></tr><tr><td>

Automatically include business or application services related to CIs with conflicts in the Impacted CI related list

</td><td>

**change.conflict.populateimpactedcis**

</td><td>

To automatically include and list all the business and application services with related CIs that have conflicts, select **Yes**.

</td></tr><tr><td>

Identify the most critical business or application service affected when a conflict is detected against a supporting configuration item

</td><td>

**change.conflict.identifymostcritical**

</td><td>

To identify the most affected business or application services that have a related conflicting CI, select **Yes**.

</td></tr><tr><td>

Define the number of days to be factored after the respective Planned start/end date of a Change record when searching for the next available time. This window is used to find all potentially conflicting Changes, the larger the window, the more Changes that need to be factored per search. Default value is 90 days; the value must be a positive integer.

</td><td>

**change.conflict.next\_available.schedule\_window**

</td><td>

To factor from the scheduled planned start date or end date of the change request to find the next available time, enter the number of days. -   Type: Integer
-   The default value is **90**

</td></tr><tr><td>

Define the number of suggestions to be calculated for the next available time field on a Change. The greater the value, the more time taken to calculate the next available times to implement the change. Default value is 100 suggestions; the value must be a positive integer.

</td><td>

**change.conflict.next\_available.choice\_limit**

</td><td>

Enter the number of suggestions to calculate and display for the next available time.-   Type: Integer
-   The default value is **100**

</td></tr><tr><td>

Logging level for ChangeCheckConflict \(default: Notice\)

</td><td>

**change.conflict.log**

</td><td>

Select any of the logging levels for the change conflict.-   **Emergency**
-   **Alert**
-   **Critical**
-   **Error**
-   **Warning**
-   **Notice**
-   **Info**
-   **Debug**

 The default level is **Notice**.

</td></tr><tr><td>

Handle contiguous change request that has overlapping schedules that results in conflicts.

</td><td>

**change.conflict.allow\_contiguous\_changes**

</td><td>

This property is enabled by default.

</td></tr><tr><td>

Show message when scheduling conflict is detected.

</td><td>

**change.conflict.show\_conflict\_message**

</td><td>

Shows a message when scheduling conflict is detected. Choose any of the given options to configure the display of the conflict message. -   **User Preference**: Displays a UI menu option where the user can toggle to show or hide the conflict message.
-   **Always**: Always displays the conflict message.
-   **Never**: The conflict message is not displayed unless the property is changed to either **User Preference** or **Always**.

By default, **User Preference** is selected.

</td></tr><tr><td>

Consolidate conflicts so a conflict is only registered for each unique combination of conflict type and schedule or conflicting-change.

</td><td>

change.conflict.consolidated\_conflicts

</td><td>

Displays only the conflicts that results from a unique combination of the conflict type and schedule or conflict type and conflicting-change. By default, the property is enabled.

</td></tr></tbody>
</table>