---
title: Detect change conflicts
description: Detect change conflicts by setting Change Management conflict analysis properties. Use the resulting information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.Conflict detection includes properties that determine how the conflict detection capability is executed.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Detect change conflicts

Detect change conflicts by setting Change Management conflict analysis properties. Use the resulting information to calculate conflicts for change requests and review and modify the change to eliminate conflicts.

## Before you begin

Role required: admin

## About this task

By default, not all properties are selected in the Change Management Conflict Analysis Properties page. Modify or customize conflict detection capabilities to meet the needs of your organization.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Conflict Properties**.

2.  In the Change Management Conflict analysis properties page, enter the roles that have access to the conflict detection feature.

3.  Configure the remaining customization properties.

    For more information on conflict detection properties, see [Conflict detection properties](configure-conflict-properties.md#).

4.  Select **Save**.


**Parent Topic:**[Conflict detection](../concept/c_ConflictDetection.md)

**Related topics**  


[Create blackout and maintenance schedules in Change Management](t_CreateBlkoutMaintSched.md)

[Configure a change request to monitor outside maintenance schedule conflicts](monitor-maintenance-schedule.md)

[Conflict calendar](../concept/change-conflict-calendar.md)

[Enable automatic change conflict detection](t_RunAutomatedConflictDetection.md)

[Detect conflicts manually and review conflict details](t_RunManualConflictDetection.md#)

## Conflict detection properties

Conflict detection includes properties that determine how the conflict detection capability is executed.

Initiate properties without other settings by setting the value to Yes.

**Note:** You can determine the mechanism for conflict detection. You can choose between the Flow and Progress Worker options by updating the **change.conflict.useprogressworker** system property. It is set to false by default.

<table id="table_pdf_gy2_3fb"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**change.conflict.role**

</td><td>

A comma-separated list of roles that have access to the conflict detection feature. Roles included here should have access to the underlying change\_request record. Roles are entered exactly as they appear in **User Administration** &gt; **Roles**. For example, itil.

</td></tr><tr><td>

**change.conflict.blackout**

</td><td>

Checks whether the change request falls within the blackout window.

</td></tr><tr><td>

**change.conflict.relatedchildblackout**

</td><td>

Checks whether the change request of any of the child configuration items \(CIs\) falls within the blackout window.

</td></tr><tr><td>

**change.conflict.relatedparentblackout**

</td><td>

Checks whether the change request of the parent CI falls within the blackout window.

</td></tr><tr><td>

**change.conflict.currentci**

</td><td>

Checks whether the change request is already scheduled against the given CI.

</td></tr><tr><td>

**change.conflict.currentwindow**

</td><td>

Checks whether the change request of the CI falls within the maintenance window.

</td></tr><tr><td>

**change.conflict.relatedchildwindow**

</td><td>

Checks whether the change request of any of the child CIs falls within the maintenance window.

</td></tr><tr><td>

**change.conflict.relatedparentwindow**

</td><td>

Checks whether the change request of the parent CI falls within the maintenance window.

</td></tr><tr><td>

**change.conflict.ci\_maint\_sched**

</td><td>

Checks whether the change request falls within the scheduled maintenance defined for the CI in the maintenance schedule reference field.

</td></tr><tr><td>

**change.conflict.relatedservices**

</td><td>

Checks whether a change request that falls within the maintenance or blackout windows affects other related application services, such as the services created that include the CI scheduled for change or any other CI within that service.**Note:** This action requires any business services identified to be converted to an application service. For more information, see [Convert business services to application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/convert-bus-to-app-svc-intro.md). For information about application services, see [Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md) [Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/application-services.md).

</td></tr><tr><td>

**change.conflict.assigned\_to**

</td><td>

Checks whether any other change request is assigned to the same change request assigned to a user. For example, if you assign a change request to a user who is already scheduled to implement another change request at that date and time, a conflict error will be displayed.

</td></tr><tr><td>

**change.conflict.mode**

</td><td>

Determines the conflict mode for a CI. The available values are:-   Basic: Checks only change requests of the CI against the change request for the CI and all affected CIs.
-   Advanced: Checks both the CI for the current change request and affected CIs against other change requests for the CI and affected CIs.

</td></tr><tr><td>

**change.conflict.refresh.conflicts**

</td><td>

Refreshes and run conflict detection automatically when any of the following field values are changed:-   Configuration item
-   Planned start date
-   Planned end date

</td></tr><tr><td>

**change.conflict.populateimpactedcis**

</td><td>

Automatically includes and lists all the business and application services with related CIs that have conflicts.

</td></tr><tr><td>

**change.conflict.identifymostcritical**

</td><td>

Identifies the most affected business or application services that have a related conflicting CI.

</td></tr><tr><td>

**change.conflict.next\_available.schedule\_window**

</td><td>

Factors from the scheduled planned start date or end date of the change request to find the next available time, enter the number of days. -   Type: Integer
-   The default value is 90.

</td></tr><tr><td>

**change.conflict.next\_available.choice\_limit**

</td><td>

The number of suggestions to calculate and display for the next available time. The greater the value, the more time taken to calculate the next available times to implement the change.-   Type: Integer
-   The default value is 100.

</td></tr><tr><td>

**change.conflict.log**

</td><td>

The logging levels for change conflicts: The available options are:-   Emergency
-   Alert
-   Critical
-   Error
-   Warning
-   Notice
-   Info
-   Debug

 The default level is Notice.

</td></tr><tr><td>

**change.conflict.show\_conflict\_message**

</td><td>

Determines whether or when a message is displayed when a scheduling conflict is detected. The available options are: -   **User Preference**: The user can select whether to show or hide the conflict message through a UI menu option.
-   **Always**: Always displays the conflict message.
-   **Never**: Conflict messages are not displayed.

By default, **User Preference** is selected.

</td></tr><tr><td>

**change.conflict.allow\_contiguous\_changes**

</td><td>

Handles contiguous change requests with overlapping schedules. This property is active by default.

</td></tr><tr><td>

**change.conflict.consolidated\_conflicts**

</td><td>

Displays only conflicts that result from a combination of the conflict type and schedule or conflict type and conflicting change. This property is active by default.

</td></tr><tr><td>

**change.conflict.max\_count**

</td><td>

The maximum number of conflict records that can be generated for each conflict type when conflict detection runs. Create this system property if it is not already present.-   Type: Integer
-   The minimum value is 1000. If you set a lesser number, 1000 is displayed as the default value.

</td></tr></tbody>
</table>