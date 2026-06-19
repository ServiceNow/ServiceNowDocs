---
title: Microsoft .NET web services client examples
description: Examples demonstrating an integration with Microsoft .NET Web Services Client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_MS.NETWebServicesClientExamples.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Microsoft .NET web services client examples

Examples demonstrating an integration with Microsoft .NET Web Services Client.

## Requirements

.NET 2.0 Versions and Higher:

-   An "elementFormDefault" value of qualified means that an unqualified element is in the default namespace defined on an ancestor. If it is "unqualified" then an unqualified element is in the empty namespace \(xmlns=""\). The default is "unqualified".
-   To Resolve the .NET Client deserialization failure you should go to **System Properties** &gt; **Web Services** and uncheck the property that sets the elementFormDefault attribute of the embedded XML schema to the value of unqualified. Save the property setting and recreate your WSDL Reference.cs class. See Also "Compatibility with Clients generated from WSDL" below.

**Parent Topic:**[Inbound web service examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_InboundWebServiceExamples.md)

