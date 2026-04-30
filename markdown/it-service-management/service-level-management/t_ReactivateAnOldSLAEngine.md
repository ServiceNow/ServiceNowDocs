---
title: Reactivate escalation engine
description: Escalation engine is replaced with 2011 SLA Engine.
locale: en-US
release: zurich
product: Service Level Management
classification: service-level-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Level Agreement \(Legacy\) engines, Reference, Service Level Management, IT Service Management]
---

# Reactivate escalation engine

Escalation engine is replaced with 2011 SLA Engine.

## Before you begin

Role required: admin

## About this task

ServiceNow Express used the legacy Escalation Engine to process SLAs. If for any reason a customer who has upgraded from ServiceNow Express to ServiceNow Enterprise wants to reactivate the Escalation engine, they can follow the steps below.

## Procedure

1.  Navigate to sys\_properties.list.

2.  Update the property **com.snc.sla.run\_old\_sla\_engine** to `true`.

    **Note:**

    ServiceNow recommends using the 2011 SLA Engine.


**Parent Topic:**[Service Level Agreement \(Legacy\) engines](../concept/c_GetStartedWithSLAs.md)

