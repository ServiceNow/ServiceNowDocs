---
title: HttpRequestData - Scoped
description: The HttpRequestData API provides methods to build and manipulate a REST request before applying a signature and sending it to an endpoint.Instantiates an HttpRequestData object.Adds a header to the HttpRequestData object.Adds a query parameter to the HttpRequestData object.Removes a header from the HttpRequestData object.Returns the sys\_id of the Connection &amp; Credential alias associated with the Integration Hub REST step.Returns the value of a connection attribute associated with the Connection &amp; Credential alias associated with Integration Hub REST step.Returns the content of the request in the HttpRequestData object.Returns the date when the request was signed.Returns whether the signature is applied to the request in the header or as a query parameter.Returns the endpoint set for the request.Returns the time in seconds before the signature expires starting when the request was signed using the generateAuth\(\) method in the RequestAuthAPI class.Returns the value associated with the given HTTP header.Returns an object containing the headers included in the request.Returns the host used in the request.Returns the HTTP method used in the request.Returns the value of the specified query parameter.Returns an object containing the query parameters included in the request.Returns the region for the request that will be used in signing.Returns the service defined in the request.Defines the content to send in the request.Defines the date of the request used for signing.Defines whether to apply the signature to the request in a header or as a query parameter.Defines the endpoint to send the request to.Sets the amount of time before the signature expires starting when the request is signed using the generateAuth\(\) method in the RequestAuthAPI class.Defines the host used in the request.Sets the HTTP method to use in the request.Defines the region to use for the request in signing.Defines the service for the request.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# HttpRequestData- Scoped

The HttpRequestData API provides methods to build and manipulate a REST request before applying a signature and sending it to an endpoint.

Generate outbound signing requests using these APIs in the following order:

1.  HttpRequestData: Build the API request.
2.  AuthCredential: Create a credential object or update an existing one. Use the credential to sign the request through the RequestAuthAPI class.
3.  RequestAuthAPI: Sign the request and return an HttpRequestAuthedData object.
4.  HttpRequestAuthedData: Get information about the signed request.
5.  GlideHTTPRequest: Send the signed request.

Before using these APIs, you must [configure an authentication algorithm](https://www.servicenow.com/docs/access?context=configure-authentication-algorithm&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) to sign the request and associate it with the credential used to authenticate the request.

Use this API in scoped scripts with the `sn_auth` namespace identifier. You can instantiate this class using the constructor, or you can return an HttpRequestData object from the getHttpRequestData\(\) method in the RequestAuthAPI class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## HttpRequestData - HttpRequestData\(\)

Instantiates an HttpRequestData object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var httpRequestData = new sn_auth.HttpRequestData();
```

## HttpRequestData - addHeader\(String key String value\)

Adds a header to the HttpRequestData object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the HTTP header.|
|value|String|Value of the HTTP Header.|

|Type|Description|
|----|-----------|
|void| |

This example creates a REST request payload.

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl', 'public-read' );
```

## HttpRequestData - addQueryParam\(String key, String value\)

Adds a query parameter to the HttpRequestData object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the query parameter.|
|value|String|Value of the query parameter.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addQueryParam('api_version', 'v2 );
​
```

## HttpRequestData - deleteHeader\(String key\)

Removes a header from the HttpRequestData object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the HTTP header to remove.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.deleteHeader('x-amz-acl');
```

## HttpRequestData - getConnectionAliasID\(\)

Returns the sys\_id of the Connection &amp; Credential alias associated with the Integration Hub REST step.

You can pass the sys\_id to the ConnectionInfoProvider API to retrieve information about the connection.

**Note:** You can only use this method in an Integration Hub REST step. For more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the alias record from the Connection &amp; Credential Aliases \[sys\_alias\] table associated with the request.|

```
var httpRequestData = new sn_auth.HttpRequestData();
var id = httpRequestData.getConnectionAliasID();
 
var credential = new sn_cc.ConnectionInfoProvider().
var connectionInfo = credential.getConnectionInfo(id);
```

## HttpRequestData - getConnectionExtendedAttribute\(String name\)

Returns the value of a connection attribute associated with the Connection &amp; Credential alias associated with Integration Hub REST step.

**Note:** You can only use this method in an Integration Hub REST step. For more information, see [REST step](https://www.servicenow.com/docs/access?context=rest-request-action-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

For more information about connection attributes, see [Create connection attributes for Integration Hub](https://www.servicenow.com/docs/access?context=create-connection-attributes&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the connection attribute.|

|Type|Description|
|----|-----------|
|String|Value of the connection attribute.|

This example returns the value of a connection attribute set on the Connection &amp; Credential alias associated with the REST step.

```
var httpRequestData = new sn_auth.HttpRequestData();​
gs.info("API Version is: " + httpRequestData.getConnectionExtendedAttribute('api_version'));
```

## HttpRequestData - getContent\(\)

Returns the content of the request in the HttpRequestData object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Content of the request.|

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
var ct = httpRequestData.getContent();
```

Output:

```
Action=SendMessage&MessageBody=This is a test message
```

## HttpRequestData - getDate\(\)

Returns the date when the request was signed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_kf4_zsx_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The difference between January 1, 1970 UTC and when the request was signed.Unit: Milliseconds

</td></tr></tbody>
</table>```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​

gs.info( "Date: " + httpRequestData.getDate());
```

Output:

```
Date: 1349333576093
```

## HttpRequestData - getDirective\(\)

Returns whether the signature is applied to the request in the header or as a query parameter.

By default, the system applies the signature to the header. You can apply the signature as a query parameter using the setDirective\(\) API.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_sjy_btx_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Whether the signature is applied to the header or as a query parameter. Values include:

 -   HEADER: The signature is applied to the request header.
-   QUERY: The signature is applied as a query parameter.

</td></tr></tbody>
</table>```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​

gs.info( "Signature applied to: " + httpRequestData.getDirective() );
```

Output:

```
Signature applied to: HEADER
```

## HttpRequestData - getEndpoint\(\)

Returns the endpoint set for the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Endpoint set for the request.|

```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​
httpRequestData.setDirective("query");​
​
gs.info( "Endpoint is: " + httpRequestData.getEndpoint() );
```

Output:

```
Endpoint is: https://s3.amazonaws.com
```

## HttpRequestData - getExpiry\(\)

Returns the time in seconds before the signature expires starting when the request was signed using the generateAuth\(\) method in the RequestAuthAPI class.

The expiration is commonly set by the third-party service you are sending the request to, which overrides any value set by the setExpiry\(\) method. For example, if the expiration is set to 900 seconds by the third-party service and you use the setExpiry\(\) method to set the expiration to 300 seconds, the getExpiry\(\) method returns 900 seconds.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wr1_ftx_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Time before the signature expires.Unit: Seconds

</td></tr></tbody>
</table>```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​
httpRequestData.setDirective("query");​
httpRequestData.setExpiry(300);

gs.info("Signature expires in: " + httpRequestData.getExpiry());
```

Output:

```
Signature expires in: 300
```

## HttpRequestData - getHeader\(String key\)

Returns the value associated with the given HTTP header.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of HTTP header.|

|Type|Description|
|----|-----------|
|String|Value of the given HTTP header.|

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl', 'public-read' );
​

gs.info( "Header value is: " + httpRequestData.getHeader('x-amz-acl') );
```

Output:

```
Header value is: public-read
```

## HttpRequestData - getHeaderMap\(\)

Returns an object containing the headers included in the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_thk_3tx_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Key-value pairs that define all of the headers associated with the request. Each key-value pair includes these parts:

 -   Key: String. Name of the header.
-   Value: String. Value of the header.

</td></tr></tbody>
</table>```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl', 'public-read' );
httpRequestData.addHeader('content-type', 'application/json' );

var map = httpRequestData.getHeaderMap();

for(var x in map) {
    var y = map[x]

    gs.info(x, y);
}
```

Output:

```
*** Script: x-amz-acl
*** Script: content-type
```

## HttpRequestData - getHost\(\)

Returns the host used in the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Host used in the request.|

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setHost('myHost')
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl' , 'public-read' );

gs.info("Host is: " + httpRequestData.getHost());
```

Output:

```
Host is: myHost
```

## HttpRequestData - getHttpMethod\(\)

Returns the HTTP method used in the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|HTTP method used in the request.|

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl', 'public-read' );
​

gs.info("HTTP method is: " + httpRequestData.getHttpMethod());
```

Output:

```
HTTP method is: PUT
```

## HttpRequestData - getQueryParam\(String key\)

Returns the value of the specified query parameter.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the query parameter to get the value of.|

|Type|Description|
|----|-----------|
|String|Value of the query parameter.|

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addQueryParam('api_version', 'v2' );

gs.info("API version is: " + httpRequestData.getQueryParam('api_version'));
```

Output:

```
API version is: v2
```

## HttpRequestData - getQueryParamMap\(\)

Returns an object containing the query parameters included in the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qk3_rtx_sjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Key-value pairs that define the query parameters associated with the request. Each key-value pair includes these parts:

 -   Key: String. Name of the query parameter.
-   Value: String. Value of the query parameter.

</td></tr></tbody>
</table>```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addQueryParam('api_version', 'v2' );
httpRequestData.addQueryParam('limit', '1000' );
httpRequestData.addQueryParam('offset', '1' );


var map = httpRequestData.getQueryParamMap();
gs.info("api_version is: " + map['api_version']);
```

Output:

```
api_version is: v2
```

## HttpRequestData - getRegion\(\)

Returns the region for the request that will be used in signing.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the region.|

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);

gs.info("Region is: " + httpRequestData.getRegion());
```

Output:

```
Region is: us-east-1
```

## HttpRequestData - getService\(\)

Returns the service defined in the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Service defined in the request.|

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');

gs.info("Service is: " + httpRequestData.getService());
```

Output:

```
Service is: s3
```

## HttpRequestData - setContent\(String content\)

Defines the content to send in the request.

**Note:** This method is not supported in script includes or MID server scripts.

|Name|Type|Description|
|----|----|-----------|
|content|String|Content to send in the request.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "This is a test message";
httpRequestData.setContent(content);
```

## HttpRequestData - setDate\(Number date\)

Defines the date of the request used for signing.

Use this method only when testing whether the signature is created correctly based on a time stamp. In production, the signing request uses the time that you generated the signature; manually setting this value may cause the signing request to fail.

<table id="table_xzg_pcy_sjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

date

</td><td>

Number

</td><td>

The difference between January 1, 1970 UTC and the date used to sign the request.Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');
httpRequestData.setDate(1349333576093);
```

## HttpRequestData - setDirective\(String directive\)

Defines whether to apply the signature to the request in a header or as a query parameter.

<table id="table_nxn_rcy_sjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

directive

</td><td>

String

</td><td>

Whether to apply the signature to the header or as a query parameter. Values include:

 -   `query`: Applies signature as a query parameter.
-   `header`: Applies signature to the request header.

 Default: header

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​
httpRequestData.setDirective("query");​
```

## HttpRequestData - setEndpoint\(String endpoint\)

Defines the endpoint to send the request to.

|Name|Type|Description|
|----|----|-----------|
|endpoint|String|Endpoint to send the request to. The endpoint can include query parameters, path, and version.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint="https://third-party-endpoint/path-parameters/version";

var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);

```

## HttpRequestData - setExpiry\(Number expiry\)

Sets the amount of time before the signature expires starting when the request is signed using the generateAuth\(\) method in the RequestAuthAPI class.

The expiration is commonly set by the third-party service you are sending the request to, which overrides any value set by the setExpiry\(\) method. For example, if the expiration is set to 900 seconds by the third-party service and you use the setExpiry\(\) method to set the expiration to 300 seconds, the getExpiry\(\) method returns 900 seconds.

<table id="table_wbj_5cy_sjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

expiry

</td><td>

Number

</td><td>

Amount of time before the signature expires.Unit: Seconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";​
var httpRequestData = new sn_auth.HttpRequestData();​
httpRequestData.setEndpoint(endpoint);​
httpRequestData.addQueryParam("list-type", "2");​
httpRequestData.setService('s3');​
httpRequestData.setHttpMethod('get');​
httpRequestData.setExpiry(300);​
```

## HttpRequestData - setHost\(String host\)

Defines the host used in the request.

|Name|Type|Description|
|----|----|-----------|
|host|String|Name of the HTTP request host.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https:third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setHost('myHost')
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl', 'public-read' );
```

## HttpRequestData - setHttpMethod\(String httpMethod\)

Sets the HTTP method to use in the request.

|Name|Type|Description|
|----|----|-----------|
|httpMethod|String|HTTP method to use in the request.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
```

## HttpRequestData - setRegion\(String region\)

Defines the region to use for the request in signing.

|Name|Type|Description|
|----|----|-----------|
|region|String|The region to use to sign the request. Available values are determined by the third-party API's requirements.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https:third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod('put');
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
```

## HttpRequestData - setService\(String service\)

Defines the service for the request.

|Name|Type|Description|
|----|----|-----------|
|service|String|The service for the request.|

|Type|Description|
|----|-----------|
|void| |

```
var endpoint= "https://s3.amazonaws.com";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');

```

