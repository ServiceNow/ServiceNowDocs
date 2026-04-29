---
title: RESTMessageV2 - Scoped, Global
description: The RESTMessageV2 API provides methods that allow you to send outbound REST messages using JavaScript.Instantiates an empty RESTMessageV2 object.Instantiates a RESTMessageV2 object using information from a REST message record.Disables forced variable substitution in outbound REST messages.Sends the REST message to the endpoint.Sends the REST message to the endpoint asynchronously. The instance does not wait for a response from the web service provider when making asynchronous calls.Gets the URL of the endpoint for the REST message.Gets the content of the REST message body.Gets the value for an HTTP header specified in the REST message.Gets HTTP headers that were set by the REST client and the associated values.Configures the REST message to save the returned response body as an attachment record.Configures the REST message to save the returned response body as an encrypted attachment record.Sets one or more URIs allowed to be redirected to. Controlling the allowed outbound URIs reduces security concerns and helps prevent URL redirect attacks that send users to malicious sites.Sets the credentials for the REST message using an existing basic auth or OAuth 2.0 profile.Sets basic authentication headers for the REST message.Associates outbound requests and the resulting response record in the ECC queue. This method only applies to REST messages sent through a MID Server.Overrides a value from the database by writing to the REST message payload. This method only applies to REST messages sent through a MID Server.Sets the endpoint for the REST message.Sets the HTTP method this REST message performs, such as GET or PUT.Sets the amount of time the REST message waits for a response from the web service provider before the request times out.Sets the log level for this message and the corresponding response.Configures the REST message to communicate through a MID Server.Sets the mutual authentication protocol profile for the REST message.Appends a parameter to the end of the request URL with the form name=value.Sets the body content to send to the web service provider when using PUT or POST HTTP methods.Sets the request body using an existing attachment record.Sets an HTTP header in the REST message to the specified value.Overrides the default requestor profile for the REST message in order to retrieve an OAuth access token associated with a different requestor.Sets a REST message function variable with the specified name from the REST message record to the specified value.Sets a REST message function variable with the specified name from the REST message record to the specified value.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RESTMessageV2 - Scoped, Global

The RESTMessageV2 API provides methods that allow you to send outbound REST messages using JavaScript.

Use this API to manage the response returned by the REST provider.

The User-Agent value is "ServiceNow/1.0". To change this, add the glide.http.user.agent system property in the System Properties \[sys\_properties\] table.

This API runs in the `sn_ws` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RESTMessageV2 - RESTMessageV2\(\)

Instantiates an empty RESTMessageV2 object.

When using an object instantiated this way, you must manually specify an HTTP method and endpoint.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var sm = new sn_ws.RESTMessageV2();
```

## RESTMessageV2 - RESTMessageV2\(String name, String methodName\)

Instantiates a RESTMessageV2 object using information from a REST message record.

You must have a REST message record defined before you can use this constructor. For instructions, see [Create a REST message](../../../../../integrate/outbound-rest/task/t_ConfiguringARESTMessage.md).

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the REST message record in the REST Message \[sys\_rest\_message\] table.|
|methodName|String|The name of the HTTP method to use, such as GET/get or PUT/put - case insensitive.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get");
// Might throw exception if message doesn't exist or not visible due to scope.
```

## RESTMessageV2 - disableForcedVariableSubstitution\(\)

Disables forced variable substitution in outbound REST messages.

**Note:** Use of curly brackets or dollar signs in your request may inadvertently return a truncated output. If your request erroneously truncates the response or splits the response onto new lines, refer to [this Community article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1442596) for a potential solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get");
sm.disableForcedVariableSubstitution();
var response = sm.execute();
```

## RESTMessageV2 - execute\(\)

Sends the REST message to the endpoint.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|RESTResponse|The response returned by the REST provider.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.execute(); //Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password.
```

## RESTMessageV2 - executeAsync\(\)

Sends the REST message to the endpoint asynchronously. The instance does not wait for a response from the web service provider when making asynchronous calls.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|RESTResponse|The response returned by the REST provider.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance. When using `executeAsync`, consider processing the response body in a separate business rule to take advantage of the asynchronous call.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var response = sm.executeAsync(); //Might throw exception if http connection timed out or some issue with sending request itself because of encryption/decryption of password.

```

## RESTMessageV2 - getEndpoint\(\)

Gets the URL of the endpoint for the REST message.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The URL of the REST web service provider.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var endpoint = sm.getEndpoint();
```

## RESTMessageV2 - getRequestBody\(\)

Gets the content of the REST message body.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|the REST message body.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var body = sm.getRequestBody();
```

## RESTMessageV2 - getRequestHeader\(String headerName\)

Gets the value for an HTTP header specified in the REST message.

By default, this method cannot return the value for a header set automatically by the system. To grant this method access to all headers, set the property glide.http.log\_debug to true.

|Name|Type|Description|
|----|----|-----------|
|headerName|String|Request header you want to get the value for.|

|Type|Description|
|----|-----------|
|String|The value of the specified header.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var header = sm.getRequestHeader("Accept");
```

## RESTMessageV2 - getRequestHeaders\(\)

Gets HTTP headers that were set by the REST client and the associated values.

This method does not return headers set automatically by the system. To configure this method to return all headers, set the property glide.http.log\_debug to true.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|An Object that maps the name of each header to the associated value.|

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
var headers = sm.getRequestHeaders();
```

## RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName\)

Configures the REST message to save the returned response body as an attachment record.

When you use this function with a REST message that is sent through a MID server, the MID server user must have any roles required to read and write attachment records, as well as any roles required to read and write records on the table specified in the **tableName** parameter.

The response body does not need to be a binary file to be saved as an attachment. Response bodies using text formats, such as JSON or XML can also be saved. If the instance fails to save the attachment, call getErrorMessage\(\) on the related RESTResponseV2 object for error details.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Specify the table that contains the record you want to attach the saved file to.|
|recordSysId|String|Specify the sys\_id of the record you want to attach the saved file to.|
|fileName|String|Specify the file name to give to the saved file.|

|Type|Description|
|----|-----------|
|void| |

```
(function sampleRESTMessageV2() {
  try{
    var request  = new sn_ws.RESTMessageV2();        
    request.setHttpMethod('get');

    var attachment_sys_id  = '<attachment_record_sys_id>', 
      tablename = 'incident',
      recordSysId = '<incident_sys_id>',            
      response,            
      httpResponseStatus,             
      filename ='<filename>';

    //endpoint - ServiceNow REST Attachment API        
    request.setEndpoint('https://<instance_name>.service-now.com/api/now/attachment/' + attachment_sys_id  +'/file');        
    request.setBasicAuth('<username>', '<password>');

    //RESTMessageV2 - saveResponseBodyAsAttachment(String tableName, String recordSysId, String fileName)        
    request.saveResponseBodyAsAttachment(tablename, recordSysId, filename);        

    response = request.execute();        
    httpResponseStatus = response.getStatusCode();  
      
    gs.info(" http response status_code:  " + httpResponseStatus);    
  }
  catch(ex){
    var message  = ex.getMessage();        
    gs.info(message);    
  }
})();
```

## RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName, String encryptContext\)

Configures the REST message to save the returned response body as an encrypted attachment record.

When you use this function with a REST message that is sent through a MID server, the MID server user must have any roles required to read and write attachment records, as well as any roles required to read and write records on the table specified in the **tableName** parameter.

The response body does not need to be a binary file to be saved as an attachment. Response bodies using text formats, such as JSON or XML can also be saved. If the instance fails to save the attachment, call getErrorMessage\(\) on the related RESTResponseV2 object for error details.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Specify the table that contains the record you want to attach the saved file to.|
|recordSysId|String|Specify the sys\_id of the record you want to attach the saved file to.|
|fileName|String|Specify the file name to give to the saved file.|
|encryptContext|String|Specify the sys\_id of an encryption context. The saved file is encrypted using this context.|

|Type|Description|
|----|-----------|
|void| |

## RESTMessageV2 - setAllowedRedirectURIs\(Array Uris\)

Sets one or more URIs allowed to be redirected to. Controlling the allowed outbound URIs reduces security concerns and helps prevent URL redirect attacks that send users to malicious sites.

For a more comprehensive means of redirecting URIs, see [UriMatcher - Scoped](../../UriMatcherScoped/concept/UriMatcherScopedAPI.md#).

|Name|Type|Description|
|----|----|-----------|
|Uris|Array|One or more URIs allowed for redirection. Each URI must be listed in "string" format.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to add one or more URLs allowed for redirection for a REST message method.

```
// Redirection URI Allow list
try{
	var rm = new sn_ws.RESTMessageV2('<REST_message_record>', '<REST_Msg_method_name>');
	rm.setAllowedRedirectURIs(['https://www.google.com']);

	var response = rm.execute();
	var responseBody = response.getBody();
	var httpStatus = response.getStatusCode();
	gs.info(responseBody);
	gs.info(httpStatus);
} catch(ex) {
	var message = ex.getMessage();
}
```

## RESTMessageV2 - setAuthenticationProfile\(String type, String profileId\)

Sets the credentials for the REST message using an existing basic auth or OAuth 2.0 profile.

|Name|Type|Description|
|----|----|-----------|
|type|String|The type of authentication profile to use. Valid values are 'basic' to use basic authentication, or 'oauth2' to use OAuth 2.0.|
|profileId|String|The sys\_id of an authentication profile record. When using basic auth, specify the sys\_id of a Basic Auth Configuration \[sys\_auth\_profile\_basic\] record. When using OAuth 2.0, specify the sys\_id of a OAuth Entity Profile \[oauth\_entity\_profile\] record.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var requestBody;
var responseBody;
var status;
var sm;
try{
       // Might throw exception if message doesn't exist or not visible due to scope.
	sm = new sn_ws.RESTMessageV2("<REST_message_record>", "get");  

       //set auth profile to an OAuth 2.0 profile record.
	sm.setAuthenticationProfile('oauth2', '1234adsf123212131123qasdsf'); 

	sm.setStringParameter("symbol", "NOW");
	sm.setStringParameterNoEscape("xml_data","<data>test</data>");

       //In milliseconds. Wait at most 10 seconds for response from http request.
	sm.setHttpTimeout(10000); 
       //Might throw exception if http connection timed out or some issue 
       //with sending request itself because of encryption/decryption of password.
	response = sm.execute();	
       responseBody = response.haveError() ? response.getErrorMessage() : response.getBody();
	status = response.getStatusCode();
} catch(ex) {
	responseBody = ex.getMessage();
	status = '500';
} finally {
	requestBody = sm ? sm.getRequestBody():null;
}
```

## RESTMessageV2 - setBasicAuth\(String userName, String userPass\)

Sets basic authentication headers for the REST message.

Setting security values using this method overrides basic authentication values defined for the REST message record.

|Name|Type|Description|
|----|----|-----------|
|userName|String|Username you want to use to authenticate the REST message.|
|userPass|String|Password for the specified user.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setBasicAuth("username","password");
```

## RESTMessageV2 - setEccCorrelator\(String correlator\)

Associates outbound requests and the resulting response record in the ECC queue. This method only applies to REST messages sent through a MID Server.

The correlator provided populates the **Agent correlator** field on the ECC queue record for the response. Provide a unique correlator for each outbound request to associate the correct results in the ECC queue with the request when designing asynchronous automation through a MID Server.

|Name|Type|Description|
|----|----|-----------|
|correlator|String|Unique identifier|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setEccCorrelator("unique_identifier");
```

## RESTMessageV2 - setEccParameter\(String name, String value\)

Overrides a value from the database by writing to the REST message payload. This method only applies to REST messages sent through a MID Server.

Use this method when a value from the REST message in the database is invalid, such as when the endpoint URL is longer than the maximum REST endpoint field length. You can set only the endpoint URL using this method by passing source as the name parameter.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the parameter, such as source.|
|value|String|The value to assign to the specified parameter.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setEccParameter("source","http://very.long.endpoint.url");
```

## RESTMessageV2 - setEndpoint\(String endpoint\)

Sets the endpoint for the REST message.

By default, the REST message uses the endpoint specified in the REST message record. Use this method to override this default. You must call this method when using the [RESTMessageV2 - RESTMessageV2\(\)](c_RESTMessageV2API.md#) constructor with no parameters.

|Name|Type|Description|
|----|----|-----------|
|endpoint|String|The URL of the REST provider you want to interface with.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2();
sm.setEndpoint("http://web.service.endpoint");
```

## RESTMessageV2 - setHttpMethod\(String method\)

Sets the HTTP method this REST message performs, such as GET or PUT.

You must set an HTTP method when using the [RESTMessageV2 - RESTMessageV2\(\)](c_RESTMessageV2API.md#) constructor with no parameters.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

method

</td><td>

String

</td><td>

Sets the HTTP method this REST message performs. The provided HTTP method is not case sensitive. The following HTTP methods are supported:

-   GET
-   POST
-   PUT
-   PATCH
-   DELETE
-   HEAD

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2();
sm.setHttpMethod("post");
```

## RESTMessageV2 - setHttpTimeout\(Number timeoutMs\)

Sets the amount of time the REST message waits for a response from the web service provider before the request times out.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

timeoutMs

</td><td>

Number

</td><td>

Amount of time in milliseconds before the call to the REST provider times out.**Note:** This value sets a timeout on the socket and only times out if the socket does not receive data within the specified time. For environments in which responses are streamed, it's possible that connections last much longer than the timeout value.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

To use the following example, replace *&lt;REST\_message\_record&gt;* with the name of the REST message record from your instance.

```
// Might throw exception if message doesn't exist or not visible due to scope.
var sm = new sn_ws.RESTMessageV2("<REST_message_record>", "get");
sm.setHttpTimeout(6000);
```

## RESTMessageV2 - setLogLevel\(String level\)

Sets the log level for this message and the corresponding response.

Setting a log level using the RESTMessageV2 API overrides the log level configured on the REST message record. This log level may not apply if the endpoint domain is excluded, or if the property **glide.outbound\_http\_log.override** is true. To view outbound web service logs, navigate to **System Logs** &gt; **Outbound HTTP Requests**.

|Name|Type|Description|
|----|----|-----------|
|level|String|The log level. Valid values are basic, elevated, and all.|

|Type|Description|
|----|-----------|
|void| |

```
var rm = new sn_ws.RESTMessageV2();
rm.setLogLevel('all');
```

## RESTMessageV2 - setMIDServer\(String midServer\)

Configures the REST message to communicate through a MID Server.

|Name|Type|Description|
|----|----|-----------|
|midServer|String|Name of the MID Server to use. Your instance must have an active MID Server with the specified name.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setMIDServer("mid_server_name");
```

## RESTMessageV2 - setMutualAuth\(String profileName\)

Sets the mutual authentication protocol profile for the REST message.

Setting a protocol profile using this method overrides the protocol profile selected for the REST message record.

|Name|Type|Description|
|----|----|-----------|
|profileName|String|The **Name** of the protocol profile to use for mutual authentication.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setMutualAuth("mutual_auth_profile_name");
```

## RESTMessageV2 - setQueryParameter\(String name, String value\)

Appends a parameter to the end of the request URL with the form name=value.

For example, the code setQueryParameter\("sysparm\_query","active=true^ORDERBYnumber^ORDERBYDESCcategory"\); appends the text sysparm\_query=active=true^ORDERBYnumber^ORDERBYDESCcategory to the request URL.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the URL parameter to pass.|
|value|String|Value to assign the URL parameter.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2();
//Set up message, including endpoint and authentication
sm.setQueryParameter("sysparm_query","active=true^ORDERBYnumber^ORDERBYDESCcategory");
```

## RESTMessageV2 - setRequestBody\(String body\)

Sets the body content to send to the web service provider when using PUT or POST HTTP methods.

When you set the body content using this method, variables in the body are not substituted for parameters from the REST message function record. You must explicitly define all values within the REST message body.

|Name|Type|Description|
|----|----|-----------|
|body|String|Request body to send.|

|Type|Description|
|----|-----------|
|void| |

```
var sm = new sn_ws.RESTMessageV2("Update user","post"); //Might throw exception if message doesn't exist or not visible due to scope.
var body = "<Message body content>";
sm.setRequestBody(body);
```

## RESTMessageV2 - setRequestBodyFromAttachment\(String attachmentSysId\)

Sets the request body using an existing attachment record.

When you use this function with a REST message that is sent through a MID Server, the MID Server user must have any roles required to read attachment records.

|Name|Type|Description|
|----|----|-----------|
|attachmentSysId|String|Sys\_id of the Attachment \[sys\_attachment\] record you want to send in this REST message.|

|Type|Description|
|----|-----------|
|void| |

```
(function sampleRESTMessageV2() {
    try {
        var request = new sn_ws.RESTMessageV2();
        request.setHttpMethod('post');
        request.setEndpoint('<web service endpoint URL>');
        request.setRequestBodyFromAttachment('<attachment sys_id>');
        
        var response = request.execute();
        var httpResponseStatus = response.getStatusCode();
      
        gs.info("http response status_code: " + httpResponseStatus);        
    }
    catch (ex) {
        var message = ex.getMessage();
        gs.info(message);
    }
})();
```

## RESTMessageV2 - setRequestHeader\(String name, String value\)

Sets an HTTP header in the REST message to the specified value.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the header.|
|value|String|Value to assign to the specified header.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setRequestHeader("Accept","Application/json");
```

## RESTMessageV2 - setRequestorProfile\(String requestorContext, String requestorId\)

Overrides the default requestor profile for the REST message in order to retrieve an OAuth access token associated with a different requestor.

This method applies only to REST messages configured to use OAuth 2.0 authentication. This method is optional and is unnecessary in most configurations.

|Name|Type|Description|
|----|----|-----------|
|requestorContext|String| |
|requestorId|String| |

|Type|Description|
|----|-----------|
|void| |

## RESTMessageV2 - setStringParameter\(String name, String value\)

Sets a REST message function variable with the specified name from the REST message record to the specified value.

XML reserved characters in the value are converted to the equivalent escaped characters. Use setStringParameterNoEscape to set a variable without escaping XML reserved characters.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the REST message variable. This parameter must be defined in the REST message record before you can assign a value to it.|
|value|String|Value to assign the variable.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setStringParameter("s","NOW");
```

## RESTMessageV2 - setStringParameterNoEscape\(String name, String value\)

Sets a REST message function variable with the specified name from the REST message record to the specified value.

This method is equivalent to setStringParameter but does not escape XML reserved characters.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the REST message variable. This parameter must be defined in the REST message record before you can assign a value to it.|
|value|String|Value to assign the variable.|

|Type|Description|
|----|-----------|
|void| |

In the following example, replace *REST\_message\_record* with the name of the REST message record from your instance.

```
var sm = new sn_ws.RESTMessageV2("<REST_message_record>","get"); //Might throw exception if message doesn't exist or not visible due to scope.
sm.setStringParameterNoEscape("s","NOW");
```

