---
title: Managed IT Resource types
description: There are three IT Resource categories in ServiceNow Cloud Cost Management - Server, PaaS Resources, and IaaS Storage.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-17"
reading_time_minutes: 1
breadcrumb: [Manage Cloud Cost Management subscriptions, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Managed IT Resource types

There are three IT Resource categories in ServiceNow Cloud Cost Management - Server, PaaS Resources, and IaaS Storage.

-   Server is any physical or virtual server that is represented as a configuration item \(CI\) in the CMDB tables listed in the following license resource categories and managed by the Cloud Cost Management application. Server includes virtual machines in AWS, Azure, or GCP.
-   PaaS Resources are cloud-based platform services that are represented as a CI in the CMDB tables listed in the following license resource categories and managed by the Cloud Cost Management application. PaaS resources include databases.
-   IaaS Storage is any cloud-based infrastructure service represented as a CI in a CMDB table listed in the following license resource categories and managed by the Cloud Cost Management application. IaaS resources include storage volumes.

<table id="table_qfg_twd_4qb"><thead><tr><th>

Resource category

</th><th>

Subscription unit ratio

</th><th>

Model category

</th></tr></thead><tbody><tr><td>

Server

</td><td>

1:1

</td><td>

cmdb\_ci\_vm\_instanceAny CMDB classes derived from the listed classes and not defined as another Managed IT Resource type.

</td></tr><tr><td>

PaaS resources

</td><td>

1:3

</td><td>

-   cmdb\_ci\_database
-   cmdb\_ci\_cloud\_database

 Any child classes of the listed classes.

</td></tr><tr><td>

IaaS storage

</td><td>

1:3

</td><td>

cmdb\_ci\_storage\_volumeAny child classes of the listed class.

</td></tr></tbody>
</table>An example for calculating license resource consumption:

Suppose your organization manages 2 servers, 3 databases or PaaS resources, and 3 storage volumes or IaaS resources.

The total number of license resource units consumed is: \(2 + 1 + 1\) = 4 resource units.

To calculate cost, multiply each resource count by the applicable per-unit rate from your entitlement. For example, at a rate of n per resource unit: \(2\*n\) + \(1\*n\) + \(1\*n\) = 4n.

**Parent Topic:**[Manage Cloud Cost Management subscriptions](managing-ccm-subscriptions.md)

