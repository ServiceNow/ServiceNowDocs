---
title: CTIOperationRequest - Scoped, Global
description: The CTIOperationRequest script include provides methods to set and get data on the current CTIOperationRequest object.Instantiates a CTIOperationRequest object.Returns the authentication token set on the associated CTIOperationRequest object.Returns the interaction GlideRecord associated with the operation request.Returns the sys\_id of the interaction record associated with the current CTIOperationRequest object.Returns the ISO 639.1 language code that was set on the current CTIOperationRequest object.Returns the major version of the computer telephony integrator \(CTI\) software set on the current CTIOperationRequest object.Returns the minor version of the computer telephony integrator \(CTI\) software associated with a CTIOperationRequest object.Returns the name of the operation that the computer telephony integration \(CTI\) provider is requesting to execute.Returns the substep operation handler name set on the current CTIOperationRequest object.Returns the value of a specified key previously set on the current CTIOperationRequest object.Returns the key-value pairs for all parameters that were previously set on the current CTIOperationRequest object.Returns the value of a specified session attribute key set on the current CTIOperationRequest object.Returns a key-value pair map of all session attributes set on the current CTIOperationRequest object.Returns the handling behavior for a subsep when a substep's operation handler is not found.Sets an authentication token on the current CTIOperationRequest object.Sets the sys\_id of the interaction record associated with the operation request on the current CTIOperationRequest object.Sets the ISO 639.1 language code to use when processing the associated operation on a CTIOperationRequest object.Sets the major version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationRequest object.Sets the minor version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationRequest object.Sets the name of the operation that the computer telephony integration \(CTI\) provider is attempting to execute on the current CTIOperationRequest object.Sets the operation substep name on the current CTIOperationRequest object.Sets the specified key-value pair on the parameter object of the current CTIOperationRequest object.Sets the specified session attribute key-value pair on the current CTIOperationRequest object.Sets the behavior to perform if the current substep's operation handler is not found.
locale: en-US
release: yokohama
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 38
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CTIOperationRequest - Scoped, Global

The CTIOperationRequest script include provides methods to set and get data on the current CTIOperationRequest object.

You use CTIOperationRequest objects to pass information between a message transformer and an operation handler within the ServiceNow Voice framework.

Typically, a message transformer is responsible for parsing an incoming CTI-specific payload and setting the payload data on an associated CTIOperationRequest object. An operation handler is then responsible for getting the information from the CTIOperationRequest object and using the data to process the requested operation.

The ServiceNow base system provides working operation handlers and message transformers that enable connection to Amazon Connect. When building contact flows within Amazon Connect, there are two integration points between Amazon services and a ServiceNow instance:

-   Amazon Web Services \(AWS\) Lambda Proxy \(Invoke AWS Lambda function\)
-   AWS Lex Bot \(Get Customer Input\)

You can find the available operation handlers and message transformers for these integration points in the Operation Handlers \[sn\_cti\_operation\_handler\] and Provider Message Transformer \[sn\_cti\_provider\_msg\_transormer\] tables.

A payload is passed into a ServiceNow instance from an external source, such as from a computer telephony integration \(CTI\) provider that is making an operation request. When a request is received, a message transformer parses the payload and uses the CTIOperationRequest set methods to set payload values, such as the operation handler name, onto an operation and contact-specific CTIOperationRequest object.

For example, the following message transformer script parses the passed in JSON payload and sets the values required by the associated operation handler on the CTIOperationRequest object.

```
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {					
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

After the message transformer finishes parsing the passed in payload, the ServiceNow Voice framework instantiates the specified operation handler. The operating handler uses the CTIOperationResponse script include get methods to obtain the information that it needs from the associated CTIOperationRequest object to process the requested operation.

For example, the following operation handler script stores values that were set on the CTIOperationRequest object in the interaction record associated with the call.

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, ctx) {
  // Returns the sys_id of the interaction record.
  var interactionSysId = request.getInteractionSysId();
  var number = request.getParameter('number');
  var addComment = request.getParameter('add_comment');
  addComment = addComment ? addComment.toLowerCase() : addComment;
  addComment = 'yes' === addComment || 'true' === addComment || '1' === addComment;
  var workNotes = request.getParameter('work_notes');
  var message = gs.getMessage('Thankyou');
  var interactionGr = request.getInteractionRecord();
  var openedFor = interactionGr ? interactionGr.getValue('opened_for') : null;
  if (openedFor && number && addComment && workNotes) {
    var now_GR = new GlideRecordSecure('incident');
    now_GR.addQuery('caller_id', openedFor);
    now_GR.addQuery('number', number);
    now_GR.query();
    if (now_GR.next()) {
      now_GR.work_notes += workNotes;
      now_GR.update();
      message = now_GR.getMessage('Your comment was added');
    }
  }
  response.setStatusCode(200);
  response.setMessage(message);
})(request, response, ctx);
```

For additional information on creating operation handlers, see [Configure a contact flow for an automated caller interaction](https://www.servicenow.com/docs/access?context=establish-automated-bot-interactions&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

This script include runs in the `sn_cti_core` namespace. Before you are able to access the CTIOperationRequest script include, the ServiceNow Voice \(sn\_cti\_core\) plugin must be activated. For information on activating ServiceNow Voice, see [Install ServiceNow Voice applications](https://www.servicenow.com/docs/access?context=install-ccc-apps&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

For additional information on the ServiceNow Voice, see [ServiceNow Voice](https://www.servicenow.com/docs/access?context=cloud-call-center-overview&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CTIOperationRequest - CTIOperationRequest\(String origin\)

Instantiates a CTIOperationRequest object.

<table id="table_mvz_lgy_glb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

origin

</td><td>

String

</td><td>

Optional. Origin of the request. Usually the name of the computer telephony integrator provider. Default: null

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationRequest('AWS Connect');
request.setSessionAttribute('contact.phone', '+15552222345');
request.setSessionAttribute('contact.okToCall', true);
request.setSessionAttribute('contact.address', {
    street: '1234 Main St'
    city: 'API City',
    zip: 91335
});
```

## CTIOperationRequest - getAuthToken\(\)

Returns the authentication token set on the associated CTIOperationRequest object.

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
|String|The authentication token associated with the current ServiceNow Voice user.|

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

## CTIOperationRequest - getInteractionRecord\(\)

Returns the interaction GlideRecord associated with the operation request.

An interaction represents a customer request for assistance made through a chat, phone call, or in-person. Interactions can be routed to queues for assignment or assigned to agents directly. Interaction records are stored in the Interaction \[interaction\] table and can contain any type of data that describes service account interactions with a customer for a specific session.

Interaction records are associated with a CTIOperationRequest object through the [CTIOperationRequest - setInteractionSysId\(String Id\)](CTIOperationRequestAPI.md#) method. This method is typically called by the message transformer and must be called prior to calling the getInteractionRecord\(\) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|Interaction GlideRecord object associated with the current CTIOperationRequest object. If the interaction record sys\_id has not been set on the CTIOperationRequest object, returns null.|

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, /*Context*/ ctx) {	
  var notes = '', lang = request.getLanguage();
  try { 
    // Returns the interaction record (GlideRecord) set on the passed in CTIOperationRequest object		
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

## CTIOperationRequest - getInteractionSysId\(\)

Returns the sys\_id of the interaction record associated with the current CTIOperationRequest object.

The [CTIOperationRequest - setInteractionSysId\(String Id\)](CTIOperationRequestAPI.md#) method must have been called prior to calling this method.

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

The sys\_id of the interaction record set on the current CTIOperationRequest object.If the sys\_id was not set on the associated CTIOperationRequest object, the method returns null.

</td></tr></tbody>
</table>```
(function( /*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, ctx) {
  // Returns the sys_id of the interaction record associated with the CTIOperationRequest object.
  var interactionSysId = request.getInteractionSysId();
  var number = request.getParameter('number');
  var addComment = request.getParameter('add_comment');
  addComment = addComment ? addComment.toLowerCase() : addComment;
  addComment = 'yes' === addComment || 'true' === addComment || '1' === addComment;
  var workNotes = request.getParameter('work_notes');
  var message = gs.getMessage('Thankyou');
  var interactionGr = request.getInteractionRecord();
  var openedFor = interactionGr ? interactionGr.getValue('opened_for') : null;
  if (openedFor && number && addComment && workNotes) {
    var now_GR = new GlideRecordSecure('incident');
    now_GR.addQuery('caller_id', openedFor);
    now_GR.addQuery('number', number);
    now_GR.query();
    if (now_GR.next()) {
    now_GR.work_notes += workNotes;
    now_GR.update();
      message = gs.getMessage('Your comment was added');
    }
  }
  response.setStatusCode(200);
  response.setMessage(message);
})(request, response, ctx);
```

## CTIOperationRequest - getLanguage\(\)

Returns the ISO 639.1 language code that was set on the current CTIOperationRequest object.

Using the customer preferred language enables you to use platform-provided internationalization and localization capabilities to customize messages and other communications with the associated caller.

Typically an operation handler calls the getLanguage\(\) method and the message transformer sets the language on the CTIOperationRequest object by calling the [CTIOperationRequest - setLanguage\(String languageCode\)](CTIOperationRequestAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The ISO 639.1 language code set on the current CTIOperationRequest object. If the language code is not set, returns `en`.|

The following example shows an operation handler calling getLanguage\(\) to obtain the caller's preferred language.

```
(function(/*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response) {
  // Obtain the contact's preferred language
  var notes = "", announcement, lang = request.getLanguage();
  try {
		
    var interactionGr = request.getInteractionRecord();
		
    announcement = gs.getMessageLang("We are currently experiencing issues with VPN. If you are calling about VPN issues, you may hang up the call.", lang);
    // Use the contact's language to customize the response messages and notes	
    if(announcement) {	
      notes = gs.getMessageLang("Listened to announcement: {0}", lang, [announcement]);
      response.setStatusCode(200);
    } else {
      announcement = gs.getMessageLang("There are currently no known outage announcements", lang);
      //use the status case as the flag to check for announcements in contact flow
      response.setStatusCode(404);
    }			
    response.setMessage(announcement);	
			
    if(interactionGr && notes) {			
      interactionGr.work_notes = notes;		
      interactionGr.update();
    }
		
  } catch(e) {
    ctx.setError(e);
  }

})(request, response);
```

## CTIOperationRequest - getMajorVersion\(\)

Returns the major version of the computer telephony integrator \(CTI\) software set on the current CTIOperationRequest object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different processing behavior. If the processing behavior is only slightly different between the software versions, it may make sense to have only a single operation handler. You can then handle the processing differences by just checking the version of software making the request and process the request/data within your operation handler. If the required processing is significantly different between versions, it may be more effective to use multiple operation handlers.

Typically the message transformer sets the software version on the CTIOperationRequest object by calling the [CTIOperationRequest - setMajorVersion\(Number majorVersion\)](CTIOperationRequestAPI.md#) method and an operation handler then consumes the set value using this method. You can also get/set the minor version value of a provider's software using the [CTIOperationRequest - getMinorVersion\(\)](CTIOperationRequestAPI.md#) and [CTIOperationRequest - setMinorVersion\(Number minorVersion\)](CTIOperationRequestAPI.md#) methods.

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
var request = new sn_cti_core.CTIOperationRequest('origin');
var majorVersion = request.getMajorVersion();
```

## CTIOperationRequest - getMinorVersion\(\)

Returns the minor version of the computer telephony integrator \(CTI\) software associated with a CTIOperationRequest object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different processing behavior. If the processing behavior is only slightly different between the software versions, it may make sense to have only a single operation handler. You can then handle the processing differences by just checking the version of software making the request and process the request/data within your operation handler. If the required processing is significantly different between versions, it may be more effective to use multiple operation handlers.

Typically the message transformer sets the software version on the CTIOperationRequest object by calling the [CTIOperationRequest - setMinorVersion\(Number minorVersion\)](CTIOperationRequestAPI.md#) [CTIOperationRequest - setMinorVersion\(Number minorVersion\)](CTIOperationRequestAPI.md#) method and an operation handler then consumes the set value using this method. You can also get/set the major version value of a provider's software using the [CTIOperationRequest - getMajorVersion\(\)](CTIOperationRequestAPI.md#) [CTIOperationRequest - getMajorVersion\(\)](CTIOperationRequestAPI.md#) and [CTIOperationRequest - setMajorVersion\(Number majorVersion\)](CTIOperationRequestAPI.md#) [CTIOperationRequest - setMajorVersion\(Number majorVersion\)](CTIOperationRequestAPI.md#) methods.

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

Minor version number of the CTI software. If the minor version was never set, returns `0`.

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationRequest('origin');
var minorVersion = request.getMinorVersion();
```

## CTIOperationRequest - getOperationName\(\)

Returns the name of the operation that the computer telephony integration \(CTI\) provider is requesting to execute.

The operation name determines the operation handler that is used to process a request. Typically the message transformer sets the operation name on the CTIOperationRequest object using the [CTIOperationRequest - setOperationName\(String name\)](CTIOperationRequestAPI.md#) method.

**Note:** The getOperationName\(\) method does not instantiate the associated operation handler. This is done by the ServiceNow Voiceframework. This method simply returns the associated operation handler name.

**Note:** For Amazon Connect Lex Bot implementations, intent names are appended with a five letter suffix as different Amazon intents cannot have the same intent name. In the ServiceNow Voice framework, the intent name equals the operation handler name. An operation handler can either be specific for an intent, having an operation handler name that includes this suffix \(myOperation\_SUFFX\), or it can be generic and used by multiple CTI providers or different use cases, such as using the same handler for processing an HR request and a helpdesk request \(myOperation\).

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the operation that the CTI provider is requesting to execute. If the operation name is not set, returns null.|

```
var request = new sn_cti_core.CTIOperationRequest('origin');
var name = request.getOperationName();

```

## CTIOperationRequest - getOperationSubStepName\(\)

Returns the substep operation handler name set on the current CTIOperationRequest object.

Use substeps to perform actions such as initialization and validation before processing an operation. Unlike operation handlers that are meant to be generic and used by all CTI providers, substeps are CTI provider specific and use terminology and naming conventions that are specific to the CTI provider.

The ServiceNow Voice framework performs the following steps to locate the required operation handler and any associated substep operation handlers.

**Note:** For Amazon Connect Lex Bot implementations, intent names are appended with a five letter suffix as different Amazon intents cannot have the same intent name. In the ServiceNow Voice framework, the intent name equals the operation handler name. An operation handler can either be specific for an intent, having an operation handler name that includes this suffix \(myOperation\_SUFFX\), or it can be generic and used by multiple CTI providers or different use cases, such as using the same handler for processing an HR request and a helpdesk request \(myOperation\).

1.  Tries to locate the operation handler associated with the request.
    -   First checks for an operation handler called `myOperation_SUFFX`.
    -   If not found, checks for the operation handler `myOperation`. If not found, errors out.
2.  If the handler is found, checks the **auth\_required** flag on the operation handler. If set, it checks that a valid authentication token \(obtained through the getAuthToken\(\) method\) is present on the request. If present and valid, continue processing, else throw an error.
3.  Looks up the operation handler for the passed in substep. For this example let's assume `subStepName=SubStep`.
    -   First checks for an operation handler named `myOperation_SUFFX.SubStep`. If found, executes the handler.
    -   If not found, checks for the handler `myOperation.SubStep`. If found executes the handler.
    -   If not found, checks if a `subStepNotFoundBehavior` was set on the request object.
    -   If set, executes the behavior, otherwise, errors out.
4.  Executes the primary operation handler \(`myOpersation_SUFFX` or `myOperation`.\)

Typically the message transformer sets the substep name on the CTIOperationRequest object using the [CTIOperationRequest - setOperationSubStepName\(String name\)](CTIOperationRequestAPI.md#) method. You can override this behavior if you are creating your own transformer by calling the [CTIOperationRequest - setSubStepNotFoundBehaviour\(Object behaviour\)](CTIOperationRequestAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The name of the substep operation handler set on the CTIOperationRequest object. If it does not exist, returns null.|

```
var request = new sn_cti_core.CTIOperationRequest('origin');
var name = request.getOperationSubStepName();
```

## CTIOperationRequest - getParameter\(String key\)

Returns the value of a specified key previously set on the current CTIOperationRequest object.

Using the get/set parameter methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation request. The operation handler determines what key/value pairs are required as it consumes these values. Typically the message transformer sets these parameters on the CTIOperationRequest object by calling the [CTIOperationRequest - setParameter\(String key, Object value\)](CTIOperationRequestAPI.md#) method and the operation handler consumes them using this method.

|Name|Type|Description|
|----|----|-----------|
|key|String|The name of the key value to return.|

|Type|Description|
|----|-----------|
|String or Number|Value of the specified key. If no such key exists, returns null.|

```
(function( /*CTIOperationRequest*/ request, /*CTIOperationResponse*/ response, ctx) {
  var interactionSysId = request.getInteractionSysId();
  // Returns the number and add_comment parameters from the CTIOperationRequest object
  var number = request.getParameter('number');
  var addComment = request.getParameter('add_comment');
  addComment = addComment ? addComment.toLowerCase() : addComment;
  addComment = 'yes' === addComment || 'true' === addComment || '1' === addComment;
  var workNotes = request.getParameter('work_notes');
  var message = gs.getMessage('Thankyou');
  var interactionGr = request.getInteractionRecord();
  var openedFor = interactionGr ? interactionGr.getValue('opened_for') : null;
  if (openedFor && number && addComment && workNotes) {
    var now_GR = new GlideRecordSecure('incident');
    now_GR.addQuery('caller_id', openedFor);
    now_GR.addQuery('number', number);
    now_GR.query();
    if (now_GR.next()) {
    now_GR.work_notes += workNotes;
    now_GR.update();
      message = gs.getMessage('Your comment was added');
    }
  }
  response.setStatusCode(200);
  response.setMessage(message);
})(request, response, ctx);
```

## CTIOperationRequest - getParameters\(\)

Returns the key-value pairs for all parameters that were previously set on the current CTIOperationRequest object.

Using the get/set parameter methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation request. The operation handler determines what key/value pairs are required as it consumes these values. Typically the message transformer sets these parameters on the CTIOperationRequest object by calling the [CTIOperationRequest - setParameter\(String key, Object value\)](CTIOperationRequestAPI.md#) method and the operation handler consumes them using this method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A map of key-value pairs that were previously set on the CTIOperationRequest object. This key-value pairs are free-form and defined by the needs of the operation handler. The returned values are either Strings or Numbers.|

```
var request = new sn_cti_core.CTIOperationRequest('origin');
var parms = request.getParameters();
for(var key in parms) {
    gs.info(key + '=' + parms[key]);
}
```

## CTIOperationRequest - getSessionAttribute\(String key\)

Returns the value of a specified session attribute key set on the current CTIOperationRequest object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The sessionAttribute object can contain zero or more key/value pairs of data that are valid for the duration of a computer telephony integration provider defined session, such as the contact's phone number. Session attributes can also be accessed within a contact flow. The operation handler determines what session attribute key/value pairs are needed as it consumes these values. Typically the message transformer sets these attributes on the CTIOperationRequest object by calling the [CTIOperationRequest - setSessionAttribute\(String key, Object value\)](CTIOperationRequestAPI.md#) method. Session attributes are different than parameters in that they persist for the life of the session \(such as the entire call\) and should be passed back by the CTI provider with each operation request within that call session.

|Name|Type|Description|
|----|----|-----------|
|key|String|The name of the key value to return.|

|Type|Description|
|----|-----------|
|String or Number|Value of the specified key. If no such key exists, returns null.|

```
var request = new sn_cti_core.CTIOperationRequest('origin');
var phoneAttribute = request.getSessionAttribute('contact.phone');
```

## CTIOperationRequest - getSessionAttributes\(\)

Returns a key-value pair map of all session attributes set on the current CTIOperationRequest object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The sessionAttribute object can contain zero or more key/value pairs of data that are valid for the duration of a computer telephony integration provider defined session, such as the contact's phone number. Session attributes can also be accessed within a contact flow. The operation handler determines what session attribute key/value pairs are needed as it consumes these values. Typically the message transformer sets these attributes on the CTIOperationRequest object by calling the [CTIOperationRequest - setSessionAttribute\(String key, Object value\)](CTIOperationRequestAPI.md#) method. Session attributes are different than parameters in that they persist for the life of the session \(such as the entire call\) and should be passed back by the CTI provider with each operation request within that call session.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|A map of session attribute key-value pairs that were set on the associated CTIOperationResponse object. This map is free-form and defined by the needs of the operation handler.|

```
var request = new sn_cti_core.CTIOperationRequest('origin');
var parms = request.getSessionAttributes();
for(var key in parms) {
    gs.info(key + '=' + parms[key]);
}
```

## CTIOperationRequest - getSubStepNotFoundBehaviour

Returns the handling behavior for a subsep when a substep's operation handler is not found.

Use substeps to perform actions such as initialization and validation before processing an operation. Unlike operation handlers that are meant to be generic and used by all CTI providers, substeps are CTI provider specific and use terminology and naming conventions that are specific to the CTI provider.

If the requested substep operation handler cannot be found by the ServiceNow Voice framework, it attempts to use the "step not found behavior". This behavior is typically set by the message transformer when an operation is initially requested.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_hxb_rg2_1lb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OperationNotFoundBehaviours

</td><td>

The behavior/handling to perform when an operation handler cannot be found for the operation/substep combination \(**&lt;operation\_name&gt;**.SubStep&gt;\). If not defined, returns null.Possible values:

-   OperationNotFoundBehaviours.ThrowError: Throw an error.
-   OperationNotFoundBehaviours.PassThrough: Do not perform any further processing on the request, just return.
-   OperationNotFoundBehaviours.RouteToOperation: Use the parent operation handler **&lt;operation\_name&gt;**.

</td></tr></tbody>
</table>```
var request = new sn_cti_core.CTIOperationRequest('origin');
var behavior = request.getSubStepNotFoundBehaviour();
```

## CTIOperationRequest - setAuthToken\(String id\)

Sets an authentication token on the current CTIOperationRequest object.

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
|id|String|The authentication token for the associated ServiceNow Voice user.|

|Type|Description|
|----|-----------|
|void| |

Example of message transformer script that saves the passed in authentication token.

```
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {					
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
		    case 'statusCode':
		    case 'message':
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setInteractionSysId\(String Id\)

Sets the sys\_id of the interaction record associated with the operation request on the current CTIOperationRequest object.

If you want to maintain contact interaction information within a contact-specific interaction record, the interaction record sys\_id must be maintained for the entire ServiceNow Voice call session.

Typically, an operation handler creates an interaction record when a new contact call is initiated. It then sets the interaction record sys\_id and table name on the associated CTIOperationResponse object as session attributes using the [CTIOperationRequest - setSessionAttribute\(String key, Object value\)](../../CTIOperationResponse/concept/CTIOperationResponseAPI.md#) method. The associated method transformer then translates this information into the computer telephony integration \(CTI\) provider payload and sends it back to the CTI provider.

The CTI provider must store the interaction record sys\_id for the contact session locally. Each time the CTI provider interacts with the ServiceNow Voice for this contact session, it must pass back the corresponding interaction record sys\_id in its payload. The receiving message transformer then parses the payload and uses the CTIOperationRequest - setInteractionSysId\(\) method to set the interaction record sys\_id on the associated CTIOperationtRequest object.

The [CTIOperationRequest - getInteractionRecord\(\)](CTIOperationRequestAPI.md#) method uses this sys\_id to obtain the correct interaction record for the contact session.

<table id="table_usk_lrg_ykb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

String

</td><td>

Sys\_id of the interaction record to associate with the request.Table: Interaction \[interaction\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Example of a message transformer script that extracts the interaction record sys\_id from the incoming payload \(passed as a parameter\) and sets it on the associated CTIOperationRequest object.

```
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {					
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
                 // Associate the existing customer interaction record with the request
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
		    case 'statusCode':
		    case 'message':
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setLanguage\(String languageCode\)

Sets the ISO 639.1 language code to use when processing the associated operation on a CTIOperationRequest object.

Using the customer preferred language enables you to use platform-provided internationalization and localization capabilities to customize messages and other communications with the associated caller. Typically the message transformer sets the language on the CTIOperationRequest object.

|Name|Type|Description|
|----|----|-----------|
|languageCode|String|The ISO 639.1 language code to use when processing the associated operation.|

|Type|Description|
|----|-----------|
|void| |

```
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {					
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
		    case 'statusCode':
		    case 'message':
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setMajorVersion\(Number majorVersion\)

Sets the major version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationRequest object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different processing behavior. If the processing behavior is only slightly different between the software versions, it may make sense to have only a single operation handler. You can then handle the processing differences by just checking the version of software making the request and process the request/data within your operation handler. If the required processing is significantly different between versions, it may be more effective to use multiple operation handlers.

Typically the message transformer sets the software version on the CTIOperationRequest object by calling this method and an operation handler then consumes the set value using the [CTIOperationRequest - getMajorVersion\(\)](CTIOperationRequestAPI.md#) method. You can also get/set the minor version value of a provider's software using the [CTIOperationRequest - getMinorVersion\(\)](CTIOperationRequestAPI.md#) and [CTIOperationRequest - setMinorVersion\(Number minorVersion\)](CTIOperationRequestAPI.md#) methods.

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
var request = new sn_cti_core.CTIOperationRequest('origin');
request.setMajorVersion(2);
```

## CTIOperationRequest - setMinorVersion\(Number minorVersion\)

Sets the minor version of the computer telephony integrator \(CTI\) provider software making the request on the associated CTIOperationRequest object.

Use this method if the CTI providers connected to your ServiceNow instance are running multiple versions of their software, as different software versions may require different processing behavior. If the processing behavior is only slightly different between the software versions, it may make sense to have only a single operation handler. You can then handle the processing differences by just checking the version of software making the request and process the request/data within your operation handler. If the required processing is significantly different between versions, it may be more effective to use multiple operation handlers.

Typically the message transformer sets the software version on the CTIOperationRequest object by calling this method and an operation handler then consumes the set value using the [CTIOperationRequest - getMinorVersion\(\)](CTIOperationRequestAPI.md#) method. You can also get/set the major version value of a provider's software using the [CTIOperationRequest - getMajorVersion\(\)](CTIOperationRequestAPI.md#) and [CTIOperationRequest - setMajorVersion\(Number majorVersion\)](CTIOperationRequestAPI.md#) methods.

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
var request = new sn_cti_core.CTIOperationRequest('origin');
...
request.setMinorVersion(3);
```

## CTIOperationRequest - setOperationName\(String name\)

Sets the name of the operation that the computer telephony integration \(CTI\) provider is attempting to execute on the current CTIOperationRequest object.

The operation name determines the operation handler that is used to process the request. Call this method from the associated message transformer.

**Note:** For Amazon Connect Lex Bot implementations, intent names are appended with a five letter suffix as different Amazon intents cannot have the same intent name. In the ServiceNow Voice framework, the intent name equals the operation handler name. An operation handler can either be specific for an intent, having an operation handler name that includes this suffix \(myOperation\_SUFFX\), or it can be generic and used by multiple CTI providers or different use cases, such as using the same handler for processing an HR request and a helpdesk request \(myOperation\).

<table id="table_msx_jpw_zkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

String

</td><td>

The name of the operation that the CTI provider is currently attempting to execute. This name must be the same as the name of the operation handler to use to process the request. If it is not, an error is thrown. You can locate the available operation handlers in the Operation Handler \[sn\_cti\_operation\_handler\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {	
           // Set the operation handler to use to process the request				
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
		    case 'statusCode':
		    case 'message':
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setOperationSubStepName\(String name\)

Sets the operation substep name on the current CTIOperationRequest object.

Use substeps to perform actions such as initialization and validation before processing an operation. Unlike operation handlers that are meant to be generic and used by all CTI providers, substeps are CTI provider specific and use terminology and naming conventions that are specific to the CTI provider.

The ServiceNow Voice framework performs the following steps to locate the required operation handler and any associated substep operation handlers.

**Note:** For Amazon Connect Lex Bot implementations, intent names are appended with a five letter suffix as different Amazon intents cannot have the same intent name. In the ServiceNow Voice framework, the intent name equals the operation handler name. An operation handler can either be specific for an intent, having an operation handler name that includes this suffix \(myOperation\_SUFFX\), or it can be generic and used by multiple CTI providers or different use cases, such as using the same handler for processing an HR request and a helpdesk request \(myOperation\).

1.  Tries to locate the operation handler associated with the request.
    -   First checks for an operation handler called `myOperation_SUFFX`.
    -   If not found, checks for the operation handler `myOperation`. If not found, errors out.
2.  If the handler is found, checks the **auth\_required** flag on the operation handler. If set, it checks that a valid authentication token \(obtained through the getAuthToken\(\) method\) is present on the request. If present and valid, continue processing, else throw an error.
3.  Looks up the operation handler for the passed in substep. For this example let's assume `subStepName=SubStep`.
    -   First checks for an operation handler named `myOperation_SUFFX.SubStep`. If found, executes the handler.
    -   If not found, checks for the handler `myOperation.SubStep`. If found executes the handler.
    -   If not found, checks if a `subStepNotFoundBehavior` was set on the request object.
    -   If set, executes the behavior, otherwise, errors out.
4.  Executes the primary operation handler \(`myOpersation_SUFFX` or `myOperation`.\)

You can set the default behavior of a substep by calling the [CTIOperationRequest - setSubStepNotFoundBehaviour\(Object behaviour\)](CTIOperationRequestAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|name|String|The name of the substep that the CTI provider is trying to execute.|

|Type|Description|
|----|-----------|
|void| |

```
(function( /*HTTPRequest*/ httpRequest, /*CTIOperationRequest*/ operationRequest, /*Context*/ ctx) {
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
      var event = jsonPayload.event;
      if (event) {
        var intent = event.currentIntent;
	 var inputTranscript = event.inputTranscript;
	 if(inputTranscript) {
	   operationRequest.setParameter('$utterance', inputTranscript);
	 }
        if (intent) {
          operationRequest.setOperationName(intent.name);
	   // Add this because intent name gets changed through the pipeline
	   operationRequest.setParameter('$original_intent', intent.name);
          var sessionAttributes = event.sessionAttributes;
          if (sessionAttributes) {
            for (var sk in sessionAttributes) {
              switch (sk) {
                case 'interactionId':
                  operationRequest.setInteractionSysId(sessionAttributes[sk]);
                  break;
                case 'authToken':
                  operationRequest.setAuthToken(sessionAttributes[sk]);
                  break;
		  case 'language':
		    operationRequest.setLanguage(sessionAttributes[sk]);
		    break;
                case 'statusCode':
                case 'message':
                  break;
                default:
                  operationRequest.setSessionAttribute(sk, sessionAttributes[sk]);
              }
            }
          }
          var slots = intent.slots;
	   // Always copy in slots they are the parameters for the operation
          if (slots) {
            for (var pk in slots) {
              operationRequest.setParameter(pk, slots[pk]);
            }
          }
          var invocationSource = event.invocationSource;
	   operationRequest.setParameter('$$invocationSource', invocationSource);
          // Specific handling for dialog hooks with a way to override for Amazon specific provider
          if (invocationSource === 'DialogCodeHook') {
	     // Set substep to trigger forwarding to another handler IF it s present
	     operationRequest.setOperationSubStepName(invocationSource);
	     // Allow pass through behavior
	     var behaviourToUse = sn_cti_core.CTIOperationRequest.OperationNotFoundBehaviours.PassThrough;
	     operationRequest.setSubStepNotFoundBehaviour(behaviourToUse);
	     // Reserved - copy slots in so we can just use delegate as default if the call isn't handled
	     operationRequest.setParameter('$$slots', slots);
          }
        }
      }
    }
  } catch (e) {
      ctx.setError(e);
  }
  return operationRequest;
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setParameter\(String key, Object value\)

Sets the specified key-value pair on the parameter object of the current CTIOperationRequest object.

Using the get/set parameter methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The parameter object can contain zero or more key/value pairs of data that directly correlate to the current operation request. The operation handler determines what key/value pairs are required as it consumes these values. Typically the message transformer sets these parameters on the CTIOperationRequest object by calling this method and the operation handler consumes them using the [CTIOperationRequest - getParameter\(String key\)](CTIOperationRequestAPI.md#) or [CTIOperationRequest - getParameters\(\)](CTIOperationRequestAPI.md#) method.

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

Value to store.Valid data types:

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
{	
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
	var event = jsonPayload.event;
	if (event) {
	  var details = event.Details;
	  if (details) {					
	    operationRequest.setOperationName(details.Parameters['sn_operation']);
	    var contactData = details.ContactData;
	    if(contactData) {
		// Call id should be surfaced in openframe call log so it can be tied to transcription later
		operationRequest.setParameter('contact.call_id', contactData.ContactId);
		for(var ck in contactData.CustomerEndpoint) {
		  operationRequest.setParameter('contact.' + ck, contactData.CustomerEndpoint[ck]);
	       }
	       operationRequest.setParameter('contact.id', contactData.ContactId);
	       operationRequest.setParameter('contact.phone', contactData.CustomerEndpoint.Address);
	    }
	    var parameters = details.Parameters;
	    if (parameters) {
		for (var pk in parameters) {
		  switch(pk) {
		    case 'interactionId':
			operationRequest.setInteractionSysId(parameters[pk]);
			break;
		    case 'authToken':
			operationRequest.setAuthToken(parameters[pk]);
			break;
		    case 'language':
			operationRequest.setLanguage(parameters[pk]);
			break;
		    case 'statusCode':
		    case 'message':
			break;
								
		    default:
			operationRequest.setParameter(pk, parameters[pk]);
		 }						
            }
          }					
        }
      }
    }
  } catch(e) {
		ctx.setError(e);
  }
})(httpRequest, operationRequest, ctx);
```

## CTIOperationRequest - setSessionAttribute\(String key, Object value\)

Sets the specified session attribute key-value pair on the current CTIOperationRequest object.

Using the get/set session attribute methods enables the passing of virtually any string or number value between a message transformer and an operation handler. The sessionAttribute object can contain zero or more key/value pairs of data that are valid for the duration of a computer telephony integration provider defined session. Session attributes can also be accessed within a contact flow. The operation handler determines what session attribute key/value pairs are needed as it consumes these values. Typically the message transformer sets these attributes on the CTIOperationRequest object by calling this method and the operation handler gets the attributes using the [CTIOperationRequest - getSessionAttribute\(String key\)](CTIOperationRequestAPI.md#) or [CTIOperationRequest - getSessionAttribute\(\)](CTIOperationRequestAPI.md#) method.

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

Name of the key under which to store the associated value.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to store.Valid data types:

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
var request = new sn_cti_core.CTIOperationRequest('origin');
request.setSessionAttribute('contact.phone', '+15552222345');
request.setSessionAttribute('contact.okToCall', true);
request.setSessionAttribute('contact.address', {
    street: '1234 Main St'
    city: 'API City',
    zip: 91335
});
```

## CTIOperationRequest - setSubStepNotFoundBehaviour\(Object behaviour\)

Sets the behavior to perform if the current substep's operation handler is not found.

This method should be called by the input message transformer.

<table id="table_k4q_dmf_1lb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

behaviour

</td><td>

OperationNotFoundBehaviours

</td><td>

Behavior to use if a handling behavior is not specified for the substep. This must be a behavior defined on the CTIOperationRequest.OperationNotFoundBehaviours object.Possible values:

-   ThrowError: Throw an error.
-   PassThrough: Do not perform any further processing on the request, just return.
-   RouteToOperation: Use the parent operation handler **&lt;operation\_name&gt;**.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
(function( /*HTTPRequest*/ httpRequest, /*CTIOperationRequest*/ operationRequest, /*Context*/ ctx) {
  try {
    var jsonPayload = httpRequest.body.data;
    if (jsonPayload) {
      var event = jsonPayload.event;
      if (event) {
        var intent = event.currentIntent;
	 var inputTranscript = event.inputTranscript;
	 if(inputTranscript) {
	   operationRequest.setParameter('$utterance', inputTranscript);
	 }
        if (intent) {
          operationRequest.setOperationName(intent.name);
	   // Add this because intent name gets changed through the pipeline
	   operationRequest.setParameter('$original_intent', intent.name);
          var sessionAttributes = event.sessionAttributes;
          if (sessionAttributes) {
            for (var sk in sessionAttributes) {
              switch (sk) {
                case 'interactionId':
                  operationRequest.setInteractionSysId(sessionAttributes[sk]);
                  break;
                case 'authToken':
                  operationRequest.setAuthToken(sessionAttributes[sk]);
                  break;
		  case 'language':
		    operationRequest.setLanguage(sessionAttributes[sk]);
		    break;
                case 'statusCode':
                case 'message':
                  break;
                default:
                  operationRequest.setSessionAttribute(sk, sessionAttributes[sk]);
              }
            }
          }
          var slots = intent.slots;
	   // Always copy in slots they are the parameters for the operation
          if (slots) {
            for (var pk in slots) {
              operationRequest.setParameter(pk, slots[pk]);
            }
          }
          var invocationSource = event.invocationSource;
	   operationRequest.setParameter('$$invocationSource', invocationSource);
          // Specific handling for dialog hooks with a way to overide for Amazon specific provider
          if (invocationSource === 'DialogCodeHook') {
	     // Set substep to trigger forwarding to another handler IF it s present
	     operationRequest.setOperationSubStepName(invocationSource);
	     // Allow pass through behavior
	     var behaviourToUse = sn_cti_core.CTIOperationRequest.OperationNotFoundBehaviours.PassThrough;
	     operationRequest.setSubStepNotFoundBehaviour(behaviourToUse);
	     // Reserved - copy slots in so we can just use delegate as default if the call isn't handled
	     operationRequest.setParameter('$$slots', slots);
          }
        }
      }
    }
  } catch (e) {
      ctx.setError(e);
  }
  return operationRequest;
})(httpRequest, operationRequest, ctx);
```

