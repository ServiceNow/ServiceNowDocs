---
title: Discovery Admin Workspace status details
description: The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Schedules, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace status details

The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.

To access Discovery status details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **Discovery status**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.8.0 or later. Specific version requirements are noted for individual features where applicable.

After selecting a discovery status from the table, the schedule header displays key information such as Discovery details, MID Server details, and anomaly severity.

![Discovery schedule and status details display in the headers](../image/daw-status-details-schedule-header.png "Discovery schedule and status headers")

**Note:** Starting with v1.10.0, the schedule header displays 'Quick Discovery' when the schedule is created using the Quick Discovery feature. Additionally, if the schedule associated with a run is deleted, the header no longer displays the schedule name.

The status header shows run-related details, including start and end times, the number of probes triggered and completed, and any anomalies detected.

**Important:** Anomaly information only displays when anomaly detection is enabled. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

If the status is Active or Starting, selecting the **Refresh** icon \(![](../image/daw-refresh-icon.png)\) updates the Started and Completed values in the header in real time.

## Key features

-   **Details**

    The **Details** tab includes visualizations that provide detailed information about the Discovery status. Depending on whether the status pertains to a discovery that is IP-based or cloud-based, the visualizations provide a detailed overview of the schedule’s performance and current status. They highlight key metrics such as the number of devices and IPs discovered, cloud resources identified, and any errors encountered during the run.

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

    |Report title|Discovery Type|Description|
    |------------|--------------|-----------|
    |Errors|Both IP and cloud-based|Displays the number of errors that were detected during the run.|
    |Total Devices|IP-based|Displays the number of devices that were discovered during the run.|
    |New Devices|Displays the number of new devices that were discovered during the run.|
    |Total IPs|Displays the number of IP addresses that were discovered during the run.|
    |Duplicate IPs|Displays the number of duplicate IP addresses that were discovered during the run.|
    |Total Cloud Resources|Cloud-based|Displays the number of cloud resources that were discovered during the run.|

    Selecting an indicator reveals related information in a table. By default, detected errors display, sorted by priority. Each error card includes details such as the Error Code, Operating System, and, when available, a link to supporting documentation. If a task has been created, task-related information is shown on the card, along with the option to edit the task. For errors without an associated task, you can choose to either create a task or ignore the error. Selecting the **Total Errors** hyperlink opens the Error Stats Page, where you can view instructions and take action based on the error.

    For IP-based schedules, the **Total Devices**, **New Devices**, and **Duplicate IPs** tables provide additional details such as the Source, Classification probe, and Scan status. Selecting the **Source** hyperlink opens a page where you can view more information about the device, apply tags, and access the Discovery Log and ECC Queue details. Selecting the **Total IPs** indicator opens the Shazzam Summary table, where you can access details such as IP addresses, IP Range, and Network Range. To learn more about a specific item, simply select its hyperlink in the table.

    For cloud-based schedules, selecting the **Total Cloud Resources** indicator reveals a bar chart that categorizes each discovered cloud resource by its CI type. Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), to refresh or save the chart.

-   **Debugging**

    The **Debugging** tab provides information about the Discovery Log and ECC Queue.

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), to refresh the data for each visualization in this section.

    By default, the **Discovery Log** table displays information such as classification failures, CMDB updates, and authentication failures. A Discovery Log record is created for each action associated with a discovery status.

    Selecting the **ECC Queue** indicator displays entries in the **ECC Queue** provide you with a connected flow of probe and sensor activity, as well as the actual XML payload that is sent to or from an instance.


