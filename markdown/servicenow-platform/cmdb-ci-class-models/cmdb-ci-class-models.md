---
title: CMDB CI Class Models
description: The CMDB contains base-system classes that store data about configuration items \(CIs\). The CMDB CI Class Models ServiceNow Store app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable.
locale: en-US
release: yokohama
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-03-05"
reading_time_minutes: 3
breadcrumb: [Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB CI Class Models

The CMDB contains base-system classes that store data about configuration items \(CIs\). The CMDB CI Class Models ServiceNow® Store app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable.

## Classes added by the CMDB CI Class Models app

For the full list of added classes, see [List of classes added by the CMDB CI Class Models app](../reference/cmdb-ci-class-model-list-of-classes.md).

The app adds classes, columns, and associated metadata as related records in the following tables:

-   CMDB Class Information \[cmdb\_class\_info\]: Class descriptions
-   Identifier \[cmdb\_identifier\]: Identification rules
-   Identifier Entry \[cmdb\_identifier\_entry\]: Identification entries
-   CMDB Metadata Hosting Rules \[cmdb\_metadata\_hosting\]: Dependent relationships

## Using the classes

You can use the added classes like any other class. Applications such as Discovery and Service Mapping can use class extensions to populate CIs and to discover technologies and software.

Related ServiceNow® Store apps and reference information:

-   [Configuration Management database](c_ConfigurationManagementDatabase.md): A collection of class diagrams and class attributes for key CMDB classes.
-   [CMDB tables descriptions](../reference/cmdb-tables-details.md): Descriptions of key CMDB tables in the base system.
-   [Populating the CMDB](c_OptionsToPopulateCMDB.md): Information about the various options for populating the CMDB.
-   [Discovery patterns](https://www.servicenow.com/docs/access?context=c_MappingPatternsCustomization&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US): A ServiceNow Store app that provides a library of Discovery patterns for discovering specific devices and applications in the industry.
-   [Service Graph Connectors](cmdb-third-party-integrations.md): ServiceNow Store apps that provide predefined integrations for importing and integrating common third-party data into CMDB classes. Also includes the [IntegrationHub ETL](integrationhub-etl.md) wizard for creating new ETL transform maps.

## Discover using extension classes

The following table lists the software and technologies that applications can discover using the extension classes. It provides links to documentation for CMDB CI Class Models and the corresponding discovery patterns.

|Software/Technology|CMDB CI Class Models Store app|Discovery patterns|
|-------------------|------------------------------|------------------|
|Avi load balancer|[Avi load balancer extension classes](cmdb-ci-class-models-avi-lb.md)|[Avi Vantage load balancer discovery](https://www.servicenow.com/docs/access?context=avi-load-balancer-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|
|BYOL Model of RDS for Oracle|[BYOL model of RDS for Oracle extension classes](cmdb-ci-class-models-byol-aws-rds.md)| |
|Firewall|[Firewall extension classes](cmdb-ci-class-models-fw.md)| |
|IBM Hardware Management Console \(HMC\)|[IBM Hardware Management Console \(HMC\) extension classes](cmdb-ci-class-models-ibm-hmc.md)|[IBM Virtualization and Hardware Management Console discovery](https://www.servicenow.com/docs/access?context=ibm-hmc-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|
|Internet of Things \(IoT\)|[Internet of Things \(IoT\) extension classes](cmdb-ci-class-models-iot.md)|N/A|
|Nutanix|[Nutanix extension classes](cmdb-ci-class-models-nutanix.md)|[Nutanix Acropolis discovery](https://www.servicenow.com/docs/access?context=nutanix-pattern&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|
|OpenStack|[OpenStack extension classes](cmdb-ci-class-models-openstack.md)|[OpenStack resource discovery](https://www.servicenow.com/docs/access?context=openstack-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|
|Red Hat Virtualization \(RHV\)|[Red Hat Virtualization \(RHV\) extension classes](cmdb-ci-class-models-redhat-rhv.md)|[Red Hat Virtualization discovery](https://www.servicenow.com/docs/access?context=red-hat-virtualization-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|
|Transport Layer Security \(TLS\)|[Transport Layer Security \(TLS\) extension classes](cmdb-ci-class-models-tls.md)|Discovery procedures provided by Certificate Inventory and Management ServiceNow Store app|
|VMware NSX load balancer|[VMware NSX load balancer extension classes](cmdb-ci-class-models-vmware-nsx.md)|[VMware NSX Advanced load balancer discovery](https://www.servicenow.com/docs/access?context=vmware-nsx-lb-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)|

