---
title: Data model for denormalized tables in Field Service Management
description: Use the table below to reference the Field Service Management weekly resource span denormalized table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/field-service-management/flat-table-model.html
release: yokohama
product: Field Service Management
classification: field-service-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Field Service Management reference, Field Service Management]
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

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/field-service-management/fsm-reference.md)

