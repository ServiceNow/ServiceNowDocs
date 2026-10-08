---
title: Data mapping for Service Graph Connector for Tanium Atlas
description: Data from the Tanium Atlas data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-data-mapping-tanium-atlas.html
release: brazil
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [Tanium Atlas, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Tanium Atlas

Data from the Tanium Atlas data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Service Graph Connector for Tanium Atlas

When you complete setting up the connection, you can configure the integration to periodically pull data from Tanium Atlas.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for the Service Graph Connector for Tanium Atlas.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th></tr></thead><tbody><tr><td>

SG-Tanium-Atlas Hardware-Software

</td><td>

sg\_tanium\_atlas\_hardware\_software

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md) [Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [File System 1 - Computer \[cmdb\_ci\_file\_system\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Disk 1 - Computer \[cmdb\_ci\_disk\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr><tr><td>

SG-Tanium-Atlas Remove Software

</td><td>

sn\_cmdb\_int\_util\_remove\_record

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr><tr><td>

SG-Tanium-Atlas Hardware Delta

</td><td>

sg\_tanium\_atlas\_hardware\_software

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md) [Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [File System 1 - Computer \[cmdb\_ci\_file\_system\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Disk 1 - Computer \[cmdb\_ci\_disk\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr><tr><td>

SG-Tanium-Atlas Identity-Network

</td><td>

sg\_tanium\_atlas\_hardware\_software

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md) [Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [File System 1 - Computer \[cmdb\_ci\_file\_system\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Disk 1 - Computer \[cmdb\_ci\_disk\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr><tr><td>

SG-Tanium-Atlas Usage

</td><td>

sg\_tanium\_atlas\_usage

</td><td>

SG-Tanium-Atlas Usage

</td></tr><tr><td>

SG-Tanium-Atlas Installed Applications

</td><td>

sg\_tanium\_atlas\_hardware\_software

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md) [Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [File System 1 - Computer \[cmdb\_ci\_file\_system\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Disk 1 - Computer \[cmdb\_ci\_disk\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr><tr><td>

SG-Tanium-Atlas Additional Sensors

</td><td>

sg\_tanium\_atlas\_hardware\_software

</td><td>

[Software 1 - Computer \[cmdb\_ci\_spkg\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md) [Virtual Machine Instance 2 - Handheld Computing Device \[cmdb\_ci\_vm\_instance\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Computer \[cmdb\_ci\_computer\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [File System 1 - Computer \[cmdb\_ci\_file\_system\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Disk 1 - Computer \[cmdb\_ci\_disk\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Network Adapter \[cmdb\_ci\_network\_adapter\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [IP Address 2 - Handheld Computing Device \[cmdb\_ci\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

 [Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-atlas-classes.md)

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

