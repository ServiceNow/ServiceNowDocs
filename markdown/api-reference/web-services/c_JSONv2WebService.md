---
title: JSONv2 web service
description: The ability to describe sets of data in JSON format is a natural extension to the JavaScript language.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Inbound, Web services, API implementation, API implementation and reference]
---

# JSONv2 web service

The ability to describe sets of data in JSON format is a natural extension to the JavaScript language.

ServiceNow supports a web service interface that operates on the JSON object as the data input and output format.

The JSONv2 web service is provided by a platform-level processor similar to the services for SOAP, WSDL, CSV, Excel, and XML. Like those services, the JSON web service is triggered by a standalone JSONv2 URL parameter. For example:

```
https://<instance name>.service-now.com/mytable.do?JSONv2
```

Having the JSON object available as a data format for web services means that you can create \(insert\), update, and query any data in the system using the JSON object format, and get results in the JSON object format.

## Security

Like all other HTTP-based web services available on the platform, the JSONv2 web service is required to authenticate using basic authentication by default. The user ID that is used for authentication is subjected to access control in the same way as an interactive user.

-   **[JSON object format](c_JSONObjectFormat.md)**  
The JSON object is built in two structures.
-   **[JSON response status](c_ResponseStatus.md)**  
JSONv2 requests may return one of several response statuses.
-   **[Setting the number of rows returned](c_SettingTheNumberOfRowsReturned.md)**  
The following system property controls how many rows JSON returns with each query.
-   **[Requiring basic authentication for incoming JSONv2 requests](c_ReqBasicAuthIncomJSONv2Requ.md)**  
The following system property controls whether basic authentication is required for incoming JSONv2 requests.
-   **[Action parameters](c_ActionParameters.md)**  
Action parameters are separate and different from data parameters because they specify the action to take when the JSON object parameter is part of an HTTP GET or POST request.
-   **[JSON Data Retrieval API](c_DataRetrievalAPI.md)**  
Query for data by issuing an HTTPS GET request to the instance.
-   **[JSON Data Modification API](c_DataModificationAPI.md)**  
Modify data using the JSON web service by sending an HTTPS POST request to the instance.

**Parent Topic:**[Inbound web services](../../web-services/concept/inbound-web-services.md)

**Related topics**  


[SOAP web services security](../../inbound-soap/concept/c_SOAPWebService.md)

