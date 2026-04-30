---
title: getRecords
description: Query the targeted table by example values and return all matching records and their fields.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data Retrieval API, SOAP direct web service API functions, Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# getRecords

Query the targeted table by example values and return all matching records and their fields.

## Input fields

Any field value in the targeted table.

## Output fields

The getRecordResponse element may contain one or more getRecordsResult elements that encapsulate elements representing the field values of records matching the query.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:getRecords>
         <number>INC0000002</number>
      </inc:getRecords>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP request using an encoded query to filter where incident number is INC0000001 or INC0000002

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:getRecords>
         <__encoded_query>number=INC0000001^ORnumber=INC0000002</__encoded_query>
      </inc:getRecords>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response that contains 1 record

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <getRecordsResponse>
         <getRecordsResult>
            <caller_id>5137153cc611227c000bbd1bd8cd2007</caller_id>
            <caller_id.email>david.loo@service-now.com</caller_id.email>
            <closed_at/>
            <number>INC0000002</number>
            <opened_at>2009-12-14 23:07:12</opened_at>
            <short_description>Can't get to network file shares</short_description>
         </getRecordsResult>
      </getRecordsResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

Sample SOAP response that contains more than 1 record

```
<soapenv:Envelope xmlns:inc="http://www.service-now.com/incident" xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Header/>
   <soapenv:Body>
      <getRecordsResponse>
         <getRecordsResult>
            <caller_id>5137153cc611227c000bbd1bd8cd2006</caller_id>
            <caller_id.email>rick.berzle@yourcompany.com</caller_id.email>
            <closed_at>2009-12-17 22:55:16</closed_at>
            <number>INC0000009</number>
            <opened_at>2009-12-16 22:50:23</opened_at>
            <short_description>Reset my password</short_description>
         </getRecordsResult>
         <getRecordsResult>
            <caller_id>5137153cc611227c000bbd1bd8cd2005</caller_id>
            <caller_id.email>fred.luddy@yourcompany.com</caller_id.email>
            <closed_at>2009-12-15 22:54:55</closed_at>
            <number>INC0000010</number>
            <opened_at>2009-12-10 22:53:02</opened_at>
            <short_description>Need Oracle 10GR2 installed</short_description>
         </getRecordsResult>
      </getRecordsResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

## Language-specific sample messages

For language-specific getRecords samples, refer to the following topics:

[Perl SOAP::Lite](../../examples/concept/c_PerlWebServicesClientExamples.md#getRecords)

[Java Apache Axis2](../../examples/concept/c_JAAWbSrvcsClntExUpdt.md)

[Python](../../examples/concept/c_PythonWebServicesClientExamples.md#getRecords)

**Parent Topic:**[Data Retrieval API](r_DataRetrievalAPI.md)

