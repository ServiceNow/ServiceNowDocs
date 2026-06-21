---
title: Customize response
description: Follow this example to customize and control the XML payload of a SOAP response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/web-services/t\_CustomizeResponse.html
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Scripted SOAP web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Customize response

Follow this example to customize and control the XML payload of a SOAP response.

## Before you begin

Role required: web\_service\_admin or admin

## Procedure

1.  Create a customized XML document using the [XMLDocument](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/scripts/c_XMLDocumentScriptObject.md) script include object.

    **Note:** When creating a scripted web service in a scoped application you must use the [XMLDocument2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/server-api-reference/c_XMLDocument2ScopedAPI.md) API.

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


**Parent Topic:**[Scripted SOAP web services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/web-services/c_ScriptedWebServices.md)

