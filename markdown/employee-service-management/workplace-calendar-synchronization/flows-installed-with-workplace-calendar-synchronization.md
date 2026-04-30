---
title: Flows installed with Workplace Calendar Synchronization
description: Below are the flows that run on different timelines.
locale: en-US
release: yokohama
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Flows installed with Workplace Calendar Synchronization

Below are the flows that run on different timelines.

|Flow|Scope|Active|Time|Description|
|----|-----|------|----|-----------|
|Sync reservation paths from Reservable module configuration flow|Workplace Reservation Management|True|Daily|This flow checks the current Reservable module configuration of Reservation paths and synchronizes it with the Reservation path records.|
|Process reservations stuck in sync required|Workplace Calendar Synchronization|True|Repeats every 15 minutes|This flow triggers synchronization for reservations that have been waiting for a third party data for more than 15 minutes \(for example Virtual Meeting details\) before triggering a sync call to the calendar.|
|Renew Subscriptions|Microsoft Exchange Online Spoke|True|Daily|This flow retrieves all the subscription records and renews them if renewal is required, based on their expiration time. If a subscription is marked with status as Being deleted, then the record is deleted and is not considered for renewal.|

