---
title: VMs on undiscovered servers list in Cloud Migration Assessment
description: Cloud Migration Assessment presents information on virtual machines hosted by undiscovered servers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/cloud-migration-vm-undiscovered-list.html
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud Migration Assessment reference, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# VMs on undiscovered servers list in Cloud Migration Assessment

Cloud Migration Assessment presents information on virtual machines hosted by undiscovered servers.

## Information available in the VMs on undiscovered servers list

<table id="table_kmv_8972jedw"><thead><tr><th>

Column \(from left to right\)

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the virtual machine \(VM\) instance.

</td></tr><tr><td>

VM Instance

</td><td>

The name of the VM instance. For VMs discovered without a server that hosts them, the VM Instance and the Name fields are the same.

</td></tr><tr><td>

State

</td><td>

The state of the VM.-   On
-   Off
-   Paused
-   Scheduled
-   Starting
-   Stopping
-   Retired
-   Terminated
-   Error
-   Canceled
-   Pausing
-   Terminating

</td></tr><tr><td>

State

</td><td>

The server assignment state: -   Assigned - The server is assigned to an assessment task.
-   Unassigned - The server is not assigned to an assessment task
-   Ignored - The server is on the ignored list.

</td></tr><tr><td>

IP Address

</td><td>

The IP address of the server.

</td></tr><tr><td>

Manufacturer

</td><td>

The manufacturer of the server.

</td></tr><tr><td>

CPUs

</td><td>

The number of server CPUs.

</td></tr><tr><td>

Memory \(MB\)

</td><td>

The VM memory size.

</td></tr><tr><td>

IT Environment

</td><td>

The current IT environment containing this VM instance. -   On-Premises
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

</td></tr></tbody>
</table>## List actions

<table id="id_ths_tx4_zrb"><thead><tr><th>

Button

</th><th>

Action

</th></tr></thead><tbody><tr id="refresh-list-button"><td>

Refresh list \[Omitted image "list-refresh-button.png"\] Alt text: Refresh list button

</td><td>

Refreshes the list to display the most updated information.

</td></tr><tr id="list-actions-butons"><td>

List actions \[Omitted image "list-actions-button.png"\] Alt text: List actions button

</td><td>

Selects actions supported for this list:-   **Edit columns** - Adjusts the list to display required columns in the order you choose.
-   **Save as** - Creates a copy of this list and save it under **My Lists**.
-   **Reset widths** - Returns the column width to default.

</td></tr><tr id="copy-url-button"><td>

Copy Url \[Omitted image "list-copy-url-button.png"\] Alt text: Copy URL button

</td><td>

Copies the URL for this list.

</td></tr><tr id="show-filter-button"><td>

Show filter panel \[Omitted image "show-filter-panel-button.png"\] Alt text: Show filter panel button

</td><td>

Displays the filter panel on the right. If there are filters applied to the list, the Show filter panel button has the number of active filters.

</td></tr><tr id="export-button"><td>

Export

</td><td>

Saves the list in one of the supported formats: Excel, CSV, JSON, PDF.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Migration Assessment reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/cloud-migration-reference.md)

