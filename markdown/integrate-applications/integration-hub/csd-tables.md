---
title: Tables installed
description: These tables are installed with the Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\).
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with client software distribution, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Tables installed

These tables are installed with the Client Software Distribution plugin \(com.snc.orchestration.client\_sf\_distribution\).

|Table|Description|
|-----|-----------|
|Client Software Distribution Catalog Item \[sn\_client\_sf\_dist\_cat\_item\]|Contains all catalog items created for client software distribution. This table extends the Catalog Item \[sc\_cat\_item\] table.|
|Client Software Distribution Software Request \[sn\_client\_sf\_dist\_req\_software\]|Contains all requested software, and their statuses.|
|Client Software Distribution Application \[sn\_client\_sf\_dist\_application\]|Contains all discovered CSD applications.|
|Client Software Distribution Provider \[sn\_client\_sf\_dist\_provider\]|Contains all software distribution providers.|
|Client Software Distribution Extension Key \[sn\_client\_sf\_dist\_extension\_key\]|Contains the predefined CSD extension keys.|
|Client Software Distribution Extension Point \[sn\_client\_sf\_dist\_extension\_point\]|Contains the customization script for the extension keys.|
|Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\]|Base table for all software provider configurations.|
|SCCM Server Instance \[sn\_client\_sf\_dist\_cmdb\_ci\_sccm\_server\]|Contains all SCCM server instances. This table extends the Configuration Item \[cmdb\_ci\] table.|
|SCCM Application \[sn\_client\_sf\_dist\_sccm\_application\]|Contains all discovered SCCM applications. This table extends the Client Software Distribution Application \[sn\_client\_sf\_dist\_application\] table.|
|SCCM Application Catalog Item \[sn\_client\_sf\_dist\_sccm\_app\_cat\_item\]|Contains all catalog items created for SCCM applications. This table extends the Client Software Distribution Catalog Item \[sn\_client\_sf\_dist\_cat\_item\] table.|
|SCCM Collection \[sn\_client\_sf\_dist\_sccm\_collection\]|Contains all discovered SCCM collections. Contains all discovered SCCM collections.|
|SCCM Deployment \[sn\_client\_sf\_dist\_sccm\_deployment\]|Contains all discovered SCCM deployments. Contains all discovered SCCM deployments.|
|SCCM Configuration \[sn\_client\_sf\_dist\_sccm\_config\]|Contains the SCCM application, install and uninstall collections, and Discovery model. This table extends the Client Software Distribution Software Configuration \[sn\_client\_sf\_dist\_software\_config\]|

**Parent Topic:**[Components installed with client software distribution](comp-installed-csd-ihub.md)

