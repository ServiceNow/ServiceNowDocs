---
title: Field service holiday schedules
description: Location-based holiday calendars map holidays to specific regions so managers and dispatchers can plan shifts accurately and reduce manual scheduling adjustments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/workforce-optimization-for-field-service/fsm-holiday-schedule.html
release: australia
product: Workforce Optimization for Field Service
classification: workforce-optimization-for-field-service
topic_type: concept
last_updated: "2026-05-27"
reading_time_minutes: 2
keywords: [holiday schedule, field service, workforce management, dispatcher workspace, location-based calendar]
breadcrumb: [Configuring an agent calendar, Set up workforce, Configure, Field Service Management]
---

# Field service holiday schedules

Location-based holiday calendars map holidays to specific regions so managers and dispatchers can plan shifts accurately and reduce manual scheduling adjustments.

Field service teams often operate across multiple regions where holidays differ by country or location. Without location-aware scheduling, managers must manually adjust shifts when holidays occur, which can lead to scheduling conflicts, coverage gaps, and additional administrative overhead. Location-based holiday calendar management addresses this by associating holiday schedules with specific locations so that holidays are automatically reflected in workforce planning tools.

Administrators create and maintain location schedules that define individual holidays by date and recurrence. The time zone can be set to a fixed value such as US/Pacific, which applies a consistent holiday time to all technicians tied to that schedule, or to a floating value, which automatically converts holiday dates to each technician's local time zone. A scheduled job runs daily to map holidays to technicians based on the location assigned to them on their user record.

## Holiday visibility in Dispatcher Workspace

In Dispatcher Workspace, holidays appear as labeled blocks on the scheduling calendar for each technician row, giving dispatchers immediate visibility into which technicians are on holiday on a given day. Dispatchers can identify coverage gaps and make informed dispatching decisions. When a location-level schedule is deleted, holiday assignments are automatically removed from affected technicians, keeping scheduling data accurate.

## Holiday visibility in Manager Workforce

In Manager Workforce, holidays are visible across the team calendar and the Shifts tab in day, week, and month views. Managers can select any holiday block to view additional details about the holiday event. When a manager creates a shift, edits an existing shift, or initiates a shift swap that falls on a holiday date, a conflict warning appears. This conflict detection reduces scheduling errors. In cases where a shift must proceed despite a holiday, managers can override the conflict. If permitted by the event configuration, managers can also delete a holiday assignment for a specific technician to handle exceptions.

## Related information

Holiday schedules use the platform's scheduling framework, which supports parent-child schedule relationships, domain separation, and reusable holiday entries. For background on how individual holidays are defined as schedule entries and how holiday schedules can be nested within work schedules, see [Holidays](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_Holidays.md). For guidance on structuring schedules across multiple regions that share the same working hours but observe different holidays, see [Create a holiday schedule for multiple regions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateAHolidaySchedMultiRegions.md).

Customer Service Management \(CSM\) holiday calendar support functions the same way that Field Service Management holiday calendar support does. The CSM implementation covers the full setup workflow for location schedules, time zone configuration, floating time zone behavior, and holiday visibility across team and personal technician calendars. For complete configuration details, see [Location Based Holiday Calendar Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/location-based-holiday-calendar-management.md).

**Related topics**  


[Configuring Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/configuring-dispatcher-workspace.md)

[Setting up your workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/workforce-optimization-for-field-service/setting-up-workforce.md)

