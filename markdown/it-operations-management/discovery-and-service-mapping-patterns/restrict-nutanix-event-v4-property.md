---
title: Restrict Nutanix v4 event discovery to specific Prism Centrals
description: Create a MID Server property to target specific Prism Central instances for Nutanix v4 event discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/restrict-nutanix-event-v4-property.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-05-18"
reading_time_minutes: 2
breadcrumb: [Nutanix Acropolis, Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Restrict Nutanix v4 event discovery to specific Prism Centrals

Create a MID Server property to target specific Prism Central instances for Nutanix v4 event discovery.

## Before you begin

-   Verify that you have at least version 1.31.0 of Discovery and Service Mapping Patterns.
-   Verify that Nutanix Components discovery has run and that the Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\] table is populated.
-   Verify that the MID Servers for Nutanix event discovery have **All** or **Nutanix** capability.

Role required: discovery\_admin.

## About this task

By default, Nutanix v4 event discovery runs against all Prism Central instances in the Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\] table, using any MID Server with the **All** or **Nutanix** capability. Starting with Discovery and Service Mapping Patterns version 1.31.0, you can create a MID Server property to target specific Prism Central instances. You can create multiple properties for different Prism Central and MID Server combinations.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Select **New**.

3.  Fill in the form.

<table id="table_nutanix_events_v4_property_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Property name. Enter `sn_itom_pattern.nutanix_events_v4.prism_ips`.

</td></tr><tr><td>

Value

</td><td>

Comma-separated list of IP addresses or hostnames of the Prism Central instances to target.The instances must already be present in the Nutanix Prism Central \[cmdb\_ci\_nutanix\_prism\_central\] table.

</td></tr><tr><td>

MID server

</td><td>

MID Server to use for these Prism Central instances. Leave empty to use any MID Server with the **All** or **Nutanix** capability.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Enable the Nutanix event discovery scheduled job. For more information, see [Enable Nutanix event discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-nutanix-event-job.md).

**Parent Topic:**[Nutanix Acropolis discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

**Related topics**  


[Nutanix Acropolis discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/nutanix-pattern.md)

[Enable Nutanix event discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/enable-nutanix-event-job.md)

