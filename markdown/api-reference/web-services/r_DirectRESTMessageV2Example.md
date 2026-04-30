---
title: Direct RESTMessageV2 example
description: You can send an outbound REST message directly to the endpoint.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripting outbound REST, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Direct RESTMessageV2 example

You can send an outbound REST message directly to the endpoint.

In this example, the script sends a REST message requesting a stock quote and waits for a response. If there is no response from the web service provider, or if the specified REST message record is unavailable, the script throws an error, handled in this example by the try-catch block.

```
var requestBody;
var responseBody;
var status;
var sm;
try{
	sm = new sn_ws.RESTMessageV2("Yahoo Finance", "get");  // Might throw exception if message doesn't exist or not visible due to scope.
	sm.setBasicAuth("admin","admin");
	sm.setStringParameter("symbol", "NOW");
	sm.setStringParameterNoEscape("xml_data","<data>test</data>");
	sm.setHttpTimeout(10000); //In milliseconds. Wait at most 10 seconds for response from http request.

	response = sm.execute();//Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password.
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

**Parent Topic:**[Scripting outbound REST](../../../../../integrate/outbound-rest/concept/c_ScriptingOutboundREST.md)

