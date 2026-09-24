---
title: Create a change lockdown
description: Create a change lockdown to pause in-flight change requests during major unplanned IT, critical, or financial events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/create-change-lockdown.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [change lockdown, create lockdown, schedule entry]
breadcrumb: [Change lockdown, Configure, Change Management, IT Service Management]
---

# Create a change lockdown

Create a change lockdown to pause in-flight change requests during major unplanned IT, critical, or financial events.

## Before you begin

Role required: `change_manager`

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Administration** &gt; **Change Lockdown**.

    The list shows the existing lockdown records with their name, type, time zone, and the date on which each record was updated.

2.  Select **New**.

3.  Fill in the fields on the **Change Lockdown** form, as described in the following table.

    **Note:** The **CI Condition** tab appears only when you select the **Filter by CI** check box. If you clear the check box, the lockdown applies to all change requests that match the **Change Request Condition** field.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a name for the change lockdown.|
    |**Description**|Enter the purpose of the change lockdown.|
    |**Time zone**|Select the time zone that the lockdown schedule uses. The default value is **-- Floating --**.|
    |**Filter by CI**|Select this check box to limit the lockdown to specific configuration items \(CIs\). The **CI Condition** tab appears when you select this check box.|
    |**Source**|Select the method that identifies the CIs, such as **CI Class**.|
    |**Applies to** \(**CI Condition** tab\)|Select the table that the **Condition** field filters. The default value is `Configuration Item [cmdb_ci]`. This field is available only when you select the **Filter by CI** check box.|
    |**Condition** \(**CI Condition** tab\)|Add the conditions that filter the records in the table that you select in the **Applies to** field. This field is available only when you select the **Filter by CI** check box.|
    |**Change Request Condition** \(**Change Condition** tab\)|Add the conditions that select the change requests to place on hold.|
    |**Assignment group**|Select the group that receives the lockdown approval.|
    |**Assigned to**|Select the user who receives the lockdown approval.|
    |**State**|Displays the state of the change lockdown. A new change lockdown starts in the **Draft** state. This field is read-only.|

4.  Select **Submit**.

    The record indicates that the schedule has no schedule entry. A change lockdown takes effect only after you add a schedule entry.

5.  On the **Schedule Entries** tab, select **New** and then define the period that the lockdown covers.

    A schedule entry sets values such as **All day**, **Repeat on**, and **End date time**.


## What to do next

After the schedule entry is saved, the **Preview** button becomes available. Preview the affected change requests before you request approval. For more information, see [Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md).

**Parent Topic:**[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

**Related topics**  


[Change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-lockdown.md)

[Manage a change lockdown](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/manage-change-lockdown.md)

