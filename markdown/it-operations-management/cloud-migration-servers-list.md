---
title: Server list in Cloud Migration Assessment
description: Cloud Migration Assessment presents information on server resources in several lists: All servers, Windows servers, and Linux servers.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Cloud Migration Assessment reference, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Server list in Cloud Migration Assessment

Cloud Migration Assessment presents information on server resources in several lists: All servers, Windows servers, and Linux servers.

## Information available on the Server list in Cloud Migration Assessment

<table id="table_kmv_lbt_vrb"><thead><tr><th>

Column \(from left to right\)

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the resource: The server or the server together with its VM.

</td></tr><tr><td>

Server

</td><td>

The server name.

</td></tr><tr><td>

IP Address

</td><td>

The IP address of the server.

</td></tr><tr><td>

Operating System

</td><td>

The operating system of the server.

</td></tr><tr><td>

Manufacturer

</td><td>

The manufacturer of the server.

</td></tr><tr><td>

Discovery source

</td><td>

The application that discovered the server: -   ServiceNow - horizontal discovery by Discovery.
-   ServiceWatch - top-down discovery by Service Mapping.
-   Other options if third-party applications are deployed.

</td></tr><tr><td>

CPU count

</td><td>

The number of server CPIs.

</td></tr><tr><td>

Cluster

</td><td>

The name of the cluster containing the server.

</td></tr><tr><td>

State

</td><td>

The server assignment: -   Assigned - The server is assigned to an assessment task.
-   Unassigned - The server is not assigned to an assessment task.
-   Ignored - The server is hidden from the lists.

</td></tr><tr><td>

IT Environment

</td><td>

The current IT environment containing this server:-   On-Premises
-   Cloud

</td></tr><tr><td>

Category

</td><td>

The server category: -   Physical Server
-   VMware Virtualization
-   Hyper-V Virtualization
-   IBM HMC Virtualization
-   OpenStack Virtualization
-   Solaris Virtualization
-   Nutanix Virtualization
-   AWS
-   Microsoft Azure
-   Google Cloud
-   IBM Cloud

</td></tr><tr><td>

VM Instance

</td><td>

The virtual machine \(VM\) instance that is registered on the server.

</td></tr><tr><td>

IP Address

</td><td>

The IP address of the VM instance.

</td></tr><tr><td>

Manufacturer

</td><td>

The manufacturer of the VM.

</td></tr><tr><td>

CPUs

</td><td>

The number of VM instance CPUs.

</td></tr><tr><td>

Memory \(MB\)

</td><td>

The server memory size.

</td></tr></tbody>
</table>## List actions

<table id="id_ths_tx4_zrb"><thead><tr><th>

Button

</th><th>

Action

</th></tr></thead><tbody><tr id="refresh-list-button"><td>

Refresh list ![Refresh list button](../image/list-refresh-button.png)

</td><td>

Refreshes the list to display the most updated information.

</td></tr><tr id="list-actions-butons"><td>

List actions ![List actions button](../image/list-actions-button.png)

</td><td>

Selects actions supported for this list:-   **Edit columns** - Adjusts the list to display required columns in the order you choose.
-   **Save as** - Creates a copy of this list and save it under **My Lists**.
-   **Reset widths** - Returns the column width to default.

</td></tr><tr id="copy-url-button"><td>

Copy Url ![Copy URL button](../image/list-copy-url-button.png)

</td><td>

Copies the URL for this list.

</td></tr><tr id="show-filter-button"><td>

Show filter panel ![Show filter panel button](../image/show-filter-panel-button.png)

</td><td>

Displays the filter panel on the right. If there are filters applied to the list, the Show filter panel button has the number of active filters.

</td></tr><tr id="export-button"><td>

Export

</td><td>

Saves the list in one of the supported formats: Excel, CSV, JSON, PDF.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Migration Assessment reference](cloud-migration-reference.md)

**Related topics**  


[Assign resources to assessment tasks in Configurable Workspace](../task/migration-assign-resource-task.md)

[Create assessment tasks for cloud migration in Configurable Workspace](../task/create-assessment-task.md)

[Review detailed server information in Configurable Workspace](../task/migration-review-server-info.md)

