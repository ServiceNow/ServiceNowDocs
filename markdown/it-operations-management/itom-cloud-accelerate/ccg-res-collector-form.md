---
title: Cloud Configuration Governance Resource collector form
description: The Resource collector form contains detailed information about the resource collector.
locale: en-US
release: australia
product: ITOM Cloud Accelerate
classification: itom-cloud-accelerate
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Cloud Configuration Governance reference, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Cloud Configuration Governance Resource collector form

The Resource collector form contains detailed information about the resource collector.

<table id="table_tpl_3vy_gsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name that uniquely identifies the configuration key.

</td></tr><tr><td>

Scan mode

</td><td>

Level at which the resource collector imports the resource from the cloud.Supported values are as follows:

 -   **Run per LDC**: Import the resource at the datacenter level. That is, once from each datacenter.
-   **Run per service account**: Import the resource at the service account level.

</td></tr><tr><td>

Provider type

</td><td>

Cloud that hosts the resources to be imported.

</td></tr><tr><td>

Resource type

</td><td>

Cloud resource type that you want to import through the resource collector.If Cloud Configuration Governance doesn't contain the required resource type, you can create it as follows:

 1.  Select the lookup using list icon \(![Lookup using list icon.](../image/lookup-using-list.png)\).
2.  Select **New**.
3.  In the **Name** field, enter the cloud resource type.
4.  Select **Submit**.

</td></tr><tr><td>

Flow

</td><td>

Resource collector flow that can import the given resource type.

</td></tr></tbody>
</table>**Parent Topic:**[Cloud Configuration Governance reference](ccg-reference.md)

