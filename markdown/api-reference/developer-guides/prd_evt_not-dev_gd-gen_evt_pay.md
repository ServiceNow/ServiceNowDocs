---
title: Generate the payload for a new trouble ticket event
description: When adding a trouble ticket event to your implementation, you must create a function that generates the required TMF-compliant payload for that event type. In addition, you must add that function to the case statement that directs the logic to this function when processing this type of event record.
locale: en-US
release: australia
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure trouble ticket notifications using the Producer Event Notification Framework, Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Generate the payload for a new trouble ticket event

When adding a trouble ticket event to your implementation, you must create a function that generates the required TMF-compliant payload for that event type. In addition, you must add that function to the case statement that directs the logic to this function when processing this type of event record.

## Create a method that generates the payload for the new trouble ticket event

In the `TroubleTicketNotificationUtil` script include, you must add a method that constructs the required TMF-compliant payload for the new trouble ticket event and then return that payload.

For examples of methods that create payloads for the base system trouble ticket events, refer to the following methods in the [`TroubleTicketNotificationUtilOOB`](../../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#) script include:

-   [generateCreateTroubleTicketEventPaylaod\(\)](../../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#)
-   [generateCreateTroubleTicketEventPaylaodForCase\(\)](../../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#)
-   [generateTroubleTicketAttributeChangePayload\(\)](../../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#)
-   [generateTroubleTicketStatusChangePayload\(\)](../../../../app-store/dev_portal/API_reference/TroubleTicketNotificationUtilOOB/concept/TroubleTicketNotifScopedAPI.md#)

## Add the event to the fetchEventHandlerAndCreateTMFEvent\(\) switch/case logic

For the function that you created to be executed, you must add it in the `switch/case` logic within the fetchEventHandlerAndCreateTMFEvent\(\) method of the `EventProcessorUtil` script include. The following code snippet shows the updates necessary to add the `ResolveTroubleTicketEventForIncident` event type to this method. For details on the fetchEventHandlerAndCreateTMFEvent\(\) method, see [EventProcessorUtilOOB - fetchEventHandlerAndCreateTMFEvent\(Object eventSnapshot, String eventType, String eventId\)](../../../../app-store/dev_portal/API_reference/EventProcessorUtilOOB/concept/EventProcessorUtilOOBScopedAPI.md#).

```
fetchEventHandlerAndCreateTMFEvent: function(eventSnapshot, eventType, eventId) {
  var eventPayload;
  switch (eventType) {
    case Constants.EVENT_TYPES.TROUBLE_TICKET_STATUS_CHANGE:
      eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateTroubleTicketStatusChangePayload(eventSnapshot, eventType, eventId);
      break;

    case Constants.EVENT_TYPES.TROUBLE_TICKET_CREATE:
      eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateCreateTroubleTicketEventPaylaod(eventSnapshot, eventType, eventId);
      break;

    case Constants.EVENT_TYPES.TROUBLE_TICKET_ATTRIBUTE_CHANGE:
      eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateTroubleTicketAttributeChangePayload(eventSnapshot, eventType, eventId);
      break;

    case Constants.EVENT_TYPES.TROUBLE_TICKET_CREATE_FOR_CASE:
      eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateCreateTroubleTicketEventPaylaodForCase(eventSnapshot, eventType, eventId);
      break;

    // Add a new case statement for the ResolveTroubleTicketEventForIncident event type
    case 'ResolveTroubleTicketEventForIncident':
      eventPayload = new sn_ind_tsm_sdwan.TroubleTicketNotificationUtil().generateResolveTroubleTicketEventPyaload(eventSnapshot, eventType, eventId);
      break;

    default:
      this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
      eventPayload = null;
  }
  return eventPayload;
},
```

