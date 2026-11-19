---
title: Technician preference combinations
description: Check which technician preferences work together on the same work order task \(WOT\) to avoid configuration errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/technician-preference-combinations.html
release: brazil
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 1
breadcrumb: [Schedule Optimization components, Reference, Field Service Management]
---

# Technician preference combinations

Check which technician preferences work together on the same work order task \(WOT\) to avoid configuration errors.

## Technician preferences

Technician preferences control which technicians Schedule Optimization considers when it assigns a work order task \(WOT\). You set a preference of Preferred, Secondary, Excluded, or Required for a technician on a WOT record. You can't combine every preference on the same task. The following tables show which combinations you can set for the same technician and for different technicians.

To assign technician preferences, see [Configure the policy to assign preferred technicians to tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/configure-the-policy-to-assign-preferred-technicians-to-tasks.md) and [Set technician preferences for tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/assign-preferred-agents-tasks.md).

## Preferences on the same technician

Use the following scenarios to understand which preferences you can combine when assigning them to the same technician on a single WOT.

|Scenario|Example|Allowed/Not allowed|
|--------|-------|-------------------|
|Preferred + Secondary|Alex: Preferred + Secondary|Yes|
|Same preference twice|Alex: Preferred + Preferred|No|
|Required + any other preference|Alex: Required + Preferred|No|
|Excluded + any other preference|Alex: Excluded + Secondary|No|

**Note:** Preferred and Secondary are the only preferences that you can combine for the same technician.

## Preferences on different technicians

Use the following scenarios to understand which preferences you can combine when assigning them to different technicians on the same WOT.

|Scenario|Example|Allowed/Not allowed|
|--------|-------|-------------------|
|Preferred, Secondary, or Excluded in any combination|Alex: Preferred; Jamie: Excluded|Yes|
|Required on multiple technicians|Alex: Required; Jamie: Required|Yes|
|Required + Preferred, Secondary, or Excluded|Alex: Required; Jamie: Preferred|No|

**Parent Topic:**[Schedule Optimization components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/schedule-optimization-components.md)

