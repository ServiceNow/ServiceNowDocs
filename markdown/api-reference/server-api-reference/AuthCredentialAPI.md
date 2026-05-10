---
title: AuthCredential - Scoped
description: The AuthCredential\(\) API provides methods that enable you to build credentials for a REST request.Instantiates a new AuthCredential object, or modifies an existing one.Returns the value of an AuthCredential attribute.Sets an attribute for an AuthCredential object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AuthCredential- Scoped

The AuthCredential\(\) API provides methods that enable you to build credentials for a REST request.

Generate outbound signing requests using these APIs in the following order:

1.  HttpRequestData: Build the API request.
2.  AuthCredential: Create a credential object or update an existing one. Use the credential to sign the request through the RequestAuthAPI class.
3.  RequestAuthAPI: Sign the request and return an HttpRequestAuthedData object.
4.  HttpRequestAuthedData: Get information about the signed request.
5.  GlideHTTPRequest: Send the signed request.

Before using these APIs, you must [configure an authentication algorithm](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/configure-authentication-algorithm.md) to sign the request and associate it with the credential used to authenticate the request.

You can create an empty AuthCredential object, instantiate an existing AuthCredential object, or use the StandardCredentialsProvider class to instantiate an AuthCredential object using a Credential record from the Credentials \[discovery\_credentials\] table. If you create an empty AuthCredential object, use the setAttribute\(\) method to add properties to the object.

The following example shows how to instantiate an AuthCredential using StandardCredentialsProvider:

```
// Return an AuthCredential object using a Credential sys_id
var credential = new sn_cc.StandardCredentialsProvider().getAuthCredentialByID("5b61c16f73533300f662cff8faf6a74b");
```

Use the AuthCredential API in scoped scripts with the `sn_auth` namespace identifier.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AuthCredential - AuthCredential\(Object authCredential\)

Instantiates a new AuthCredential object, or modifies an existing one.

You can create an empty AuthCredential object, instantiate an existing AuthCredential object, or use the StandardCredentialsProvider class to instantiate an AuthCredential object using a Credential record from the Credentials \[discovery\_credentials\] table. If you create an empty AuthCredential object, use the setAttribute\(\) method to add properties to the object.

|Name|Type|Description|
|----|----|-----------|
|authCredential|Object|Optional. Include this parameter to update an existing AuthCredential object.|

## AuthCredential - getAttribute\(String key\)

Returns the value of an AuthCredential attribute.

<table id="table_ss5_hsx_5jb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Key of the attribute to return the value for. If you created an empty AuthCredential object, you must use the setAttribute\(\) method to add properties to the object.

 If you used a credential record to instantiate the AuthCredential object, pass a field name from the Credential \[discovery\_credentials\] table to access the value.

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
httpRequestData.addHeader('x-amz-acl', 'public-read' );
 
// Get AuthCredential object and set an attribute
var credential = new sn_auth.AuthCredential();
credential.setAttribute("user_name", "admin");
 
// Sign the request and return an AuthCredential attribute value
var signingAPI = new sn_auth.RequestAuthAPI(httpRequestData, credential);
var signingCredential = signingAPI.getAuthCredential();
name = signingCredential.getAttribute("name");
```

## AuthCredential - setAttribute\(String key, String value\)

Sets an attribute for an AuthCredential object.

|Name|Type|Description|
|----|----|-----------|
|key|String|Name of the attribute to set. If you created an empty AuthCredential object, you must use the this method to add properties to the object. If you used a credential record to instantiate the AuthCredential object, pass a field name from the Credential \[discovery\_credentials\] table to set the value.|
|value|String|Value of the attribute.|

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
httpRequestData.addHeader('x-amz-acl' , 'public-read' );
 
// Get AuthCredential object and set an attribute
var credential = new sn_auth.AuthCredential();
credential.setAttribute("user_name", "admin");
```

