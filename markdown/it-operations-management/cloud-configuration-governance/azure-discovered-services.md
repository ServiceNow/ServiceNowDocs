---
title: Service categories discovered in Azure
description: The Discovery process discovers Microsoft Azure services.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud accounts, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Service categories discovered in Azure

The Discovery process discovers Microsoft Azure services.

## Services categories discovered in Azure

**Note:**

The CAPI-based discovery method is deprecated. Follow [Migrate from CAPI to Patterns](../../discovery/task/migrate-from-capi-to-pattern.md) for more information.

|Service Category|Name|CI Class|Pattern|Product|
|----------------|----|--------|-------|-------|
| |Azure Datacenter|cmdb\_ci\_azure\_datacenter| | |
| |Azure Subscription|cmdb\_ci\_cloud\_service\_account| | |
| |Cloud Resource|cmdb\_ci\_cmp\_resource| | |
|Application Services|Microsoft \(Unknown Resource Type\)| | |Microsoft \(Unknown Product\)|
|Application Services|Microsoft.ApiManagement/service| | |Microsoft.ApiManagement|
|Application Services|Microsoft.Cache| | |Microsoft.Cache|
|Application Services|Microsoft.Web/serverFarms| | |Microsoft.Web|
|Application Services|Microsoft.Web/sites|cmdb\_ci\_cloud\_webserver| |Microsoft.Web|
|Compute|Microsoft.Compute/availabilitySets|cmdb\_ci\_availability\_zone| |Microsoft.Compute|
|Compute|Microsoft.Compute/images|cmdb\_ci\_os\_template| |Microsoft.Compute|
|Compute|Microsoft.Compute/virtualMachines|cmdb\_ci\_vm\_instance| |Microsoft.Compute|
|Compute|Microsoft.Compute/virtualMachineScaleSets| | |Microsoft.Compute|
|Compute|Microsoft.ServiceFabric/clusters| | |Microsoft.Compute|
|Compute|Microsoft.Compute/vmSize|cmdb\_ci\_compute\_template| |Microsoft.Compute|
|Compute|Microsoft.Resources/deployments|cmdb\_ci\_azure\_deployment| |Microsoft.Compute|
|Compute|Microsoft.Resources/resourceGroups|cmdb\_ci\_resource\_group| |Microsoft.Compute|
|Database|Microsoft.DocumentDB| | |Microsoft.DocumentDB|
|Database|Microsoft.Sql/servers|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.sql/managedInstances|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.dbformysql|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.documentdb/databaseaccounts|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.cache/redis|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.dbforpostgresql/servers|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|microsoft.dbformysql/servers|cmdb\_ci\_cloud\_database|Azure Database|Microsoft.Sql|
|Database|Microsoft.Sql/servers/databases|cmdb\_ci\_database|Azure Database|Microsoft.Sql|
|Load Balancer|Microsoft.Network/loadBalancers|cmdb\_ci\_cloud\_load\_balancer| |Microsoft.LoadBalancer|
|Network|Microsoft.Network/applicationGateways| | |Microsoft.Network|
|Network|Microsoft.Network/networkInterfaces|cmdb\_ci\_nic| |Microsoft.Network|
|Network|Microsoft.Network/networkSecurityGroups|cmdb\_ci\_compute\_security\_group| |Microsoft.Network|
|Network|Microsoft.Network/publicIPAddresses|cmdb\_ci\_cloud\_public\_ipaddress| |Microsoft.Network|
|Network|Microsoft.Network/routeTables|cmdb\_ci\_route\_table| |Microsoft.Network|
|Network|Microsoft.Network/subnets|cmdb\_ci\_cloud\_subnet| |Microsoft.Network|
|Network|Microsoft.Network/virtualNetworks|cmdb\_ci\_network| |Microsoft.Network|
|Security|Microsoft.Security| | |Microsoft.Security|
|Storage|Microsoft.Storage/blobs|cmdb\_ci\_storage\_volume| |Microsoft.Storage|
|Storage|Microsoft.Storage/storageAccounts|cmdb\_ci\_cloud\_storage\_account| |Microsoft.Storage|
|Tools|Microsoft.Insights/components| | |Microsoft.Insights|
|Tools|Microsoft.ServiceBus| | |Microsoft.ServiceBus|

**Parent Topic:**[Cloud accounts](../concept/cloud-accounts.md)

