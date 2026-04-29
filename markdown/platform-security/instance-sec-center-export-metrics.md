---
title: Export metrics
description: Analyze export metrics to see what data is most commonly exported and which users export the most data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# Export metrics

Analyze export metrics to see what data is most commonly exported and which users export the most data.

<table id="table_kjx_d4x_gpb"><tbody><tr><td>

-   **1. Export chart**

Each report displays the number of export events by date, using a color coded key to indicate which users performed the export. Click a colored section of a column to see the list of **Export Events** \[isc\_export\_event\] records matching that entry.

-   **2. Report key**

The key at the bottom of the report indicates which colors identify which users or tables.

-   **3. Preview pop-up**

Point to an entry in the chart to see a pop-up preview. This preview shows the user or table name, as well as a count of exports and a percentage of the total on that column.

-   **4. Image export**

Click the icon to save the report as an image. You can save the report in PNG or JPEG format.

-   **5. Report date range**

Use the **Show** list to display exports within the last 24 hours or within the last 7 days.


</td><td>

![Export metrics report interface](../image/isc-export-interface.png)

</td></tr></tbody>
</table>## Export metrics reports

The export metrics page displays four reports.

-   **Exports by user**

    Use the **Exports by User** report to see which of your users are exporting the most data.

-   **Classified exports by user**

    Use the **Classified Exports by User** report to see which of your users are exporting the most data matching classifications like confidential, restricted, or personal information. Administrators can define which classifications this report uses in the **Settings** tab.

-   **Exports by table**

    Use the **Exports by Table** report to see which tables are exported from most frequently.

-   **Classified exports by table**

    Use the **Classified Exports by Table** report to see which tables are exported from most frequently that match classifications like confidential, restricted, or personal information. Administrators can define which classifications this report uses in the **Settings** tab.


**Note:** Export metric reports only track export events. Exports from other sources, such as rest APIs or workflows are not tracked as part of this feature.

-   **[Export metrics settings](isc-export-metrics-settings.md)**  
Use the configuration options in the Settings tab to narrow down reporting results.

**Parent Topic:**[Monitor instance metrics](monitoring-user-email-antivirus-metrics.md)

