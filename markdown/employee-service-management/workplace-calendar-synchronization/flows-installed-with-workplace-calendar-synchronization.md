---
title: Flows installed with Workplace Calendar Synchronization
description: Below are the flows that run on different timelines.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workplace Calendar Synchronization references, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Flows installed with Workplace Calendar Synchronization

Below are the flows that run on different timelines.

|Flow|Scope|Active|Time|Description|
|----|-----|------|----|-----------|
|Sync reservation paths from Reservable module configuration flow|Workplace Reservation Management|True|Daily|This flow checks the current Reservable module configuration of Reservation paths and synchronizes it with the Reservation path records.|
|Process reservations stuck in sync required|Workplace Calendar Synchronization|True|Repeats every 15 minutes|This flow triggers synchronization for reservations that have been waiting for a third party data for more than 15 minutes \(for example Virtual Meeting details\) before triggering a sync call to the calendar.|
|Renew Subscriptions|Microsoft Exchange Online Spoke|True|Daily|This flow retrieves all the subscription records and renews them if renewal is required, based on their expiration time. If a subscription is marked with status as Being deleted, then the record is deleted and is not considered for renewal.|

**Parent Topic:**[Workplace Calendar Synchronization references](../concept/workplace-calendar-sync-references.md)

**Related topics**  


[Components installed with Workplace Calendar Synchronization](components-installed-with-workplace-calendar-syncn.md)

[Properties installed with Workplace Calendar Synchronization](properties-installed-with-workplace-calendar-syncn.md)

[Scheduled jobs installed with Workplace Calendar Synchronization](scheduled-jobs-installed-with-workplace-calendar-synchronization.md)

[Instance scan findings](sacn-finding-messages.md)

