---
title: Discovery Admin Workspace Schedules
description: The Schedules page provides a single place to monitor Discovery performance, efficiently manage schedules and statuses, and set up new IP-based or Cloud Discovery schedules.Discovery Admin Workspace enables you to conveniently view, edit, and run both IP-based and Cloud Discovery schedules conveniently within a single interface.The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
keywords: [Discovery, Admin, Workspace, Discovery, Admin, Workspace, Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace Schedules

The Schedules page provides a single place to monitor Discovery performance, efficiently manage schedules and statuses, and set up new IP-based or Cloud Discovery schedules.

To access the Discovery Admin Workspace Schedules page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.13.0. Specific version requirements are noted for individual features where applicable.

## Key features

-   **Quick Discovery option**

    Enables you to perform an IP-based discovery in just a few steps. You can select an IP range, choose the MID selection method, pick the MID Server, and run the discovery all within one interface. This option is available from any tab on the Schedules page.

-   **New Discovery option**

    Enables you to choose how you want to discover your resources, either through IP-based or Cloud-based discovery. This option is available from any tab on the Schedules page.

-   **Overview tab**

    The **Schedules overview** section enables you to make data-driven decisions through powerful visualizations.

    **Note:** You can configure the time scale reflected in the displayed counts on the [Settings](discovery-admin-workspace-setup.md) page.

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

<table id="table_cb2_yjv_fsb"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active schedules

</td><td>

Indicator

</td><td>

Displays the total number of IP-based and Cloud Discovery schedules that are configured and enabled to run on a recurring basis.Select the number to view all Discovery schedules.

</td></tr><tr><td>

Schedules completed without anomalies

</td><td>

Indicator

</td><td>

Displays the number of IP-based and Cloud Discovery schedules that were completed without anomalies in a certain time period.**Important:** This count only displays when anomaly detection is turned on. If anomaly detection is turned off, select **Turn on** to be redirected to the [Settings](discovery-admin-workspace-setup.md) page.

</td></tr><tr><td>

X day schedule trends

</td><td>

Line chart

</td><td>

Displays Discovery schedule trends over a certain time period. Schedules that failed to run are marked as critical anomalies. Schedules that have a low CI discovery rate are marked as major anomalies. Schedules that have a long run time or have a high error count are marked as minor anomalies.The timeline displays events that occurred during the schedule. Use the magnifying glass icon \( ![magnifying glass icon](../image/zoom-in-magnify.png)\) or scroll to zoom in on the timeline and hover over the indicator to expose event details. You can toggle event indicators on and off using the **Show legend** feature.

Select **View discovery status** to view the status of all scheduled IP-based and Cloud discoveries.

Select **View anomalies** to view anomalous schedules.

</td></tr><tr><td>

Schedules by location

</td><td>

Map

</td><td>

Displays Discovery schedules by location.Select an area of the map to view Discovery schedules in the region selected.

</td></tr><tr><td>

Schedules with anomalies

</td><td>

Bar chart

</td><td>

Displays Discovery schedules with anomalies detected in a certain time period, indicating the schedules that failed, had a low CI discovery rate, had increased error counts, or had long run times. Select the number or **View all** to view the anomalous schedules.

**Important:** This count only displays when anomaly detection is turned on. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

</td></tr><tr><td>

Errors by category

</td><td>

Donut chart

</td><td>

Displays the count of all Discovery errors by category.Select a category to add or remove it from the chart. Select **View details** to view a list of all errors from all discoveries.

</td></tr></tbody>
</table>-   **IP-based discovery tab**

    Provides a centralized view for monitoring and managing IP‑based Discovery schedules and coverage.

    Depending on your IPv6 IP Address Management \(IPAM\) integration, items that require attention are displayed, such as IPs that aren't currently covered by Discovery schedules or schedules that were auto created from IPAM that require activation. Select **Review missing coverage** to access the [CMDB Coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-coverage.md) page where you can view coverage analysis results and create Discovery schedules from IP Ranges. If you haven't enabled auto-created Discovery schedules via IPAM, select **Review in Settings** to access the [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md) page. When auto‑created schedules are enabled, a notification displays the number of Discovery schedules that require activation. Select **View and activate schedules** to open the Auto‑created schedules page. For details on activating these schedules, see [Activate auto-created Discovery schedules](../task/activate-auto-disco-schedule.md). For more information about IPv6 IPAM integration, see [IPAM Discovery integration](ipv6-ipam-disco-integration.md).

    IP resources are available via Additional information. Select the **Total IP address** link to access a [CMDB Coverage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-coverage.md) analysis.

    **Note:** You must have the CMDB Coverage application v1.0.0 installed to access this link.

    Select the **All IP range sets** to access the Discovery Range Sets \[discovery\_range\] table.

    Select a Discovery schedule from the table to view extensive details and update schedule field parameters. For more information, see [Discovery Admin Workspace schedule details](discovery-admin-workspace-schedules.md#).

-   **Cloud discovery tab**

    Gives you quick access to all of your cloud-based Discovery schedules.

    Select a Discovery schedule from the table to view extensive details and update schedule field parameters. For more information, see [Discovery Admin Workspace schedule details](discovery-admin-workspace-schedules.md#).

-   **Discovery status tab**

    Shows the status of scheduled discoveries. You can select a Discovery status number to view detailed information. For more details, see [Discovery Admin Workspace status details](discovery-admin-workspace-schedules.md#).


**Related topics**  


[Create an IP-based Discovery schedule in Discovery Admin Workspace](../task/t-dawCreateNewDiscoSchedule.md)

[Create an Alibaba Cloud Discovery schedule in Discovery Admin Workspace](../task/create-alibaba-schedule-DAW.md)

[Create an AWS Discovery schedule in Discovery Admin Workspace](../task/create-AWS-schedule-DAW.md)

[Create an Azure Discovery schedule in Discovery Admin Workspace](../task/create-azure-schedule-DAW.md)

[Create a GCP Discovery schedule in Discovery Admin Workspace](../task/create-gcp-schedule-DAW.md)

[Create an IBM Discovery schedule in Discovery Admin Workspace](../task/create-ibm-schedule-DAW.md)

[Create an OCI Discovery schedule in Discovery Admin Workspace](../task/create-oci-schedule-DAW.md)

[Create an OpenStack Discovery schedule in Discovery Admin Workspace](../task/create-openstack-schedule-DAW.md)

[Create an oVirt Discovery schedule in Discovery Admin Workspace](../task/create-ovirt-schedule-DAW.md)

[Create a VMware Discovery schedule in Discovery Admin Workspace](../task/create-vmware-schedule-DAW.md)

## Discovery Admin Workspace schedule details

Discovery Admin Workspace enables you to conveniently view, edit, and run both IP-based and Cloud Discovery schedules conveniently within a single interface.

To access Discovery schedule details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **Discovery schedules**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.8.0 or later. Specific version requirements are noted for individual features where applicable.

After selecting a schedule name from the table, the schedule header displays key information such as Discovery details, MID Server details, and anomaly severity.

**Important:** Anomaly information only displays when anomaly detection is enabled. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

### Key features

-   **Overview**

    The **Overview** tab includes visualizations that provide detailed information about the Discovery schedule. These visualizations offer a comprehensive view of the schedule's performance and status, showing key metrics like the number of discoveries completed, success rate, and any errors encountered. Additionally, the visualizations highlight trends over time, enabling you to quickly identify patterns and potential issues. For a full list of the visualizations available on this tab, see [Discovery Admin Workspace data visualizations](../reference/r_dawScheduleDetailsOverview.md).

    **Note:** The time scale reflected on this page can be configured on the Settings page. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

-   **Schedule Details**

    The **Schedule Details** tab provides in-depth information about the Discovery schedule and enables you to update the information directly within the interface.

    Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), to access additional actions for customizing and managing the form interface.

    To create a range of IP addresses to discover, select **Quick Ranges**. Execute a run by selecting **Discover now**. For more information about Discovery schedule configuration, see [Schedule a horizontal discovery](../task/t_CreateADiscoverySchedule.md#).

-   **Run History**

    The **Run History** tab displays the status of the last 10 scheduled discoveries, including icons for anomaly detection, when enabled. Select a Discovery status number to view detailed information. For more details, see [Discovery Admin Workspace status details](discovery-admin-workspace-schedules.md#).


## Discovery Admin Workspace status details

The Discovery Status Details page offers a summary of a discovery initiated from a schedule, detailing the devices identified, any errors encountered, and any anomalies found.

To access Discovery status details in Discovery Admin Workspace, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **Discovery status**.

**Note:** The capabilities described here are available in Discovery Admin Workspace v1.8.0 or later. Specific version requirements are noted for individual features where applicable.

After selecting a discovery status from the table, the schedule header displays key information such as Discovery details, MID Server details, and anomaly severity.

![Discovery schedule and status details display in the headers](../image/daw-status-details-schedule-header.png "Discovery schedule and status headers")

**Note:** Starting with v1.10.0, the schedule header displays 'Quick Discovery' when the schedule is created using the Quick Discovery feature. Additionally, if the schedule associated with a run is deleted, the header no longer displays the schedule name.

The status header shows run-related details, including start and end times, the number of probes triggered and completed, and any anomalies detected.

**Important:** Anomaly information only displays when anomaly detection is enabled. For more information, see [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md).

If the status is Active or Starting, selecting the **Refresh** icon \(![](../image/daw-refresh-icon.png)\) updates the Started and Completed values in the header in real time.

### Key features

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


