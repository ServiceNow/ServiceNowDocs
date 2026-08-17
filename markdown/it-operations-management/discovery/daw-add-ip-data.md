---
title: Add IP data
description: Use the New IP data dialog in the IP inventory page to add IP addresses, ranges, networks, or range sets to your discovery configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/daw-add-ip-data.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 2
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Add IP data

Use the New IP data dialog in the IP inventory page to add IP addresses, ranges, networks, or range sets to your discovery configuration.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace v1.19.0 must be installed.
-   The ServiceNow AI Platform must be running the Australia release, or the Zurich release starting with Patch 8.

Role required: discovery\_admin

## About this task

The New IP data dialog is shared across the **IP Address Lists**, **IP Ranges**, **IP Networks**, and **Discovery Range Sets** tabs. When you open the dialog from a tab, the check box for that tab is selected automatically. The system removes duplicate entries automatically.

For collection types and format details, see [Discovery IP address configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-ip-address-configuration.md). To view and manage your entries, see [Discovery Admin Workspace IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-ip-inventory.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **IP-based discovery**.

2.  Select **View inventory** from the IP inventory section.

3.  Select the tab that contains the IP data to add, such as **IP Address Lists**.

4.  Select **New**.

    A New IP data dialog displays.

    \[Omitted image "new-ip-data.png"\] Alt text: New IP data dialog

5.  Enter the required information for each IP data type you're adding.

<table id="choicetable_pxd_mzd_ckc"><thead><tr><th align="left" id="d230912e155">

IP data type

</th><th align="left" id="d230912e158">

What to enter

</th></tr></thead><tbody><tr><td id="d230912e164">

**IP address list**

</td><td>

Enter a name, then enter one or more IP addresses separated by commas.

</td></tr><tr><td id="d230912e173">

**IP ranges**

</td><td>

Enter each range as startIP-endIP, separated by commas. For example: `10.0.0.1-10.0.0.254`

</td></tr><tr><td id="d230912e186">

**IP networks**

</td><td>

Enter each network in CIDR notation, separated by commas. For example: `192.168.1.0/24`

</td></tr><tr><td id="d230912e199">

**Discovery range set**

</td><td>

Enter a name, then enter any mix of addresses, ranges, or networks, separated by commas.

</td></tr></tbody>
</table>6.  Select the check box for each additional IP data type to add.

    **Note:** If you open the New IP data dialog from the **Discovery Range Sets** tab, you can add data only as a range set.

7.  For an IP range, IP network, or range set, select the **Active** toggle switch to turn the entry on or off.

8.  To save your entered data in a range set, select the check box, then either search for an existing range set or select **Create a new Range Set** and enter a name.

9.  Select **Save**.

    The New IP data dialog closes.

10. Select the **Refresh** icon \(\[Omitted image "daw-refresh-icon.png"\]\) to view the new data in the IP Address Lists \[discovery\_range\_item\_ip\] table.


**Related topics**  


[Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-add-ip-range-set.md)

