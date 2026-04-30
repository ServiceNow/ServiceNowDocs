---
title: Hierarchical SOAP Message
description: When the SOAP message is constructed from the hierarchical web service described by the WSDL and invoked, it will create the incident, u\_custom\_comments, and u\_comment\_items records.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Insert related records, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Hierarchical SOAP Message

When the SOAP message is constructed from the hierarchical web service described by the WSDL and invoked, it will create the `incident`, `u_custom_comments`, and `u_comment_items` records.

## Endpoint URL

`https://instance.service-now.com/incident.do?SOAP&hierarchical=true`

## Request

```
<soapenv:Envelope
    xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <inc:insert>
         <short_description>test hierarchical</short_description>
         <u_custom_comments>
            <u_comment>comment 1</u_comment>
            <u_comment_type>travel</u_comment_type>
            <u_comment_items>
               <u_name>name 1</u_name>
               <u_value>value 1</u_value>
            </u_comment_items>
         </u_custom_comments>
      </inc:insert>
   </soapenv:Body>
</soapenv:Envelope>
```

## Reponse

```
<soapenv:Envelope 
    xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" 
    xmlns:inc="http://www.service-now.com/incident">
   <soapenv:Header/>
   <soapenv:Body>
      <insertResponse>
         <sys_id>8422ebe7c0a8006e7d23848c2dc8ba47</sys_id>
         <number>INC0010001</number>
      </insertResponse>
   </soapenv:Body>
</soapenv:Envelope>
```

**Parent Topic:**[Insert related records using SOAP](../task/t_InsertRelatedRecordsUsingSOAP.md)

