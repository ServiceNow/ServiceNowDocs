---
title: System Events
description: Track various system events such as creation of files or loss of the network with the System Events connector as part of your automation Workflow. The connector also enables you to stop tracking events, whenever needed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Connectors, Automation components, RPA Desktop Design Studio, Workflow Data Fabric]
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

-   To use the connector, see [Use a connector in RPA Desktop Design Studio](../task/use-connector.md).
-   To expose the methods, see [Use connector method](../task/use-connector-method.md).
-   To use the methods, see [Use a component in RPA Desktop Design Studio](../task/configure-components.md).

-   **[SystemEvents connector methods](../reference/connectors-systemevents-methods.md)**  
The SystemEvents connector methods watch various system events and, if needed, stop watching.
-   **[Parameters of the SystemEvent connector methods](../reference/parameters-systemevents-methods.md)**  
Learn about the various parameters of the SystemEvent connector methods in RPA Desktop Design Studio.

**Parent Topic:**[Connectors](connectors.md)

