---
title: SOAPMessageV2 MID server example
description: You can send an outbound SOAP message through a MID Server.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scripting outbound SOAP, SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# SOAPMessageV2 MID server example

You can send an outbound SOAP message through a MID Server.

By sending the message through a MID Server, you can access endpoints that are behind a firewall or within a private network. All SOAP messages sent through a MID Server are asynchronous.

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
	sm.setMIDServer('mid_server_name');
	response = sm.execute();//Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password and stuff
 
	response.waitForResponse(60);// In Seconds, Wait at most 60 seconds to get response from ECC Queue/Mid Server //Might throw exception timing out waiting for response in ECC queue
 
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

