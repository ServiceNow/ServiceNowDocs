---
title: Data mapping for SolarWinds
description: Data from the SolarWinds data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-data-mapping-solarwinds.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-04"
reading_time_minutes: 1
breadcrumb: [SolarWinds, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for SolarWinds

Data from the SolarWinds data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for SolarWinds

When you complete setting up the connection, you can configure the integration to periodically pull data from SolarWinds.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for SolarWinds.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-SolarWinds MS SQL Servers

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_ms\_sql\_servers

</td><td>

[Hardware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[MS SQL Database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[MSFT SQL Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds CPU

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_cpu

</td><td>

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Hardware

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_hardware

</td><td>

[Software Package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md) [Hardware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Software

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_software

</td><td>

[Software Package](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds IIS

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_iis

</td><td>

[Hardware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[IIS Virtual Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Microsoft IIS Web Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Disk

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_disk

</td><td>

[Hardware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[Disk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Network Adapter

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_network\_adapter

</td><td>

[Hardware](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[Network Adapter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Cloud Volumes

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_cloud\_volumes

</td><td>

[Storage Volume](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[Logical Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[VM Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr><tr><td>

SG-SolarWinds Cloud

</td><td>

sn\_solarwinds\_inte\_solarwinds\_cmdb\_cloud

</td><td>

[Image](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)[Hardware Type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Availability Zone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Logical Datacenter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Cloud Network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[VM Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Cloud KeyPair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Cloud Subnet](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

[Cloud Service Account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/cmdb-solarwinds-classes.md)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

