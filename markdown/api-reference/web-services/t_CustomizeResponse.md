---
title: Customize response
description: Follow this example to customize and control the XML payload of a SOAP response.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Scripted Services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Customize response

Follow this example to customize and control the XML payload of a SOAP response.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Create a customized XML document using the [XMLDocument](../../../script/server-scripting/concept/c_XMLDocumentScriptObject.md) script include object.

    **Note:** When creating a scripted web service in a scoped application you must use the [XMLDocument2](../../../app-store/dev_portal/API_reference/XMLDocument2ScopedAPI/concept/c_XMLDocument2ScopedAPI.md#) API.

2.  Set its document element to the variable *response.soapResponseElement* in a scripted web service.

    For example, the following scripted web service script:

    ```
    var xmldoc = new XMLDocument2();
        xmldoc.parseXML("<myResponse></myResponse>");
        xmldoc.createElementWithTextValue("element_one", "test");  
        xmldoc.createElementWithTextValue("element_two", "new2 value");  
    
        var el = xmldoc.createElement("element_three");
        xmldoc.setCurrentElement(el);  
        xmldoc.createElementWithTextValue("newChild", "test child element");
    
        response.soapResponseElement = xmldoc.getDocumentElement();
    ```

    Is used to accept the following request:

    ```
    <soapenv:Envelope 
       xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
       xmlns:tes="http://www.service-now.com/TestCustomResponse">
       <soapenv:Header/>
       <soapenv:Body>
          <tes:execute/>
       </soapenv:Body>
    </soapenv:Envelope>
    ```

    Which will respond with the following SOAP response:

    ```
    <soapenv:Envelope 
        xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
        xmlns:tes="http://www.service-now.com/TestCustomResponse">
       <soapenv:Header/>
       <soapenv:Body>
          <myResponse>
             <element_one>test</element_one>
             <element_two>new2 value</element_two>
             <element_three>
                <newChild>test child element</newChild>
             </element_three>
          </myResponse>
       </soapenv:Body>
    </soapenv:Envelope>
    ```

    WSDL support will need to be created externally. The SOAP endpoint will need to be referred back to the scripted web service in question.


**Parent Topic:**[Scripted SOAP web services](../concept/c_ScriptedWebServices.md)

