---
title: DEX Insights reports
description: The Digital End-User Experience \(DEX\) Insights tab provides reports on the user device battery health, system compliance, system performance, and system time, which enables efficient monitoring and issue identification.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
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

State of the battery health.Battery states include the following: Good, Moderate, Poor, Unknown

</td></tr><tr><td>

Battery condition

</td><td>

Battery condition values vary by OS.Each OS has the following values:

-   Windows: Degraded, Error, Lost Comm, No Contact, NonRecover, OK, Pred Fail, Service, Starting, Stopping, Stressed, Unknown.
-   macOS: Normal, Service Needed, Permanent Failure, Check Battery.

</td></tr><tr><td>

Full charge capacity \(mWh\)

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
</table>## File management

**Note:** The data appears on this page only after File management has been set up.

<table id="table_ch5_hts_v2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File name

</td><td>

Name of the file set up for monitoring.

</td></tr><tr><td>

Category

</td><td>

One of the following categories assigned to the file: Application, Malicious, Security, Development tools, System, Others, Installers, Potentially Unwanted Programs.

</td></tr><tr><td>

Device count

</td><td>

Number of devices that have the file. You can select the number to see all devices where the file was detected.

</td></tr></tbody>
</table>## System compliance

<table id="table_lv1_fld_ycc"><thead><tr><th>

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

Compliance rating \(%\)

</td><td>

Device's adherence to tracked applications and policy metrics, measured in percentage.The score is calculated by dividing the number of compliant applications and policy metrics by the total number of applications monitored.

</td></tr><tr><td>

Noncompliant applications

</td><td>

Applications monitored for compliance but not currently running on this device.

</td></tr><tr><td>

Noncompliant policy metrics

</td><td>

System policy metrics that don't return the expected or compliant values as required by your organization's compliance standards.

</td></tr><tr><td>

Alert

</td><td>

Alert triggered by a noncompliance event.

</td></tr><tr><td>

Operating system

</td><td>

OS that manages and controls the device hardware, as well as enables the execution of applications such as Windows or macOS.

</td></tr><tr><td>

Location

</td><td>

Physical location of the device.

</td></tr></tbody>
</table>## System performance

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

CPU usage \(%\)

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

Process of reading data from storage devices, such as hard drives or solid-state drives, within a computer system.This field appears only for installed applications.

Excessive I/O read operations might lead to performance bottlenecks, increased latency, and slower system response times. Monitoring I/O read activities can verify that the data retrieval processes don't limit application performance.

</td></tr><tr><td>

IO usage write \(kbps\)

</td><td>

Process within a computer system of writing data to storage devices like hard drives or solid-state drives.This field appears only for installed applications.

Excessive I/O write operations might lead to performance bottlenecks, increased latency, and slower system response times. Monitoring I/O write activities can verify that the data storage processes don't limit application performance.

</td></tr></tbody>
</table>## System time

|Field|Description|
|-----|-----------|
|Device|Monitored digital devices, like laptops and desktops.|
|User|Owner of the device.|
|Boot time|Amount of time took for the device to boot.|
|Up time|Amount of time that the device has been running.|
|Time since provisioning|Amount of time that has passed since the device was provisioned.|
|Last boot timestamp|Indicates when the boot time started.|
|Last refresh time|Last time the device record was updated.|

## Windows registry

**Note:** The data on the devices with Windows keys issues appears on this page only after the Windows registry has been set up and after the policy has run.

<table id="table_pbg_rsx_v2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Path

</td><td>

Full Windows registry key path.

</td></tr><tr><td>

Device count

</td><td>

Number of devices that have issues with the registry key. **Note:** The number of devices shown in the report for each registry key identifies the devices where the reported registry key value is different from the expected value. You can select the number to see all devices where the key issue was detected.

The error `No value (check the configuration)` appears when the path is incomplete or the key path configured for monitoring isn’t present on the device.

</td></tr></tbody>
</table>**Parent Topic:**[DEX Application and Device Health reference](dex-console-reference.md)

