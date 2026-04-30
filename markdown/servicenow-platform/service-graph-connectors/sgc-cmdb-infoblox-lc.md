---
title: Life cycle management of records in Service Graph Connector for Infoblox
description: Life cycle management in the Service Graph Connector for Infoblox monitors and updates the statuses of Infoblox resources throughout their life cycle, from creation to deletion.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Reference, Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle management of records in Service Graph Connector for Infoblox

Life cycle management in the Service Graph Connector for Infoblox monitors and updates the statuses of Infoblox resources throughout their life cycle, from creation to deletion.

The life cycle management process helps maintain the accuracy and integrity of data in the Configuration Management Database \(CMDB\).

Soft deletion of Infoblox configuration items \(CIs\) is implemented in Service Graph Connector for Infoblox version 1.5.0 and later. The **operational\_status** attribute of CIs is updated from `operational` to `retired` for CIs that aren't discovered during the latest pull. You can decide whether to delete or retain the retired CIs.

Life cycle management is supported for the following tables:

-   Managed Network \[cmdb\_ci\_managed\_network\]
-   IP Pool \[cmdb\_ci\_ip\_pool\]
-   Subnet \[cmdb\_ci\_ip\_network\_subnet\]
-   Detailed Network \[sn\_infoblox\_integ\_sg\_infoblox\_detailed\_subnetwork\]
-   Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]

**Parent Topic:**[Service Graph Connector for Infoblox reference](sgc-cmdb-infoblox-reference.md)

