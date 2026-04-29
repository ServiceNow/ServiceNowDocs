---
title: Microsoft .NET web services client examples
description: Examples demonstrating an integration with Microsoft .NET Web Services Client.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Microsoft .NET web services client examples

Examples demonstrating an integration with Microsoft .NET Web Services Client.

## Requirements

.NET 2.0 Versions and Higher:

-   An "elementFormDefault" value of qualified means that an unqualified element is in the default namespace defined on an ancestor. If it is "unqualified" then an unqualified element is in the empty namespace \(xmlns=""\). The default is "unqualified".
-   To Resolve the .NET Client deserialization failure you should go to **System Properties** &gt; **Web Services** and uncheck the property that sets the elementFormDefault attribute of the embedded XML schema to the value of unqualified. Save the property setting and recreate your WSDL Reference.cs class. See Also "Compatibility with Clients generated from WSDL" below.

![](../image/ElementFormDefaultProperty.png "Element Form Default Property")

**Parent Topic:**[Inbound web service examples](c_InboundWebServiceExamples.md)

