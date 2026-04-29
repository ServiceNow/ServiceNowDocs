---
title: update
description: Updates an existing record in the targeted table in the URL, identified by the mandatory sys\_id field.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data modification, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# update

Updates an existing record in the targeted table in the URL, identified by the mandatory **sys\_id** field.

## Input fields

All fields from the targeted table, excluding system fields, which will be used for updating the existing record. The **sys\_id** field is used to locate the existing record.

## Output fields

Returns the **sys\_id** of the record that was updated.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:update>
         <sys_id>46e18c0fa9fe19810066a0083f76bd56</sys_id>
         <short_description>this is updated</short_description>
      </inc:update>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <updateResponse>
         <sys_id>46e18c0fa9fe19810066a0083f76bd56</sys_id>
      </updateResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Language-specific sample messages

For language-specific update samples, refer to the following topics:

[Perl SOAP::Lite](../../examples/concept/c_PerlWebServicesClientExamples.md#update)

Java Apache Axis2

Microsoft .NET

Python

**Parent Topic:**[Data Modification API](r_DataModificationAPI.md)

