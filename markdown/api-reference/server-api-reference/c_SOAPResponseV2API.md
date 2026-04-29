---
title: SOAPResponseV2 - Scoped, Global
description: The SOAPResponseV2 API provides methods that use the data returned by an outbound SOAP message in JavaScript code.Returns all headers contained in the response, including any duplicate headers.Gets the content of the SOAP response body.Returns all cookies included in the response.Gets the numeric error code if there was an error during the SOAP transaction.Gets the error message if there was an error during the SOAP transaction.Gets the value for a specified HTTP header.Gets all HTTP headers returned in the SOAP response and the associated values.Gets the numeric HTTP status code returned by the SOAP provider.Indicates if there was an error during the SOAP transaction.Sets the amount of time the instance waits for a response from the web service provider.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SOAPResponseV2 - Scoped, Global

The SOAPResponseV2 API provides methods that use the data returned by an outbound SOAP message in JavaScript code.

A SOAPResponseV2 object is returned by the SOAPMessageV2 methods execute\(\) and executeAsync\(\).

You can use this API in scoped applications or within the global scope.

This API runs in the `sn_ws` namespace.

See also:

-   [Direct SOAPMessageV2 example](../../SOAPMessageV2/reference/r_DirectSOAPMessageV2Example.md)
-   [Recordless SOAPMessageV2 example](../../SOAPMessageV2/reference/r_RecordlessSOAPMessageV2Example.md)
-   [Asynchronous SOAPMessageV2 example](../../SOAPMessageV2/reference/r_AsyncronousSOAPMessageV2Example.md)
-   [SOAPMessageV2 MID server example](../../SOAPMessageV2/reference/r_SOAPMessageV2MIDServerExample.md)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SOAPResponseV2 - getAllHeaders\(\)

Returns all headers contained in the response, including any duplicate headers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|List&lt;GlideHTTPHeader&gt;|List of headers contained in the response. Each header is represented as a GlideHTTPHeader object which contains the header *name* and *value*.|

```
var r = new sn_ws.SOAPMessageV2('<A SOAP message>', 'get');
var response = r.execute();
var headers = response.getAllHeaders();
for(var i in headers){
  gs.info(headers[i].name + ': ' + headers[i].value);
}
```

## SOAPResponseV2 - getBody\(\)

Gets the content of the SOAP response body.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|SOAP response body.|

```
var body = response.getBody();
```

## SOAPResponseV2 - getCookies\(\)

Returns all cookies included in the response.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Array of strings representing cookies. Iterate through the array to perform operations on each cookie.|

Display individual cookies from the response.

```
var cookies = response.getCookies();
for (var i = 0; i < cookies.length; i++) {
  gs.info('cookie: ' + cookies.get(i));
}
```

Output:

```
cookie: JSESSIONID=4135AA97A5D12DA22EF614AA2B0CAFD8.node20; Path=/; Secure; HttpOnly
cookie: SABASESSIONID=370152970.36895.0000; path=/
```

## SOAPResponseV2 - getErrorCode\(\)

Gets the numeric error code if there was an error during the SOAP transaction.

This error code is specific to the ServiceNow AI Platform, it is not an HTTP error code. Provide this error code if you require assistance from Customer Service and Support.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Numeric error code, such as 1 for a socket timeout.|

```
var errorCode = response.getErrorCode();
```

## SOAPResponseV2 - getErrorMessage\(\)

Gets the error message if there was an error during the SOAP transaction.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Error message|

```
var errorMsg = response.getErrorMessage();
```

## SOAPResponseV2 - getHeader\(String name\)

Gets the value for a specified HTTP header.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the header that you want the value for, such as Set-Cookie.|

|Type|Description|
|----|-----------|
|String|Value of the specified header.|

```
var headerVal = response.getHeader("Accept");
```

## SOAPResponseV2 - getHeaders\(\)

Gets all HTTP headers returned in the SOAP response and the associated values.

**Note:** If a header is present more than once in the response, such as a Set-Cookie header, this function returns only the last of the duplicate headers. To return all headers including duplicates, use the getAllHeaders\(\) function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object that maps the name of each header to the associated value.|

```
var headers = response.getHeaders();
```

## SOAPResponseV2 - getStatusCode\(\)

Gets the numeric HTTP status code returned by the SOAP provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Numeric status code returned by the SOAP provider, such as 200 for a successful response.|

```
var statusCode = response.getStatusCode();
```

## SOAPResponseV2 - haveError\(\)

Indicates if there was an error during the SOAP transaction.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|boolean|Returns true if there was an error, false if there was no error.|

```
var error = response.haveError();
```

## SOAPResponseV2 - waitForResponse\(Number timeoutSecs\)

Sets the amount of time the instance waits for a response from the web service provider.

This method overrides the property glide.soap.outbound.ecc\_response.timeout for this SOAP response.

|Name|Type|Description|
|----|----|-----------|
|timeoutSecs|Number|Amount of time, in seconds, to wait for this response.|

|Type|Description|
|----|-----------|
|void| |

```
response.waitForResponse(60);
```

