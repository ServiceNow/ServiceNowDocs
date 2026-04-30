---
title: Processing Events
description: Event processing is the process of taking events or streams of events, analyzing them and taking automatic action. The process includes viewing events, event binding, event rules and event field mapping.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Processing Events

Event processing is the process of taking events or streams of events, analyzing them and taking automatic action. The process includes viewing events, event binding, event rules and event field mapping.

An event is a notification from one or more monitoring tools that indicate something of interest has occurred, such as a log message, warning, or error. Events are processed and alerts are generated based on the following factors:

Event collection configuration via a MID Server, script, SNMP trap collector, or email message.

An Event rule, alert binding, or event field mapping configuration for processing events from various sources. When a package of events that contains events with a custom \(non-supported\) state is processed, the events with the custom state are not processed.

For more information, see [Exploring Event Management](exploring-event-management.md).

-   **[View events](../task/t_EMManageEvent.md)**  
Event Management tracks individual events to manage external systems. These events are notifications from monitoring tools indicating occurrences of interest, like log messages, warnings, or errors. Event Management gathers events from external sources and stores them in the Event \[em\_event\] table, offering a list of raw incoming events.
-   **[Team-based integrations in Event Management](team-based-integrations.md)**  
Team-based integrations empower teams to optimize event processing within Event Management to enhance efficiency and operational effectiveness.
-   **[Event rules](create-event-rules.md)**  
Use event rules to generate alerts for tracking and remediation. Event rules are stored in the Event Rule \[em\_match\_rule\] table. Configure and customize event rules to manage events and alert generation.
-   **[Event field mapping configuration](c_EMEventFieldMapping.md)**  
Use Event field mappings rules to map values from specific fields to values in other fields.
-   **[Event identifiers](c_EMEventIdentifier.md)**  
Event fields uniquely identify each event. Event Management uses this information to determine whether to create a new alert or update an existing one.
-   **[Alert tags](alert-tags.md)**  
Alert tags allow consolidation for all normalized fields and improve the admin experience to transform and normalize alert fields \(key/value\)​ enabling reuse of normalized fields across different sources.​ This improves alert quality for correlation and provides more out-of-the-box TBAC \(Tag Based Automatic Correlation\) definitions​.
-   **[Event field format for event collection](c_EMIntegrateRequirementEvent.md)**  
Event Management requires all events to use a standard form, regardless of how they arrive at the instance.
-   **[Custom alert fields](populate-custom-alert-fields.md)**  
You can populate custom alert fields with data contained in **Additional information** field of the event.
-   **[Testing and sending events](../task/t_EMCreateEventManually.md)**  
You can manually test and send events to confirm that Event Management properly manages events and generates alerts.
-   **[View event processing statistics](../task/monitor-event-processing-metrics.md)**  
Extract statistics from your instance to ensure that performance is not affected and extract metrics related to event processes to monitor event processing status.

**Parent Topic:**[Configuring Event Management](using-event-management.md)

