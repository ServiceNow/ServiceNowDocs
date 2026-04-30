---
title: Configure Service Mapping to work with the Configuration Management Database \(CMDB\)
description: Configure Service Mapping to use the existing data within your CMDB to run top-down discovery and map application services.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Advanced Service Mapping configuration, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Configure Service Mapping to work with the Configuration Management Database \(CMDB\)

Configure Service Mapping to use the existing data within your CMDB to run top-down discovery and map application services.

## Before you begin

Verify that the necessary tables are populated with data according to the process explained in [CMDB-based mapping](../concept/cmdb-based-mapping.md).

-   Transmission Control Protocol \(TCP\) Connection \[cmdb\_tcp\] table
-   Running Process \[cmdb\_running\_process\] table
-   Hardware \[cmdb\_ci\_hardware\] table

Confirm that you have installed the Service Mapping Plus August 2024 version from the ServiceNow® Store.

Role required: service\_mapping\_admin

## Procedure

1.  Enter `sys_properties.list` in the navigation filter.

2.  In the System Properties \[sys\_properties\] table, search for the **sa.topdown.enable\_cmdb\_based\_mapping** property.

3.  Set the **sa.topdown.enable\_cmdb\_based\_mapping** system property to configure Service Mapping to use the data in your CMDB.

    1.  Confirm that the **Type** field value is set to true\|false.

    2.  Set the **Value** field to `true`.


