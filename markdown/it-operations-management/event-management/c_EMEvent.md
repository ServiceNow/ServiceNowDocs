---
title: Event Management Integrations
description: An event is a notification from one or more monitoring tools that indicate something of interest has occurred, such as a log message, warning, or error.Event Management receives external events via an integration or scripts. If you are using a script to collect events, no configuration is required. All other integrations require configuration.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management Integrations

An event is a notification from one or more monitoring tools that indicate something of interest has occurred, such as a log message, warning, or error.

Events are processed and alerts are generated based on the following factors:

-   Event collection configuration via a MID Server, script, SNMP trap collector, or email message.
-   An Event rule, alert binding, or event field mapping configuration for processing events from various sources.

When a package of events that contains events with a custom \(non-supported\) state is processed, the events with the custom state are not processed.

-   **[Event Management Connectors domain personalization](domain-separation-connectors-personalization.md)**  
Create events in different domains for all Event Management connectors using just a single connector instance by personalizing domain separation of Event Management connectors.
-   **[Configure Event Management connectors](../reference/connectors-and-listeners.md)**  
Event Management provides many connectors to pull or push events from external devices. Connectors are available from the ServiceNow store as well as from third parties. You can also create custom connectors.

**Parent Topic:**[Configuring Event Management](using-event-management.md)

## Integration with external events

Event Management receives external events via an integration or scripts. If you are using a script to collect events, no configuration is required. All other integrations require configuration.

When an integration is configured, Event Management can collect events that are sent directly to the ServiceNow AI Platform instance or via the MID Server, SNMP trap or email.

The integration with external systems can be initiated from a ServiceNow AI Platform instance using a pull connector, or from an external system using a push mechanism.

### Integration via a ServiceNow AI Platform instance

The ServiceNow AI Platform instance includes push connectors that help external monitoring systems to integrate with Event Management directly.

You can configure the authentication in the ServiceNow AI Platform instance and update the external monitoring systems to use endpoints to send the events for the push connectors that are available. For more information, see [Push Connectors](push-event-listener.md).

### Integration via MID Server

The MID Server facilitates communication and movement of data between external applications, data sources, services, and the ServiceNow AI Platform instance.

|Connector operation|Description|
|-------------------|-----------|
|Pull|You can configure connector instances to use connector definitions \(script instructions\). This enables the MID Server to connect to external servers to obtain event information using a pull operation.|
|Push|You can configure external systems to push event information to the ServiceNow AI Platform instance via MID Server. For example, you can configure the MID WebService Event Collector to push event messages to the MID Server. For more information, see [Pushing events to the MID Server using web service API](event-collection-via-MID-using-push.md).|

### Standard event form

A standard event form must be used by all events, regardless of how they arrive at the ServiceNow AI Platform instance. For more information, see [Event field format for event collection](c_EMIntegrateRequirementEvent.md).

