---
title: SolarWinds properties
description: SolarWinds properties control the behavior of the connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-solarwinds-properties.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 1
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# SolarWinds properties

SolarWinds properties control the behavior of the connector.

## System properties

These system properties are available for SolarWinds.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_sys_props_solarwinds"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_solarwinds\_inte.monetize.url

</td><td>

-   Type: string
-   Default value: `https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/it-operations-management-overview.pdf`
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_solarwinds\_inte.page\_size

</td><td>

The number of records to fetch in a SolarWinds API call-   Type: integer
-   Default value: `10000`
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>