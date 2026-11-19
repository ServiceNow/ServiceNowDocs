---
title: EventLog connector event and methods
description: The Eventlog connector provides methods and an event to listen to events from sources and write them to the Microsoft Event Viewer as part of an automation. The methods and events have properties that you can update.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/connector-eventlog-methods.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Eventlog, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# EventLog connector event and methods

The Eventlog connector provides methods and an event to listen to events from sources and write them to the Microsoft Event Viewer as part of an automation. The methods and events have properties that you can update.

## OnEntryWritten

This is a predefined event that occurs when an entry is written to the event log of your local computer.

-   **Event output**

    [Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)

    [Source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)

    [Message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)


## Write

Writes a warning, information, or error to the Microsoft Event Viewer, which includes a message and the source of the event.

-   **Inputs**

    [Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)

    [Source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)

    [Message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-eventlog-methods.md)


## Dispose

When you execute the Write method, an object to the Microsoft Event Viewer is written and a connection is established with the RPA Desktop Design Studio. When you connect the Dispose method with the Write method, the object is disconnected.

## ListenEvents

Listens to the events that are specified in the OnEntryWritten event.

## UnsubscribeToEvents

Discontinues listening to the events from the OnEntryWritten event.

## OnEntryWritten

Provides as outputs the event type, descriptive message, and the source of the event.

**Parent Topic:**[Eventlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/eventlog.md)

