---
title: Discovery Admin Workspace status details
description: The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/daw-disco-status-details.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Schedules, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace status details

The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.

To access Discovery status details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **Discovery status**.

**Note:** The capabilities described here are available starting with Discovery Admin Workspace v1.8.0. Specific version requirements are noted for individual features where applicable.

After selecting a discovery status from the table, the schedule header displays key information such as Discovery details, MID Server details, and anomaly severity.

\[Omitted image "daw-status-details-schedule-header.png"\] Alt text: Discovery schedule and status details display in the headers

**Note:** Starting with v1.10.0, the schedule header displays 'Quick Discovery' when the schedule is created using the Quick Discovery feature. Additionally, if the schedule associated with a run is deleted, the header no longer displays the schedule name.

The status header shows run-related details, including start and end times, the number of probes triggered and completed, and any anomalies detected.

**Important:** Anomaly information only displays when anomaly detection is enabled. For more information, see [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md).

If the status is Active or Starting, selecting the **Refresh** icon \(\[Omitted image "daw-refresh-icon.png"\]\) updates the Started and Completed values in the header in real time.

## Key features

-   **Details**

    The **Details** tab includes visualizations that provide detailed information about the Discovery status. The visualizations provide an overview of the schedule's performance and current status for IP-based, cloud-based, and certificate discoveries. Key metrics include devices and IPs discovered, cloud resources identified, certificates collected, and errors encountered during the run.

    **Note:** Certificate discovery is available in Discovery Admin Workspace starting with v1.20.0 and requires the Brazil, Australia, or Zurich release starting with Patch 8.

    Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\), then select **Refresh** to refresh the data for each visualization in this section, or export the data as a CSV or Excel file.

<table id="table_of4_5xx_jgc"><thead><tr><th>

Report title

</th><th>

Discovery type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Errors

</td><td>

IP-based, Cloud-based, and Certificate

</td><td>

Displays the number of errors that were detected during the run.

</td></tr><tr><td>

Total Devices

</td><td rowspan="4">

IP-based

</td><td>

Displays the number of devices that were discovered during the run.

</td></tr><tr><td>

New Devices

</td><td>

Displays the number of new devices that were discovered during the run.

</td></tr><tr><td>

Total IPs

</td><td>

Displays the number of IP addresses that were discovered during the run.

</td></tr><tr><td>

Duplicate IPs

</td><td>

Displays the number of duplicate IP addresses that were discovered during the run.

</td></tr><tr><td>

Total Cloud Resources

</td><td>

Cloud-based

</td><td>

Displays the number of cloud resources that were discovered during the run.

</td></tr><tr><td>

Total Certificates

</td><td>

Certificate

</td><td>

Displays the number of certificates that were collected during the run.

</td></tr></tbody>
</table>    Selecting an indicator reveals related information in a table. By default, detected errors display, sorted by priority. Each error card includes details such as the error title, severity, refined code, occurrence count, and error category. Selecting an error card or the **Occurrences** link opens the Error Details page, where you can view the root cause, remediation steps, and individual error instances. For more information, see [Discovery Admin Workspace Error Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-error-details.md).

    For IP-based schedules, the **Total Devices**, **New Devices**, and **Duplicate IPs** tables provide additional details such as the Source, Classification probe, and Scan status. Selecting the **Source** hyperlink opens a page where you can view more information about the device, apply tags, and access the Discovery Log and ECC Queue details. Selecting the **Total IPs** indicator opens the Shazzam Summary table, where you can access details such as IP addresses, IP Range, and Network Range. To learn more about a specific item, select its hyperlink in the table.

    For cloud-based schedules, selecting the **Total Cloud Resources** indicator reveals a bar chart that categorizes each discovered cloud resource by its CI type. Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\) to refresh the data or export the chart as a CSV, JPEG, PNG, or Excel file.

    For certificate discovery schedules, selecting the **Total Certificates** indicator reveals a table of certificates collected during the run. Select a hyperlink in the table to learn more about a specific certificate. Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\) to refresh the data or export it as a CSV or Excel file.

-   **Debugging**

    The **Debugging** tab provides information about the Discovery Log and ECC Queue.

    Select the **More Options** icon \(\[Omitted image "icon-menu-sow.png"\]\), then select **Refresh** to refresh the data for each visualization in this section, or export the data as a CSV or Excel file.

    By default, the **Discovery Log** table displays information such as classification failures, CMDB updates, and authentication failures. A Discovery Log record is created for each action associated with a discovery status.

    Select the **ECC Queue** indicator to display entries in the **ECC Queue**. The entries show a connected flow of probe and sensor activity and the actual XML payload sent to or from an instance.


