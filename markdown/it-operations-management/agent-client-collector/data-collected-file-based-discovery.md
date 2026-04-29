---
title: Data collected during Agent Client Collector for Visibility - Content file-based Discovery
description: The following tables describe the data collected during Agent Client Collector for Visibility - Content file-based Discovery.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC-VC reference, Agent Client Collector reference, Agent Client Collector, IT Operations Management]
---

# Data collected during Agent Client Collector for Visibility - Content file-based Discovery

The following tables describe the data collected during Agent Client Collector for Visibility - Content file-based Discovery.

<table id="table_lzp_rgp_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record. For example: Java@hostname

</td></tr><tr><td>

Physical Machine Name

</td><td>

Name of the host CI

</td></tr><tr><td>

Machine Type

</td><td>

Either Server\(S\) or Desktop\(D\)

</td></tr><tr><td>

Java Publisher/Runtime Vendor

</td><td>

Java Vendor name

</td></tr><tr><td>

Operating System

</td><td>

Operating system in which the java is run

</td></tr><tr><td>

Environment Type

</td><td>

Production or Development or QA environment

</td></tr><tr><td>

Java Release/Version/Build

</td><td>

Java Version

</td></tr><tr><td>

Installation Path

</td><td>

Absolute installation path of the java binary

</td></tr><tr><td>

Installation Date \(DateTime\)

</td><td>

The date and time of the java binary file created on the file system

</td></tr><tr><td>

Release File \(Y / N\)

</td><td>

Indicates if a *release.md* file exists in the installation

</td></tr><tr><td>

Processor Make/Model

</td><td>

Processor model name

</td></tr><tr><td>

Sockets \(Integer\)

</td><td>

Number of CPU sockets

</td></tr><tr><td>

Cores \(Integer\)

</td><td>

Number of CPU cores

</td></tr><tr><td>

V6 and earlier

</td><td>

Indicates if you have a 6 or earlier java version

</td></tr><tr><td>

Open Source

</td><td>

Indicates if you have an open-source java installation

</td></tr><tr><td>

Unlock Commercial features

</td><td>

Indicates if you have the commercial features \(like JFR\) enabled.Not collected during ACC-VC file-based discovery \(FBD\).

</td></tr><tr><td>

Mission Control

</td><td>

Indicates if the mission control plugin is enabled

</td></tr><tr><td>

AMC Agent

</td><td>

Indicates if the AMC agent plugin is enabled.Not collected during ACC-VC file-based discovery \(FBD\).

</td></tr><tr><td>

Usage Tracker

</td><td>

Indicates if the Usage Tracker feature is enabled

</td></tr><tr><td>

Virtual Machine Object ID

</td><td>

Object ID of the Virtual machine instance

</td></tr><tr><td>

PID

</td><td>

Running process PID

</td></tr><tr><td>

IP Address

</td><td>

IP address of the host/VM

</td></tr><tr><td>

First Discovered

</td><td>

The date of the first discovery

</td></tr><tr><td>

Most recent discovery

</td><td>

The date of the most recent discovery

</td></tr><tr><td>

Discovery Source

</td><td>

The discovery method

</td></tr><tr><td>

Application

</td><td>

Reference to the \[cmdb\_ci\_appl\] table

</td></tr><tr><td>

Software installation

</td><td>

Reference to the \[cmdb\_sam\_sw\_install\] table

</td></tr><tr><td>

Java evidence

</td><td>

Reference to the \[cmdb\_ora\_java\_evidence\] table

</td></tr><tr><td>

Host

</td><td>

Reference to the \[cmdb\_ci\] table

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Running process|Reference to the \[cmdb\_running\_process\] table|
|Host CI|Reference to the \[cmdb\_ci\_computer\] table|
|File information|Provides a reference to the \[cmdb\_file\_information\] table. Relevant only for file-based discovery \(FBD\); in pattern-based discovery, this field remains empty.|

**Parent Topic:**[Agent Client Collector for Visibility - Content reference](../concept/agent-client-collector-for-visibility-references.md)

**Related topics**  


[Discover java installation data using Agent Client Collector for Visibility - Content file-based discovery](../task/acc-file-based-discovery.md)

