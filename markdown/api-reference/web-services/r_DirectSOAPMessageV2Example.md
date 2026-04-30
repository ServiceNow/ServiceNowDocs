---
title: Direct SOAPMessageV2 example
description: You can send an outbound SOAP message directly to the endpoint.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Scripting outbound SOAP, Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Direct SOAPMessageV2 example

You can send an outbound SOAP message directly to the endpoint.

In this example, the script sends a SOAP message requesting a stock quote and waits for a response. If there is no response from the web service provider, or if the specified SOAP message record is unavailable, the script throws an error, handled in this example by the try-catch block.

```
var requestBody;
var responseBody;
var status;
var sm;
try{
	sm = new sn_ws.SOAPMessageV2("StockQuote", "GetQuote");  // Might throw exception if message doesn't exist or not visible due to scope
	sm.setBasicAuth("admin","admin");
	sm.setStringParameter("symbol", "NOW");
	sm.setStringParameterNoEscape("xml_data","<data>test</data>");
	sm.setHttpTimeout(10000) //In Milli seconds. Wait at most 10 seconds for response from http request.

	response = sm.execute();//Might throw exception if http connection timed out or some issue with sending request itself because 	of encryption/decryption of password and stuff
	responseBody = response.haveError() ? response.getErrorMessage() : response.getBody();
	status = response.getStatusCode();
} catch(ex) {
	responseBody = ex.getMessage();
	status = '500';
} finally {
	requestBody = sm ? sm.getRequestBody():null;
}
gs.info("Request Body: " + requestBody);
gs.info("Response: " + responseBody);
gs.info("HTTP Status: " + status);
```

**Parent Topic:**[Scripting outbound SOAP](../../../../../integrate/outbound-soap/reference/r_ScriptingOutboundSOAP.md)

