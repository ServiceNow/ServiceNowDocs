---
title: Create a static WSDL script include
description: Create a script include to define the majority of the code used to process static WSDL requests.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a scripted SOAP web service using a static WSDL, Scripted SOAP web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Create a static WSDL script include

Create a script include to define the majority of the code used to process static WSDL requests.

## Before you begin

Role required: script\_include\_admin or admin

## About this task

By implementing the majority of the custom functionality in a script include, you can reuse the script include in multiple areas.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Script Includes**.

2.  Click **New**.

3.  Enter a **Name** for the script include that matches the name of the static WSDL, such as FakeStockValue.

4.  Enter the script include code in the **Script** field.

5.  Click **Submit**.


-   **[Static WSDL script include example](../reference/r_StaticWSDLScriptInclude.md)**  
This example demonstrates the FakeStockValue script include that implements much of the static WSDL behavior.

**Parent Topic:**[Create a scripted SOAP web service using a static WSDL](../reference/createSOAPwebserviceStaticWSDL.md)

