---
title: SOAP direct web service API functions
description: The standard SOAP API is a set of small, globally defined functions that can be performed on a targeted resource.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/r\_DirectWebServiceAPIFunctions.html
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# SOAP direct web service API functions

The standard SOAP API is a set of small, globally defined functions that can be performed on a targeted resource.

The targeted resource \(or table\) is defined in the URL by the format `https://<instance name>.service-now.com/<table name>.do`.

|Method Summary|Description|
|--------------|-----------|
|[insert](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_Insert.md)|Creates a new record for the table targeted in the URL.|
|[insertMultiple](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_InsertMultiple.md)|Creates multiple new records for the table targeted in the URL. To enable multiple inserts, activate the [Web service import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/c_WebServiceImportSets.md).|
|[update](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_Update.md)|Updates a existing record in the targeted table in the URL, identified by the mandatory **sys\_id** field.|
|[deleteRecord](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_DeleteRecord.md)|Deletes a record from the targeted table by supplying its `sys_id`.|
|[deleteMultiple](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_DeleteMultiple.md)|Delete multiple records from the targeted table by example values.|

|Method Summary|Description|
|--------------|-----------|
|[getKeys](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_GetKeys.md)|Query the targeted table by example values and return a comma delimited `sys_id` list.|
|[getRecords](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_GetRecords.md)|Query the targeted table by example values and return all matching records and their fields.|
|get|Query a single record from the targeted table by `sys_id` and return the record and its fields.|
|[aggregate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_Aggregate.md)|Query using and aggregate functions SUM, COUNT MIN, MAX, LAST, and AVG. To enable the aggregate functions, activate the Aggregate Web Service Plugin.|

-   **[Data Retrieval API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_DataRetrievalAPI.md)**  
Data Retrieval API method summaries and descriptions.
-   **[Data Modification API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/r_DataModificationAPI.md)**  
Data Modification API method summaries and descriptions.

**Parent Topic:**[Direct web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response]()

[Return the display value for reference variables]()

[Clear values from a target instance]()

[Retrieve journal entries using direct web services]()

[Retrieve choice fields using direct web services]()

[Persist an HTTP session across all SOAP calls]()

