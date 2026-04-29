---
title: SOAP strategies
description: Retrieve the information that you need and make your integration more efficient.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record retrieval limitations, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# SOAP strategies

Retrieve the information that you need and make your integration more efficient.

-   **[Use filters to limit the number of results](../reference/r_UseFiltersLimitNumberOfResults.md)**  
One way to make your web service calls fit within the 250 record limit is to think about the design of your integrating application.
-   **[Use a local data store to pull data from](../reference/r_LclDtaStorePullDta.md)**  
If a large amount of data needs to be queried often, and the data does not need to be real-time, perform a sync of the ServiceNow table that you're interested in with your integrating application's data store.
-   **[Use Java/C\#/PHP code to fetch the XML data using basic authentication](../reference/r_FetchTheXMLData.md)**  
If a local data store is not an option, another way to get the data is to call the CSV/XML processor directly and then parse the results.

**Parent Topic:**[Retrieve a large number of records using SOAP](c_RtvLrgNmbrRcrdSOAP.md)

