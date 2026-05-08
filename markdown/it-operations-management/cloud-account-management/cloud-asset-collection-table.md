---
title: Cloud Asset Collection table
description: Stores metadata of cloud assets collected from providers for IT operations.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Cloud Account Management reference, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Asset Collection table

Stores metadata of cloud assets collected from providers for IT operations.

A Cloud Asset Collection Table is a structured repository in IT Operations Management that stores and manages metadata of cloud resources collected from multiple cloud service providers. The table stores all discovered or synced cloud assets, such as virtual machines, storage buckets, and databases after collection from cloud environments.

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

High-level classification of collected cloud assets, such as Compute, Storage, Networking, Database, or Security.

</td></tr><tr><td>

Subcategory

</td><td>

Granular classification under the main category. Examples include Virtual Machines, Containers, and Functions under Compute; Block Storage, Object Storage, and File Storage under Storage.

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

</td></tr><tr><td>

Comments

</td><td>

Free-text field for notes or context about the configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Account Management reference](../reference/cam-reference.md)

