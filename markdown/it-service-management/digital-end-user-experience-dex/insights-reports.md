---
title: DEX Insights reports
description: The Digital End-User Experience \(DEX\) Insights tab provides reports on the user device battery health, system compliance, system performance, and system time, which enables efficient monitoring and issue identification.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# DEX Insights reports

The Digital End-User Experience \(DEX\) Insights tab provides reports on the user device battery health, system compliance, system performance, and system time, which enables efficient monitoring and issue identification.

## Battery health

<table id="table_s12_zmv_xbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Device

</td><td>

Name of the monitored digital device, like a laptop or a desktop.

</td></tr><tr><td>

User

</td><td>

Owner of the device.

</td></tr><tr><td>

Operating system

</td><td>

OS that manages and controls the device hardware, as well as enables the execution of applications such as Windows or macOS.

</td></tr><tr><td>

Battery health

</td><td>

State of the battery health. States include the following:-   Good
-   Moderate
-   Poor
-   Unknown

</td></tr><tr><td>

Battery condition

</td><td>

Battery condition values vary by OS. Each OS has the following values:-   Windows: Degraded, Error, Lost Comm, No Contact, NonRecover, OK, Pred Fail, Service, Starting, Stopping, Stressed, Unknown
-   macOS: Normal, Service Needed, Permanent Failure, Check Battery

</td></tr><tr><td>

Fully charged capacity

</td><td>

Capacity of the battery when fully charged.

</td></tr><tr><td>

Percent of designed capacity

</td><td>

Current capacity divided by the designed capacity.

</td></tr><tr><td>

Cycle count

</td><td>

Cycle count before replacement.

</td></tr><tr><td>

Battery serial number

</td><td>

Serial number of the battery.

</td></tr><tr><td>

Last refresh time

</td><td>

Last time the record was updated.

</td></tr></tbody>
</table>## System compliance

|Field|Description|
|-----|-----------|
|Device|Name of the monitored digital device, like a laptop or a desktop.|
|User|Owner of the device.|
|Compliance rating|Device's adherence to tracked applications and policy metrics, measured in percentage. It's calculated by dividing the number of compliant applications and policy metrics by the total number of applications monitored.|
|Noncompliant applications|Applications monitored for compliance but not currently running on this device.|
|Noncompliant metric values|System policies that don't return the expected or compliant values as required by your organization's compliance standards.|
|Alert|Alert triggered by a noncompliance event.|
|Operating system|OS that manages and controls the device hardware, as well as enables the execution of applications such as Windows or macOS.|
|Location|Physical location of the device.|

## System performance

<table id="table_rjs_1md_ycc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Device

</td><td>

Name of the monitored digital device, like a laptop or a desktop.

</td></tr><tr><td>

User

</td><td>

Owner of the device.

</td></tr><tr><td>

CPU usage

</td><td>

Amount of processing power consumed by an application, measured in percentage.High CPU usage might result in degraded application performance, slower response times, and decreased user satisfaction. Identifying performance bottlenecks can help optimize application performance.

</td></tr><tr><td>

Memory usage \(%\)

</td><td>

Amount of memory or RAM consumed by an application, measured in percentage.High memory usage might result in degraded application performance, slower response times, crashes, and system instability. Monitoring memory usage can help optimize resource allocation and capacity planning.

</td></tr><tr><td>

Disk usage \(%\)

</td><td>

Proportion of storage capacity consumed by data and applications on a disk drive, measured in percentage.Elevated disk usage might lead to slower system performance, increased loading times, and potential storage-related issues. Monitoring disk usage can help optimize storage resources, avoid data bottlenecks, and promote efficient data management.

</td></tr><tr><td>

IO usage read \(kbps\)

</td><td>

Process of reading data from storage devices, such as hard drives or solid-state drives, within a computer system.Excessive I/O read operations might lead to performance bottlenecks, increased latency, and slower system response times. Monitoring I/O read activities can verify that the data retrieval processes don't limit application performance.

This field appears only for installed applications.

</td></tr><tr><td>

IO usage write \(kbps\)

</td><td>

Process of writing data to storage devices, like hard drives or solid-state drives, within a computer system.Excessive I/O write operations might lead to performance bottlenecks, increased latency, and slower system response times. Monitoring I/O write activities can verify that the data storage processes don't limit application performance.

This field appears only for installed applications.

</td></tr></tbody>
</table>## System time

|Field|Description|
|-----|-----------|
|Device|Monitored digital devices, like laptops and desktops.|
|User|Owner of the device.|
|Boot time|Time when the device last rebooted.|
|Up time|Amount of time that the device has been running.|
|Device serial number|Serial number of the device.|
|Device age|Age of the device.|
|Operating system|OS that manages and controls the device hardware, as well as enables the execution of applications, such as Windows or macOS.|
|Last refresh time|Last time the device record was updated.|

**Parent Topic:**[DEX Application and Device Health reference](dex-console-reference.md)

