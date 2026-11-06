---
title: Installed application Performance page
description: The Performance page for an installed application presents details on the location and app version, the number of crashes and freezes, and CPU, memory, and I/O performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/installed-app-health-form.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Applications list, DEX Application and Device Health reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Installed application Performance page

The Performance page for an installed application presents details on the location and app version, the number of crashes and freezes, and CPU, memory, and I/O performance.

**Note:** Application performance metrics are available for the previous 2 hours, 24 hours, or 30 days. Select the required time window from the drop-down list to update the visualization.

One chart displays the application performance metrics, and the other displays the aggregated metric data for the selected time window.

<table id="table_qhx_3zy_zwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Total number of crashes - Last 2 hours

</td><td>

Aggregate number of crashes in the last 2 hours.**Note:** The number of crashes pertains to applications that emit a Windows application crash event \(event id = 1000\) on crashing such as Microsoft OneDrive, Microsoft Teams, Microsoft Excel, Microsoft OneNote, Microsoft PowerPoint, Microsoft Outlook, and Microsoft Word.

</td></tr><tr><td>

Number of crashes - Last 2 hours

</td><td>

Number of application crashes over the last 2 hours by version.

</td></tr><tr><td>

Total number of freezes - Last 2 hours

</td><td>

Aggregate number of freezes in the last 2 hours.

</td></tr><tr><td>

Number of freezes - Last 2 hours

</td><td>

Number of application freezes over the last 2 hours by version.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Average CPU usage - Last 2 hours|Average CPU usage of the application.|
|CPU usage - Last 2 hours|The percentage of total processor \(CPU\) capacity consumed by the application.|
|Average memory usage - Last 2 hours|Average memory usage of the application.|
|Memory usage - Last 2 hours|The percentage of total memory or RAM consumed by the application.|
|Average I/O read - Last 2 hours|The average speed at which the application reads data from storage \(for example, when opening a large file\).|
|I/O read - Last 2 hours|The speed at which the application reads data from storage.|
|Average I/O write - Last 2 hours|The average speed at which the application saves data to storage \(for example, when creating log files or saving a project\).|
|I/O write - Last 2 hours|The speed at which the application saves data to storage.|

**Note:** You can filter the performance metrics by either searching by location of the device or by app version running on the device in a selected time period.

**Parent Topic:**[Applications list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/application-form.md)

