---
title: Auto Query page
description: The Auto Query page contains the automatic asset queries for the Discovery Console for OT.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the Console pages, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Auto Query page

The Auto Query page contains the automatic asset queries for the Discovery Console for OT.

## Auto Query

The Auto Query page contains a list of all the automatic asset queries available for your system. Each Auto Query is displayed in columns with the following headings and information.

-   Name
-   Enabled
-   Status
-   Sensors
-   Recurring
-   Targets
-   Queried
-   Ignored
-   Skipped
-   Run Query
-   Created On
-   Updated On
-   Last Executed On
-   Completed
-   Delete

The following image shows an example of the Auto Query page.

![Auto Query page](../images/auto-query-full-page.png)

**Note:** When a query is enabled but not running, the Status column displays idle icon ![](../../msi-console/image/idle.png) to indicate it is idle. When related or all Sensors are offline, the All Sensors Offline icon ![](../images/offline.png) displays.

## Actions

The **Actions** button is a drop-down menu that includes the following options.

![Auto Query Action button](../images/actions-menu-quick-scan-small.png)

-   **Show Detail Columns**: Toggles between Show and Hide. When showing the Detail Columns, additional columns display on the page. The additional columns shown include:
    -   Run Count
    -   Last Run Started
    -   Last Run Ended
    -   Next Scheduled Run
    -   Current Sites
    -   Last Delay
    -   Exec Time
-   **Select Multiple**: Opens check boxes by each query in the list. You can check a box and the **Delete Selected** option is activated. This option deletes the selected queries. To turn off this option, select the **Actions** button again and select **Cancel Select Multiple**.

    ![Cancel multiple deletion](../images/cancel-multiples-action-menu.png)

-   **Create Default Auto Queries**: There are 5 default queries to choose from. Selecting this option opens the Create Auto Queries window. Select from the following default auto queries:

    -   **Console Hostname Lookup**: Reverses the DNS look up performed by Console.
    -   **Asset ICS Discovery**: Finds the ICS assets based on common open ports and queries using native protocols.
    -   **Location Set**: Sets a label and a location field using the Site name.
    -   **SNMP**: Queries to discover SNMP service. This tries only the SNMP port.
    -   **OS Detection**: Use with caution, especially in production environments. This query can disrupt or crash poorly configured or sensitive assets. Queries Linux / Windows endpoint for any discoverable services.
    ![Create default auto queries](../images/default-auto-queries-new.png)

-   **Quick Scans**: When selected, this selection displays a list of any current Quick Scans. You can create a Quick Scan by selecting the add icon ![](../../msi-console/image/add-icon-msi.jpg). Set the parameters of the Quick Scan in the Create Quick Scan page. Quick Scans are meant to run quickly and only once. Quick Scan targets can be assets selected by their URLs, IP Addresses, or IP ranges. See [Create a Quick Scan](ot-discovery-console-user-guide/task/create-quick-scan.md) for more information on Quick Scans.

