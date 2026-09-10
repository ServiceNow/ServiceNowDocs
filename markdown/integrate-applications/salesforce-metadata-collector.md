---
title: Salesforce metadata collector
description: Salesforce metadata collector provides read-only access to metadata from a Salesforce instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/salesforce-metadata-collector.html
release: australia
topic_type: concept
last_updated: "2026-07-28"
reading_time_minutes: 2
breadcrumb: [Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Salesforce metadata collector

Salesforce metadata collector provides read-only access to metadata from a Salesforce instance.

The collector harvests metadata for Salesforce Objects and Fields, Reports, and Dashboards in a Salesforce instance and make it searchable and discoverable in the data catalog.

## Metadata cataloged

The collector catalogs the following information.

|Object|Information cataloged|
|------|---------------------|
|Object|Name, Description, Custom Object \(true or false\), Mergeable Object \(true or false\), Queryable Object \(true or false\)|
|Field|Name, Description, Field Type, Security Classification, Compliance Group, Inline Help Text, Length, Default Value, Formula \(calculated fields\), Allowed Values \(picklist fields\), Created Date, Created By, Last Modified Date, Last Modified By|
|Summary field|Summarized object, Aggregation type, Aggregated field, Any filters on the summarization \(filter field, filter operation, and filter value\)|
|Dashboard|Name, Type, External URL|
|Report|Name, Type, Format|
|Detail column|Name, Fully-Qualified Name|
|Grouping column|Name, Fully-Qualified Name, Grouping level|
|Aggregation column|Name, Formula|

Following additional information is cataloged when you run the collector with the Enable Governance Metadata Collection parameter.

|Object|Information cataloged|
|------|---------------------|
|Row Filter Access Control|Name|
|Column Mask Access Control|Name|
|Attribute Based Access Control|Name, Description, Created by, Created at, Modified by, Modified at, On securable type, For securable type, To principals, Except principals|
|Workspace bindings|Workspace ID, Binding type|
|Privileges|Granted to, Granted by, Privilege type, Granted on object, Inherited from|

## Relationships between objects

Catalog pages show relationships between the following data asset types:

|Object|Relationship|
|------|------------|
|Field|Object|
|Report|Detail Column, Grouping Column, Aggregate Column|
|Grouping Column|Report|
|Aggregation Column|Report|
|Detail Column|Report|
|Row Filter Access Control|Applies to table, Uses function, Using column, Contained within schema|
|Column Mask Access Control|Applies to column, Uses function, Contained within schema|
|Attribute Based Access Control|Applies to catalog, Schema and table, Defined on catalog, Schema and table, Uses function|
|Catalog|Has workspace bindings, Has privileges|
|Schema|Has privileges|
|Table|Has privileges|
|Storage credential|Has workspace bindings|
|External Location|Has workspace bindings|

## Lineage for Salesforce

The following lineage information is collected by the Salesforce collector:

| | |
|---|---|
|Field|Report Column that uses data from the field|

## Authentication supported

The collector uses username and password authentication to connect to Salesforce via [connected applications](https://docs.data.world/en/197977-preparing-to-run-the-salesforce-collector.html#UUID-d6750602-acdf-aa41-e87d-17b7fe18833a_section-idm234447327721945).

-   **[Prepare to run the Salesforce collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/prepare-to-run-the-salesforce-collector.md)**  
Set up access for cataloging Salesforce resources by configuring user credentials, security tokens, and connected applications.
-   **[Create a Salesforce metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-salesforce-metadata-collector.md)**  
Create a collector to import metadata from Salesforce.

**Parent Topic:**[Configuring metadata collectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/configure-metadata-collectors-dc.md)

