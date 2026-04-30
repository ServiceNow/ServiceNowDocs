---
title: Java Apache Axis2 web services client examples
description: Examples demonstrating an integration with Axis2 Version 1.4.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Inbound web service examples, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Java Apache Axis2 web services client examples

Examples demonstrating an integration with Axis2 Version 1.4.

## Requirements

-   An "elementFormDefault" value of qualified means that an unqualified element is in the default namespace defined on an ancestor. If it is "unqualified" then an unqualified element is in the empty namespace \(xmlns=""\). The default is "unqualified".
-   To Resolve the Axis Client deserialization failure you should go to **System Properties** &gt; **Web Services** and uncheck the property that sets the elementFormDefault attribute of the embedded XML schema to the value of unqualified. Save the property setting and regenerate your Axis2 client code if your client code was generated before changing this property.

    ![](../image/ElementFormDefaultProperty.png "Element Form Default Property")


-   **[Java Apache Axis2 web services client examples insert](c_JAAWbSrvcsClntExInst.md)**  
An example class to insert an incident record.
-   **[Java Apache Axis2 web services client examples update](c_JAAWbSrvcsClntExUpdt.md)**  
An example of an Axis Client program that calls the getKeys function to query all incidents where the category is Hardware.
-   **[Java Apache Axis2 web services client examples advanced](c_JAAWbSrvcsClntExAdv.md)**  
Examples showing how to construct and use an Axis2 client to consume a ServiceNow Web Service.

**Parent Topic:**[Inbound web service examples](c_InboundWebServiceExamples.md)

