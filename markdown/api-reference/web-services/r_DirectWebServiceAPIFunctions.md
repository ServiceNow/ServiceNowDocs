---
title: SOAP direct web service API functions
description: The standard SOAP API is a set of small, globally defined functions that can be performed on a targeted resource.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# SOAP direct web service API functions

The standard SOAP API is a set of small, globally defined functions that can be performed on a targeted resource.

The targeted resource \(or table\) is defined in the URL by the format `https://<instance name>.service-now.com/<table name>.do`.

|Method Summary|Description|
|--------------|-----------|
|[insert](r_Insert.md)|Creates a new record for the table targeted in the URL.|
|[insertMultiple](r_InsertMultiple.md)|Creates multiple new records for the table targeted in the URL. To enable multiple inserts, activate the [Web service import sets](https://www.servicenow.com/docs/access?context=c_WebServiceImportSets&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).|
|[update](r_Update.md)|Updates a existing record in the targeted table in the URL, identified by the mandatory **sys\_id** field.|
|[deleteRecord](r_DeleteRecord.md)|Deletes a record from the targeted table by supplying its `sys_id`.|
|[deleteMultiple](r_DeleteMultiple.md)|Delete multiple records from the targeted table by example values.|

|Method Summary|Description|
|--------------|-----------|
|[getKeys](r_GetKeys.md)|Query the targeted table by example values and return a comma delimited `sys_id` list.|
|[getRecords](r_GetRecords.md)|Query the targeted table by example values and return all matching records and their fields.|
|get|Query a single record from the targeted table by `sys_id` and return the record and its fields.|
|[aggregate](r_Aggregate.md)|Query using and aggregate functions SUM, COUNT MIN, MAX, LAST, and AVG. To enable the aggregate functions, activate the Aggregate Web Service Plugin.|

-   **[Data Retrieval API](r_DataRetrievalAPI.md)**  
Data Retrieval API method summaries and descriptions.
-   **[Data Modification API](r_DataModificationAPI.md)**  
Data Modification API method summaries and descriptions.

**Parent Topic:**[Direct web services](../../inbound-soap/concept/c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response](../../inbound-soap/concept/using-forms-limit-extend-query-resp.md)

[Return the display value for reference variables](../../inbound-soap/concept/return-display-reference-variables.md)

[Clear values from a target instance](../../inbound-soap/concept/clearing-values-target.md)

[Retrieve journal entries using direct web services](../../inbound-soap/concept/retrieving-journal-entries.md)

[Retrieve choice fields using direct web services](../../inbound-soap/concept/retrieving-choice-fields-direct-ws.md)

[Persist an HTTP session across all SOAP calls](../../inbound-soap/concept/persist-session-all-soap-calls.md)

