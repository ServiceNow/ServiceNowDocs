---
title: deleteMultiple
description: Delete multiple records from the targeted table by example values.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/web-services/r\_DeleteMultiple.html
release: xanadu
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data Modification API, SOAP direct web service API functions, Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# deleteMultiple

Delete multiple records from the targeted table by example values.

## Input fields

All fields from the targeted table, including system fields, are used in query-by-example \(QBE\) fashion to locate records to be deleted. Query example fields can have special prefixes to constrain the search function.

## Output fields

A &lt;count&gt; element within the deleteRecordResponse parent element indicating the number of records deleted.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:deleteMultiple>
         <category>hardware</category>
      </inc:deleteMultiple>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <deleteMultipleResponse>
         <count>6</count>
      </deleteMultipleResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Language-specific sample messages

For language-specific deleteRecord samples, refer to the following topics:

[Perl SOAP::Lite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/web-services/c_PerlWebServicesClientExamples.md)

Java Apache Axis2

Microsoft .NET

Python

**Parent Topic:**[Data Modification API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/web-services/r_DataModificationAPI.md)

