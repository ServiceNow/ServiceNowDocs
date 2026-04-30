---
title: RESTResponseV2 - Scoped, Global
description: The RESTResponseV2 API provides methods that allow you to use the data returned by an outbound REST message in JavaScript code.Returns all headers contained in the response, including any duplicate headers.Gets the content of the REST response body.Returns all cookies included in the response.Gets the numeric error code if there was an error during the REST transaction.Gets the error message if there was an error during the REST transaction.Gets the value for a specified header.Gets all headers returned in the REST response and the associated values.Gets the fully-resolved query sent to the REST endpoint..Gets the sys\_id value of the attachment created from the response body content.Gets the numeric HTTP status code returned by the REST provider.Indicates if there was an error during the REST transaction.Set the amount of time the instance waits for a response from the web service provider.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTResponseV2 - Scoped, Global

The RESTResponseV2 API provides methods that allow you to use the data returned by an outbound REST message in JavaScript code.

A RESTResponseV2 object is returned by the RESTMessageV2 methods execute\(\) and executeAsync\(\).

You can use this API in scoped applications or within the global scope.

This API runs in the `sn_ws` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTResponseV2 - getAllHeaders\(\)

Returns all headers contained in the response, including any duplicate headers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|List&lt;GlideHTTPHeader&gt;|List of headers contained in the response. Each header is represented as a GlideHTTPHeader object which contains the header *name* and *value*.|

The follow code example shows how to call the REST Table API and then lists out all of the headers found in the response.

```
var request = new sn_ws.RESTMessageV2();
request.setEndpoint('http://<SN_Instance_host>/api/now/table/incident');
request.setHttpMethod('GET');

request.setBasicAuth('username', 'password');
request.setRequestHeader("Accept", "application/json");
var res = request.execute();
if (res.getStatusCode() != 200) {
  gs.info('Bad Request');
}

var headers = res.getAllHeaders();
for(var i in headers){
  gs.info(headers[i].name + ': ' + headers[i].value);
}
```

Response headers

```
X-Is-Logged-In: true
X-Transaction-ID: e3003cb2db8c
X-Total-Count: 66
X-Content-Type-Options: nosniff
Pragma: no-store,no-cache
Cache-Control: no-cache,no-store,must-revalidate,max-age=-1
Expires: 0
Content-Type: application/json;charset=UTF-8
Date: Fri, 14 May 2021 16:05:10 GMT
Connection: close
Server: ServiceNow
JSESSIONID=5041870726ADADFAB2EE2BF8E7E01596; Path=/; HttpOnly; SameSite=None; Secure
Set-Cookie: glide_user=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT; Path=/; HttpOnly; SameSite=None; Secure
Set-Cookie: glide_user_session=; Max-Age=0; Expires=Thu, 01-Jan-1970 00:00:10 GMT; Path=/; HttpOnly; SameSite=None; Secure
Set-Cookie: glide_user_route=glide.f1aa2015b3fa5fa8dfe567386cde8fd5; Max-Age=2147483647; Expires=Wed, 01-Jun-2089 19:19:17 GMT; Path=/; HttpOnly; SameSite=None; Secure
Set-Cookie: glide_session_store=AF003CB2DB8CF8103DD9C39D139619C7; Max-Age=1800; Expires=Fri, 14-May-2021 16:35:10 GMT; Path=/; HttpOnly; SameSite=None; Secure
Set-Cookie: BIGipServerpool_ddershem=2643023626.45630.0000; path=/; Httponly; Secure; SameSite=None; Secure
Strict-Transport-Security: max-age=63072000; includeSubDomains
```

## RESTResponseV2 - getBody\(\)

Gets the content of the REST response body.

Use this function when you want to get the request body as text content. Do not use this method when saving the response as a binary attachment. If a RESTMessageV2 object called the saveResponseBodyAsAttachment\(...\) function, using getBody\(\) on the associated RESTResponseV2 object will cause an error. When saving the response as an attachment, if the outbound REST message fails, call getErrorMessage\(\) on the response to retrieve the body content.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|REST response body.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var responseBody = response.getBody();
```

## RESTResponseV2 - getCookies\(\)

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

## RESTResponseV2 - getErrorCode\(\)

Gets the numeric error code if there was an error during the REST transaction.

This error code is specific to the ServiceNow AI Platform, it is not an HTTP error code. Provide this error code if you require assistance from ServiceNow Customer Support.

**Note:** To retrieve the contents of the actual error message, use the [getBody\(\)](c_RESTResponseV2API.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Numeric error code, such as 1 for socket timeout.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var errorCode = response.getErrorCode();
```

## RESTResponseV2 - getErrorMessage\(\)

Gets the error message if there was an error during the REST transaction.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Error message.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var errorMsg = response.getErrorMessage();
```

## RESTResponseV2 - getHeader\(String name\)

Gets the value for a specified header.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the header that you want the value for, such as Set-Cookie.|

|Type|Description|
|----|-----------|
|String|Value of the specified header.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var headerVal = response.getHeader("Content-Type");
```

## RESTResponseV2 - getHeaders\(\)

Gets all headers returned in the REST response and the associated values.

**Note:** If a header is present more than once in the response, such as a Set-Cookie header, this function returns only the last of the duplicate headers. To return all headers including duplicates, use the getAllHeaders\(\) function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Object that maps the name of each header to the associated value.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var headers = response.getHeaders();
```

## RESTResponseV2 - getQueryString\(\)

Gets the fully-resolved query sent to the REST endpoint..

This query contains the endpoint URL as well as any values assigned to variables in the REST message. Use this method only with responses to direct requests. This method is not supported for requests sent asynchronously, or requests sent using a MID server.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Fully-resolved query.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var queryString = response.getQueryString();
```

## RESTResponseV2 - getResponseAttachmentSysid\(\)

Gets the sys\_id value of the attachment created from the response body content.

If the RESTMessageV2 object associated with this response called the saveResponseBodyAsAttachment\(...\) function, use getResponseAttachmentSysid\(\) to get the sys\_id of the created attachment record. Use this function when you want to perform additional operations with the new attachment record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the new attachment record.|

## RESTResponseV2 - getStatusCode\(\)

Gets the numeric HTTP status code returned by the REST provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Numeric status code returned by the REST provider, such as 200 for a successful response.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var statusCode = response.getStatusCode();
```

## RESTResponseV2 - haveError\(\)

Indicates if there was an error during the REST transaction.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|boolean|Returns true if there was an error, false if there was no error.|

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute();
var error = response.haveError();
```

## RESTResponseV2 - waitForResponse\(Number timeoutSecs\)

Set the amount of time the instance waits for a response from the web service provider.

This method overrides the property glide.rest.outbound.ecc\_response.timeout for this REST response.

|Name|Type|Description|
|----|----|-----------|
|timeoutSecs|Number|The amount of time, in seconds, to wait for this response.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2("Yahoo Finance","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.executeAsync();
response.waitForResponse(60);
```

