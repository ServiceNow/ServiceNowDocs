---
title: Create a new scripted SOAP web service
description: Follow these examples to create a new scripted SOAP web service.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripted Services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Create a new scripted SOAP web service

Follow these examples to create a new scripted SOAP web service.

When the Web Services Provider - Scripted plugin is activated, a new module Scripted Web Services is available under the System Web Services application.

![Scripted SOAP Web Services](../image/scripted-soap-web-services.png)

## Example 1: Retrieving a system property

The first step is to define the incoming and return parameters. This is done by adding an entry to the Input Parameters and Output Parameters. These parameters are used to construct and present a meaningful WSDL, and they do not add to the functionality of processing the actual Web Service itself.

![GetProperty Input Parameters](../image/soap-GetProperty-input-parameters.png)

![GetProperty Output Parameters](../image/soap-GetProperty-output-parameters.png)

The parameters are referenced in the script of the Web Service. Any of the input parameters are retrieved using the following syntax:

```
var a= request.property;
```

The output parameters are set by using the following syntax:

```
response.property="ABC";
```

The following example demonstrates how to retrieve a system property and return it as part of the SOAP response. The example shows how to create a custom scripted web service to do something specific that the base ServiceNow system direct Web Services cannot.

![GetProperty web service](../image/GetProperty-soap-web-service.png)

## Example 2: Ordering a Blackberry

[Direct web services](../concept/c_DirectWebServices.md) operate on tables and their data. The following example shows how to initiate a business solution, such as ordering a Blackberry, by invoking a scripted web service. The following input and output parameters support the Blackberry example:

![OrderBlackBerry Input Parameters](../image/soap-blackberry-input-parameters.png)

![OrderBlackBerry Output Parameters](../image/soap-blackberry-output-parameters.png)

This script shows how to use the above parameters to add a Blackberry to the service catalog shopping cart and order it. The request number is returned in the request\_number field of the SOAP response.

```
var cart = new Cart();
var item = cart.addItem('e2132865c0a8016500108d9cee411699');
cart.setVariable(item,'original', request.phone_number);
 
// set the requested for
var gr = new GlideRecord("sys_user");
gr.addQuery("user_name", request.requested_for);
gr.query();

if(gr.next()){
  var cartGR = cart.getCart();
  cartGR.requested_for = gr.getUniqueValue();
  cartGR.update();
}
 
var rc = cart.placeOrder();
response.request_number= rc.getValue('number');
```

**Parent Topic:**[Scripted SOAP web services](../concept/c_ScriptedWebServices.md)

