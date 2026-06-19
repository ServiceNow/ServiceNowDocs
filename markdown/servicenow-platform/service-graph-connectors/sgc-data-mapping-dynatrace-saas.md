---
title: Data mapping for Service Graph Connector for Observability - Dynatrace SaaS
description: Data from the Dynatrace data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgc-data-mapping-dynatrace-saas.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-06-03"
reading_time_minutes: 1
breadcrumb: [Observability - Dynatrace SaaS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for Observability - Dynatrace SaaS

Data from the Dynatrace data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

When you complete setting up the connection, you can configure the integration to periodically pull data from Dynatrace.

**Important:** The Service Graph Connector for Observability - Dynatrace SaaS is designed for the Dynatrace SaaS \(3rd‑generation\) platform and leverages DQL-based APIs and the Grail architecture to import data from Dynatrace into the CMDB. If you're in a Dynatrace managed \(self‑hosted\) or legacy SaaS environment, you should use the Service Graph Connector for Observability - Dynatrace.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for Dynatrace.

<table id="table_data_mapping" class="custom-rows"><thead><tr><th class="filter">

Data source

</th><th>

Staging table

</th><th>

Target tables

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

SGO-Dynatrace SaaS Frontend

</td><td>

SGO-Dynatrace SaaS Frontend \[sn\_dynatrace\_saas\_sgo\_dynatrace\_saas\_frontend\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

</td><td>

-

</td></tr><tr><td>

SGO-Dynatrace SaaS Host

</td><td>

SGO-Dynatrace SaaS Host \[sn\_dynatrace\_saas\_sgo\_dynatrace\_saas\_host\]

</td><td>

[Computer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md) [IP Address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

[Serial Number](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

[Key Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

When the Software Asset Management \(SAM\) application isn't installed:

-   [Software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)
-   [Software Instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

When the SAM application is installed: [Software Installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

</td><td>

Host classification: Depending on the operating system \(OS\), data is imported into the Linux Server \[cmdb\_ci\_linux\_server\], Windows Server \[cmdb\_ci\_win\_server\], AIX Server \[cmdb\_ci\_aix\_server\], or Solaris Server \[cmdb\_ci\_solaris\_server\] classes. For other OS types, the data is imported into the Computer \[cmdb\_ci\_computer\] class.

</td></tr><tr><td>

SGO-Dynatrace SaaS Processes

</td><td>

SGO-Dynatrace SaaS Processes \[sn\_dynatrace\_saas\_sgo\_dynatrace\_saas\_processes\]

</td><td>

[Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

</td><td>

The target table is populated using Application Dependency Mapping \(ADM\). ADM classifies the processes based on the attributes in the Process Classification \[discovery\_classy\_proc\] table. To learn about process classification, see Discovery classifiers.

</td></tr><tr><td>

SGO-Dynatrace SaaS Service

</td><td>

SGO-Dynatrace SaaS Service \[sn\_dynatrace\_saas\_sgo\_dynatrace\_saas\_service\]

</td><td>

[Calculated Application Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-classes.md)

</td><td>

-

</td></tr></tbody>
</table>You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

