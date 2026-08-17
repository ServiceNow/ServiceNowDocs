---
title: Discovery Admin Workspace IP inventory
description: The IP inventory page centralizes the IP addresses, ranges, networks, and range sets that Discovery uses to scan your environment. Use it to review existing IP data and add entries to Discovery range sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/daw-ip-inventory.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Schedules, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery Admin Workspace IP inventory

The IP inventory page centralizes the IP addresses, ranges, networks, and range sets that Discovery uses to scan your environment. Use it to review existing IP data and add entries to Discovery range sets.

To access the IP inventory page, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **IP-based Discovery** &gt; **View inventory**.

You can also access the IP inventory page from the [Discovery Admin Workspace Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-admin-workspace-setup.md) page.

**Note:** The IP inventory page is available starting with Discovery Admin Workspace v1.19.0 and requires the Australia, Zurich Patch 8, or later release of the ServiceNow AI Platform.

## Key features

Each tab displays a list of IP data with the following controls:

-   **New**: Create IP data. For more information, see [Add IP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-data.md).
-   **Add to Range Set**: Map IP data to a range set. For more information, see [Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-range-set.md).
-   **Refresh** icon: Update the data
-   **Export**: Download the list as Excel, CSV, JSON, or PDF, or send it by email.
-   **More Actions** icon: Add or remove columns or coy the URL.

The following sections describe the IP data on each tab.

-   **IP Address Lists**

    The **IP Address Lists** tab displays your IP address lists, grouped by list. A list can contain both IPv4 and IPv6 addresses, but not IPv6 subnets or networks. An IP address can belong to more than one list. Discovery removes duplicate addresses at the start of a discovery when the lists are on the same schedule.

    \[Omitted image "daw-ip-address-lists.png"\] Alt text: IP Address Lists tab in IP inventory

    An IP address list requires a name. The Name column is hidden by default because existing records may not have a name. To add the Name column to the table, select the **More Actions** icon \(\[Omitted image "more-options-horizontal.png"\]\) and select **Personalize fields**.

-   **IP Ranges**

    The **IP Ranges** tab displays your IP ranges. If an IP range belongs to a range set used in multiple Discovery schedules, the Range Set column displays a **Multiple** label.

    \[Omitted image "daw-ip-ranges.png"\] Alt text: IP Ranges tab in IP inventory

    Select one or more IP ranges from the table to enable the **Add to Range Set** option. For more information, see [Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-range-set.md).

    **Note:** An IP range can belong to only one range set.

-   **IP Networks**

    The **IP Networks** tab displays your IP networks.

    \[Omitted image "daw-ip-networks.png"\] Alt text: IP Networks tab in IP inventory

    Select one or more IP ranges from the table to enable the **Add to Range Set** option. For more information, see [Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-range-set.md).

    **Note:** An IP range can belong to only one range set.

-   **Discovery Range Sets**

    The **Discovery Range Sets** tab displays your discovery range sets. A range set can be associated with one or more Discovery schedules.

    \[Omitted image "daw-range-sets.png"\] Alt text: Discovery Range Sets tab in IP inventory

    This tab doesn't include the **Add to Range Set** action, because the records are already range sets. Select **New** to create a range set.

-   **IPAM data**

    The **IPAM data** tab contains the **IP schedule mapping** and **Imported IPs** sections.

    The IP schedule mapping section contains the **IPv6 addresses** and **IPv4 subnets** tabs, which display the IPv6 addresses and IPv4 subnets that are mapped to auto-created Discovery schedules.

    The **Imported IPs** section contains the **IP addresses** and **IP subnets** tabs. These tabs display the IP addresses and IP subnets imported from your IPAM solutions.

    **Warning:** To avoid data corruption, don't edit or add IP data in the Imported IPs table.


**Related topics**  


[Discovery IP address configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/discovery-ip-address-configuration.md)

[Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-range-set.md)

