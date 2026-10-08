---
title: Data mapping for Service Graph Connector for BlueCat
description: Data from the Service Graph Connector for BlueCat data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/service-graph-connectors/sgc-data-mapping-bluecat.html
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [BlueCat, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Data mapping for Service Graph Connector for BlueCat

Data from the Service Graph Connector for BlueCat data sources is mapped and transformed into the ServiceNow CMDB Configuration Item \(CI\) class definitions using the Robust Transform Engine \(RTE\). Data is inserted into the ServiceNow CMDB using the Identification and Reconciliation Engine \(IRE\).

## Data mapping for Service Graph Connector for BlueCat

When you complete setting up the connection, you can configure the integration to periodically pull data from BlueCat.

The following table lists the data sources, the staging tables, and the target tables as CMDB CI classes for the Service Graph Connector for BlueCat.

|Data source|Staging table|Target tables|
|-----------|-------------|-------------|
|SG-BlueCat-Networks|sn\_bluecat\_integ\_sg\_bluecat\_networks|[Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-classes.md)|
|SG-BlueCat-Blocks|sn\_bluecat\_integ\_sg\_bluecat\_blocks|[Managed IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-classes.md)|
|SG-BlueCat-Allocated IP Address|sn\_bluecat\_integ\_sg\_bluecat\_allocated\_ip\_address|[Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-classes.md)|
|SG-BlueCat-Configuration|sn\_bluecat\_integ\_sg\_bluecat\_configuration|[Managed Network \[cmdb\_ci\_managed\_network\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/service-graph-connectors/sgc-bluecat-classes.md)|

You can use the IntegrationHub ETL app to view the data maps. See [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) for more information.

