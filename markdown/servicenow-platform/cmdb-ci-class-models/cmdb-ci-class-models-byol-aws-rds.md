---
title: BYOL model of RDS for Oracle extension classes
description: The CMDB CI Class Models app adds or updates classes for the BYOL Model of RDS for Oracle.
locale: en-US
release: australia
product: CMDB CI Class Models
classification: cmdb-ci-class-models
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB CI class models, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# BYOL model of RDS for Oracle extension classes

The CMDB CI Class Models app adds or updates classes for the BYOL Model of RDS for Oracle.

CMDB CI Class Models is a ServiceNow Store app that adds class models that extend the CMDB class hierarchy. The new or updated classes include class descriptions, identification rules, identifier entries, and, if applicable, dependent relationships. You can use the added classes just like any other CMDB class. Applications such as Discovery and Service Mapping Patterns can use the class extensions to populate CIs and discover technologies and software.

See the [full release notes for all CMDB CI Class Models](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/it-operations-management/store-rn-itom-cmdb-class-models.html?emcs_t=S2h8ZW1haWx8Ym9hcmRfc3Vic2NyaXB0aW9ufE1FMlVTSFREVDc3S0hTfDMzNDcxMjV8U1VCU0NSSVBUSU9OU3xoSw).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## BYOL Model of RDS for Oracle

The Amazon RDS for Oracle is a fully managed commercial database that makes it easy to set up, operate, and scale Oracle deployments in the cloud. You can run Amazon RDS for Oracle in one of two different licensing models: “License Included” and “Bring-Your-Own-License \(BYOL\)“. In the “License Included” service model, you do not need separately purchased Oracle licenses; the Oracle Database software has been licensed by AWS.

The base system supports discovery of the RDS Databases and their licenses.

## Classes

This section lists the classes that the CMDB CI Class Models app adds or updates. CMDB CI Class Models: Release 1.23.0 adds the following classes for the BYOL Model of RDS for Oracle. For the list of classes in the base system, including classes that this app might extend, see [CMDB tables descriptions](../reference/cmdb-tables-details.md).

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

