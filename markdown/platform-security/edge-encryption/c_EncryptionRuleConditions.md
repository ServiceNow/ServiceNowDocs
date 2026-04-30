---
title: Encryption rule conditions
description: Encryption rule conditions determine if the rule should be executed.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Encryption rule conditions

Encryption rule conditions determine if the rule should be executed.

An encryption rule condition must return true if the rule is to handle the HTTP request; otherwise, it must return false.

As you build your condition, keep in mind that only one rule is executed per request. As a result, the condition must be as general or specific as needed to run under the intended circumstances.

**Note:** Be careful when performing checks on content in the condition. Excessive checks can be expensive for the proxy server and may cause increased latency when handling complex requests.

The condition can use the method type, content type, URL path, or any URL query string parameters to determine if the rule should handle the request. The condition has access to these fields via the [request](c_requestAPI.md#) object. Be sure that, prior to creating an encryption rule condition, you have inspected the client request and understand the conditions needed to trigger the rule.

**Note:** To build efficient rules, consider easy ways to rule out requests that you do not want to be evaluated by a rule. Build your condition to return false for those requests first. This method increases performance and quickly routes the request to the correct rule faster.

[Encryption rule objects and APIs](api-overview.md) are available to encryption rule conditions.

## Example using path and postParams

```
/*This condition checks if the request coming in has a path ending in 
"/sample_processor.do" and if a post parameter exists in that request called myPostParam */

function SampleCondition(request) {
   if (endsWith(request.path, "/sample_processor.do") && request.postParams.myPostParam) {
       return true;
   }    
   return false;
}
```

## Example using urlParams and contentType

```
/* This condition checks if a url parameter exists in the query called 
myUrlParam and if the content type contains 'xml' 
(if so, you can expect the body to be an XML payload). 
Then, it checks if the xml payload contains myXmlTag */

function SampleCondition2(request) {
   if (request.urlParams.myUrlParam && request.contentType.indexOf('xml') > -1 && request.xmlContains('myXmlTag')) {
       return true;
   }    
 return false;
}
```

**Parent Topic:**[Define a custom encryption rule](c_EncryptionRules.md)

