---
title: Configure a change request to monitor outside maintenance schedule conflicts
description: Configure a change request to detect conflicts outside the maintenance window. Conflict detection flags planned start and end dates that fall outside the maintenance schedule, so you can modify the change schedule accordingly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/monitor-maintenance-schedule.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Configure a change request to monitor outside maintenance schedule conflicts

Configure a change request to detect conflicts outside the maintenance window. Conflict detection flags planned start and end dates that fall outside the maintenance schedule, so you can modify the change schedule accordingly.

## Before you begin

Role required: personalize\_ui or admin

## About this task

The **Outside maintenance schedule** check box is informational. The instance sets its value and disregards any changes that you make to it. The check box is selected automatically when either of the following occurs:

-   The planned start and end dates in the change request with an associated CI are outside the maintenance schedule.
-   Affected CIs associated with the change request are checked against their assigned maintenance schedules, if any.

**Note:** Only the maintenance window for the primary CI or affected CIs is checked; the upstream and downstream items are not checked.

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Open** and select an existing change request.

2.  If the **Outside maintenance schedule** field does not appear, add the field to the form.

    1.  Select the form context menu icon, and then select **Additional actions** &gt; **Configure** &gt; **Form Layout**.

    2.  Move **Outside maintenance schedule** to the Selected list.

    3.  Select **Save**.


## Result

When you save a change request that is outside the maintenance schedule, a warning appears for each item \(primary or affected\). This warning also displays the planned dates that fall outside the maintenance window.

**Parent Topic:**[Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts]()

[Create blackout and maintenance schedules in Change Management]()

[Schedule types in conflict detection]()

[Conflict calendar]()

[Enable automatic change conflict detection]()

[Detect conflicts manually and review conflict details]()

