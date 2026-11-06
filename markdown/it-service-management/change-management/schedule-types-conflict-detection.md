---
title: Schedule types in conflict detection
description: Conflict detection uses maintenance, blackout, and information schedules to evaluate when change requests can be implemented. Each schedule type supports a category and optional ownership fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/schedule-types-conflict-detection.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-10-14"
reading_time_minutes: 4
keywords: [information schedule, schedule category, blackout schedule, maintenance schedule, schedule owner]
breadcrumb: [Conflict detection, Configure, Change Management, IT Service Management]
---

# Schedule types in conflict detection

Conflict detection uses maintenance, blackout, and information schedules to evaluate when change requests can be implemented. Each schedule type supports a category and optional ownership fields.

All three schedule types extend the Condition Schedule \[cmn\_schedule\_condition\] table, so they share the same base fields, such as **Name**, **Time zone**, **Source**, and **Condition**. For information about creating maintenance and blackout schedules, see [Create blackout and maintenance schedules in Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md).

## Schedule types

|Schedule type|Table|How conflict detection uses it|
|-------------|-----|------------------------------|
|Maintenance schedule|cmn\_schedule\_maintenance|Specifies times during which change requests should be scheduled. Conflict detection raises a conflict when a change request is outside a required maintenance window.|
|Blackout schedule|cmn\_schedule\_blackout|Specifies times during which normal change activity should not be scheduled. Conflict detection raises a conflict when a change request is inside a blackout window.|
|Information schedule|cmn\_schedule\_information|Records events that change teams should be aware of, such as holidays or organizational events. Conflict detection doesn't create conflict records for information schedules.|

## Schedule categories

Each schedule type has a **Category** field with its own set of choices. For example, a blackout schedule can be categorized as a hard freeze or a soft freeze. The **Category** field is empty by default. The category is stored only after you select a value and save the schedule.

When conflict detection generates a conflict record for a maintenance or blackout schedule, the conflict record includes the category of that schedule.

For the full list of categories, see [Schedule categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-categories-reference.md).

## Schedule ownership

You can assign an owner to any maintenance, blackout, or information schedule by using the **Assigned to** and **Assignment group** fields. You can specify a user, a group, or both. The **Assigned to** field depends on the **Assignment group** field. Users who can edit schedules can populate these fields.

## Information schedule properties

The following system properties control how conflict detection evaluates information schedules. For other conflict detection properties, see [Conflict detection properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/configure-conflict-properties.md).

|Property|Description|Default value|
|--------|-----------|-------------|
|**change.conflict.information**|Includes information windows when checking change request conflicts.|true|
|**change.conflict.relatedchildinformation**|Checks whether the change request falls within the information windows of child CIs.|false|
|**change.conflict.relatedparentinformation**|Checks whether the change request falls within the information windows of parent CIs.|false|

-   **[Create an information schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-information-schedule.md)**  
Create an information schedule to record events such as holidays or organizational events that change teams should be aware of. Conflict detection doesn't create conflict records for information schedules.
-   **[Schedule categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-categories-reference.md)**  
Maintenance, blackout, and information schedules each have their own set of categories that describe the purpose of the schedule.

**Parent Topic:**[Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_ConflictDetection.md)

**Related topics**  


[Detect change conflicts]()

[Create blackout and maintenance schedules in Change Management]()

[Configure a change request to monitor outside maintenance schedule conflicts]()

[Conflict calendar]()

[Enable automatic change conflict detection]()

[Detect conflicts manually and review conflict details]()

[Conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/c_ConflictDetection.md)

[Create an information schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-information-schedule.md)

[Create blackout and maintenance schedules in Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md)

