---
title: Features of the Investigation tab
description: The Investigation tab displays CI metrics information along with various options. Use the options and the metrics information to view the data that helps to resolve the CI-related issues.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Incident Management in Service Operations Workspace reference, Incident Management in Service Operations Workspace, Operate, Service Operations Workspace for ITSM, IT Service Management]
---

# Features of the Investigation tab

The **Investigation** tab displays CI metrics information along with various options. Use the options and the metrics information to view the data that helps to resolve the CI-related issues.

You can select the following drop-down options to view the metrics information for the CI:

-   Initial metrics: Metrics information of the affected CI that is retrieved from 30 minutes before to 30 minutes after the incident is created. The metrics information of the CI is displayed only if the CI is populated in that one hour time period. You can configure the **sn\_sow.initial\_metric\_fetch\_window** property to change the one hour time period.

    **Note:** Initial Metrics is available only for the primary CI.

-   Recent metrics: Latest metrics information that is available for the affected CI. By default, the **Recent Metric** option is selected.

**Note:** The metrics information for the CI is retrieved in any one of the following conditions:

-   When the primary CI is updated or added to the incident. You can also configure when and how the metric information is retrieved for a CI by configuring the collection rule. For more information, see [Configure the collection rules for the Investigate tab](../concept/customize-the-incident-record-page.md#).
-   When you select the Get latest metrics icon \(![get latest matrix refresh](../image/get-latest-matrix.png)\), it refreshes, retrieves, and displays the latest metrics on demand. This option is available only when you’re viewing data in the Recent Metrics.

The metrics data includes the following information:

-   Overview: Displays overview information of the CI, such as name, operating system, and model number, from the ServiceNow database records and CMDB CI computer using the glide record query. The **Name** field contains a hyperlinked value, which displays the CI record on a separate tab when selected.
-   System information: Select to display the system information for the selected CI on a separate modal. The system information modal includes the following data:
    -   Microsoft system \(msinfo32\): Displays information about the computer and a comprehensive view of the hardware resources, system summary, components, and software environments, which can be used to diagnose the computer issues. You can also search and view any specific system parameter, if necessary.
    -   Azure \(dsregcmd\): Displays information on the state of the CI device that is managed by the Azure Active Directory \(Azure AD\). This information is used to diagnose and troubleshoot the device. The date and time when the information is last retrieved is also displayed. You can also search and view any device parameter, if necessary.

        **Note:** You can only use this option when the Agent Client Collector for Investigation \(sn\_acc\_adapter\) adapter is integrated with the Investigation Framework.

-   Device health: Select the **Device health** link to launch the Digital End-User Experience application and device health page for the selected CI on a separate tab, within the incident view. This tab enables agents to view all the available metrics and the device health for the selected CI, which were collected by DEX. You can also access this feature using the **View device health** option on the CI record in Service Operations Workspace.

    **Note:** DEX requires a separate entitlement.

    This link is available to the agent only if the following conditions are met:

    -   The selected CI is of type Device, which is also known as Endpoint.
    -   The DEX plugin is installed on the instance. For more information on DEX, see [Digital End-User Experience](../../digital-end-user-experience/concept/dex-landing.md).
    -   The DEX agent is installed on the selected CI.
-   Asset utilization: Utilization of the assets for the CI. The following information is displayed along with the date and time:

    -   Memory utilization: Amount of the memory used on the CI. The value is displayed in percentage.
    -   Disk utilization: Disk utilization of the logical drives for the affected CI. The value is displayed in percentage.
    -   CPU utilization: CPU utilization for the CI. The value is displayed in percentage.
    -   Uptime: Uptime \(boot time\) of the assets. The days and time since when the assets are up and running.
    **Note:** The following metrics are color-coded based on the threshold values to highlight the warning or critical level:

    |Asset utilization metrics|Warning \(Yellow color code\)|Critical \(Red color code\)|
    |-------------------------|-----------------------------|---------------------------|
    |Memory utilization|Greater or equal to 80|Greater or equal to 95|
    |Disk utilization|Greater or equal to 80|Greater or equal to 95|
    |CPU utilization|Greater or equal to 80|Greater or equal to 95|

    However, you can also customize these threshold values, if necessary. For more information, see [Customize the Investigate tab](../concept/customize-the-incident-record-page.md#).

-   Top processes by CPU: Top processes sorted based on the CPU utilization of the processes in the affected CI.

    **Note:** The Top processes by CPU metrics are color-coded based on the threshold values to highlight the critical level when the value is greater or equal to 90. However, you can also customize these values, if necessary.

-   Top processes by memory: Top processes sorted based on the memory consumed by the processes in the affected CI.

    **Note:** The Top processes by memory metrics are color-coded based on the threshold values to highlight the critical level when the value is greater or equal to 90. However, you can also customize these values, if necessary.

-   Services: List of services \(device or server\) running on the affected CI.
-   Logged in users: List of the logged-in users in the affected CI.
-   Installed applications: List of the applications installed on the CI.

    **Note:** For devices with the Windows OS, the Installed applications don't include a list of pre-packed application.


Use the **View History** button to view the historical metrics data for the CI on a separate tab. You can select the time range from the drop-down options to view the historical data for that time range. For more information, see [Viewing the historical data of CI metrics](view-investigate-history-data.md).

-   **[Viewing the historical data of CI metrics](view-investigate-history-data.md)**  
View the historical data of the CI metrics for the selected time range.

**Parent Topic:**[Incident Management in Service Operations Workspace reference](../concept/sow-im-reference.md)

