---
title: RESTMessageV2 MID server example
description: You can send an outbound REST message through a MID Server.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripting outbound REST, Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# RESTMessageV2 MID server example

You can send an outbound REST message through a MID Server.

By sending the message through a MID Server, you can access endpoints that are behind a firewall or within a private network. All REST messages sent through a MID Server are asynchronous.

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
	sm.setMIDServer('mid_server_name');
	response = sm.executeAsync(); // Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password.

	response.waitForResponse(60); // In seconds. Wait at most 60 seconds to get response from ECC Queue/Mid Server //Might throw exception timing out waiting for response in ECC queue.

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

**Note:** This example uses `waitForResponse` to pause for a response, and then details how the response is handled. However, when using `executeAsync`, consider processing the response body in a separate business rule to take advantage of the asynchronous call rather than using `waitForResponse`.

**Parent Topic:**[Scripting outbound REST](../../../../../integrate/outbound-rest/concept/c_ScriptingOutboundREST.md)

