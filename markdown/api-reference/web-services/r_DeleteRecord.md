---
title: deleteRecord
description: Delete a record from the targeted table by supplying its sys\_id.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data modification, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# deleteRecord

Delete a record from the targeted table by supplying its **sys\_id**.

## Input fields

An element &lt;sys\_id&gt; identifying the **sys\_id** of the record to be retrieved.

## Output fields

A &lt;count&gt; element within the deleteRecordResponse parent element indicating the number of records deleted, this will always equal to "1" for `deleteRecord`.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:deleteRecord>
         <sys_id>46e18c0fa9fe19810066a0083f76bd56</sys_id>
      </inc:deleteRecord>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <deleteRecordResponse>
         <count>1</count>
      </deleteRecordResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Language-specific sample messages

For language-specific deleteRecord samples, refer to the following topics:

[Perl SOAP::Lite](../../examples/concept/c_PerlWebServicesClientExamples.md#update)

Java Apache Axis2

Microsoft .NET

Python

**Parent Topic:**[Data Modification API](r_DataModificationAPI.md)

