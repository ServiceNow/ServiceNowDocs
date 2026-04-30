---
title: Transform Virtual Agent API request and response
description: You can transform Virtual Agent API request and response into supported formats through the scripted extension points provided in Virtual Agent API.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Transform Virtual Agent API request and response

You can transform Virtual Agent API request and response into supported formats through the scripted extension points provided in Virtual Agent API.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extensions Points** &gt; **Scripted Extension Points**

    -   The sn\_va\_as\_service.va\_api\_payload\_transformation extension point transforms primary bot payload into standard Virtual Agent API supported format before processing the request. The sn\_va\_as\_service.va\_api\_output\_transformation extension point transforms Virtual Agent API response into a format supported by the primary bot.
    -   Both the scripted extension points have two parameters: **shouldTransform** and **transform**. **shouldTransform** is used to determine whether the implementation is executed. **transform** is used to transform the request or response.
2.  If you want to transform the request payload, complete the following steps.

    1.  Select sn\_va\_as\_service.va\_api\_payload\_transformation extension point

    2.  In the Related Links section, select **Create implementation**.

    3.  Update the extension point script according to your requirements.

        In sn\_va\_as\_service.va\_api\_payload\_transformation extension point, the request parameter is an object with two keys: **payload** and **headers**. **payload** is the request payload received from the primary bot, and **headers** are the headers sent in the request payload. The following is a sample implementation.

        ```
        
        var va_api_payload_transformation = Class.create();
        va_api_payload_transformation.prototype = {
            initialize: function() {},
        
            shouldTransform: function(request) {
                return request.payload.caller === "examplebot";
            },
        
            /* 
            return object for transform function should be in the following format
            transformedRequest = {
            payload: request.payload,
            headers: request.headers
            };
            */transform: function(request) {
            var payload = request.payload;
            var headers = request.headers;
        
            var vaAPIPayload = {
        	"userId": payload.userId,
        	"emailId": payload.email,
        	"message": {
        	    "text": payload.message,
        	    "typed": true
        	},
        	"contextVariables": {
        	    "requester_session_language": payload.user_language
        	},
        	"appInboundId": "custom_1"
            };
        	
            return {
        	payload: vaAPIPayload,
        	headers: headers
            };
        },
        
        ```

        ![Scripted extension point for the transformation of request payload](../images/va-api-payload-transformation-extension-point.png "sn_va_as_service.va_api_payload_transformation extension point")

    4.  Select **Update**.

3.  If you want to transform the response payload, complete the following steps.

    1.  Select sn\_va\_as\_service.va\_api\_output\_transformation extension point

    2.  In the Related Links section, select **Create implementation**.

    3.  Update the extension point script according to your requirements.

        In sn\_va\_as\_service.va\_api\_output\_transformation extension point, the response parameter is an object with two keys: inputPayload and responsePayload. **inputPayload** is the request payload received from Virtual Agent API, and **responsePayload** is the response from Virtual Agent API which you can use to build the transformed response. Use the appInboundId field of the request payload to determine whether to return true or false. The following is a sample implementation.

        ```
        
        var va_api_output_transformation = Class.create();
        va_api_output_transformation.prototype = {
            initialize: function() {},
        
            shouldTransform: function(response) {
        	return (response.inputPayload.appInboundId === 'custom_1');
            },
        
            /*
            input object param for transform function should be in the following format
            response = {
                inputPayload: response.inputPayload,
        	responsePayload: response.responsePayload
            };
            */
            transform: function(response) {
        	//return only transformed payload
                return {
        	    'custom_structure': response.responsePayload
        	};
            },
        
            type: 'va_api_output_transformation'
        };
        
        ```

        ![Scripted extension point for the transformation of response payload](../images/va-api-output-transformation-extension-point.png "sn_va_as_service.va_api_output_transformation extension point")

    4.  Select **Update**.


**Parent Topic:**[Using Virtual Agent API](../concept/use-virtual-agent-api.md)

