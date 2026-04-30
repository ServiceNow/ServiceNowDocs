---
title: Direct JDBC Probe
description: A direct JDBC probe specifies all the parameters necessary in the outbound ECC Queue XML payload.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [JDBCProbe, Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Direct JDBC Probe

A direct JDBC probe specifies all the parameters necessary in the outbound ECC Queue XML payload.

It is a standalone probe that is decoupled from a JDBC Data Source and does not insert into an import set. The required field in the ECC Queue record for a direct JDBC probe is **Topic** and it must equal **JDBCProbe**. The **Source** field is reserved for the `sys_id` of the data source record in the case of a JDBC data source.

**Note:** If you have ServiceNow Discovery enabled on your platform, add the **skip\_sensor** parameter to the probe to avoid the discovery sensors from processing the probe and resulting in a "No sensors defined" error.

## XML Structure

A direct JDBC probe has the following XML payload structure

```
<parameters><parameter name = "skip_sensor" value = "true" /><parameter name = "parameter_name" value = "parameter_value" />
  ...
  <parameter name = "work" ><select  ... >
      ...
    </select></parameter></parameters>
```

**Parent Topic:**[JDBCProbe](../task/t_JDBCProbe.md)

**Related topics**  


[JDBCProbe](../task/t_JDBCProbe.md)

