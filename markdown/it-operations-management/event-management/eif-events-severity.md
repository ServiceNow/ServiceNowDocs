---
title: EIF events warning severity
description: If the EIF event payload has a warning severity, it will be mapped differently in the ServiceNow instance.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integrate Event Integration \(EIF\) format event connector, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# EIF events warning severity

If the EIF event payload has a warning severity, it will be mapped differently in the ServiceNow instance.

|EIF events severity|ServiceNow events severity mapping|
|-------------------|----------------------------------|
|UNKNOWN|Warning|
|Warning|Minor|
|Minor|Major|
|Critical|Critical|
|Fatal|Critical|

**Parent Topic:**[Integrate Event Integration \(EIF\) format event connector](../task/eif-events-integration.md)

