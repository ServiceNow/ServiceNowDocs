---
title: Recordless SOAPMessageV2 example
description: You can use the SOAPMessageV2\(\) constructor with no parameters to define a SOAP message entirely in the script.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Scripting, SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Recordless SOAPMessageV2 example

You can use the SOAPMessageV2\(\) constructor with no parameters to define a SOAP message entirely in the script.

When using this constructor you must provide an endpoint and SOAP action. In this example, the script creates an empty SOAP message and sets the values needed to insert an incident record.

```
var s = new sn_ws.SOAPMessageV2(); //create an empty SOAP message
s.setBasicAuth('admin','admin');
s.setSOAPAction('http://www.service-now.com/incident/insert'); //set the SOAP action to perform
s.setEndpoint('http://<instance>.service-now.com/incident.do?SOAP'); //set the web service provider endpoint
s.setRequestBody('<soapenv:Envelope xmlns:soapenv=\"http://schemas.xmlsoap.org/soap/envelope/\" xmlns:inc=\"http://www.service-now.com/incident\"><soapenv:Header/><soapenv:Body><inc:insert><short_description>Test Dynamic SOAP</short_description></inc:insert></soapenv:Body></soapenv:Envelope>');
var response = s.execute();
var xmldoc = new XMLDocument(response.getBody());
var incident_sysid = xmldoc.getNodeText('//sys_id');
```

**Parent Topic:**[Scripting outbound SOAP](../../../../../integrate/outbound-soap/reference/r_ScriptingOutboundSOAP.md)

