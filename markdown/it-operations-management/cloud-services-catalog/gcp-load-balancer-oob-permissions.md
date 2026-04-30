---
title: Google Cloud Platform Load Balancer Out Of Box permissions
description: Google Cloud Platform HTTP Load Balancer Out Of Box permissions
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Google Cloud Platform Load Balancer, Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Google Cloud Platform Load Balancer Out Of Box permissions

Google Cloud Platform HTTP Load Balancer Out Of Box permissions

<table id="table_ug3_wqz_dbc"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permission

</th></tr></thead><tbody><tr><td rowspan="4">

CSC GCP HTTP Load Balancer

</td><td>

Provision

</td><td>

-   compute.backendServices.create
-   compute.backendServices.get
-   compute.backendServices.use
-   compute.globalAddresses.create
-   compute.globalAddresses.get
-   compute.globalAddresses.use
-   compute.globalForwardingRules.create
-   compute.globalForwardingRules.get
-   compute.healthChecks.create
-   compute.healthChecks.get
-   compute.healthChecks.useReadOnly
-   compute.instanceGroups.create
-   compute.instanceGroups.get
-   compute.instanceGroups.update
-   compute.instanceGroups.use
-   compute.instances.use
-   compute.targetHttpProxies.create
-   compute.targetHttpProxies.get
-   compute.targetHttpProxies.use
-   compute.urlMaps.create
-   compute.urlMaps.get
-   compute.urlMaps.use
-   compute.networks.get

</td></tr><tr><td>

Pointed discovery

</td><td>

-   compute.backendServices.list
-   compute.forwardingRules.list
-   compute.healthChecks.list
-   compute.httpHealthChecks.list
-   compute.httpsHealthChecks.list
-   compute.instanceGroupManagers.list
-   compute.instanceGroups.list
-   compute.instances.list
-   compute.targetHttpProxies.list
-   compute.targetHttpsProxies.list
-   compute.targetSslProxies.list
-   compute.targetTcpProxies.list
-   compute.urlMaps.list
-   compute.regions.list
-   compute.zones.list

</td></tr><tr><td>

LB- Deprovision

</td><td>

-   compute.globalForwardingRules.delete
-   compute.targetHttpProxies.delete
-   compute.urlMaps.delete

</td></tr><tr><td>

Stack - Deprovision

</td><td>

-   compute.globalAddresses.delete
-   compute.backendServices.delete
-   compute.healthChecks.delete
-   compute.instanceGroups.delete
-   compute.globalForwardingRules.delete
-   compute.targetHttpProxies.delete
-   compute.urlMaps.delete

</td></tr></tbody>
</table>**Parent Topic:**[Google Cloud Platform Load Balancer](google-cloud-platform-load-balancer.md)

