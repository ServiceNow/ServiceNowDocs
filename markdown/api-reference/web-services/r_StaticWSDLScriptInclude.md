---
title: Static WSDL script include example
description: This example demonstrates the FakeStockValue script include that implements much of the static WSDL behavior.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a static WSDL script include, Creating with static WSDLs, Scripted Services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Static WSDL script include example

This example demonstrates the FakeStockValue script include that implements much of the static WSDL behavior.

```
var FakeStockValue = Class.create();
 
FakeStockValue.prototype = {
  initialize : function(requestXML) {
    //Use some backend XML utilities...you could use string tools if you wish
    this.xmlutil = Packages.com.glide.util.XMLUtil;
    //converting the string to an XML Document
    this.fSoapDoc = new XMLDocument(requestXML);
  },
 
  process : function() {
    var soapBody = this.fSoapDoc.getNode("/Envelope/Body");
    //Our WSDL was formatted to have the only first child element be the function
    var funcNode = this.xmlutil.getFirstChildElement(soapBody);
    var nodeName = this.xmlutil.getNodeNameNS(funcNode);
 
    //If the function for this SOAP request is TradePriceRequest, perform the necessary actions
    if (nodeName == "TradePriceRequest") {
      return this.fakeOutTradePriceRequest(funcNode);
    }
 
    //Couldn't find any supported functions in this SOAP request
    return this.generateSoapFault("un-supported API call: " + nodeName);
  },
 
  fakeOutTradePriceRequest : function (funcNode) {
    //Create the beginnings of our XML response
    var r = new XMLDocument("<GetLastTradePriceOutput xmlns='https://www.service-now.com/vws/FakeStockValue'/>");
 
    //Do the necessary actions here...we're going to get the USER ID of the user
    //used to make this SOAP call.  Then we will return the 
    //stock symbol they were asking about
    var usersysid = gs.getUserID();
    var now_GR = new GlideRecord("sys_user");
    gr.get(usersysid);
    var username = gr.user_name;
    var quoteSymbol = this.xmlutil.getText(funcNode);
    //Create a "message" element to store our response message
    r.createElement("message", username + ", You were looking for a quote on "+quoteSymbol);
    return r.getDocumentElement();
  },
 
 
  generateSoapFault : function (str) {
     var f = "<SOAP-ENV:Fault>" +
               "<faultcode xsi:type='xsd:string'>SOAP-ENV:FakeStockValue</faultcode>" +
               "<faultstring xsi:type='xsd:string'>" + str + 
               "</faultstring>" +
             "</SOAP-ENV:Fault>"
     var s = new XMLDocument(f);
     return s.getDocumentElement();
  }
}

```

## initialize function

The initialize function takes the XML request string and converts it to an XML Document object that you can navigate and manipulate using libraries. Alternatively, you can leave the XML request as a string and navigate it using regular expressions.

## process function

The process function is called by the scripted web service. This function grabs the first child element in the XML after the body element. The WSDL uses this child element to determine which function to use. In this WSDL there is only one possible function but most WSDLs provide many functions. If more functions were available, there would be more "if" statements that tested the first child element for the various function names.

## fakeOutTradePriceRequest function

The fakeOutTradePriceRequest function is the implementation of the only available function in the WSDL. This function looks up the user that the SOAP request authenticated as and retrieves the **user\_name** then returns it to the SOAP client. The fakeOutTradePriceRequest function could be expanded to perform useful activities, such as looking up a stock symbol and returning the last traded price.

## generateSoapFault function

The generateSoapFault function returns a SOAP error that can be called if there are problems.

**Parent Topic:**[Create a static WSDL script include](../task/t_CreateAStatickWSDLScriptInclude.md)

