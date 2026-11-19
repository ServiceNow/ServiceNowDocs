---
title: WSDL Schema with related records
description: When a WSDL for the target Incident table is requested with an additional parameter of hierarchical=true, the WSDL schema for the Insert function will reflect available related records that may participate in the hierarchical data payload.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/api-reference/web-services/r\_WSDLSchemaWithRelatedRecords.html
release: yokohama
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Insert related records using SOAP, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# WSDL Schema with related records

When a WSDL for the target Incident table is requested with an additional parameter of **hierarchical=true**, the WSDL schema for the Insert function will reflect available related records that may participate in the hierarchical data payload.

For example, the insert portion of the schema of the incident table, when requested with **hierarchical=true** displays its hierarchy as follows:

`https://instance.service-now.com/incident.do?WSDL&hierarchical=true`

\[Omitted image "WSDLSchema.png"\] Alt text:

...

\[Omitted image "WSDLSchema2.png"\] Alt text:

The WSDL above shows the incident table having a related table `u_custom_comments` that itself has a related table `u_comment_items`.

**Parent Topic:**[Insert related records using SOAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/api-reference/web-services/t_InsertRelatedRecordsUsingSOAP.md)

