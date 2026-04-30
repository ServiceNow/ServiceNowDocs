---
title: CTIOperationResponse - Scoped, Global
description: The CTIOperationResponse script include provides methods to set and get data on the current CTIOperationResponse object.Instantiates a CTIOperationResponse object.Returns the authentication token that was set on the CTIOperationResponse object.Returns the error object associated with the current CTIOperationResponse object.Returns the sys\_id of the interaction record associated with the call session that was set on the CTIOperationResponse object.Returns the major version of the computer telephony integrator \(CTI\) software set on the current CTIOperationResponse object.Returns the message string set on the current CTIOperationResponse object.Returns the minor version of the computer telephony integrator \(CTI\) software set on the current CTIOperationResponse object.Returns the value of a specified key previously set on the current CTIOperationResponse object.Returns the key-value pairs for all parameters that were previously set on the current CTIOperationResponse object.Returns the value for a specified session attribute key set on the current CTIOperationResponse object.Returns the key-value pairs for all session attributes that were previously set on the current CTIOperationResponse object.Returns the status code set on the current CTIOperationResponse object.Sets an authentication token on the current CTIOperationResponse object.Sets the error object in the current CTIOperationResponse object.Sets the sys\_id of the interaction record associated with the operation request on the current CTIOperationResponse object.Sets the major version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationResponse object.Sets a text message on the current CTIOperationResponse object.Sets the minor version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationResponse object.Sets the specified key-value pair on the associated CTIOperationResponse object.Sets the specified session attribute key-value pair on the associated CTIOperationResponse object.Sets the status code of the current operation request on the CTIOperationResponse object.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 22
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CTIOperationResponse - Scoped, Global

The CTIOperationResponse script include provides methods to set and get data on the current CTIOperationResponse object.

You use CTIOperationResponse objects to pass information between an operation handler and a message transformer within the ServiceNow Voice framework.

Typically, an operation handler is responsible for setting values on the CTIOperationResponse object as it processes the associated request. A message transformer is then responsible for getting the values from the CTIOperationRequest object and building the CTI-specific payload that is sent back to the computer telephony integrator \(CTI\) provider.

The ServiceNow base system provides working operation handlers and message transformers that enable connection to Amazon Connect. When building contact flows within Amazon Connect, there are two integration points between Amazon services and a ServiceNow instance:

-   Amazon Web Services \(AWS\) Lambda Proxy \(Invoke AWS Lambda function\)
-   AWS Lex Bot \(Get Customer Input\)

You can find the available operation handlers and message transformers for these integration points in the Operation Handlers \[sn\_cti\_operation\_handler\] and Provider Message Transformer \[sn\_cti\_provider\_msg\_transormer\] tables.

The following operation handler script shows how to use various CTIOperationResponse methods to set values on the CTIOperationResponse object.

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response) {

  try {
    var state = request.getParameter('$state');
    if(!state) {
      state = 'new';
    }
    var phone = request.getParameter('contact.phone');
    var username = request.getParameter('contact.username');
    var someDataPresent = phone || username;
    if(!someDataPresent) {
      throw 'phone or username must be supplied';
    }
    if('new' === state) {
      var userGr = null;
      if(phone || username) {
        userGr = new GlideRecordSecure('sys_user');
        var qc = null;
        if(phone) {
          qc = userGr.addQuery('phone', phone);
          qc.addOrCondition('mobile_phone', phone);
          qc.addOrCondition("home_phone", phone);
        }
        if(username) {
          if(qc) {
            qc.addOrCondition('user_name', username);
          } else {
            qc = userGr.addQuery('user_name', username);
          }
        }
        // If there was criteria then run the query
        if(qc) {
          userGr.query();
        } else {
          userGr = null;
        }
      }
			
      var foundUser = userGr && userGr.next();

      var phonelogGr = new GlideRecord('sn_openframe_phone_log');
      phonelogGr.initialize();
      phonelogGr.setValue('call_id', request.getParameter('contact.id'));
      phonelogGr.setValue('phone_number', phone);
      if(foundUser) {
        phonelogGr.setValue('contact', userGr.getUniqueValue());
      }
      phonelogGr.insert();
			
      var interactionGr = new GlideRecordSecure('interaction');
      interactionGr.initialize();
      interactionGr.setValue('type', 'phone');
      interactionGr.setValue('short_description', 'User Contact via Phone: ' + phone);
      interactionGr.setValue('channel_metadata_table', 'sn_openframe_phone_log');
      interactionGr.setValue('channel_metadata_document',phonelogGr.getUniqueValue());
			
      if(foundUser) {
        interactionGr.setValue('opened_for', userGr.getUniqueValue());
        response.setSessionAttribute('snc_user_first_name', userGr.getValue('first_name'));
        response.setSessionAttribute('snc_user_last_name', userGr.getValue('last_name'));
        response.setSessionAttribute('snc_user_sys_id', userGr.getUniqueValue());
      } else {
        response.setSessionAttribute('snc_user_sys_id', "USER_NOT_FOUND");
      }
      interactionGr.setValue('state', 'new');

      var interactionId = interactionGr.insert();

      response.setStatusCode(200);
      response.setMessage('success');
      response.setSessionAttribute('interactionTable', 'interaction');
      response.setSessionAttribute('interactionId', interactionId);

    }
  } catch(e) {
    ctx.setError(e);
  }

})(request, response);
```

For additional information on creating operation handlers, see [Configure a contact flow for an automated caller interaction](https://www.servicenow.com/docs/access?context=establish-automated-bot-interactions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The following message transformer script gets the values set on the CTIOperationResponse object and stores them in the CTI-specific payload that is then sent back to the CTI provider.

```
(function (/*CTIOperationResponse*/operationResponse, /*HTTPResponse*/ httpResponse) {
	// AWS Connect Lambda expects name value pairs only
	var out = {};
	for(var k in operationResponse.getSessionAttributes()) {
		out[k] = operationResponse.getSessionAttributes()[k];
	}
	out.statusCode = operationResponse.getStatusCode();
	out.message = operationResponse.getMessage();
	httpResponse.setBody(out);
})(operationResponse, httpResponse);
```

This script include runs in the `sn_cti_core` namespace. Before you are able to access the CTIOperationRequest script include, the ServiceNow Voice Core \(sn\_cti\_core\) plugin must be installed. For information on this installation, see [Install ServiceNow Voice applications](https://www.servicenow.com/docs/access?context=install-ccc-apps&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

For additional information on the ServiceNow Voice, see [ServiceNow Voice](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CTIOperationResponse - CTIOperationResponse\(String origin\)

Instantiates a CTIOperationResponse object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setMinorVersion(3);
```

## CTIOperationResponse - getAuthToken\(\)

Returns the authentication token that was set on the CTIOperationResponse object.

This token is used by the ServiceNow Voice framework to authenticate the current ServiceNow Voice user before executing the requested operation handler if the handler's **auth\_required** flag is set to true. The **auth\_required** flag is a field in the Operation Handler \[sn\_cti\_operation\_handler\] table. The life of an authentication token should be for the life of the call session, but is determined by the CTI provider.

You can define whatever authentication/authorization handling required by your implementation by creating your own authentication operation handler. Regardless of how the authentication token is generated, the message translator must pass the token back in the CTI payload. Additionally, the CTI provider must store this authentication token locally and pass it in each operation request that requires authentication.

If using the instance provided authenticate operation handler, the handler initiates the creation of the authentication token based on a four-digit user-entered pin. It then sets the authentication token in the sessionAttributes object of the CTIOperationResponse object. The associated message transformer translates the sessionAttributes object into the CTI-specific payload and then sends it to the CTI provider.

**Note:** If the authentication token is not passed, all requests to execute operation handlers with the **auth\_required** flag set will fail. If you do not use authentication, you do not need to maintain authentication tokens.

The ServiceNow base system provides working operation handlers and message transformers that enable connection to Amazon Connect. When building contact flows within Amazon Connect, there are two integration points between Amazon services and a ServiceNow instance:

-   Amazon Web Services \(AWS\) Lambda Proxy \(Invoke AWS Lambda function\)
-   AWS Lex Bot \(Get Customer Input\)

You can find the available operation handlers and message transformers for these integration points in the Operation Handlers \[sn\_cti\_operation\_handler\] and Provider Message Transformer \[sn\_cti\_provider\_msg\_transormer\] tables.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The authentication token previously set on the CTIOperationRequest object. If not set, returns null.|

```
var response = new sn_cti_core.CTIOperationResponse();
var token = response.getAuthToken();
```

## CTIOperationResponse - getError\(\)

Returns the error object associated with the current CTIOperationResponse object.

You might use this information to formulate the payload returned to the computer telephony integration \(CTI\) provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Operation error information. The format of this object is determined by the CTI provider. If an error does not exist, returns null.|

```
(function( /*CTIProviderResponseExecutionContext*/ ctx, /*CTIOperationRequest*/ operationRequest, /*CTIOperationResponse*/ operationResponse, /*HTTPResponse*/ httpResponse) {
    var sessionAttributes = {},
        intentResponse;
    var statusCode = -1;
    var message = 'Unprocessed';
    if (operationResponse) {
        statusCode = operationResponse.getStatusCode();
        sessionAttributes = operationResponse.getSessionAttributes();
        message = operationResponse.getMessage();
        var error = operationResponse.getError();
        if (error) {
            sessionAttributes.error = error;
        }
    }
    if (sn_cti_core.CTIRequestDispatcher.Constants.HTTP.Status.AUTH_REQUIRED.code === statusCode) {
        //first call for a secure action without authentication token
        sessionAttributes.statusCode = 401;
        sessionAttributes.message = message;
        intentResponse = {
            sessionAttributes: sessionAttributes,
            dialogAction: {
                type: 'Close',
                fulfillmentState: 'Fulfilled',
                message: {
                    contentType: 'PlainText',
                    content: 'This operation requires authentication. Say authenticate for authentication.'
                }
            }
        };
    } else if ('DialogCodeHook' === operationRequest.getParameter('$$invocationSource')) {
        //pass back authToken and interactionId
        sessionAttributes.authToken = operationRequest.getAuthToken();
        sessionAttributes.interactionId = operationRequest.getInteractionSysId();
		var originalSlots = operationRequest.getParameter('$$slots');
        var responseParameters = operationResponse ? operationResponse.getParameters() : {};
        responseParameters = responseParameters ? responseParameters : {};
        // See if we processing happened and we got a dialogAction
		var responseDialogAction = responseParameters['dialogAction'];
		// Default dialog action
        var dialogAction = {
            type: 'Delegate',
            slots: originalSlots
        };
		// If the response doesn't contain an override replay the inputs
        if (responseDialogAction) {
            // We bypassed dialoghook so delegate and pass through inputs
            dialogAction = responseDialogAction;
        }
        intentResponse = {
            sessionAttributes: sessionAttributes,
            dialogAction: dialogAction
        };
    } else {
        // Override required session attributes
        sessionAttributes.statusCode = statusCode;
        sessionAttributes.message = message;
        // Build response template
        intentResponse = {
            sessionAttributes: sessionAttributes,
            dialogAction: {
                type: 'Close',
                fulfillmentState: 'Fulfilled',
                message: {
                    contentType: 'PlainText',
                    content: message
                }
            }
        };
    }
    httpResponse.setBody(intentResponse);
})(ctx, operationRequest, operationResponse, httpResponse);
```

## CTIOperationResponse - getInteractionSysId\(\)

Returns the sys\_id of the interaction record associated with the call session that was set on the CTIOperationResponse object.

The [CTIOperationResponse - setInteractionSysId\(String Id\)](CTIOperationResponseAPI.md#) method must have been called prior to calling this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_djp_gpg_ykb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Sys\_id of the interaction record set on the CTIOperationResponse object.If the interaction record sys\_id is not set, the method returns null.

Table: Interaction \[interaction\]

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationResponse();
var interactionId = request.getInteractionSysId();

```

## CTIOperationResponse - getMajorVersion\(\)

Returns the major version of the computer telephony integrator \(CTI\) software set on the current CTIOperationResponse object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different payloads. If the payload is only slightly different between the software versions, it may make sense to have only a single message transformer. You can then handle the payload differences by just checking the version of software making the request within your message transformer. If the required payload is significantly different between versions, it may be more effective to use multiple message transformers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_plp_qvg_ykb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Major version number of the CTI software.If the major version was never set, returns `1`.

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationResponse();
var majorVersion = response.getMajorVersion();
```

## CTIOperationResponse - getMessage\(\)

Returns the message string set on the current CTIOperationResponse object.

Typically this is a message that is spoken back to the user once an operation is complete. You can set this value using the [CTIOperationResponse - setMessage\(String message\)](CTIOperationResponseAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Message text. If no message exists, returns null.|

```
(function (/*CTIOperationResponse*/operationResponse, /*HTTPResponse*/ httpResponse) {
  // AWS Connect Lambda expects name value pairs only
  var out = {};
  for(var k in operationResponse.getSessionAttributes()) {
    out[k] = operationResponse.getSessionAttributes()[k];
  }
  out.statusCode = operationResponse.getStatusCode();
  out.message = operationResponse.getMessage();
  httpResponse.setBody(out);
})(operationResponse, httpResponse);
```

## CTIOperationResponse - getMinorVersion\(\)

Returns the minor version of the computer telephony integrator \(CTI\) software set on the current CTIOperationResponse object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different payloads. If the payload is only slightly different between the software versions, it may make sense to have only a single message transformer. You can then handle the payload differences by just checking the version of software making the request within your message transformer. If the required payload is significantly different between versions, it may be more effective to use multiple message transformers.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_dhp_z41_zkb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Minor version number of the payload associated with this interaction.If the minor version was never set, returns `0`.

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationResponse();
var minorVersion = request.getMinorVersion();
```

## CTIOperationResponse - getParameter\(String key\)

Returns the value of a specified key previously set on the current CTIOperationResponse object.

Using the get/set parameter methods enables the passing of virtually any string or number value between an operation handler and a message transformer. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation response. The operation handler determines what key/value pairs are required as it produces these values. Use the [CTIOperationResponse - setParameter\(String key, Object value\)](CTIOperationResponseAPI.md#) method to set parameters on the current CTIOperationResponse object.

|Name|Type|Description|
|----|----|-----------|
|key|String|The name of the key value to return.|

|Type|Description|
|----|-----------|
|String|The value of the passed in key. If no such key exists, returns null.|

```
var request = new sn_cti_core.CTIOperationResponse();
var parm = request.getParameter('contact.phone');
```

## CTIOperationResponse - getParameters\(\)

Returns the key-value pairs for all parameters that were previously set on the current CTIOperationResponse object.

Using the get/set parameter methods enables the passing of virtually any string or number value between an operation handler and a message transformer. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation response. The operation handler determines what key/value pairs are required as it produces these values. Use the [CTIOperationResponse - setParameter\(String key, Object value\)](CTIOperationResponseAPI.md#) method to set parameters on the current CTIOperationResponse object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A map of key-value pairs that were previously set on the CTIOperationResponse object. This key-value pairs are free-form and defined by the needs of the operation handler. The returned values are either Strings or Numbers.|

```
(function( /*CTIProviderResponseExecutionContext*/ ctx, /*CTIOperationRequest*/ operationRequest, /*CTIOperationResponse*/ operationResponse, /*HTTPResponse*/ httpResponse) {
  var sessionAttributes = {},
      intentResponse;
  var statusCode = -1;
  var message = 'Unprocessed';
  if (operationResponse) {
    statusCode = operationResponse.getStatusCode();
    sessionAttributes = operationResponse.getSessionAttributes();
    message = operationResponse.getMessage();
    var error = operationResponse.getError();
    if (error) {
      sessionAttributes.error = error;
    }
  }
  if (sn_cti_core.CTIRequestDispatcher.Constants.HTTP.Status.AUTH_REQUIRED.code === statusCode) {
    //first call for a secure action without authentication token
    sessionAttributes.statusCode = 401;
    sessionAttributes.message = message;
    intentResponse = {
      sessionAttributes: sessionAttributes,
      dialogAction: {
        type: 'Close',
        fulfillmentState: 'Fulfilled',
        message: {
          contentType: 'PlainText',
          content: 'This operation requires authentication. Say authenticate for authentication.'
        }
      }
    };
  } else if ('DialogCodeHook' === operationRequest.getParameter('$$invocationSource')) {
      //pass back authToken and interactionId
      sessionAttributes.authToken = operationRequest.getAuthToken();
      sessionAttributes.interactionId = operationRequest.getInteractionSysId();
      var originalSlots = operationRequest.getParameter('$$slots');
      var responseParameters = operationResponse ? operationResponse.getParameters() : {};
      responseParameters = responseParameters ? responseParameters : {};
      // See if processing happened and we got a dialogAction
      var responseDialogAction = responseParameters['dialogAction'];
      // Default dialog action
      var dialogAction = {
        type: 'Delegate',
        slots: originalSlots
      };
      // If the response doesn't contain an override replay the inputs
      if (responseDialogAction) {
        // We bypassed dialoghook so delegate and pass through inputs
        dialogAction = responseDialogAction;
      }
        intentResponse = {
            sessionAttributes: sessionAttributes,
            dialogAction: dialogAction
        };
    } else {
      // Override required session attributes
      sessionAttributes.statusCode = statusCode;
      sessionAttributes.message = message;
      // Build response template
      intentResponse = {
        sessionAttributes: sessionAttributes,
        dialogAction: {
          type: 'Close',
          fulfillmentState: 'Fulfilled',
          message: {
            contentType: 'PlainText',
            content: message
          }
        }
      };
  }
  httpResponse.setBody(intentResponse);
})(ctx, operationRequest, operationResponse, httpResponse);
```

## CTIOperationResponse - getSessionAttribute\(String key\)

Returns the value for a specified session attribute key set on the current CTIOperationResponse object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between an operation handler and a message transformer. Session attributes can also be accessed within a contact flow. The sessionAttribute object can contain zero or more key/value pairs of data, such as the contact's phone number, that are valid for the duration of a computer telephony integration provider defined session. The operation handler determines what session attribute key/value pairs are needed as it utilizes these values during processing. Typically the operation handler sets these attributes on the CTIOperationResponse object by calling the [CTIOperationResponse - setSessionAttribute\(String key, Object value\)](CTIOperationResponseAPI.md#) method and the message transformer consumes the attributes using this method.

|Name|Type|Description|
|----|----|-----------|
|key|String|The name of the key value to return.|

|Type|Description|
|----|-----------|
|String|Value of the passed in key. If no such key exists, returns null.|

```
var response = new sn_cti_core.CTIOperationResponse();
var phoneAttribute = response.getSessionAttribute('contact.phone');
```

## CTIOperationResponse - getSessionAttributes\(\)

Returns the key-value pairs for all session attributes that were previously set on the current CTIOperationResponse object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between an operation handler and a message transformer. Session attributes can also be accessed within a contact flow. The sessionAttribute object can contain zero or more key/value pairs of data, such as the contact's phone number, that are valid for the duration of a computer telephony integration provider defined session. The operation handler determines what session attribute key/value pairs are needed as it utilizes these values during processing. Typically the operation handler sets these attributes on the CTIOperationResponse object by calling the [CTIOperationResponse - setSessionAttribute\(String key, Object value\)](CTIOperationResponseAPI.md#) method and the message transformer consumes the attributes using this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A map of key-value pairs that were previously set on the CTIOperationResponse object. This key-value pairs are free-form and defined by the needs of the operation handler. The returned values are either Strings or Numbers.|

```
(function (/*CTIOperationResponse*/operationResponse, /*HTTPResponse*/ httpResponse) {
  // AWS Connect Lambda expects name value pairs only
  var out = {};
  for(var k in operationResponse.getSessionAttributes()) {
    out[k] = operationResponse.getSessionAttributes()[k];
  }
  out.statusCode = operationResponse.getStatusCode();
  out.message = operationResponse.getMessage();
  httpResponse.setBody(out);
})(operationResponse, httpResponse);
```

## CTIOperationResponse - getStatusCode\(\)

Returns the status code set on the current CTIOperationResponse object.

These status codes should correspond with standard HTTP status codes, such as 200 for success, 401 for authorization required. Typically, the resultant status codes are determined by the operation handler and are set on the CTIOperationResponse object using the [CTIOperationResponse - setStatusCode\(String statusCode\)](CTIOperationResponseAPI.md#) method. The message transformer then uses this method to include the status code in the payload returned to the computer telephony integrator provider.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Number|Status code of the current operation. If a status code has not been set, returns -1.|

```
(function (/*CTIOperationResponse*/operationResponse, /*HTTPResponse*/ httpResponse) {
  // AWS Connect Lambda expects name value pairs only
  var out = {};
  for(var k in operationResponse.getSessionAttributes()) {
    out[k] = operationResponse.getSessionAttributes()[k];
  }
  out.statusCode = operationResponse.getStatusCode();
  out.message = operationResponse.getMessage();
  httpResponse.setBody(out);
})(operationResponse, httpResponse);
```

## CTIOperationResponse - setAuthToken\(String token\)

Sets an authentication token on the current CTIOperationResponse object.

This token is used by the ServiceNow Voice framework to authenticate the current ServiceNow Voice user before executing the requested operation handler if the handler's **auth\_required** flag is set to true. The **auth\_required** flag is a field in the Operation Handler \[sn\_cti\_operation\_handler\] table. The life of an authentication token should be for the life of the call session, but is determined by the CTI provider.

You can define whatever authentication/authorization handling required by your implementation by creating your own authentication operation handler. Regardless of how the authentication token is generated, the message translator must pass the token back in the CTI payload. Additionally, the CTI provider must store this authentication token locally and pass it in each operation request that requires authentication.

If using the instance provided authenticate operation handler, the handler initiates the creation of the authentication token based on a four-digit user-entered pin. It then sets the authentication token in the sessionAttributes object of the CTIOperationResponse object. The associated message transformer translates the sessionAttributes object into the CTI-specific payload and then sends it to the CTI provider.

**Note:** If the authentication token is not passed, all requests to execute operation handlers with the **auth\_required** flag set will fail. If you do not use authentication, you do not need to maintain authentication tokens.

The ServiceNow base system provides working operation handlers and message transformers that enable connection to Amazon Connect. When building contact flows within Amazon Connect, there are two integration points between Amazon services and a ServiceNow instance:

-   Amazon Web Services \(AWS\) Lambda Proxy \(Invoke AWS Lambda function\)
-   AWS Lex Bot \(Get Customer Input\)

You can find the available operation handlers and message transformers for these integration points in the Operation Handlers \[sn\_cti\_operation\_handler\] and Provider Message Transformer \[sn\_cti\_provider\_msg\_transormer\] tables.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The authentication token to use to authenticate operations that have the **auth\_required** flag set.|

```
var response = new sn_cti_core.CTIOperationResponse();
var authenticate = <Your authentication code here>; // Authenticate the user
if (authenticated) {
	var claims = {
		"interactionId":interactionGr.sys_id.toString()
	};
	var jwt = new sn_cti_core.AuthHelpers().generateJWT(claims);
	response.setAuthToken(jwt);
}
```

## CTIOperationResponse - setError\(Object error\)

Sets the error object in the current CTIOperationResponse object.

You can use the error object in the component to formulate the payload to send to the computer telephony integrator \(CTI\) provider.

|Name|Type|Description|
|----|----|-----------|
|error|Object|Information about the error that was detected while processing the requested operation. The format of this object is determined by the CTI provider.|

|Type|Description|
|----|-----------|
|void| |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setError(new Error("You did not supply a field"));
```

## CTIOperationResponse - setInteractionSysId\(String Id\)

Sets the sys\_id of the interaction record associated with the operation request on the current CTIOperationResponse object.

|Name|Type|Description|
|----|----|-----------|
|sys\_id|String|The sys\_id to set for the current interaction.|

|Type|Description|
|----|-----------|
|void| |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setInteractionSysId('98529cc55380001048e5ddeeff7b120b');

```

## CTIOperationResponse - setMajorVersion\(Number majorVersion\)

Sets the major version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationResponse object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different payloads. If the payload is only slightly different between the software versions, it may make sense to have only a single message transformer. You can then handle the payload differences by just checking the version of software making the request within your message transformer. If the required payload is significantly different between versions, it may be more effective to use multiple message transformers.

<table id="table_jlt_pz1_zkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

majorVersion

</td><td>

Number

</td><td>

Major version of the CTI provider software making the operation request.If this value was not previously set, returns `1`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var request = new sn_cti_core.CTIOperationResponse();
request.setMajorVersion(2);
```

## CTIOperationResponse - setMessage\(String message\)

Sets a text message on the current CTIOperationResponse object.

Typically this is a message that is spoken back to the user once an operation is complete and is set by the associated operation handler. The message transformer then uses the [CTIOperationResponse - getMessage\(\)](CTIOperationResponseAPI.md#) method to obtain the message and pass it back to the computer telephony integration provider.

|Name|Type|Description|
|----|----|-----------|
|message|String|Message text|

|Type|Description|
|----|-----------|
|void| |

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, /*Context*/ ctx) {	
  var notes = '', lang = request.getLanguage();
  try { 
		
    var interactionGr = request.getInteractionRecord();

    var now_GR = new GlideRecord('sys_user');
    if(interactionGr && now_GR.get(interactionGr.opened_for.toString())) {	
    if(now_GR.locked_out == true) {
        notes += gs.getMessageLang("User record found locked. Unlocking the account.\n", lang);
        now_GR.locked_out=false;
        now_GR.update();
        response.setStatusCode(200);
        response.setMessage(gs.getMessageLang("Your account has been unlocked.", lang));
      } else {
        notes += gs.getMessageLang("User record not locked.\n", lang);
        response.setStatusCode(200);
        response.setMessage(gs.getMessageLang("Your account doesn't seem to be locked.", lang));
      }	
    } else {
      notes += gs.getMessageLang("User record not found. Transfer to agent\n", lang);
      response.setStatusCode(302);
      response.setMessage(gs.getMessageLang("I am unable to find your record. Let me transfer to someone who can help.", lang));
    }
    if(interactionGr) {
      interactionGr.work_notes = notes;
      interactionGr.update();
    }
  } catch(e) {
    ctx.setError(e);
  }
})(request, response, ctx);
```

## CTIOperationResponse - setMinorVersion\(Number minorVersion\)

Sets the minor version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationResponse object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different payloads. If the payload is only slightly different between the software versions, it may make sense to have only a single message transformer. You can then handle the payload differences by just checking the version of software making the request within your message transformer. If the required payload is significantly different between versions, it may be more effective to use multiple message transformers.

<table id="table_zqj_52b_zkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

minorVersion

</td><td>

Number

</td><td>

Minor version of the CTI provider software making the operation request.If this value was not previously set, returns `0`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setMinorVersion(3);
```

## CTIOperationResponse - setParameter\(String key, Object value\)

Sets the specified key-value pair on the associated CTIOperationResponse object.

Using the get/set parameter methods enables the passing of virtually any string or number value between an operation handler and a message transformer. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation request. The operation handler determines what key/value pairs are required as it consumes these values. Typically the operation handler sets these parameters on the CTIOperationResponse object by calling this method and the message transformer consumes them using the [CTIOperationResponse - getParmeter\(String key\)](CTIOperationResponseAPI.md#) or [CTIOperationResponse - getSParameters\(\)](CTIOperationResponseAPI.md#) method.

**Note:** You should only store objects that can survive a `JSON.parse(JSON.stringify(object))` operation. Objects not meeting this criteria may not propagate correctly through the entire operation processing chain.

For example:

```
var x = {
  "string": 'abc',
  "int": 123,
  "float": 1.234,
  "number": new Number(3),
  "boolean": true,
  "date": new Date(2006, 0, 2, 15, 4, 5),
  "object": {
    "string": 'abc',
    "int": 123,
    "float": 1.234,
    "number": new Number(3),
    "boolean": true,
    "date": new Date(2006, 0, 2, 15, 4, 5)
  },
  "function": function(abc) {

  }
}
var stringify = JSON.stringify(x);
gs.info(stringify);
var hydrate = JSON.parse(stringify);
var stringify2 = JSON.stringify(hydrate);
gs.info(stringify2);

```

Produces:

```
{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z","object":{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z"}}
{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z","object":{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z"}}

```

<table id="table_ab4_k3r_zkb" class="parameters"><thead><tr><th>

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

Name of the key under which to store the associated value.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to store for the key.Valid data types:

-   string
-   int
-   float
-   number
-   boolean
-   date
-   object

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setParameter('contact.phone', '+15552222345');
response.setParameter('contact.okToCall', true);
response.setParameter('contact.address', {
    street: '1234 Main St'
    city: 'API City',
    zip: 91335
});
```

## CTIOperationResponse - setSessionAttribute\(String key, Object value\)

Sets the specified session attribute key-value pair on the associated CTIOperationResponse object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between an operation handler and a message transformer. The sessionAttribute object can contain zero or more key/value pairs of data that are valid for the duration of a computer telephony integration provider defined session. Session attributes can also be accessed within a contact flow. The operation handler determines what session attribute key/value pairs are needed as it consumes these values. Typically the operation handler sets these attributes on the CTIOperationResponse object by calling this method and the message transformer gets the attributes using the [CTIOperationResponse - getSessionAttribute\(String key\)](CTIOperationResponseAPI.md#) or [CTIOperationResponse - getSessionAttribute\(\)](CTIOperationResponseAPI.md#) method.

**Note:** You should only store objects that can survive a `JSON.parse(JSON.stringify(object))` operation. Objects not meeting this criteria may not propagate correctly through the entire operation processing chain.

For example:

```
var x = {
  "string": 'abc',
  "int": 123,
  "float": 1.234,
  "number": new Number(3),
  "boolean": true,
  "date": new Date(2006, 0, 2, 15, 4, 5),
  "object": {
    "string": 'abc',
    "int": 123,
    "float": 1.234,
    "number": new Number(3),
    "boolean": true,
    "date": new Date(2006, 0, 2, 15, 4, 5)
  },
  "function": function(abc) {

  }
}
var stringify = JSON.stringify(x);
gs.info(stringify);
var hydrate = JSON.parse(stringify);
var stringify2 = JSON.stringify(hydrate);
gs.info(stringify2);

```

Produces:

```
{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z","object":{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z"}}
{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z","object":{"string":"abc","int":123,"float":1.234,"number":3,"boolean":true,"date":"2006-01-02T23:04:05.000Z"}}

```

<table id="table_ihm_rxr_zkb" class="parameters"><thead><tr><th>

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

Name of the session attribute key under which to set the associated value.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set.Valid data types:

-   string
-   int
-   float
-   number
-   boolean
-   date
-   object

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var response = new sn_cti_core.CTIOperationResponse();
response.setSessionAttribute('contact.phone', '+15552222345');
response.setSessionAttribute('contact.okToCall', true);
response.setSessionAttribute('contact.address', {
    street: '1234 Main St'
    city: 'API City',
    zip: 91335
});
```

## CTIOperationResponse - setStatusCode\(Number statusCode\)

Sets the status code of the current operation request on the CTIOperationResponse object.

You can use any integer values to define the status, but it is recommended that you emulate the HTTP status codes, such as 200 = Ok/Success, 400 = Bad Request, 401 = Unauthorized.

|Name|Type|Description|
|----|----|-----------|
|statusCode|Number|Integer that uniquely identifies the status of the requested operation.|

|Type|Description|
|----|-----------|
|void| |

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, /*Context*/ ctx) {	
  var notes = '', lang = request.getLanguage();
  try { 
		
    var interactionGr = request.getInteractionRecord();

    var now_GR = new GlideRecord('sys_user');
    if(interactionGr && now_GR.get(interactionGr.opened_for.toString())) {	
    if(now_GR.locked_out == true) {
        notes += gs.getMessageLang("User record found locked. Unlocking the account.\n", lang);
        now_GR.locked_out=false;
        now_GR.update();
        response.setStatusCode(200);
        response.setMessage(gs.getMessageLang("Your account has been unlocked.", lang));
      } else {
        notes += gs.getMessageLang("User record not locked.\n", lang);
        response.setStatusCode(200);
        response.setMessage(gs.getMessageLang("Your account doesn't seem to be locked.", lang));
      }	
    } else {
      notes += gs.getMessageLang("User record not found. Transfer to agent\n", lang);
      response.setStatusCode(302);
      response.setMessage(gs.getMessageLang("I am unable to find your record. Let me transfer to someone who can help.", lang));
    }
    if(interactionGr) {
      interactionGr.work_notes = notes;
      interactionGr.update();
    }
  } catch(e) {
    ctx.setError(e);
  }
})(request, response, ctx);
```

