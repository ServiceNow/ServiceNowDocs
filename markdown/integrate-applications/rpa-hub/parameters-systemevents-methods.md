---
title: Parameters of the SystemEvent connector methods
description: Learn about the various parameters of the SystemEvent connector methods in RPA Desktop Design Studio.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [System Events, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Parameters of the SystemEvent connector methods

Learn about the various parameters of the SystemEvent connector methods in RPA Desktop Design Studio.

|Parameter name|Description|Mandatory?|
|--------------|-----------|----------|
|Path|Path to the folder or file that the WatchFileSystem method will track.|Yes|
|FileTypes|File types that WatchFileSystem will track.|Yes|
|SubDirectories \(Boolean\)|Option to indicate whether WatchFileSystem will track subdirectories.|No|
|Name|Name of a file that is tracked by a SystemEvent method changes.|Yes|
|Path|Path of a file that is tracked by a SystemEvent method.|Yes|
|ChangeType|Type of change.|Yes|
|Name|Name of the file created.|Yes|
|Path|Path of the file created.|Yes|
|Name|Name of the file deleted.|Yes|
|Path|Path of the file deleted.|Yes|
|OldName|File name before a name change.|Yes|
|OldPath|File path before a path change.|Yes|
|NewName|New file name.|Yes|
|NewPath|New file path.|Yes|

## Configure inputs for the parameters

To enter inputs for parameters, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[System Events](../concept/system-events-connector.md)

