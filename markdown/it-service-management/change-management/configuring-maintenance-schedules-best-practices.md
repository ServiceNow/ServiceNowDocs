---
title: Configuring maintenance schedules - Best practices
description: Maintenance schedules define the periods during which a configuration item \(CI\) or change can be implemented.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/change-management/configuring-maintenance-schedules-best-practices.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Reference, Change Management, IT Service Management]
---

# Configuring maintenance schedules - Best practices

Maintenance schedules define the periods during which a configuration item \(CI\) or change can be implemented.

These schedules are incorporated into the conflict detection process for change requests. If a change request doesn't adhere to the relevant maintenance schedule, a conflict record is generated for the change request.

You can define maintenance schedules for conflict detection in two ways:

-   [Configure maintenance schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md). The **change.conflict.currentwindow** system property turns on this method.
-   Create a maintenance schedule by using the Schedule \[cmn\_schedule\] table. The **change.conflict.ci\_maint\_sched** system property turns on this method.

    **Note:** You can configure these system properties on the Conflict Properties page.


## Maintenance schedule using schedule maintenance form

All maintenance schedules defined through this method are processed based on the condition field, which must be evaluated to determine its applicability to the change request, the primary CI, or the associated Affected CIs \(if they are executed in Advanced mode\).

Multiple maintenance schedules increase the time required to determine their relevance, and this time increases with each affected CI.

If a generic schedule is applicable to numerous CIs or change requests, define the maintenance schedule by using [Configure maintenance schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/t_CreateBlkoutMaintSched.md).

If your schedules apply to a limited number of CIs, consider creating the maintenance schedule in the Schedule \[cmn\_schedule\] table.

\[Omitted image "cmn\_schedule\_maintenance\_form.png"\] Alt text: Maintenance schedule

## Maintenance schedule using schedules table

This method is designed for cases where individual CIs or small groups of CIs must follow a specific schedule.

In such cases, the maintenance schedule should be set in the Schedule \[cmn\_schedule\] table instead of the maintenance schedule table. This approach prevents the need for conflict detection to process the schedule twice using maintenance form and the schedule table.

Unlike the maintenance schedule record, the schedule record lacks a condition or an **Applies to** field, as it is intended to be directly associated with a CI. After you define the schedule record, set the **Type** field to `maintenance` to link it to a CI. To attach this schedule to a CI, it should be referenced in the **Maintenance schedule** field on the CI record; if this field is not visible, it must be added to the form.

\[Omitted image "cmn\_schedule\_form.png"\] Alt text: Schedules table

**Parent Topic:**[Reference section for Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/change-management/reference-change-management.md)

