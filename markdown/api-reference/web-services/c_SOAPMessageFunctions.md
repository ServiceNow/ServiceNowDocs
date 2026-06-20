---
title: SOAP message functions
description: After you create a SOAP message record, you can click Generate sample SOAP messages to populate the SOAP Message Functions related list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/api-reference/web-services/c\_SOAPMessageFunctions.html
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SOAP message, Outbound SOAP web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# SOAP message functions

After you create a SOAP message record, you can click **Generate sample SOAP messages** to populate the SOAP Message Functions related list.

The instance creates these functions by reading the supplied WSDL definition.

\[Omitted image "SoapMessageFunction.png"\] Alt text:

The **SOAP action**, **SOAP endpoint**, and **Envelope** fields should be populated automatically based on the WSDL definition. The **Envelope** defines the message to send to the endpoint. In this example, the **Envelope** values have this format:

```
...
<!-- optional --><short_description xsi:type="xsd:string">String</short_description>
...
```

To submit a specific value, enter the value directly in the appropriate XML tag. In this example, to set the Short description for a record, enter:

```
...
<short_description xsi:type="xsd:string">This is the short description</short_description>
...
```

**Parent Topic:**[SOAP message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/api-reference/web-services/c_SOAPMessage.md)

