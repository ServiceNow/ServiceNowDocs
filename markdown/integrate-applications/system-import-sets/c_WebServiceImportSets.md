---
title: Web service import sets
description: Web service import sets complement direct web services and scripted SOAP web services providing a web service interface to import set tables.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Import sets, Imports, Creating integrations with applications]
---

# Web service import sets

Web service import sets complement direct web services and scripted SOAP web services providing a web service interface to import set tables.

![](../image/WsIset.png "Web service import set")

By default, this type of web service transforms the incoming data synchronously based on the associated transform maps. If the associated import set mode is set to Asynchronous, the behavior is to save the data for transformation at a later time. Web service import sets tables publish all the default web service functions in the WSDL.

![](../image/SystemWebServices.jpg "System web services")

This plugin also provides the following standard import set tables:

-   Computer
-   Location
-   Notification
-   User

You can access a web service import set WSDL by specifying the import set table name + ".do?WSDL" on the URL.

For example:

`http://<instance name>.service-now.com/imp_notification.do?WSDL`.

-   **[Creating an import set web service](c_CreatingANewWebService.md)**  
Create a web service import set table to define how to stage and transform imported data.
-   **[Web service import set mode](../reference/r_ImportSetMode.md)**  
When a SOAP message inserts a record into an import set table, and there is no import set for that table in the **Loading** state, a new import set will be created with the **Mode** set to **Synchronous**.
-   **[Inserting multiple records using insertMultiple](../reference/r_InsertingMultipleRecords.md)**  
You can insert multiple records in one SOAP request by using the insertMultiple operation.
-   **[Web service import sets security requirements](c_SecurityRequirements.md)**  
Web Service Import Sets use the same security mechanisms as SOAP Web Services.

**Parent Topic:**[Import sets](../reference/import-sets-landing-page.md)

