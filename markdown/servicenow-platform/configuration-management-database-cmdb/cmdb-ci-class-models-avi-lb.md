---
title: Avi load balancer extension classes
description: The CMDB CI Class Models store app adds or updates classes for the Avi load balancer.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Avi load balancer extension classes

The CMDB CI Class Models store app adds or updates classes for the Avi load balancer.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Avi load balancer

The Avi Vantage platform is built on software-defined principles, enabling a next generation architecture to deliver the flexibility and simplicity expected by IT and lines of business. The Avi Vantage platform architecture separates the data and control planes to deliver application services beyond load balancing, such as application analytics, predictive autoscaling, micro-segmentation, and self-service, for app owners in on-premises or cloud environments. The platform provides a centrally managed, dynamic pool of load balancing resources on commodity x86 servers, virtual machines, or containers, to deliver granular services close to individual applications. Providing these services allows network services to scale near infinitely without the added complexity of managing hundreds of disparate appliances.

Discovery uses the [Avi Vantage load balancer discovery](https://www.servicenow.com/docs/access?context=avi-load-balancer-discovery&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US) pattern to find Avi load balancer resources.

![Avi load balancer extension classes integrated with the CMDB class hierarchy.](../image/cmdb-ci-class-model-AVI-jun20.png "Avi load balancer classes integrated with the CMDB class hierarchy")

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. CMDB CI Class Models: Release 1.6.0 adds the following classes for the Avi load balancer. For the list of classes in a base system, including classes that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

<table id="table_x53_n4v_phb"><thead><tr><th>

Class

</th><th>

Extends

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Avi Controller\[cmdb\_ci\_avi\_controller\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Avi Controller is a single point of management and control that is the 'brain' of the entire Avi Vantage system, and typically deployed as a redundant three-node cluster.

</td></tr><tr><td>

Avi Controller Cluster\[cmdb\_ci\_avi\_controller\_cluster\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Avi Controller cluster uses big data analytics to analyze the data and present actionable insights to administrators on intuitive dashboards on the Avi Admin Console.

</td></tr><tr><td>

Avi Service Engine\[cmdb\_ci\_avi\_service\_engine\]

</td><td>

Virtual Machine Object\[cmdb\_ci\_vm\_object\]

</td><td>

Avi Service Engines \(SEs\) handle all data plane operations within Avi Vantage by receiving and executing instructions from the Avi Controller.

</td></tr></tbody>
</table>## Class columns

CMDB CI Class Models: Release 1.6.0 adds the following column to the respective class.

|Added column|Description|
|------------|-----------|
|version|The version of the Avi Service Engine resource.|

**Related topics**  


[CMDB schema model](c_ConfigurationManagementDatabase.md)

