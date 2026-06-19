---
title: Configure C sharp with .NET
description: Configure web services within ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/web-services/t\_ConfigureCSharpWith.NET.html
release: australia
product: Web Services
classification: web-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [.NET tutorial, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Configure C sharp with .NET

Configure web services within ServiceNow.

## Procedure

1.  To configure web services within ServiceNow, access the **System Properties** &gt; **Web Services** module.

    This module displays the system properties that are specific to web services within your instance. For security reasons, you will want to make sure that you require basic authorization for incoming SOAP requests. This ensures that only authenticated users will be able to make any web services calls, whether it be via web service import sets or inserting/deleting/querying via direct web services.

    \[Omitted image "WebServicesPropertiesTop.png"\] Alt text: Web services properties top

2.  This next step is very important if you are using .NET as a client to connect to ServiceNow. You must set the **elementFormDefault** property to false.

    This property defines how the WSDLs are qualified. Of course, if you do not consume our WSDL and just create the XML manually, then this property is irrelevant.

    \[Omitted image "ElementFormDefaultProperty.png"\] Alt text: Element form default property


**Parent Topic:**[Web services C Sharp .NET end to end tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/c_CSharpNETEndEnd.md)

