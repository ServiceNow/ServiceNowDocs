---
title: SystemEvents connector methods
description: The SystemEvents connector methods watch various system events and, if needed, stop watching.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System Events, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# SystemEvents connector methods

The SystemEvents connector methods watch various system events and, if needed, stop watching.

## Methods

Provides the following methods and the events these methods track:

## WatchFileSystem

Watches the following events.

<table id="table_c5g_kf5_psb"><thead><tr><th>

Event

</th><th>

Description

</th><th>

Parameter

</th></tr></thead><tbody><tr><td>

FileChanged

</td><td>

Update to the file.

</td><td>

-   **Name**: Name of the file that is updated.
-   **Path**: Path to the file.
-   **ChangeType**: Type of update to the file.

</td></tr><tr><td>

FileCreated

</td><td>

New file created in the path watched by the WatchFileSystem method.

</td><td>

-   **Name**: Name of the file created.
-   **Path**: Path to the file that was created.

</td></tr><tr><td>

FileDeleted

</td><td>

File deleted from the path watched by the WatchFileSystem method.

</td><td>

-   **Name**: Name of the file deleted.
-   **Path**: Path to the file that was deleted.

</td></tr><tr><td>

FileRenamed

</td><td>

Name of the file changed.

</td><td>

-   **OldName**: Previous name of the file.
-   **OldPath**: Previous path to the file, if path has also changed.
-   **NewName**: New name of the file.
-   **NewPath**: New path to the file, if applicable.

</td></tr><tr><td>

FileWatchError

</td><td>

WatchFileSystem method error.

</td><td>

 

</td></tr></tbody>
</table>-   **Input**

    [Path](parameters-systemevents-methods.md#watchfilesystem-input-filepath)

    [FileTypes](parameters-systemevents-methods.md#watchfilesystem-input-filetypes)

    [SubDirectories \(Boolean\)](parameters-systemevents-methods.md#watchfilesystem-input-subdirectories)


## WatchNetworkAvailability

Watches the network availability in the system. It uses the following events. You must execute the WatchNetworkAvailability method before executing any of the following events.

|Event|Description|Parameter|
|-----|-----------|---------|
|NetworkAvailable|Watches the system when network is available.| |
|NetworkUnavailable|Watches the system when network is unavailable.| |

## WatchSessionEvents

Watches the following events.

|Event|Description|Parameter|
|-----|-----------|---------|
|OnSessionLock|When a session is locked by the user.| |
|OnSessionUnlock|When a session is unlocked by the user.| |
|OnSessionRemoteControl|When a session is remote controlled by the user.| |
|OnSessionLogoff|When the session is logged off.| |

## UnwatchFileSystem

Stops or prevents the RPA Desktop Design Studio from watching the file system events. You can use this method before or after the WatchFileSystem method was already used.

## UnwatchNetworkAvailability

Stops or prevents the RPA Desktop Design Studio watching the network availability events. You can use this method before or after the WatchNetworkAvailability method was already used.

## UnwatchSessionEvents

Stops or prevents RPA Desktop Design Studio watching the network availability events. You can use this method before or after the WatchSessionEvents method was already used.

**Parent Topic:**[System Events](../concept/system-events-connector.md)

