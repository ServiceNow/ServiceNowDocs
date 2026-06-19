---
title: Using XML import sets
description: Use an XML import set to import data from another instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/system-import-sets/c\_XMLImportSets.html
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing from another ServiceNow instance, Import sets, Imports, Workflow Data Fabric]
---

# Using XML import sets

Use an XML import set to import data from another instance.

This method allows you to:

-   Apply business rules
-   Transform incoming data
-   Reconcile sys\_id values if necessary

**Note:** Administrators cannot set the **update\_synch** attribute in Dictionary records to move data as part of update sets. This attribute was being used incorrectly to migrate data in large tables and was causing significant performance problems.

1.  [Create an XML data source to another instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateADataSource.md)  
Data sources are used to create an import set so that data can be processed, if necessary, prior to being mapped onto a production table.
2.  [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md)  
A transform map is a set of field maps that determine the relationships between fields in an import set and fields in an existing ServiceNow table, such as Incidents \[incident\] or Users \[sys\_user\].
3.  [Add onBefore scripts to the transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_AddOnBeforeScriptToTransformMap.md)  
Create one onBefore transform map script to copy the sys\_id of new records from the source to the target instance. Create a second onBefore transform map script to identify records on the target instance that have the same unique values but different sys\_id values.

**Parent Topic:**[Importing from another ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportingFromAnotherSNInstance.md)

