---
title: HttpRequestAuthedData - Scoped
description: The HttpRequestAuthedData\(\) API provides methods to access and set values in a signed REST or SOAP request.Instantiates an HttpRequestAuthedData object.Adds a header to the HttpRequestAuthedData object.Adds a query parameter to the HttpRequestAuthedData object.Returns the credential value that was included when the request was signed.Returns whether the signature is applied to the request in the header, as a query parameter, or as a credential value.Returns an object containing the headers that were included when the request was signed.Returns an object containing the query parameters included when the request was signed.Returns the status of the request signing.Returns a detailed message about the request signing. If the request signing fails, this method returns the error message.Sets a credential value for the HttpRequestAuthedData object.Defines whether to apply the signature to the signed request in the header, as a query parameter, or as a credential value.Sets the status of the request signing.Sets a status message for the request signing.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# HttpRequestAuthedData- Scoped

The HttpRequestAuthedData\(\) API provides methods to access and set values in a signed REST or SOAP request.

Generate outbound signing requests using these APIs in the following order:

1.  HttpRequestData: Build the API request.
2.  AuthCredential: Create a credential object or update an existing one. Use the credential to sign the request through the RequestAuthAPI class.
3.  RequestAuthAPI: Sign the request and return an HttpRequestAuthedData object.
4.  HttpRequestAuthedData: Get information about the signed request.
5.  GlideHTTPRequest: Send the signed request.

Before using these APIs, you must [configure an authentication algorithm](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/configure-authentication-algorithm.md) to sign the request and associate it with the credential used to authenticate the request.

Use this API in scoped scripts with the `sn_auth` namespace identifier. You can instantiate this class using the constructor, or you can return an HttpRequestAuthedData object from the generateAuth\(\) method in the RequestAuthAPI class.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## HttpRequestAuthedData - HttpRequestAuthedData\(\)

Instantiates an HttpRequestAuthedData object.

You can instantiate this class using the constructor, or you can return an HttpRequestAuthedData object from the generateAuth\(\) method in the RequestAuthAPI class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## HttpRequestAuthedData - addHeader\(String key, String value\)

Adds a header to the HttpRequestAuthedData object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the HTTP header.|
|value|String|Value of the HTTP Header.|

|Type|Description|
|----|-----------|
|void| |

```
// Define HttpRequestData
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
//Get AuthCredential
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create RequestAuthAPI and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// Update the signed response
output.addHeader('access-rights', 'public-read');
```

## HttpRequestAuthedData - addQueryParam\(String key, String value\)

Adds a query parameter to the HttpRequestAuthedData object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the query parameter.|
|value|String|Value of the query parameter.|

|Type|Description|
|----|-----------|
|void| |

```
// Define HttpRequestData
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
//Get AuthCredential
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create RequestAuthAPI and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// Update the signed response
output.addQueryParameter('api_version', 'v2');
```

## HttpRequestAuthedData - getCredentialValue\(\)

Returns the credential value that was included when the request was signed.

Use a credential value to store a cookie, signature, or other value needed for an authentication algorithm. For example, create a Get Connection Info \(GCI\) step with a script that retrieves and stores a one-time token for a REST or SOAP call.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Text of the credential value.|

This example shows the retrieval of a credential value.

```
var RequestAuthGCISigner = Class.create();
RequestAuthGCISigner.prototype = Object.extend(new RequestAuthInternal(), {
  initialize: function() {
    RequestAuthInternal.prototype.initialize.call(this);
  },

  generateAuth: function(authAPI) {
    var requestData = authAPI.getHttpRequestData();

    // get credentials
    var credential = authAPI.getAuthCredential();
    var username = credential.getAttribute("user_name");
    var password = credential.getAttribute("password");
    var httpRequestSignedData = new sn_auth.HttpRequestAuthedData();
    var directive = requestData.getDirective();

    // set CREDENTIAL_VALUE
    httpRequestSignedData.setCredentialValue(username+":"+password);
    httpRequestSignedData.setDirective("CREDENTIAL_VALUE");
    httpRequestSignedData.setStatus("SUCCESS");

    gs.info("The Credential Value is " + httpRequestSignedData.getCredentialValue());
    return httpRequestSignedData;
  },
  type: 'RequestAuthGCISigner'
});
```

Output:

```
The Credential Value is someUsername:somePassword
```

## HttpRequestAuthedData - getDirective\(\)

Returns whether the signature is applied to the request in the header, as a query parameter, or as a credential value.

By default, the system applies the signature to the header. You can apply the signature as a query parameter or credential value by using the setDirective\(\) API.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lmr_dyy_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Whether the signature is applied to the header, as a query parameter, or as a credential value. Values include:

 -   HEADER: The signature is applied to the request header.
-   QUERY: The signature is applied as a query parameter.
-   CREDENTIAL\_VALUE: The signature is applied as a credential value.

</td></tr></tbody>
</table>```
// Define HttpRequestData
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
//Get AuthCredential
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create RequestAuthAPI and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
output.setDirective("header");

gs.info("Signature applied to: " + output.getDirective());
```

Output:

```
Signature applied to: HEADER
```

## HttpRequestAuthedData - getHeaderMap\(\)

Returns an object containing the headers that were included when the request was signed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_x3n_fyy_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Key-value pairs that define all of the headers included when the request was signed. Each key-value pair includes these parts:-   key: String. Name of the header.
-   value: String. Value of the header.

</td></tr></tbody>
</table>```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
// Get an AuthCredential object
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// get the signed response detail
var authH = headerM["Authorization"];
var xamzdateH = headerM["X-Amz-Date"];
var content256 = headerM["x-amz-content-sha256"];
 
gs.debug('authH:' + authH );
gs.debug('xamzdateH:' + xamzdateH );
gs.debug('content256:' + content256 );

```

Output:

```
*** Script: [DEBUG] authH:AWS4-HMAC-SHA256 Credential=lsjfljljfllfwek/20191127/us-east-1/s3/aws4_request, 
SignedHeaders=host;x-amz-acl;x-amz-content-sha256;x-amz-date, 
Signature=5c349011324910c34596ba7abbd10e07c4127774049f8953418bd7bed7d02b90 
*** Script: [DEBUG] xamzdateH:20191127T175210Z 
*** Script: [DEBUG] content256:UNSIGNED-PAYLOAD
```

## HttpRequestAuthedData - getQueryMap\(\)

Returns an object containing the query parameters included when the request was signed.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_fjx_gyy_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Key-value pairs that define the query parameters included when the request was signed. Each key-value pair includes these parts:-   key: String. Name of the query parameter.
-   value: String. Value of the query parameter.

</td></tr></tbody>
</table>```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addQueryParam('api_version', 'v2' );
httpRequestData.addQueryParam('limit', '1000' );
httpRequestData.addQueryParam('offset', '1' );
 
// Get an AuthCredential object
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// Get the signed response
queryMap = output.getQueryMap();

gs.info("API Version is: " + queryMap["api_version"]);
```

Output:

```
API Version is: v2
```

## HttpRequestAuthedData - getStatus\(\)

Returns the status of the request signing.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qwx_3yy_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The status of the request signing. Possible values:

 -   SUCCESS: The system successfully signed the request.
-   FAIL: The system failed to sign the request.
-   SKIPPED: The system skipped signing because the information was incomplete.

</td></tr></tbody>
</table>```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
// Get an AuthCredential object
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// Get the signed status
gs.info("Status is: " + output.getStatus());
```

Output:

```
Status is: SUCCESS
```

## HttpRequestAuthedData - getStatusMessage\(\)

Returns a detailed message about the request signing. If the request signing fails, this method returns the error message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_pbq_kyy_vjb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Message about the request signing. If the request signing fails, returns one of these error messages:-   `credential is not valid`: Check the AuthCredential object you used to sign the request. Make sure an authentication algorithm is associated with the credential. For more information, see [Configure an authentication algorithm](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/configure-authentication-algorithm.md).
-   `Request data is empty. Request auth is skipped`: Check the HttpRequestData object because required information may be missing.
-   `Can't find script includes scope`: Verify that the authentication algorithm record and associated script includes used to sign the request are in the correct scope.

</td></tr></tbody>
</table>```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
httpRequestData.addQueryParam('api_version', 'v2' );
httpRequestData.addQueryParam('limit', '1000' );
httpRequestData.addQueryParam('offset', '1' );
 
// Get AuthCredential object and set an attribute
var credential = new sn_auth.AuthCredential();
credential.setAttribute("user_name", "admin");
credential.setAttribute("password", "admin");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
// Get the signed status
gs.info("Status message is: " + output.getStatusMessage());
```

Output:

```
Status message is: credential is not valid.
```

## HttpRequestAuthedData - setCredentialValue\(String credential\_value\)

Sets a credential value for the HttpRequestAuthedData object.

Use a credential value to store a cookie, signature, or other value needed for an authentication algorithm. For example, create a Get Connection Info \(GCI\) step with a script that retrieves and stores a one-time token for a REST or SOAP call.

Use the setCredentialValue\(\) method to set the **Credential Value** data pill for REST, SOAP, and GCI steps in Workflow Studio.

|Name|Type|Description|
|----|----|-----------|
|credential\_value|String|Text of the credential value.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to set a credential value for a GCI step.

```
var RequestAuthGCISigner = Class.create();
RequestAuthGCISigner.prototype = Object.extend(new RequestAuthInternal(), {
  initialize: function() {
    RequestAuthInternal.prototype.initialize.call(this);
  },

  generateAuth: function(authAPI) {
    var requestData = authAPI.getHttpRequestData();

    // get credentials
    var credential = authAPI.getAuthCredential();
    var username = credential.getAttribute("user_name");
    var password = credential.getAttribute("password");
    var httpRequestSignedData = new sn_auth.HttpRequestAuthedData();
    var directive = requestData.getDirective();
    var b64data = GlideStringUtil.base64encode(username+":"+password);

    // set CREDENTIAL_VALUE
    httpRequestSignedData.setCredentialValue("Basic " + b64data);
    httpRequestSignedData.setDirective("CREDENTIAL_VALUE");
    httpRequestSignedData.setStatus("SUCCESS");
    return httpRequestSignedData;
  },
  type: 'RequestAuthGCISigner'
});
```

## HttpRequestAuthedData - setDirective\(String directive\)

Defines whether to apply the signature to the signed request in the header, as a query parameter, or as a credential value.

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

Whether to apply the signature to the header, query parameter, or credential value of the signed request. Values include:

 -   `query`: Applies signature as a query parameter.
-   `header`: Applies signature to the request header.
-   `credential_value` : Applies signature to the credential value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
// Define HttpRequestData
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
//Get AuthCredential
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create RequestAuthAPI and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
output.setDirective("header");

```

## HttpRequestAuthedData - setStatus\(String status\)

Sets the status of the request signing.

<table id="table_pbr_4yy_vjb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

String

</td><td>

The status of the request signing. Possible values:

 -   `success`: The system successfully signed the request.
-   `fail`: The system failed to sign the request.
-   `skipped`: The system skipped signing because the information was incomplete.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
// Get an AuthCredential object
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
output.setStatus("fail");
 
// Get the signed status
gs.info("Status is: " + output.getStatus());
```

Output:

```
 Status is: FAIL
```

## HttpRequestAuthedData - setStatusMessage\(String statusMessage\)

Sets a status message for the request signing.

|Name|Type|Description|
|----|----|-----------|
|statusMessage|String|Message to set for the request signing status.|

|Type|Description|
|----|-----------|
|void| |

```
// Define the HttpRequestData object
var endpoint= "https://third-party-endpoint";
var httpRequestData = new sn_auth.HttpRequestData();
httpRequestData.setEndpoint(endpoint);
httpRequestData.setService('s3');
httpRequestData.setRegion('us-east-1');
httpRequestData.setHttpMethod("PUT");
var content = "Action=SendMessage&MessageBody=This is a test message";
httpRequestData.setContent(content);
 
// Get an AuthCredential object
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
output.setStatusMessage("The request was successfully signed.");
 
// Get the signed status message
gs.info("Status message is: " + output.getStatusMessage());
```

Output:

```
Status message is: The request was successfully signed.
```

