---
title: SOAPMessageV2 - Scoped, Global
description: The SOAPMessageV2 API provides methods to send an outbound SOAP message using JavaScript.Instantiates an empty SOAPMessageV2 object.Instantiates a SOAPMessageV2 object from a SOAP message record and a function associated with that record.Sends the SOAP message to the endpoint.Sends the SOAP message to the External Communication Channel \(ECC\) queue.Gets the endpoint for the SOAP message.Returns the content of the SOAP message body.Gets the value for an HTTP header specified by the SOAP client.Gets HTTP headers that were set by the SOAP client and the associated values.Sets one or more URIs allowed to be redirected to. Controlling the allowed outbound URIs reduces security concerns and helps prevent URL redirect attacks that send users to malicious sites.Sets basic authentication headers for the SOAP message.Associates outbound requests and the resulting response record in the ECC queue.Overrides a value from the database by writing to the SOAP message payload.Sets the endpoint for the SOAP message.Sets the parameter in the API that controls automatic HTTP redirects. By default, automatic redirects are turned off.Sets the amount of time the SOAP message waits for a response from the web service provider before the request times out.Sets the log level for this message and the corresponding response.Configures the SOAP message to be sent through a MID Server.Sets the mutual authentication protocol profile for the SOAP message.Sets the body content to send to the web service provider.Sets an HTTP header in the SOAP message to the specified value.Defines the SOAP action this SOAP message performs.Sets a variable with the specified name from the SOAP message record to the specified value.Sets a variable with the specified name from the SOAP message record to the specified value.Sets web service security values for the SOAP message.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SOAPMessageV2 - Scoped, Global

The SOAPMessageV2 API provides methods to send an outbound SOAP message using JavaScript.

Use this API to manage the response returned by the SOAP provider.

You can use this API in scoped applications or within the global scope. This API runs in the `sn_ws` namespace.

See also:

-   [Direct SOAPMessageV2 example](../reference/r_DirectSOAPMessageV2Example.md)
-   [Recordless SOAPMessageV2 example](../reference/r_RecordlessSOAPMessageV2Example.md)
-   [Asynchronous SOAPMessageV2 example](../reference/r_AsyncronousSOAPMessageV2Example.md)
-   [SOAPMessageV2 MID server example](../reference/r_SOAPMessageV2MIDServerExample.md)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SOAPMessageV2 - SOAPMessageV2\(\)

Instantiates an empty SOAPMessageV2 object.

When using an object instantiated this way, you must manually specify a SOAP action and endpoint.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var sm = new sn_ws.SOAPMessageV2();
```

## SOAPMessageV2 - SOAPMessageV2\(String soapMessage, String soapFunction\)

Instantiates a SOAPMessageV2 object from a SOAP message record and a function associated with that record.

Values such as the endpoint, authentication, or MID Server settings from the SOAP message record apply to this object.

|Name|Type|Description|
|----|----|-----------|
|soapMessage|String|SOAP message record you want to use as the base for this object.|
|soapFunction|String|SOAP function you want to execute. Available SOAP functions depend on the WSDL supplied by the web service provider.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
```

## SOAPMessageV2 - execute\(\)

Sends the SOAP message to the endpoint.

This method calls synchronously, meaning that the script execution waits until the call completes before continuing.

Things to consider when using this method:

-   Only use this method for quick service calls. You shouldn't call this method in high volume no matter how quick the service.
-   Only use this method when the timeout is very short, otherwise the instance can be brought to a standstill. There are two properties that control the timeout period, **glide.http.timeout** and **glide.http.connection\_timeout**. By default, these timeouts are set to 175 seconds and 10 seconds respectively.
-   Generally, if the request must go through the MID Server, you shouldn't use this method. MID Server requests must go through the External Communication Channel \(ECC\) queue which is an asynchronous queue. The thread isn't only held up by the request itself, but it's also held up waiting for the MID Server to respond back to the instance. If MID Servers are involved, use asynchronous calls with a sensor business rule.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|[SOAPResponseV2](../../SOAPResponseV2/concept/c_SOAPResponseV2API.md#)|Response returned by the SOAP provider.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute(); //Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password.
```

## SOAPMessageV2 - executeAsync\(\)

Sends the SOAP message to the External Communication Channel \(ECC\) queue.

SOAP messages in the ECC queue are processed by the SOAPClient business rule.

By default, this business rule doesn't run asynchronously. To configure this business rule to run asynchronously, set the **When** value to `Async` and add `current.update()` to the end of the **Script**. The instance doesn't wait for a response from the web service provider when sending a message through the ECC queue.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qpt_3f5_jq" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SOAPResponseV2 - Scoped, Global

</td><td>

Response returned by the SOAP provider.**Note:** Attempting to use the SOAP response object before the response has been processed may result in a timeout error.

</td></tr></tbody>
</table>```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.executeAsync();
```

## SOAPMessageV2 - getEndpoint\(\)

Gets the endpoint for the SOAP message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|URL of the SOAP web service provider.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var endpoint = sm.getEndpoint();
```

## SOAPMessageV2 - getRequestBody\(\)

Returns the content of the SOAP message body.

**Note:** Before calling the getRequestBody\(\) method, you must call the [execute\(\)](c_SOAPMessageV2API.md#) method to obtain the response object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|SOAP message body.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","StockQuoteSoap.GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var requestBody = response.getRequestBody();
```

## SOAPMessageV2 - getRequestHeader\(String headerName\)

Gets the value for an HTTP header specified by the SOAP client.

By default, this method cannot return the value for a header set automatically by the system. To grant this method access to all headers, set the property glide.http.log\_debug to true.

|Name|Type|Description|
|----|----|-----------|
|headerName|String|Request header you want to get the value for.|

|Type|Description|
|----|-----------|
|String|Value of the specified header.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var header = sm.getRequestHeader("Accept");
```

## SOAPMessageV2 - getRequestHeaders\(\)

Gets HTTP headers that were set by the SOAP client and the associated values.

This method does not return headers set automatically by the system. To configure this method to return all headers, set the property glide.http.log\_debug to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object that maps the name of each header to the associated value.|

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var requestHeaders = sm.getRequestHeaders();
```

## SOAPMessageV2 - setAllowedRedirectURIs\(Array Uris\)

Sets one or more URIs allowed to be redirected to. Controlling the allowed outbound URIs reduces security concerns and helps prevent URL redirect attacks that send users to malicious sites.

For a more comprehensive means of redirecting URIs, see [UriMatcher - Scoped](../../UriMatcherScoped/concept/UriMatcherScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|Uris|Array|One or more URIs allowed for redirection. Each URI must be listed in "string" format.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add a list of URLs allowed for redirection for a SOAP message function.

```
// Redirection URI Allow list
try {
	var sm = new sn_ws.SOAPMessageV2('TemperatureConvert', 'TempConvertHttpPost.FahrenheitToCelsius');
	sm.setAllowedRedirectURIs(['https://www.w3schools.com/', 'https://www.google.com']);

	sm.execute();

} catch(ex) {
	var message = ex.getMessage();
}
```

## SOAPMessageV2 - setBasicAuth\(String userName, String userPass\)

Sets basic authentication headers for the SOAP message.

Setting basic authentication headers using this method overrides basic authentication values defined in the SOAP message record.

|Name|Type|Description|
|----|----|-----------|
|userName|String|Username to use when authenticating the SOAP message.|
|userPass|String|Password for the specified user.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setBasicAuth("username","password");
```

## SOAPMessageV2 - setEccCorrelator\(String correlator\)

Associates outbound requests and the resulting response record in the ECC queue.

This method only applies to SOAP messages sent through a MID Server. The correlator provided populates the **Agent correlator** field on the ECC queue record for the response. Provide a unique correlator for each outbound request to associate the correct results in the ECC queue with the request when designing asynchronous automation through a MID Server.

|Name|Type|Description|
|----|----|-----------|
|correlator|String|Unique identifier|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setEccCorrelator("unique_id");
```

## SOAPMessageV2 - setEccParameter\(String name, String value\)

Overrides a value from the database by writing to the SOAP message payload.

This method only applies to SOAP messages sent through a MID Server. Use this method when a value from the SOAP message in the database is invalid, such as when the endpoint URL is longer than the maximum **SOAP endpoint** field length.

These are valid values for the name parameter.

-   **source**: The endpoint URL.
-   **name**: The SOAP message function to run.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the ECC parameter.|
|value|String|Value to assign to the specified ECC parameter.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setEccParameter("source","http://very.long.endpoint");
```

## SOAPMessageV2 - setEndpoint\(String endpoint\)

Sets the endpoint for the SOAP message.

By default, the SOAP message uses the endpoint specified in the SOAP message record. Use this method to override the default. You must call this method when using the [SOAPMessageV2\(\)](c_SOAPMessageV2API.md#) constructor with no parameters.

|Name|Type|Description|
|----|----|-----------|
|endpoint|String|URL of the SOAP web service provider you want to interface with.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2();
sm.setEndpoint("http://web.service.endpoint");
```

## SOAPMessageV2 - setFollowRedirect\(Boolean followRedirect\)

Sets the parameter in the API that controls automatic HTTP redirects. By default, automatic redirects are turned off.

For additional information on HTTP redirects, see [Redirections in HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Redirections).

<table id="table_nhg_cfb_vcc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

followRedirect

</td><td>

Boolean

</td><td>

Flag that indicates whether the API should automatically follow any redirects that arise when executing the SOAPMessageV2 call.Valid values:

-   true: Automatically follow redirects.
-   false: Don't automatically follow redirects. You must handle all redirect conditions within your code.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to set automatic redirects on and have the API handle the redirect.

```
var sMessage = new sn_ws.SOAPMessageV2(); //Create an empty SOAP message
sMessage.setBasicAuth('admin','admin');
sMessage.setSOAPAction('http://www.service-now.com/incident/insert'); //set the SOAP action to perform
sMessage.setEndpoint('http://<instance>.service-now.com/incident.do?SOAP'); //set the web service provider endpoint
sMessage.setRequestBody('<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:inc=\"http://www.service-now.com/incident\"><soapenv:Header/><soapenv:Body><inc:insert><short_description>Test Dynamic SOAP</short_description></inc:insert></soapenv:Body></soapenv:Envelope>');
sMessage.setFollowRedirect(true);
var response = sMessage.execute();
gs.info(response.getStatusCode());

```

Output:

```
200
```

The following code example shows the automatic redirect set to false. The returned status code is a redirect code. In this case, you must handle the redirect within your code.

```
var sMessage = new sn_ws.SOAPMessageV2(); //Create an empty SOAP message
sMessage.setBasicAuth('admin','admin');
sMessage.setSOAPAction('http://www.service-now.com/incident/insert'); //set the SOAP action to perform
sMessage.setEndpoint('http://<instance>.service-now.com/incident.do?SOAP'); //set the web service provider endpoint
sMessage.setRequestBody('<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:inc=\"http://www.service-now.com/incident\"><soapenv:Header/><soapenv:Body><inc:insert><short_description>Test Dynamic SOAP</short_description></inc:insert></soapenv:Body></soapenv:Envelope>');
sMessage.setFollowRedirect(false);
var response = sMessage.execute();
gs.info(response.getStatusCode());

```

Output:

```
3xx  // Redirect status code
```

## SOAPMessageV2 - setHttpTimeout\(Number timeoutMs\)

Sets the amount of time the SOAP message waits for a response from the web service provider before the request times out.

|Name|Type|Description|
|----|----|-----------|
|timeoutMs|Number|Amount of time to wait for a response from the web service provider, in milliseconds.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setHttpTimeout(6000);
```

## SOAPMessageV2 - setLogLevel\(String level\)

Sets the log level for this message and the corresponding response.

Setting a log level using the SOAPMessageV2 API overrides the log level configured on the SOAP message record. This log level may not apply if the endpoint domain is excluded, or if the property **glide.outbound\_http\_log.override** is true. To view outbound web service logs, navigate to **System Logs** &gt; **Outbound HTTP Requests**.

<table id="table_lxw_gnc_sw" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

level

</td><td>

String

</td><td>

Log level. Valid values:

-   all
-   basic
-   elevated

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setLogLevel("all");
```

## SOAPMessageV2 - setMIDServer\(String midServerName\)

Configures the SOAP message to be sent through a MID Server.

By default, the SOAP message uses the MID Server specified in the SOAP message function record. Use this method to override the default.

|Name|Type|Description|
|----|----|-----------|
|midServerName|String|Name of the MID Server you want to send the SOAP message through. Your instance must have an active MID Server with the specified name.|

|Type|Description|
|----|-----------|
|void| |

## SOAPMessageV2 - setMutualAuth\(String profileName\)

Sets the mutual authentication protocol profile for the SOAP message.

Setting a protocol profile using this method overrides the protocol profile selected for the SOAP message record.

|Name|Type|Description|
|----|----|-----------|
|profileName|String|Name of the protocol profile to use for mutual authentication.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setMutualAuth("auth_profile_name");
```

## SOAPMessageV2 - setRequestBody\(String requestBody\)

Sets the body content to send to the web service provider.

When you set the body content using this method, variables in the body are not substituted for parameters from the SOAP message function record. You must explicitly define all values within the SOAP message body.

|Name|Type|Description|
|----|----|-----------|
|requestBody|String|Body of the SOAP message.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
var body = "<SOAP message body>";
sm.setRequestBody(body);
```

## SOAPMessageV2 - setRequestHeader\(String headerName, String headerValue\)

Sets an HTTP header in the SOAP message to the specified value.

|Name|Type|Description|
|----|----|-----------|
|headerName|String|Name of the header.|
|headerValue|String|Value to assign to the specified header.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setRequestHeader("Accept","Application/json");
```

## SOAPMessageV2 - setSOAPAction\(String soapAction\)

Defines the SOAP action this SOAP message performs.

The WSDL for your web service provider lists SOAP actions you can perform. You must call this method when using the [SOAPMessageV2\(\)](c_SOAPMessageV2API.md#) constructor with no parameters.

|Name|Type|Description|
|----|----|-----------|
|soapAction|String|SOAP action this SOAP message performs.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2();
sm.setSOAPAction("GetQuote");
//construct SOAP message by specifying endpoint and auth
sm.execute();
```

## SOAPMessageV2 - setStringParameter\(String name, String value\)

Sets a variable with the specified name from the SOAP message record to the specified value.

XML reserved characters in the value are converted to the equivalent escaped characters.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the SOAP message variable.|
|value|String|Value to assign to the specified variable.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setStringParameter("symbol","NOW");
```

## SOAPMessageV2 - setStringParameterNoEscape\(String name, String value\)

Sets a variable with the specified name from the SOAP message record to the specified value.

This method is equivalent to setStringParameter but does not escape XML reserved characters.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the SOAP message variable.|
|value|String|Value to assign to the specified variable.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setStringParameterNoEscape("symbol","NOW");
```

## SOAPMessageV2 - setWSSecurity\(String keystoreId, String keystoreAlias, String keystorePassword, String certificateId\)

Sets web service security values for the SOAP message.

Setting security values using this method overwrites web service security values defined for the SOAP message record.

|Name|Type|Description|
|----|----|-----------|
|keystoreId|String|Sys\_id of the Java or PKCS12 key store to use.|
|keystoreAlias|String|Alias that identifies the public and private keys.|
|keystorePassword|String|Password assigned to the key store record.|
|certificateId|String|Sys\_id of the trusted server certificate.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.SOAPMessageV2("StockQuote","GetQuote"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setWSSecurity("70d65e074f3812001f6eac118110c71a","Quote keys","UXr82cqX75Z7MaSa+EyjGA==","ba969a074f3812001f6eac118110c76d");
```

