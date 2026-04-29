---
title: Prevent empty elements in SOAP messages
description: By default, an instance does not omit empty elements, elements with NULL or NIL values, from SOAP messages.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [SOAP web service, Inbound, Web services, API implementation, API implementation and reference]
---

# Prevent empty elements in SOAP messages

By default, an instance does not omit empty elements, elements with NULL or NIL values, from SOAP messages.

To prevent SOAP responses from containing empty elements, an administrator can create a system property called **glide.soap.omit\_null\_values** and set the value to **true**. This behavior is compliant with the WSDL as all elements in a SOAP message have a minOccurs=0 attribute and are therefore optional. In addition, this behavior prevents the instance from creating inefficient SOAP messages containing a large number of empty elements.

Set this property to **false** to allow SOAP messages to search for existing fields with empty values. For example, if an administrator wants to search for incidents with an empty **Assigned to** field from a SOAP message, then the SOAP message must be able to send an empty value for this field.

**Note:** Changing the value of this property may cause unintended actions in existing web service integrations. Administrators are strongly encouraged to carefully test the new behavior to ensure that existing integrations process empty elements as expected.

**Parent Topic:**[SOAP web service](c_SOAPWebService.md)

