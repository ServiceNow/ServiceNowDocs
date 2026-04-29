---
title: Service catalog data lookup
description: The Data Lookup and Record Matching Support for Service Catalog plugin offers similar features to the general Data Lookup and Record Matching Support plugin.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Service catalog data lookup

The Data Lookup and Record Matching Support for Service Catalog plugin offers similar features to the general Data Lookup and Record Matching Support plugin.

Use the plugin for service catalog to perform data lookups for variables. This lookup can be on service catalog item screens, on requested items, and on catalog tasks as a user fills out the values contained in variables.

## Service Catalog data lookup roles

Service Catalog enables specific roles to participate in the process of creating and using Service Catalog data lookups.

|Role|Description|
|----|-----------|
|catalog\_lookup\_admin|Similar to data\_lookup\_admin. Can create, update, and delete catalog data lookup definitions, matcher variable definitions, and setter variable definitions.|
|catalog\_lookup\_manager|Can read catalog data lookup definitions, matcher variable definitions, and setter variable definitions. The role can be granted to anyone using catalog data lookups so they can see the definitions for which they are creating rules. As required, grant create, read, write, or delete access to the individual data lookup rules tables created to delegate maintenance.|

-   **[Create a catalog lookup definition](../task/t_CreatACatDataLookupDefRec.md#)**  
Create a catalog data lookup definition record.
-   **[Custom data lookup](../reference/r_CreateACustomDataLookupTable.md#)**  
You can create a custom table to store lookup data.

**Parent Topic:**[Service catalog variables](c_ServiceCatalogVariables.md)

