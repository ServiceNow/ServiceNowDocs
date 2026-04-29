---
title: Device metrics page
description: Access real-time metrics like CPU, memory, disk usage, I/O operations, battery, and energy consumption for insights into system resource utilization, performance, and improvement areas.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Device details pages, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Service Management]
---

# Device metrics page

Access real-time metrics like CPU, memory, disk usage, I/O operations, battery, and energy consumption for insights into system resource utilization, performance, and improvement areas.

## Device metrics — Performance

<table id="table_nbd_jxf_1xb"><thead><tr><th>

Cards

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Memory usage

</td><td>

Trend over a selected duration in the amount of memory or RAM consumed by the device.**Note:** High memory usage might lead degraded application performance, slower response times, and crashes or system instability. You can monitor memory usage to optimize resource allocation and capacity planning, verifying that applications have enough resources to meet user needs.

</td></tr><tr><td>

Virtual memory

</td><td>

Trend over a selected duration in the total amount of memory used, including physical memory and the space allocated on the disk as virtual memory.This field appears on Windows machines only.

</td></tr><tr><td>

Pages / sec

</td><td>

Trend over a selected duration in the rate at which pages are read from or written to the disk to resolve page faults.This field appears on Windows machines only.

High values might indicate excessive paging, which can happen when the system runs low on available physical memory.

</td></tr><tr><td>

Page usage percentage

</td><td>

Trend over the selected duration in the proportion of the page file \(disk-based virtual memory\) used.This field appears on Windows machines only.

A consistently high percentage might suggest that the system is relying heavily on virtual memory due to insufficient physical RAM.

</td></tr><tr><td>

Page file size

</td><td>

Trend over a selected duration in the total size of the system page file used to store data that exceeds the capacity of physical memory.This field appears on Windows machines only.

Configurable by the operating system, this size influences the system's ability to handle memory-intensive applications.

</td></tr></tbody>
</table><table id="table_ff5_xc1_zdc"><thead><tr><th>

Cards

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CPU usage

</td><td>

Trend over the selected duration in the amount of processing power consumed by the device in percentage.**Note:** High CPU usage can result in degraded application performance, slower response times, and decreased user satisfaction. Therefore, identify performance bottlenecks and take proactive steps to improve the device performance.

</td></tr><tr><td>

User application CPU consumption

</td><td>

Trend over the selected duration in the user application CPU consumption.This field appears on Windows machines only.

This metric shows how much of the CPU capacity is dedicated to running applications and user-initiated tasks. A consistently high percentage might reflect resource-intensive applications, while low percentages mean minimal user activity or a focus on system processes.

</td></tr></tbody>
</table><table id="table_ctp_fd1_zdc"><thead><tr><th>

Cards

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disk usage

</td><td>

Trend over a selected duration in the proportion of the disk storage capacity consumed by data and applications.Elevated disk usage might lead to slower system performance, increased loading times, and potential storage-related issues. Monitoring disk usage is important for using storage resources better, avoiding data problems, and managing data efficiently.

</td></tr><tr><td>

I/O read &amp; write

</td><td>

Trend in the rate of data read from or written to a storage device over the selected duration.This metric provides insights into the data transfer speed and efficiency of the storage system.

</td></tr><tr><td>

Reads &amp; writes / sec

</td><td>

Trend over a selected duration in the number of read and write operations performed by the disk per second.This field appears on Windows machines only.

High values might indicate heavy disk activity, which could be caused by data-intensive applications or insufficient memory, leading to frequent paging.

</td></tr><tr><td>

Avg. disk sec / read, write &amp; transfer

</td><td>

Trend over a selected duration in the average time in seconds that it takes the disk to complete a read, write, or transfer operation.This field appears on Windows machines only.

Longer times might indicate disk latency issues or bottlenecks in accessing data.

</td></tr><tr><td>

Avg. disk queue length

</td><td>

Trend over a selected duration in the average number of I/O requests waiting in the queue for the disk to process.This field appears on Windows machines only.

A consistently high queue length might mean that the disk is overloaded or unable to keep up with the volume of requests.

</td></tr><tr><td>

Disk time %

</td><td>

Trend over a selected duration in the percentage of time that the disk is actively processing read or write requests.This field appears on Windows machines only.

High values mean that the disk is at or almost at its full capacity, which might make applications that use disk I/O slower.

</td></tr></tbody>
</table><table id="table_lff_fw3_yhc"><thead><tr><th>

Cards

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GPU usage

</td><td>

Displays the percentage of graphics processing unit \(GPU\) capacity in use over time.

 Monitor GPU utilization to assess graphics performance, identify bottlenecks, and troubleshoot issues with rendering or video performance. The chart shows values from 0% \(idle\) to 100% \(fully utilized\).

 **To view details:** Point to any location on the chart to see the GPU usage percentage at that time.

 This field appears on Windows machines only.

</td></tr><tr><td>

GPU VRAM Usage

</td><td>

Displays the amount of video random access memory \(VRAM\) in use by the graphics processing unit \(GPU\) over time.

 Monitor VRAM usage to identify memory-intensive applications, detect memory leaks, and troubleshoot performance issues with graphics-heavy tasks like gaming, video editing, or 3D rendering. High VRAM usage can cause stuttering, frame drops, or application crashes.

 **To view details:** Point to any location on the chart to see the VRAM usage at that time.

 This field appears on Windows machines only.

</td></tr></tbody>
</table>## Device metrics — Battery

|Field|Description|
|-----|-----------|
|Battery percentage|Trend over a selected duration in the remaining charge percentage of the battery.|

## Device metrics — Energy

<table id="table_grg_xyh_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total energy consumption

</td><td>

Overall energy usage over a selected duration.

</td></tr><tr><td>

Energy loss

</td><td>

Wasted energy over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

CPU energy consumption

</td><td>

CPU energy consumption for a selected duration.

</td></tr><tr><td>

GPU energy consumption

</td><td>

Amount of the electrical energy used by the Graphics Processing Unit \(GPU\) over a selected duration.This field appears on macOS machines only.

Monitoring GPU energy consumption helps improve energy efficiency and understand how GPU performance affects the overall device power consumption. Prolonged high GPU energy usage can also contribute to heat generation, which can reduce battery life on portable devices.

</td></tr><tr><td>

ANE energy consumption

</td><td>

Apple neural engine \(ANE\) energy consumption over a selected duration.This field appears on macOS machines only.

</td></tr><tr><td>

Disk energy consumption

</td><td>

Energy consumed by disk operations over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

Network energy consumption

</td><td>

Energy usage by network activities over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

Display energy consumption

</td><td>

Energy usage by the display over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

SOC energy consumption

</td><td>

Energy consumed by the system-on-chip \(SOC\) over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

MBB energy consumption

</td><td>

Energy used by mobile broadband \(MBB\) over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

EMI energy consumption

</td><td>

Energy used by electromagnetic interference \(EMI\) over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

Power consumption

</td><td>

Real-time device power consumption in milliwatt, showing the immediate rate that it uses electrical power and gives insight into the device's power draw over a selected duration.

</td></tr><tr><td>

Other energy consumption

</td><td>

Other energy usage, not covered by specific categories, over a selected duration.This field appears on Windows machines only.

</td></tr></tbody>
</table>## Device metrics — Wi-Fi

<table id="table_ad5_wzl_ydc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transmit and Receive rates

</td><td>

Wi-Fi transmit and receive rates over a selected duration.This field appears on Windows machines only.

</td></tr><tr><td>

Transmit rates

</td><td>

Wi-Fi transmit rates over a selected duration.This field appears on macOS machines only.

</td></tr></tbody>
</table>To return to the main device metrics page, see [Device details](../concept/dex-workspace-user-details.md).

**Parent Topic:**[Device details pages](user-device-details-pages.md)

