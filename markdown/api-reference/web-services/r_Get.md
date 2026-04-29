---
title: get
description: Query a single record from the targeted table by sys\_id and return the record and its fields.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Retrieval, API functions, Direct services, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# get

Query a single record from the targeted table by `sys_id` and return the record and its fields.

## Input fields

An element &lt;sys\_id&gt; identifying the sys\_id of the record to be retrieved.

## Output fields

A `getResponse` element encapsulating all field values for the record retrieved.

## Sample SOAP messages

Sample SOAP request

```
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:get>
         <sys_id>46e18c0fa9fe19810066a0083f76bd56</sys_id>
      </inc:get>
   </soapenv:Body>
</soapenv:Envelope>
```

The resulting response of a `get` function call looks like this:

```
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemaap/envelope/" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <soap:Body>
    <getResponse xmlns="http://www.service-now.com/incident">
      <active>1</active>
      <approval>not requested</approval>
      <assigned_to>46c6f9efa9fe198101ddf5eed9adf6e7</assigned_to>
      <caller_id>46b673a6a9fe19810007ab03cbd5849d</caller_id>
      <category>network</category>
      <cmdb_ci>0c43f35dc61122750182c132a29e3243</cmdb_ci>
      <comments>Testing</comments>
      <contact_type>phone</contact_type>
      <due_date>2007-10-28 13:29:45</due_date>
      <escalation>0</escalation>
      <impact>3</impact>
      <incident_state>1</incident_state>
      <knowledge>0</knowledge>
      <location>1081761cc611227501d063fd3475a2de</location>
      <made_sla>1</made_sla>
      <notify>1</notify>
      <number>INC10055</number>
      <opened_at>2007-09-18 00:32:09</opened_at>
      <opened_by>46bac3d6a9fe1981005f299d979b8869</opened_by>
      <priority>0</priority>
      <reassignment_count>0</reassignment_count>
      <severity>0</severity>
    </getResponse>
  </soap:Body>
</soap:Envelope>
```

**Parent Topic:**[Data Retrieval API](r_DataRetrievalAPI.md)

