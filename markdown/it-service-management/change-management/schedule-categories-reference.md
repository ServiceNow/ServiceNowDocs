---
title: Schedule categories
description: Maintenance, blackout, and information schedules each have their own set of categories that describe the purpose of the schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/schedule-categories-reference.html
release: australia
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2026-10-14"
reading_time_minutes: 1
keywords: [schedule category, hard freeze, soft freeze, information schedule]
breadcrumb: [Schedule types in conflict detection, Conflict detection, Configure, Change Management, IT Service Management]
---

# Schedule categories

Maintenance, blackout, and information schedules each have their own set of categories that describe the purpose of the schedule.

Select a category in the **Category** field of a schedule. The field is empty by default, and the category is stored only after you select a value and save the schedule.

<table id="table-schedule-categories"><thead><tr><th>

Schedule type

</th><th>

Categories

</th></tr></thead><tbody><tr><td>

Maintenance schedule

</td><td>

-   Preventive \(measures to improve resilience\)
-   Patching
-   General

</td></tr><tr><td>

Blackout schedule

</td><td>

-   Hard Freeze: A total prohibition on code deployments or infrastructure changes.
-   Soft Freeze: A voluntary restriction where nonessential changes are prohibited, but exceptions are allowed for critical defect fixes and security patches.

</td></tr><tr><td>

Information schedule

</td><td>

-   Holiday
-   Global event
-   Organisational event

</td></tr></tbody>
</table>## Categories in conflict records

When conflict detection generates a conflict record for a maintenance or blackout schedule, the conflict record includes the category of that schedule. Information schedules don't generate conflict records.

**Parent Topic:**[Schedule types in conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-types-conflict-detection.md)

**Related topics**  


[Schedule types in conflict detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/schedule-types-conflict-detection.md)

[Create an information schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/create-information-schedule.md)

