---
title: Data model for denormalized tables in Field Service Management
description: Use the table below to reference the Field Service Management weekly resource span denormalized table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/field-service-management/flat-table-model.html
release: zurich
product: Field Service Management
classification: field-service-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Field Service Management]
---

# Data model for denormalized tables in Field Service Management

Use the table below to reference the Field Service Management weekly resource span denormalized table.

|wm\_weekly\_resource\_span|
|--------------------------|
|Resource type|Choice|User/Crew/Equipmen/Schedule|
|Resource id|String \(size of 40\)| |
|Weekly start|Date/Time|Week starts at 12:00AM UTC|
|Weekly end|Date/Time|Week ends at Saturday 23:59:59PM UTC|
|Span Time zone|String \(size of 40\)| |
|Spans|JSON|List of weekly schedule and event spans|
|Domain|Domain id| |

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/field-service-management/fsm-reference.md)

