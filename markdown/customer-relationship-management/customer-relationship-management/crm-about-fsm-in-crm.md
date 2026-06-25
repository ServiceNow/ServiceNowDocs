---
title: Field Service Management
description: Field Service Management \(FSM\) is the part of the CRM solution that extends service delivery into the field, ensuring that when a customer problem requires physical intervention, it flows seamlessly from the service record rather than becoming a disconnected activity.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 1
---

# Field Service Management

Field Service Management \(FSM\) is the part of the CRM solution that extends service delivery into the field, ensuring that when a customer problem requires physical intervention, it flows seamlessly from the service record rather than becoming a disconnected activity.

## Role of FSM in CRM

FSM closes the loop between a customer case and an on-site resolution. When a service agent in CSM determines that field work is needed, a work order can be created directly from the case and dispatched to a technician, carrying the customer's account, asset, and service history with it. The technician arrives informed, completes the work using the guidance of playbooks, and the case is updated automatically when the work order is closed.

FSM also supports order fulfillment within CRM. When a Sales CRM order requires on-site installation or configuration, FSM receives the work order from the fulfillment workflow and dispatches the appropriate technician.

## FSM across the CRM portfolio

|Connection|FSM role|CSM / Sales CRM role|
|----------|--------|--------------------|
|Case-driven work orders|Receives work orders created from CSM cases and assigns them to field technicians. Work order completion updates the originating case automatically.|Agents create work orders directly from a case record when on-site service is required. The case and work order remain linked throughout.|
|Shared customer data|Account, contact, and asset information from CSM is available on work orders, giving technicians customer context before arriving on site.|CSM maintains the shared customer data model. Records are available in FSM without duplication or manual transfer.|
|Order fulfillment|Receives work orders from Sales CRM fulfillment workflows when an order requires on-site installation or configuration.|Sales CRM triggers work order creation in FSM for applicable order types. Fulfillment status in Sales CRM reflects the outcome of the field work.|

