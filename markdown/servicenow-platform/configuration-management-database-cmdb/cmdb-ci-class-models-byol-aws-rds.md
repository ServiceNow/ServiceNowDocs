---
title: BYOL model of RDS for Oracle extension classes
description: The CMDB CI Class Models store app adds or updates classes for the BYOL Model of RDS for Oracle.
locale: en-US
release: xanadu
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [CMDB CI Class Models, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# BYOL model of RDS for Oracle extension classes

The CMDB CI Class Models store app adds or updates classes for the BYOL Model of RDS for Oracle.

The app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships if applicable. You can use the added classes as any other CMDB class. Applications such as Discovery and Service Mapping patterns can use these class extensions to populate CIs and discover various technologies and software.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## BYOL Model of RDS for Oracle

The Amazon RDS for Oracle is a fully managed commercial database that makes it easy to set up, operate, and scale Oracle deployments in the cloud. You can run Amazon RDS for Oracle under two different licensing models – “License Included” and “Bring-Your-Own-License \(BYOL\)“. In the “License Included” service model, you do not need separately purchased Oracle licenses; the Oracle Database software has been licensed by AWS.

We support discovery of the RDS Databases and their licenses.

## Classes

This section lists the classes that the CMDB CI Class Models store app adds or updates. CMDB CI Class Models: Release 1.23.0 adds the following classes for the BYOL Model of RDS for Oracle. For the list of classes in a base system, including classes that this store app might be extending, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

|Class|Description|
|-----|-----------|
|cmdb\_ci\_cloud\_database|The cloud databases.|
|cmdb\_ci\_serverless\_hardware|Hardware type information of the databases.|

## Class Columns

CMDB CI Class Models: Release 1.23.0 adds the following column to the respective class.

|Added column|Description|
|------------|-----------|
|cloud\_vendor|The cloud vendor.|
|host\_type|The host type such as PaaS/IaaS.|
|cpu\_core\_count|Amount of CPU cores.|
|cpu\_core\_thread|Amount of CPU threads.|
|cpu\_count|Amount of CPUs.|
|object\_id|ID of the CI.|

|Added column|Description|
|------------|-----------|
|multi\_az|Determines if the database is deployed on multiple availability zones \(true/false\).|
|replication\_enabled|Determines if replication is enabled \(true/false\).|
|replication\_type|Replication type.|
|replica\_source|Database name of the replication source.|

