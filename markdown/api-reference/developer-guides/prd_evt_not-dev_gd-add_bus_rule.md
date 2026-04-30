---
title: Add a business rule for a new trouble ticket event
description: When adding a new trouble ticket event to your implementation, you must add a business rule to your ServiceNow instance.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure trouble ticket notifications using the Producer Event Notification Framework, Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Add a business rule for a new trouble ticket event

When adding a new trouble ticket event to your implementation, you must add a business rule to your ServiceNow instance.

This business rule must push the Glide snapshot of the corresponding incident or case record into the Producer Notification Framework inbound queue, Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table, where it is then processed and published by the Producer Notification Framework.

The following code snippet shows an example of a business rule for processing the `ResolveTroubleTicketEventForIncident` ticket notification event on the Incident \[incident\] table. When calling the pushEventsToQueue\(\) method to push the event onto the inbound queue, you must pass the event type. For this example it is `ResolveTroubleTicketEventForIncident`. This event type can be any alphanumeric value that you want, but it must be unique as it is used by the system to determine how to process the trouble ticket event. The list of event types for the base system are defined in the **Constants.EVENT\_TYPES** object in the `Constants [sn_api_notif_mgmt.Constants]` script include.

For details on creating a business rule, see [Create a business rule for your service](https://www.servicenow.com/docs/access?context=ur-create-busrule-service&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

```
// Add following lines of code in script section (Advanced tab) of BR for pushing ‘ResolveTroubleTicketEventForIncident’ to the inbound queue.

(function executeRule(current, previous /*null when async*/ ) {

// Note that event needs to be passed at BR level itself as after this step, we would be left with glide snapshot only

new TroubleTicketNotificationUtil().pushEventsToQueue(current,'ResolveTroubleTicketEventForIncident', Constants.TROUBLE_TICKET_TYPE.INCIDENT);

})(current, previous)
```

