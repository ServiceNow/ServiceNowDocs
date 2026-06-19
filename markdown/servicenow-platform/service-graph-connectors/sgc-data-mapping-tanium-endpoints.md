---
title: Data mapping for Service Graph Connector for Tanium Endpoints
description: Data from the Tanium data sources is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-data-mapping-tanium-endpoints.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Tanium Endpoints

Data from the Tanium data sources is mapped and transformed into the ServiceNow CMDB configuration item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium.

**Important:** The Service Graph Connector for Tanium Endpoints populates the Computer class with user-facing endpoints, and doesn't import data from the Server child class. Use this connector if you don't require Server data. If you require Server data, use the Service Graph Connector for Tanium.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for Tanium.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

SG-Tanium-Endpoints Hardware-Software

</td><td>

SG-Tanium-Endpoints Hardware-Software \[sg\_tanium\_endpoints\_hardware\_software\]

</td><td>

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [Disk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [File System](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [Handheld Computing Device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 [Network Adapter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 When the Software Asset Management \(SAM\) application isn't installed:

-   [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)
-   [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

 When the SAM application is installed: [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-classes.md)

</td><td>

-

</td></tr><tr><td>

SG-Tanium-Endpoints Usage

</td><td>

SG-Tanium-Endpoints Usage \[sg\_tanium\_endpoints\_usage\]

</td><td>

Software Usage \[samp\_sw\_usage\]

</td><td>

The SG-Tanium Usage data source is available only when the Software Asset Management Professional plugin \(com.snc.samp\) plugin is activated on your ServiceNow instance. See .

</td></tr><tr><td>

SG-Tanium-Endpoints Remove Software

</td><td>

Integration Commons Remove Record \[sn\_cmdb\_int\_util\_remove\_record\]

</td><td>

None

</td><td>

The SG-Tanium Remove Software data source creates import sets and uses the transform map-based method for removing any target records for software data that weren't updated in the last delta query check. See [Managing CMDB data deletion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-integration-commons/cmdb-integ-record-removal.md).

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

