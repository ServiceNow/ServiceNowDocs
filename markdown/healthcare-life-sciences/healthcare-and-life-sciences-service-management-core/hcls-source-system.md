---
title: Source system table
description: The Source system \[sn\_hcls\_source\_system\] table stores the source and destination IDs of an external healthcare system in your ServiceNow instance.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data model tables, Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Source system table

The Source system \[sn\_hcls\_source\_system\] table stores the source and destination IDs of an external healthcare system in your ServiceNow instance.

## Key features

-   All Healthcare and Life Sciences Service Management Core data tables contain a reference to the Source system \[sn\_hcls\_source\_system\] table.
-   Includes the source and destination IDs of external EMR systems or another healthcare system.

Role required to configure the table: sn\_hcls.admin.

For more information, see [Healthcare and Life Sciences data model](../concept/hcls-serv-mgmt-core-1.md).

<table id="table_mbn_w11_ftb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source ID

</td><td>

ID of the external Redox healthcare system used for processing an inbound API response from the system to your ServiceNow instance.

</td></tr><tr><td>

Destination ID

</td><td>

ID of the external Redox healthcare system used for sending an outbound API request to the system from your ServiceNow instance.

</td></tr><tr><td>

Source

</td><td>

Name to identify the external Redox healthcare system as a source system in your ServiceNow instance.

</td></tr></tbody>
</table>**Parent Topic:**[Healthcare and Life Sciences data model tables](hcls-healthcare-data-tables.md)

