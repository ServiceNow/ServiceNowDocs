---
title: RequestAuthAPI - Scoped
description: The RequestAuthAPI provides methods to apply a signature to a REST request.Instantiates a RequestAuthAPI object using a REST request and a credential.Signs the HttpRequestData object and returns an HttpRequestAuthedData object to use to send in the REST request.Returns the credential record used to sign the request.Returns the HttpRequestData object that was used to instantiate the RequestAuthAPI class.Generates a temporary, limited privilege token that you can use to provide trusted users with temporary security credentials to control third-party resources.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RequestAuthAPI- Scoped

The RequestAuthAPI provides methods to apply a signature to a REST request.

Generate outbound signing requests using these APIs in the following order:

1.  HttpRequestData: Build the API request.
2.  AuthCredential: Create a credential object or update an existing one. Use the credential to sign the request through the RequestAuthAPI class.
3.  RequestAuthAPI: Sign the request and return an HttpRequestAuthedData object.
4.  HttpRequestAuthedData: Get information about the signed request.
5.  GlideHTTPRequest: Send the signed request.

Before using these APIs, you must [configure an authentication algorithm](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/configure-authentication-algorithm.md) to sign the request and associate it with the credential used to authenticate the request.

Use this API in scoped scripts with the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RequestAuthAPI - RequestAuthAPI\(Object data, Object credential\)

Instantiates a RequestAuthAPI object using a REST request and a credential.

|Name|Type|Description|
|----|----|-----------|
|data|Object|HttpRequestData object that contains the unsigned REST request. Use the HttpRequestData class to build this object. See [HttpRequestData API](../../HttpRequestData/concept/HttpRequestDataAPI.md#).|
|credential|Object|Object that represents a record from the Credentials \[discovery\_credentials\] table. Retrieve this object using the AuthCredential class. See [AuthCredential API](../../AuthCredential/concept/AuthCredentialAPI.md#).|

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
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
 // Get a credential record
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("88772d0d40990010f8772fdd9ebc8075");
 
// Instantiate a RequestAuthAPI object
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
```

## RequestAuthAPI - generateAuth\(\)

Signs the HttpRequestData object and returns an HttpRequestAuthedData object to use to send in the REST request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HttpRequestAuthedData|Object. Data to use to obtain information about the signed result. Use the methods in the HttpRequestAuthedData class to interact with the signed result. See [HttpRequestAuthedData API](../../HttpRequestAuthedData/concept/HttpRequestAuthedDataAPI.md#).|

This example creates a request and gets a credential record to pass to the RequestAuthAPI API. The generateAuth\(\) method then signs the request.

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
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
// Get a credential record
gs.info( "date:" + httpRequestData.getDate() );
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Create the RequestAuthAPI object and sign the request
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var output = signingAPI.generateAuth();
 
```

## RequestAuthAPI - getAuthCredential\(\)

Returns the credential record used to sign the request.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|AuthCredential|Object. Data to use to obtain information about the credential record used to sign the request. Use the methods in the AuthCredential class to interact with the credential. See [AuthCredential API](../../AuthCredential/concept/AuthCredentialAPI.md#).|

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
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
// Get a credential record
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
 
// Return the AuthCredential object
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var signingCredential = signingAPI.getAuthCredential();
```

## RequestAuthAPI - getHttpRequestData\(\)

Returns the HttpRequestData object that was used to instantiate the RequestAuthAPI class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|HttpRequestData|Object. Contains the unsigned REST request. Use the methods in the HttpRequestData class to interact with the request. See [HttpRequestData API](../../HttpRequestData/concept/HttpRequestDataAPI.md#).|

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
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
 // Get a credential record
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("88772d0d40990010f8772fdd9ebc8075");
 
// Return the HttpRequestData object
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var unsignedRequest = signingAPI.getHttpRequestData();
 
gs.info("Endpoint is: " + unsignedRequest.getEndpoint());
```

Output:

```
Endpoint is: https://third-party-endpoint
```

## RequestAuthAPI - resetAuthCredential\(\)

Generates a temporary, limited privilege token that you can use to provide trusted users with temporary security credentials to control third-party resources.

To use this method, the third-party service must include an API or SDK that processes and manages limited access tokens.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
// Creates a temporary token 
function(authAPI) {​
    var requestData = authAPI.getHttpRequestData();​
    var credential= authAPI.getAuthCredential();​
    credential.setAttribute('Action', 'aws_sessionToken');​  
    authAPI.resetAuthCredential();	

    //Returns status information
    var status = credential.getAttribute('credential_reset_status'); ​
}
```

