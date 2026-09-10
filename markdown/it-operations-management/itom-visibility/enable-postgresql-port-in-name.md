---
title: Include the port number in PostgreSQL instance names
description: You can make multiple PostgreSQL instances on the same host distinguishable by port number by creating the mid.discovery.postgresql.include\_port\_in\_name MID Server property. This property is supported for UNIX hosts only.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/enable-postgresql-port-in-name.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-08-23"
reading_time_minutes: 1
keywords: [PostgreSQL discovery, PostgreSQL instance name, horizontal discovery, cmdb\_ci\_db\_postgresql\_instance, MID Server property]
breadcrumb: [PostgreSQL, Database discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Include the port number in PostgreSQL instance names

You can make multiple PostgreSQL instances on the same host distinguishable by port number by creating the **mid.discovery.postgresql.include\_port\_in\_name** MID Server property. This property is supported for UNIX hosts only.

## Before you begin

Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.

Role required: mid\_server, agent\_admin, or agent\_security\_admin

## About this task

By default, Discovery assigns every PostgreSQL instance the display name **instance@hostname**, regardless of port, making multiple instances on the same host indistinguishable in list views. The **mid.discovery.postgresql.include\_port\_in\_name** MID Server property controls this behavior. When created and set to true, Discovery uses the format **instance-port-tcp\_port@hostname** instead \(for example, **postgres-port-5432@host**\). Existing CI records aren't affected.

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Properties**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter `mid.discovery.postgresql.include_port_in_name`.|
    |Value|Enter `true`.|
    |MID server|MID Servers to use for the property. Leave this field empty to apply the property to all MID Servers.|

4.  Select **Submit**.


## What to do next

Run Discovery again to apply the change.

**Parent Topic:**[PostgreSQL discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DiscoverPostgreSQLInstances.md)

**Related topics**  


[PostgreSQL discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/r_DiscoverPostgreSQLInstances.md)

