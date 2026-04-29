---
title: getKeys
description: Query the targeted table by example values and return a comma delimited sys\_id list.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Retrieval, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# getKeys

Query the targeted table by example values and return a comma delimited `sys_id` list.

## Input fields

Any field value in the targeted table.

## Output fields

A SOAP response element **sys\_id** that contains a comma delimited list of [Unique record identifier \(sys\_id\)](https://www.servicenow.com/docs/access?context=c_UniqueRecordIdentifier&version=australia&pubname=australia-platform-administration&ft:locale=en-US) values.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:getKeys>
         <category>hardware</category>
      </inc:getKeys>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <getKeysResponse>
         <sys_id>46e18c0fa9fe19810066a0083f76bd56,46e57642a9fe1981000b96a5dca501ff,46f1784ba9fe19810018aa27fbb23482</sys_id>
         <count>7</count>
      </getKeysResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Language-specific sample messages

For language-specific getKeys samples, refer to the following topics:

[Perl SOAP::Lite](../../examples/concept/c_PerlWebServicesClientExamples.md)

[Java Apache Axis2](../../examples/concept/c_JAAWbSrvcsClntExUpdt.md)

[Python](../../examples/concept/c_PythonWebServicesClientExamples.md#getKeys)

**Parent Topic:**[Data Retrieval API](r_DataRetrievalAPI.md)

