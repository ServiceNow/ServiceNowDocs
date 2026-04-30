---
title: Discovery Admin Workspace Schedules
description: The Schedules page provides a single place to monitor Discovery performance, efficiently manage schedules and statuses, and set up new IP-based or Cloud Discovery schedules.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-12-09"
reading_time_minutes: 6
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
</table>    [Settings](discovery-admin-workspace-setup.md)

-   **IP-based discovery tab**

    Provides a centralized view for monitoring and managing IP‑based Discovery schedules and coverage.

    Depending on your IPv6 IP Address Management \(IPAM\) integration, items that require attention are displayed, such as Discovery schedules that were auto‑created from IPAM and require activation. If you haven't enabled auto-created Discovery schedules via IPAM, select **Review in Settings** to access the [Discovery Admin Workspace Settings](discovery-admin-workspace-setup.md) page. When auto‑created schedules are enabled, a notification displays the number of Discovery schedules that require activation. Select **View and activate schedules** to open the Auto‑created schedules page. For details on activating these schedules, see [Activate auto-created Discovery schedules](../task/activate-auto-disco-schedule.md). For more information about IPv6 IPAM integration, see [IPAM Discovery integration](ipv6-ipam-disco-integration.md).

    IP resources are available via Additional information. Select the **All IP range sets** to access the Discovery Range Sets \[discovery\_range\] table.

    Select a Discovery schedule from the table to view extensive details and update schedule field parameters. For more information, see [Discovery Admin Workspace schedule details](c_daw-disco-schedule-details.md).

-   **Cloud discovery tab**

    Gives you quick access to all of your cloud-based Discovery schedules.

    Select a Discovery schedule from the table to view extensive details and update schedule field parameters. For more information, see [Discovery Admin Workspace schedule details](c_daw-disco-schedule-details.md).

-   **Discovery status tab**

    Shows the status of scheduled discoveries. You can select a Discovery status number to view detailed information. For more details, see [Discovery status](c_DiscoveryStatus.md).


-   **[Create an IP-based Discovery schedule in Discovery Admin Workspace](../task/t-dawCreateNewDiscoSchedule.md)**  
Use the Discovery Admin Workspace dashboard to create IP-based Discovery schedules.
-   **[Discovery Admin Workspace schedule details](c_daw-disco-schedule-details.md)**  
Discovery Admin Workspace enables you to view, edit, and run IP-based Discovery schedules conveniently within a single interface.

**Parent Topic:**[Discovery Admin Workspace](discovery-admin-workspace.md)

**Previous topic:**[Discovery Admin Workspace Home](discovery-admin-workspace-home.md)

**Next topic:**[Create an IP-based Discovery schedule in Discovery Admin Workspace](../task/t-dawCreateNewDiscoSchedule.md)

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

