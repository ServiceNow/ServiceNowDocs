---
title: Scripted web service example
description: This example demonstrates the processing script for the FakeStockValue web service.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a scripted web service using a static WSDL, Create a scripted SOAP web service using a static WSDL, Scripted SOAP web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Scripted web service example

This example demonstrates the processing script for the FakeStockValue web service.

```
var vProcessor  = new FakeStockValue (soapRequestXML ) ;
 
  var responseElement  = vProcessor. process ( ) ; if (responseElement  != null ) {
  response. soapResponseElement = responseElement ; } else {
  response. soapResponseElement = vProcessor. generateSoapFault ( "unknown error" ) ; }
```

**Parent Topic:**[Create a scripted web service using a static WSDL](../task/t_CreateStaticWSDLScriptWebService.md)

