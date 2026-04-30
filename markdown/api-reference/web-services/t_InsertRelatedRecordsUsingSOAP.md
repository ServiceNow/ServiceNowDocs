---
title: Insert related records using SOAP
description: Support is available for inserting hierarchical data into tables or web service import set tables. The hierarchical data in the Insert API is automatically mapped to related records of the targeted table.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Insert related records using SOAP

Support is available for inserting hierarchical data into tables or web service import set tables. The hierarchical data in the Insert API is automatically mapped to related records of the targeted table.

## Before you begin

Role required: admin

## Procedure

1.  Create and set the property glide.web\_service.hierarchical to true.

    The client of the API can also override this value by invoking the SOAP web service with the URL parameter **hierarchical=true**.


## Example

For example, when a related list is created for the incident table called `u_custom_comments`:

![](../image/HierarchicalIncident.png "Hierarchical Incident")

And `u_comment_items` is created as a related list for `u_custom_comments`:

![](../image/HierarchicalCustomComments.png "Hierarchical Custom Comments")

-   **[WSDL Schema with related records](../reference/r_WSDLSchemaWithRelatedRecords.md)**  
When a WSDL for the target Incident table is requested with an additional parameter of **hierarchical=true**, the WSDL schema for the Insert function will reflect available related records that may participate in the hierarchical data payload.
-   **[Hierarchical SOAP Message](../reference/r_HierarchicalSOAPMessage.md)**  
When the SOAP message is constructed from the hierarchical web service described by the WSDL and invoked, it will create the `incident`, `u_custom_comments`, and `u_comment_items` records.

**Parent Topic:**[SOAP web service](../concept/c_SOAPWebService.md)

**Related topics**  


[WSDL Schema with related records](../reference/r_WSDLSchemaWithRelatedRecords.md)

[Hierarchical SOAP Message](../reference/r_HierarchicalSOAPMessage.md)

