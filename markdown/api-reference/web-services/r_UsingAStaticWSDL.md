---
title: Use the static WSDL
description: Load the static WSDL into a SOAP client to make requests to the SOAP web service.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a scripted SOAP web service using a static WSDL, Scripted SOAP web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Use the static WSDL

Load the static WSDL into a SOAP client to make requests to the SOAP web service.

The web service client provides

-   The FakeStockValue project.
-   The StockQuoteBinding web service.
-   The GetLastTradePrice SOAP function. This function generates request records when run.

![](../image/WSDL_Loaded.jpg "Loaded WSDL")

You can change the default request XML in the static WSDL to include a stock symbol.

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:stoc="http://example.com/stockquote.xsd">
   <soapenv:Header/>
   <soapenv:Body>
      <stoc:TradePriceRequest>IBM</stoc:TradePriceRequest>
   </soapenv:Body>
</soapenv:Envelope>
```

Submitting a SOAP request to this web service endpoint returns the following to the requesting SOAP client.

```
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
   <SOAP-ENV:Body>
      <GetLastTradePriceOutput xmlns="https://www.service-now.com/vws/FakeStockValue">
         <message>admin2, You were looking for a quote on IBM</message>
      </GetLastTradePriceOutput>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

**Parent Topic:**[Create a scripted SOAP web service using a static WSDL](createSOAPwebserviceStaticWSDL.md)

