---
title: WSDL Schema with related records
description: When a WSDL for the target Incident table is requested with an additional parameter of hierarchical=true, the WSDL schema for the Insert function will reflect available related records that may participate in the hierarchical data payload.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Insert related records, SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# WSDL Schema with related records

When a WSDL for the target Incident table is requested with an additional parameter of **hierarchical=true**, the WSDL schema for the Insert function will reflect available related records that may participate in the hierarchical data payload.

For example, the insert portion of the schema of the incident table, when requested with **hierarchical=true** displays its hierarchy as follows:

`https://instance.service-now.com/incident.do?WSDL&hierarchical=true`

WSDL Schema

```
<xsd:element name="insert">
  – <xsd:complexType>
    – <xsd:sequence>
        <xsd:element maxOccurs="1" minOccurs="0" name="active" type="xsd:boolean"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="activity_due" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="approval" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="approval_history" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="approval_set" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="assigned_to" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="assignment_group" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="business_duration" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="business_stc" type="xsd:integer"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="calendar_duration" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="calendar_stc" type="xsd:integer"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="caller_id" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="category" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="caused_by" type="xsd:string"/>
```

WSDL Schema Continued:

```
<xsd:element maxOccurs="1" minOccurs="0" name="watch_list" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="work_end" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="work_notes" type="xsd:string"/>
        <xsd:element maxOccurs="1" minOccurs="0" name="work_start" type="xsd:string"/>
      – <xsd:element minOccurs="0" name="u_custom_comments">
          – <xsd:complexType>
              – <xsd:sequence>
                    <xsd:element maxOccurs="1" minOccurs="0" name="u_comment" type="xsd:string"/>
                    <xsd:element maxOccurs="1" minOccurs="0" name="u_comment_type" type="xsd:string"/>
                    <xsd:element maxOccurs="1" minOccurs="0" name="u_incident" type="xsd:string"/>
                  – <xsd:element minOccurs="0" name="u_comment_items">
                      – <xsd:complexType>
                          – <xsd:sequence>
                                <xsd:element maxOccurs="1" minOccurs="0" name="u_comment" type="xsd:string"/>
                                <xsd:element maxOccurs="1" minOccurs="0" name="u_name" type="xsd:string"/>
                                <xsd:element maxOccurs="1" minOccurs="0" name="u_value" type="xsd:string"/>
                            </xsd:sequence>
                        </xsd:complexType>
                    </xsd:element>
                </xsd:sequence>
            </xsd:complexType>
        </xsd:element>
      </xsd:sequence>
    </xsd:complexType>
  </xsd:element>
</xsd:sequence>
</xsd:complexType>
</xsd:element>
```

**Parent Topic:**[Insert related records using SOAP](../task/t_InsertRelatedRecordsUsingSOAP.md)

