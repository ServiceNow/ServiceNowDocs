---
title: Cloud Asset Collection Configs table
description: The Cloud Asset Collection Configs table is a structured repository in IT Operations Managementthat stores and manages metadata of cloud resources collected from multiple cloud service providers for IT operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/cloud-account-management/cloud-asset-collection-table.html
release: brazil
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-11-19"
reading_time_minutes: 1
breadcrumb: [Reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Asset Collection Configs table

The Cloud Asset Collection Configs table is a structured repository in IT Operations Managementthat stores and manages metadata of cloud resources collected from multiple cloud service providers for IT operations.

The table stores all discovered or synced cloud assets, such as virtual machines, storage buckets, and databases after collection from cloud environments.

Cloud asset explorer collects assets only from the CI classes that are marked active in this table. You can't add new records to the table. See [Configure the Cloud Asset Collection Configs table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/configure-cloud-asset-collection-table.md) for steps to update a record . To see how the collected assets are listed, see [Viewing cloud assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/viewing-cloud-assets.md).

<table id="table_yk2_dlc_kgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Indicates whether this specific cloud asset collection configuration is enabled or turned off.-   True – The configuration is active for the selected CI. It has been processed and populated in the flat table, and assets are collected according to the defined schedule.
-   False – The configuration is inactive, and no assets are collected.

</td></tr><tr><td>

Category

</td><td>

High-level classification of collected cloud assets such as Compute, Database, Container, Load balancer and network, or Storage.

</td></tr><tr><td>

Subcategory

</td><td>

Granular classification under the main category. Examples include Virtual machines and Functions under Compute; Databases under Database; Cloud load balancers under Load balancer and network; and Storage volumes and Cloud object storage instances under Storage.

</td></tr><tr><td>

CI Class Name

</td><td>

CMDB class where collected assets are stored such as `cmdb_ci_vm_instance` for virtual machines.

</td></tr><tr><td>

Provider

</td><td>

Cloud service provider from which assets are collected.

</td></tr><tr><td>

Last Processed Time

</td><td>

Timestamp of the last successful Asset Collection run.Useful for:

-   Tracking data freshness
-   Troubleshooting delays or failures
-   Reprocessing the CI class: Clear this field, and the next run processes all records from the CI class.

</td></tr><tr><td>

Comments

</td><td>

Text field for notes or context about the configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Account Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cloud-account-management/cam-reference.md)

