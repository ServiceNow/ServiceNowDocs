---
title: TroubleTicketNotificationUtilOOB - Scoped
description: The TroubleTicketNotificationUtilOOB script include provides methods used to define and generate the TMF-compliant payloads for trouble ticket notification events.Adds custom event header attributes to the passed TMF trouble ticket event payload. The attributes added by this method are added to the event-level header for all trouble ticket events.Generates the TMF688-compliant header attributes in the event section of the payload. These attributes are consistent across all event payloads.Constructs the TMF-compliant payload for the associated create trouble ticket for incident event type.Constructs the TMF-compliant payload for the associated create trouble ticket for case event type.Constructs the TMF-compliant payload for the trouble ticket attribute change event for incident event type.Constructs the TMF-compliant payload for the associated trouble ticket status change event for incident event type.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TroubleTicketNotificationUtilOOB- Scoped

The TroubleTicketNotificationUtilOOB script include provides methods used to define and generate the TMF-compliant payloads for trouble ticket notification events.

Override the methods in this script include to:

-   Add/remove attributes to an existing trouble ticket event type.
-   Define attributes for a new trouble ticket event type.

For additional information, see [Configure trouble ticket notifications using the Producer Event Notification Framework](../../../../../integrate/guides/ProducerEventNotifFramework/concept/prd_evt_not-dev_gd-cfg_trbl_tkt_not.md).

This script include runs within the `sn_ind_tsm_sdwan` namespace.

The calling user must have the ticket\_integrator role.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TroubleTicketNotificationUtilOOB - addAdditionalEventAttributes\(Object tmfEventPayload\)

Adds custom event header attributes to the passed TMF trouble ticket event payload. The attributes added by this method are added to the event-level header for all trouble ticket events.

|Name|Type|Description|
|----|----|-----------|
|tmfEventPayload|Object|TMF-compliant trouble ticket event payload. For details on the format of this event payload, see the [TMF621 Trouble Ticket Management API REST Specification v5.0.0](https://www.tmforum.org/resources/standard/tmf621-trouble-ticket-management-api-rest-specification-v5-0-0/) and the [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this method.

```
constructTMFEvent: function(eventId) {
  var troubleTicketEvent = {};
  if (gs.nil(eventId)) {
    troubleTicketEvent.eventId = gs.generateGUID();
  } else {
    troubleTicketEvent.eventId = eventId;
  }
  troubleTicketEvent['@type'] = Constants.EVENT_TYPE_TROUBLE_TICKET;
  this.addAdditionalEventAttributes(troubleTicketEvent);
  return troubleTicketEvent;
},
```

## TroubleTicketNotificationUtilOOB - constructTMFEvent\(String eventId\)

Generates the TMF688-compliant header attributes in the event section of the payload. These attributes are consistent across all event payloads.

In the default implementation, this method adds the **eventId** and the **@type** header attributes.

This method calls the helper method [addAdditionalEventAttributes\(\)](TroubleTicketNotifScopedAPI.md#). In this method you can add other header attributes to the event payload. For details, see [Modify a trouble ticket event payload](../../../../../integrate/guides/ProducerEventNotifFramework/reference/prd_evt_not-dev_gd-mod-evt-pay.md).

|Name|Type|Description|
|----|----|-----------|
|eventId|String|Unique identifier of the associated event. This can be any unique value. In the default implementation, if you don't pass the event ID, the value is set to a system generated GUID.|

|Type|Description|
|----|-----------|
|Object|TMF payload with the event-level attributes set. For details on the format of this event payload, see the[TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method to construct the event header attributes when generating a trouble ticket attribute change payload.

```
generateTroubleTicketAttributeChangePayload: function(incidentGr, eventType, eventId) {
  var tmfEventPayload = this.constructTMFEvent(eventId);
  tmfEventPayload.eventType = eventType;
  tmfEventPayload.event = this.addAttributeChangeTroubleTicketAttributes(incidentGr);

  return tmfEventPayload;
},
```

## TroubleTicketNotificationUtilOOB - generateCreateTroubleTicketEventPaylaod\(Object incidentGr, String eventType, String eventId\)

Constructs the TMF-compliant payload for the associated create trouble ticket for incident event type.

This method is executed when the associated event type is `TROUBLE_TICKET_CREATE: "TroubleTicketCreateEvent"`. This method calls two helper methods:

-   [constructTMFEvent\(\)](TroubleTicketNotifScopedAPI.md#): Adds the event header attributes \(TMF688\) to the payload.
-   addCreateTroubleTicketAttributes\(\): Override this method to add trouble ticket attributes \(TMF621\), both mandatory and optional, to the payload. This method is just a stub in the default implementation.

You can override these helper methods in the `TroubleTicketNotificationUtil` script include to configure both event header and trouble ticket attributes in the TMF-compliant payload.

<table id="table_i5j_xcx_c1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

incidentGr

</td><td>

Object

</td><td id="TTNUO-incidentGr-entry">

JSON formatted glide record that caused the trouble ticket event to be generated. Use the information in this glide record to construct the TMF621-compliant trouble ticket event payload.

</td></tr><tr><td>

eventType

</td><td>

String

</td><td>

Unique identifier of the associated trouble ticket event type. For the default implementation of this method, this should always be

 `"TroubleTicketCreateEvent"`.For a list of all base trouble ticket event types, refer to *Constants.EVENT\_TYPES* in the `sn_api_notif_mgmt.Constants` script include file.

</td></tr><tr><td>

eventId

</td><td>

String

</td><td id="TTNUO-eventId-entry">

Unique identifier of the associated event.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|TMF-compliant trouble ticket event payload. For details on the format of this event payload, see the [TMF621 Trouble Ticket Management API REST Specification v5.0.0](https://www.tmforum.org/resources/standard/tmf621-trouble-ticket-management-api-rest-specification-v5-0-0/) and the [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method.

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

    default:
      this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
      eventPayload = null;
  }
return eventPayload;
},
```

## TroubleTicketNotificationUtilOOB - generateCreateTroubleTicketEventPaylaodForCase\(Object incidentGr, String eventType, String eventId\)

Constructs the TMF-compliant payload for the associated create trouble ticket for case event type.

This method is executed when the associated event type is `TROUBLE_TICKET_CREATE_FOR_CASE: "TroubleTicketCreateEventForCase"`. This method calls two helper methods:

-   [constructTMFEvent\(\)](TroubleTicketNotifScopedAPI.md#): Adds the event attributes \(TMF688\) to the payload.
-   addCreateTroubleTicketAttributesForCase\(\): Override this method to add trouble ticket attributes \(TMF621\), both mandatory and optional, to the payload. This method is just a stub in the default implementation.

You can override these helper methods in the `TroubleTicketNotificationUtil` script include to configure both event header and trouble ticket attributes in the TMF-compliant payload.

<table id="table_i5j_xcx_c1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

incidentGr

</td><td>

Object

</td><td id="TTNUO-incidentGr-entry">

JSON formatted glide record that caused the trouble ticket event to be generated. Use the information in this glide record to construct the TMF621-compliant trouble ticket event payload.

</td></tr><tr><td>

eventType

</td><td>

String

</td><td>

Unique identifier of the associated trouble ticket event type. For the default implementation of this method, this should always be

 `"TroubleTicketCreateEvent"`.For a list of all base trouble ticket event types, refer to *Constants.EVENT\_TYPES* in the `sn_api_notif_mgmt.Constants` script include file.

</td></tr><tr><td>

eventId

</td><td>

String

</td><td id="TTNUO-eventId-entry">

Unique identifier of the associated event.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|TMF-compliant trouble ticket event payload. For details on the format of this event payload, see the [TMF621 Trouble Ticket Management API REST Specification v5.0.0](https://www.tmforum.org/resources/standard/tmf621-trouble-ticket-management-api-rest-specification-v5-0-0/) and the [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method.

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

    default:
      this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
      eventPayload = null;
  }
return eventPayload;
},
```

## TroubleTicketNotificationUtilOOB - generateTroubleTicketAttributeChangePayload\(Object incidentGr, String eventType, String eventId\)

Constructs the TMF-compliant payload for the trouble ticket attribute change event for incident event type.

This method is executed when the associated event type is `TROUBLE_TICKET_ATTRIBUTE_CHANGE: "TroubleTicketAttributeChangeEvent"`. This method calls two helper methods:

-   [constructTMFEvent\(\)](TroubleTicketNotifScopedAPI.md#): Adds the event attributes \(TMF688\) to the payload.
-   addAttributeChangeTroubleTicketAttributes\(\): Override this method to add trouble ticket attributes \(TMF621\), both mandatory and optional, to the payload. This method is just a stub in the default implementation.

You can override these helper methods in the `TroubleTicketNotificationUtil` script include to configure both event header and trouble ticket attributes in the TMF-compliant payload.

<table id="table_i5j_xcx_c1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

incidentGr

</td><td>

Object

</td><td id="TTNUO-incidentGr-entry">

JSON formatted glide record that caused the trouble ticket event to be generated. Use the information in this glide record to construct the TMF621-compliant trouble ticket event payload.

</td></tr><tr><td>

eventType

</td><td>

String

</td><td>

Unique identifier of the associated trouble ticket event type. For the default implementation of this method, this should always be

 `"TroubleTicketCreateEvent"`.For a list of all base trouble ticket event types, refer to *Constants.EVENT\_TYPES* in the `sn_api_notif_mgmt.Constants` script include file.

</td></tr><tr><td>

eventId

</td><td>

String

</td><td id="TTNUO-eventId-entry">

Unique identifier of the associated event.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|TMF-compliant trouble ticket event payload. For details on the format of this event payload, see the [TMF621 Trouble Ticket Management API REST Specification v5.0.0](https://www.tmforum.org/resources/standard/tmf621-trouble-ticket-management-api-rest-specification-v5-0-0/) and the [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method.

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

    default:
      this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
      eventPayload = null;
  }
return eventPayload;
},
```

## TroubleTicketNotificationUtilOOB - generateTroubleTicketStatusChangePayload\(Object incidentGr, String eventType, String eventId\)

Constructs the TMF-compliant payload for the associated trouble ticket status change event for incident event type.

This method is executed when the associated event type is `TROUBLE_TICKET_STATUS_CHANGE: "TroubleTicketStatusChangeEvent"`. This method calls two helper methods:

-   [constructTMFEvent\(\)](TroubleTicketNotifScopedAPI.md#): Adds the event attributes \(TMF688\) to the payload.
-   addStatusChangeTroubleTicketAttributes\(\): Override this method to add trouble ticket attributes \(TMF621\), both mandatory and optional, to the payload. This method is just a stub in the default implementation.

You can override these helper methods in the `TroubleTicketNotificationUtil` script include to configure both event header and trouble ticket attributes in the TMF-compliant payload.

<table id="table_i5j_xcx_c1c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

incidentGr

</td><td>

Object

</td><td id="TTNUO-incidentGr-entry">

JSON formatted glide record that caused the trouble ticket event to be generated. Use the information in this glide record to construct the TMF621-compliant trouble ticket event payload.

</td></tr><tr><td>

eventType

</td><td>

String

</td><td>

Unique identifier of the associated trouble ticket event type. For the default implementation of this method, this should always be

 `"TroubleTicketCreateEvent"`.For a list of all base trouble ticket event types, refer to *Constants.EVENT\_TYPES* in the `sn_api_notif_mgmt.Constants` script include file.

</td></tr><tr><td>

eventId

</td><td>

String

</td><td id="TTNUO-eventId-entry">

Unique identifier of the associated event.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|TMF-compliant trouble ticket event payload. For details on the format of this event payload, see the [TMF621 Trouble Ticket Management API REST Specification v5.0.0](https://www.tmforum.org/resources/standard/tmf621-trouble-ticket-management-api-rest-specification-v5-0-0/) and the [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/).|

The following code example shows how to call this method.

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

    default:
      this._logger.debug("Event with id " + eventId + " could not find the matching payload generator");
      eventPayload = null;
  }
return eventPayload;
},
```

