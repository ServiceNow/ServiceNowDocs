---
title: Add IP data to a range set
description: Use the IP inventory page in Discovery Admin Workspace to add IP ranges or networks to a new or existing range set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/daw-add-ip-range-set.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Discovery IP address configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Add IP data to a range set

Use the IP inventory page in Discovery Admin Workspace to add IP ranges or networks to a new or existing range set.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace v1.19.0 must be installed.
-   The ServiceNow AI Platform must be running the Australia release, or the Zurich release starting with Patch 8.

Role required: discovery\_admin

## About this task

The **Add to Range Set** action is available on the **IP Ranges** and **IP Networks** tabs of the IP Inventory page in Discovery Admin Workspace. Select it to add existing IP data to a new or existing range set. The system removes duplicate entries automatically.

**Note:** To avoid performance issues, limit Discovery schedules to a maximum range of /16 \(approximately 65,536 IPs\). For better performance, consider splitting the range into smaller segments.

For collection types and format details, see [Discovery IP address configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/discovery-ip-address-configuration.md). To view and manage your range sets, see [Discovery Admin Workspace IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-ip-inventory.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules** &gt; **IP-based discovery**.

2.  Select **View inventory** from the IP inventory section.

3.  Select the tab that contains the IP data to add, such as **IP Ranges**.

4.  Select the check box for each row to add.

5.  Select **Add to Range Set**.

    The Add to Range Set dialog displays.

    \[Omitted image "add-range-set.png"\] Alt text: Add to Range Set dialog

6.  Search for and select an existing range set.

    To create a range set instead, select **Create a new Range Set** and enter a name.

7.  Select **Save**.

    The Add to Range Set dialog closes.

8.  Select the **Refresh** icon \(\[Omitted image "daw-refresh-icon.png"\]\) to view the new data in the IP Ranges \[discovery\_range\_item\] table.


**Related topics**  


[Add IP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-add-ip-data.md)

