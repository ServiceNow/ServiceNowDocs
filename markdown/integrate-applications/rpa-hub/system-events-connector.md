---
title: System Events
description: Track various system events such as creation of files or loss of the network with the System Events connector as part of your automation Workflow. The connector also enables you to stop tracking events, whenever needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/system-events-connector.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# System Events

Track various system events such as creation of files or loss of the network with the System Events connector as part of your automation Workflow. The connector also enables you to stop tracking events, whenever needed.

The System Events connector provides methods for tracking various system events. See the table.

<table id="table_ptc_xwt_psb"><thead><tr><th>

Method

</th><th>

Purpose

</th></tr></thead><tbody><tr><td>

WatchFileSystem

</td><td>

Tracks the following events:-   FileChanged
-   FileDeleted
-   FileCreated
-   FileRenamed
-   FileWatchError

</td></tr><tr><td>

WatchNetworkAvailability

</td><td>

Tracks the following events:-   NetworkAvailable
-   NetworkUnavailable

</td></tr><tr><td>

WatchSessionEvents

</td><td>

Tracks the following events:-   OnSessionLock
-   OnSessionUnlock
-   OnSessionRemoteControl
-   OnSessionLogoff

</td></tr><tr><td>

UnWatchFileSystem

</td><td>

Stops tracking the following events:-   FileChanged
-   FileDeleted
-   FileCreated
-   FileRenamed
-   FileWatchError

</td></tr><tr><td>

UnWatchNetworkAvailability

</td><td>

Stops tracking the following events:-   NetworkAvailable
-   NetworkUnavailable

</td></tr><tr><td>

UnWatchSessionEvents

</td><td>

Stops tracking the following events:-   OnSessionLock
-   OnSessionUnlock
-   OnSessionRemoteControl
-   OnSessionLogoff

</td></tr></tbody>
</table>You must first use and then expose the methods in the SystemEvents connector to use its methods.

-   To use the connector, see [Use a connector in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-connector.md).
-   To expose the methods, see [Use connector method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/use-connector-method.md).
-   To use the methods, see [Use a component in RPA Desktop Design Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-components.md).

-   **[SystemEvents connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors-systemevents-methods.md)**  
The SystemEvents connector methods watch various system events and, if needed, stop watching.
-   **[Parameters of the SystemEvent connector methods](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/parameters-systemevents-methods.md)**  
Learn about the various parameters of the SystemEvent connector methods in RPA Desktop Design Studio.

**Parent Topic:**[Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/connectors.md)

