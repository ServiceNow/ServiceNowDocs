---
title: Task template group form
description: Use the Task template group form to bundle related task templates and define dependencies between them. Apply the group from a plan, loss scenario, recovery strategy, exercise event, crisis event, or activated plan to create the underlying tasks in bulk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/task-template-group-form.html
release: australia
topic_type: reference
last_updated: "2026-05-16"
reading_time_minutes: 1
breadcrumb: [Configure Task templates and Task template groups, Configuring plan template, Setup for a BCP, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Task template group form

Use the Task template group form to bundle related task templates and define dependencies between them. Apply the group from a plan, loss scenario, recovery strategy, exercise event, crisis event, or activated plan to create the underlying tasks in bulk.

## Task template group form

\[Omitted image "task-template-groups-list.png"\] Alt text: Task template groups list showing Applicable to element definitions and Active columns.

For description of the field values, see the table.

|Field|Description|
|-----|-----------|
|Name|Unique name for the group. Names are case-insensitive and unique across the instance.|
|Description|Description shown in the **Select task template groups** dialog.|
|Active|When false, the group is hidden from every **Add groups** dialog.|
|Applicable to element definitions|**All element definitions** or **Specific element definitions**.|
|Element definitions|Visible only when **Applicable to element definitions** is set to **Specific element definitions**. Lists the element definitions the group applies to \(for example, Business services, Linux servers, Data centers\).|

## Related lists

|Related list|Description|
|------------|-----------|
|Task templates|Task templates that belong to the group. Use the **Dependencies** column to define order between tasks in the group.|
|Plan templates|Plan templates that include the group.|
|Loss scenarios|Loss scenarios that include the group.|
|Recovery strategies|Recovery strategies that include the group.|

**Parent Topic:**[Configure Task templates and Task template groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/create-task-temp-temp-groups.md)

