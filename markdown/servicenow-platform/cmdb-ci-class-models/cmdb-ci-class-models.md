---
title: CMDB CI Class Models
description: The CMDB contains base-system classes that store data about configuration items \(CIs\). The CMDB CI Class Models ServiceNow Store app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models.html
release: zurich
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB CI Class Models

The CMDB contains base-system classes that store data about configuration items \(CIs\). The CMDB CI Class Models ServiceNow® Store app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable.

You can use the added classes like any other class. Applications such as Discovery and Service Mapping can use class extensions to populate CIs and to discover technologies and software.

See the CMDB CI Class Models release notes.

Related ServiceNow® Store apps and reference information:

-   [Configuration Management database](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_ConfigurationManagementDatabase.md): A collection of class diagrams and class attributes for key CMDB classes.
-   [CMDB tables descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-tables-details.md): Descriptions of key CMDB tables in the base system.
-   [Populating the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/c_OptionsToPopulateCMDB.md): Information about the various options for populating the CMDB.
-   Discovery patterns: A ServiceNow Store app that provides a library of Discovery patterns for discovering specific devices and applications in the industry.
-   [Service Graph Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-third-party-integrations.md): ServiceNow Store apps that provide predefined integrations for importing and integrating common third-party data into CMDB classes. Also includes the [IntegrationHub ETL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/integration-hub-etl/integrationhub-etl.md) wizard for creating new ETL transform maps.

## Add class models

The app adds classes, columns, and associated metadata as related records in the following tables:

-   CMDB Class Information \[cmdb\_class\_info\]: Class descriptions
-   Identifier \[cmdb\_identifier\]: Identification rules
-   Identifier Entry \[cmdb\_identifier\_entry\]: Identification entries
-   CMDB Metadata Hosting Rules \[cmdb\_metadata\_hosting\]: Dependent relationships

## Discover using extension classes

The following table lists the software and technologies that applications can discover using the extension classes. It provides links to documentation for CMDB CI Class Models and the corresponding discovery patterns.

|Software/Technology|CMDB CI Class Models Store app|Discovery patterns|
|-------------------|------------------------------|------------------|
|Avi load balancer|[Avi load balancer extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-avi-lb.md)|Avi Vantage load balancer discovery|
|BYOL Model of RDS for Oracle|[BYOL model of RDS for Oracle extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-byol-aws-rds.md)| |
|Firewall|[Firewall extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-fw.md)| |
|IBM Hardware Management Console \(HMC\)|[IBM Hardware Management Console \(HMC\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-ibm-hmc.md)|IBM Virtualization and Hardware Management Console discovery|
|Internet of Things \(IoT\)|[Internet of Things \(IoT\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-iot.md)|N/A|
|Nutanix|[Nutanix extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-nutanix.md)|Nutanix Acropolis discovery|
|OpenStack|[OpenStack extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-openstack.md)|OpenStack resource discovery|
|Red Hat Virtualization \(RHV\)|[Red Hat Virtualization \(RHV\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-redhat-rhv.md)|Red Hat Virtualization discovery|
|Transport Layer Security \(TLS\)|[Transport Layer Security \(TLS\) extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-tls.md)|Discovery procedures provided by Certificate Inventory and Management ServiceNow Store app|
|VMware NSX load balancer|[VMware NSX load balancer extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-vmware-nsx.md)|VMware NSX Advanced load balancer discovery|

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Verify successful installation

After installing the CMDB CI Class Models store app, make sure the classes were added successfully:

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
2.  Select **Hierarchy** to display the CI Classes list.

    This list contains the added classes, such as the Nutanix classes.

3.  Select a class to see the corresponding class details, identification rules, identifier entries, and dependent relationships, if applicable.

**Warning:** Uninstalling the CMDB CI Class Models application might compromise the integrity of the CMDB and result in unexpected behavior.

