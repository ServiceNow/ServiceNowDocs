---
title: Add a business rule for a new Order Management event
description: Learn how to configure business rules on a ServiceNow instance to recognize new Order Management events and push them into the notification system.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Add a business rule for a new Order Management event

Learn how to configure business rules on a ServiceNow® instance to recognize new Order Management events and push them into the notification system.

When you want ServiceNow® to notify external systems about a new type of order event, you must create a business rule. The business rule captures the event \(like creating a new order\) and pushes a snapshot of the order record into the Inbound Queue \[sn\_tmt\_core\_inbound\_queue\] table. The Producer Notification Framework then processes this queue and sends out the appropriate notification. You need to specify the event type in your business rule code \(event must be unique\).

## Supported business rules

The following business rules supported for Order Management notifications.

Product Order Management:

1.  Trigger Cancel ProductOrder Create Event
2.  Trigger cancelProductOrderStateChange
3.  Trigger Product Order Create Event
4.  Trigger Product Order Delete Event
5.  Trigger product order jeopardy event
6.  Trigger Product Order State Change Event

Service Order Management:

1.  Trigger Cancel Service Order Event
2.  Trigger cancelServiceOrderStateChange
3.  Trigger Service Order Create Event
4.  Trigger Service Order Delete Event
5.  Trigger service order jeopardy event
6.  Trigger Service Order State Change Event

## Example

The following code example adds a business rule for processing the ProductOrderCreateEvent order notification event on the Customer Order \[sn\_ind\_tmt\_orm\_order\] table. When calling the pushEventsToQueue\(\) method to push the event onto the inbound queue, you must pass the event type. The example below uses the ProductOrderCreateEvent event type. This event type can be any alphanumeric value that you want, but it must be unique because it is used by the system to determine how to process the order management event. The list of event types for the base system are defined in the Constants.EVENT\_TYPES object in the Constants \[sn\_api\_notif\_mgmt.Constants\] script include.

```
// Add following lines of code in script section (Advanced tab) of BR for pushing ‘ProductOrderCreateEvent’ to the inbound queue.
(function executeRule(current, previous /*null when async*/ ) { 

// Note that event needs to be passed at BR level itself as after this step, we would be left with glide snapshot only. 
new OrderNotificationUtilOOB().pushEventsToQueue(current, sn_api_notif_mgmt.Constants.EVENT_TYPES.PRODUCT_ORDER_CREATE);

})(current, previous)
```

