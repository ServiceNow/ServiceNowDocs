---
title: Parameters for WMI connector methods
description: The parameters for the Windows Management Instrumentation \(WMI\) connector methods enable you to send custom inputs to the WMI to perform different actions such as get disk details, environment value, CPU usage, and more as part of an automation Workflow in RPA Desktop Design Studio.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [ITSM connector, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Parameters for WMI connector methods

The parameters for the Windows Management Instrumentation \(WMI\) connector methods enable you to send custom inputs to the WMI to perform different actions such as get disk details, environment value, CPU usage, and more as part of an automation Workflow in RPA Desktop Design Studio.

|Parameter name|Description|Mandatory?|
|--------------|-----------|----------|
|Hostname|Hostname of the local or remote computer.|Yes|
|Username|Username of the host.|Yes|
|Password|Password to connect to the local or remote host.|Yes|
|Hashtable|Disk details in the local or remote computer in the form of a hash table.|Not applicable|
|Var|Environment variable name.|Yes|
|Return|Environment variable value.|Not applicable|
|Class|Class as input.|Yes|
|Filter|Filter as input.|Yes|
|Return \(Sorted Dictionary\)|Returns the memory usage values as key-value pairs in a sorted dictionary.|Not applicable|
|Return \(Sorted Dictionary\)|Returns the CPU usage values as key-value pairs in a sorted dictionary.|Not applicable|
|Return|Returns the usage values of system files in Windows as objects.|Not applicable|
|Return|Returns the page fault values per second as an object.|Not applicable|
|Return \(Object\)|Returns the usage of memory in percentage terms as an object.|Not applicable|
|Return|Returns the usage values of the processor in percentage terms as objects.|Not applicable|
|Return|Returns the available memory in bytes as integers.|Not applicable|
|Return|Query result as an object.|Not applicable|

## Input parameter values

To input the parameter values, see [Configure port properties](../task/configure-input-port-properties.md).

**Parent Topic:**[ITSM connector](../concept/itsm.md)

