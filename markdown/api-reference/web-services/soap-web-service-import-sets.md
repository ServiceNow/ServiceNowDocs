---
title: SOAP web service import sets
description: Web service import sets complement direct web services and scripted SOAP web services by providing a web service interface to import sets tables.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# SOAP web service import sets

Web service import sets complement direct web services and scripted SOAP web services by providing a web service interface to import sets tables.

By default, this type of web service synchronously transforms the incoming data based on the associated transform maps. If the associated import set mode is set to Asynchronous, the behavior is to save the data for transformation at a later time. Web service import sets tables publish all default web service functions in the WSDL.

You can access a web service import set WSDL by specifying the import set table name + ".do?WSDL" on the URL.

For example:

`http://<instance name>.service-now.com/imp_notification.do?WSDL`.

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

**Related topics**  


[Web service import sets](https://www.servicenow.com/docs/access?context=c_WebServiceImportSets&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

[Import sets key concepts](https://www.servicenow.com/docs/access?context=c_ImportSetsKeyConcepts&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

