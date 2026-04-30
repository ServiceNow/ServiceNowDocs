---
title: Data Retrieval API
description: Data Retrieval API method summaries and descriptions.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Data Retrieval API

Data Retrieval API method summaries and descriptions.

|Method Summary|Description|
|--------------|-----------|
|[getKeys](r_GetKeys.md)|Query the targeted table by example values and return a comma delimited `sys_id` list.|
|[getRecords](r_GetRecords.md)|Query the targeted table by example values and return all matching records and their fields.|
|get|Query a single record from the targeted table by `sys_id` and return the record and its fields.|
|[aggregate](r_Aggregate.md)|Query using and aggregate functions SUM, COUNT MIN, MAX, LAST, and AVG. To enable the aggregate functions, activate the Aggregate Web Service Plugin.|

-   **[getKeys](r_GetKeys.md)**  
Query the targeted table by example values and return a comma delimited `sys_id` list.
-   **[getRecords](r_GetRecords.md)**  
Query the targeted table by example values and return all matching records and their fields.
-   **[get](r_Get.md)**  
Query a single record from the targeted table by `sys_id` and return the record and its fields.
-   **[aggregate](r_Aggregate.md)**  
Query a table using an aggregate function including SUM, COUNT, MIN, MAX, LAST, and AVG.

**Parent Topic:**[SOAP direct web service API functions](r_DirectWebServiceAPIFunctions.md)

**Related topics**  


[Data Modification API](r_DataModificationAPI.md)

