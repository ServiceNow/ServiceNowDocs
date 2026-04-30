---
title: Modify a trouble ticket event payload
description: The base trouble ticket event notification implementation provides multiple default trouble ticket event type examples. You may need to alter the payloads for these events within your implementation to meet your actual needs. You may also need to configure the payload for any new trouble ticket events that you add to your implementation.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure trouble ticket notifications using the Producer Event Notification Framework, Producer Event Notification Framework developer guide, Developer guides, API implementation and reference]
---

# Modify a trouble ticket event payload

The base trouble ticket event notification implementation provides multiple default trouble ticket event type examples. You may need to alter the payloads for these events within your implementation to meet your actual needs. You may also need to configure the payload for any new trouble ticket events that you add to your implementation.

This section describes how to modify the payload for the "Attribute change event for Incident" trouble ticket event. Use these same steps to modify the payload of any trouble ticket event type.

## Add event header attributes to all trouble ticket event payloads

To add event header attributes to all trouble ticket event payloads, you must override the addAdditionalEventAttributes\(\) method in the `TroubleTicketNotificationUtil` script include. Adding new attributes in this method adds header-level attributes to all trouble ticket event payloads.

The following code example shows how to add the attribute `schemaLocation` to all trouble ticket event payloads.

```
addAdditionalEventAttributes’: function(tmfEventPayload) {
  // Add "schemaLocation" as a header attribute
  TroubleTicketEventObject.schemaLocation = "http://xx/Event.schema.json",
}
```

## Add attributes to a specific trouble ticket event payload

To add attributes to a specific trouble ticket event payload, you must override the method associated with that event such as the addAttributeChangeTroubleTicketAttributes\(\) method in the `TroubleTicketNotificationUtil` script include. Adding new attributes in this method adds event-level attributes to that specific trouble ticket event payload.

The following code example shows how to add the attribute `correlationId` to the "Attribute change event for Incident" trouble ticket event.

```
addAttributeChangeTroubleTicketAttributes: function(troubleTicketGr) {
  var troubleTicketResource = {};
  var troubleTicketAttributesObj = {};
  this.addMandatoryTroubleTicketAttributes(troubleTicketAttributesObj, troubleTicketGr);

// Add the new attribute correlation id.
  TroubleTicketAttributesObj.correlationId = troubleTicketGr._value.correlation_id;
  troubleTicketResource.troubleTicket = troubleTicketAttributesObj;
  return troubleTicketResource;
},
```

