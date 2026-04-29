---
title: Life cycle management of records in Service Graph Connector for Microsoft Defender Endpoint
description: Life cycle management in the Service Graph Connector for Microsoft Defender Endpoint monitors and updates the statuses of Microsoft Defender for Endpoint resources throughout their entire life cycle, from creation to deletion.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Microsoft Defender for Endpoint, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle management of records in Service Graph Connector for Microsoft Defender Endpoint

Life cycle management in the Service Graph Connector for Microsoft Defender Endpoint monitors and updates the statuses of Microsoft Defender for Endpoint resources throughout their entire life cycle, from creation to deletion.

The life cycle management process helps maintain the accuracy and integrity of data in the Configuration Management Database \(CMDB\).

## Life cycle management for CIs in Service Graph Connector for Microsoft Defender Endpoint

The following table lists the configuration items \(CIs\) in CMDB and other non-CMDB tables for which life cycle management is available in the Service Graph Connector for Microsoft Defender Endpoint. The Install Status \[install\_status\] attribute of the CIs is updated to installed or retired according to the state of the CI.

|Data source|CIs|Life cycle management available|
|-----------|---|-------------------------------|
|SG-Defender Machines|Windows Server \[cmdb\_ci\_win\_server\]|Yes|
|SG-Defender Machines|IP Address \[cmdb\_ci\_ip\_address\]|Yes|
|SG-Defender Machines|Network Adapter \[cmdb\_ci\_network\_adapter\]|Yes|
|SG-Defender Machines|Computer \[cmdb\_ci\_computer\]|Yes|

