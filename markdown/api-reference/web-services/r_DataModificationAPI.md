---
title: Data Modification API
description: Data Modification API method summaries and descriptions.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Data Modification API

Data Modification API method summaries and descriptions.

|Method Summary|Description|
|--------------|-----------|
|[insert](r_Insert.md)|Creates a new record for the table targeted in the URL.|
|[insertMultiple](r_InsertMultiple.md)|Creates multiple new records for the table targeted in the URL. To enable multiple inserts, activate the [Web service import sets](https://www.servicenow.com/docs/access?context=c_WebServiceImportSets&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).|
|[update](r_Update.md)|Updates a existing record in the targeted table in the URL, identified by the mandatory **sys\_id** field.|
|[deleteRecord](r_DeleteRecord.md)|Deletes a record from the targeted table by supplying its `sys_id`.|
|[deleteMultiple](r_DeleteMultiple.md)|Delete multiple records from the targeted table by example values.|

-   **[insert](r_Insert.md)**  
Creates a new record for the table targeted in the URL.
-   **[insertMultiple](r_InsertMultiple.md)**  
Creates multiple new records for the table targeted in the URL.
-   **[update](r_Update.md)**  
Updates an existing record in the targeted table in the URL, identified by the mandatory **sys\_id** field.
-   **[deleteRecord](r_DeleteRecord.md)**  
Delete a record from the targeted table by supplying its **sys\_id**.
-   **[deleteMultiple](r_DeleteMultiple.md)**  
Delete multiple records from the targeted table by example values.

**Parent Topic:**[SOAP direct web service API functions](r_DirectWebServiceAPIFunctions.md)

**Related topics**  


[Data Retrieval API](r_DataRetrievalAPI.md)

