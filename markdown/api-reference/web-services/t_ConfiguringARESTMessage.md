---
title: Create a REST message
description: Send requests to a REST web service endpoint by creating a REST message record.
locale: en-US
release: yokohama
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Outbound REST web service, Outbound web services, Web services, API implementation, API implementation and reference]
---

# Create a REST message

Send requests to a REST web service endpoint by creating a REST message record.

## Before you begin

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

2.  Click **New**.

3.  Complete the following fields:

<table id="table_RestMessageForm"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a descriptive name for this message.

</td></tr><tr><td>

Endpoint

</td><td>

Enter the endpoint that this REST message is sent to. The endpoint value may include variables using the format **$\{variable\}**.

</td></tr><tr><td>

Authentication type

</td><td>

Select the type of authentication to use, if any, and the profile record that contains the user credentials. Outbound REST supports basic authentication and OAuth 2.0. Outbound REST supports mutual authentication with basic authentication only.

 Authentication configured here is inherited by the associated HTTP methods. You can configure authentication for each method which overrides any authentication setting at the message level.

</td></tr><tr><td>

HTTP Headers

</td><td>

Double-click a row in the **HTTP Headers** embedded list to define the header **Name** and **Value**.The web service provider determines which headers are supported or required.

</td></tr></tbody>
</table>4.  Click **Submit**.

    After creating the REST message, a GET HTTP method is created automatically using the values from the REST message record.


## What to do next

Create or edit HTTP methods and run a request.

-   **[Define a REST message HTTP method](t_DefineAnHTTPMethod.md)**  
Define an HTTP method such as GET or POST to send a request to a web service provider.
-   **[Define a REST message HTTP header](t_DefineAnHTTPHeader.md)**  
Define an HTTP header for a REST message or HTTP method to send that header with REST requests.
-   **[Sending outbound REST messages through a MID Server](../concept/c_OutboundRESTMIDServerSupport.md)**  
You can configure a REST message HTTP method to be sent through a MID Server.
-   **[Using special characters in URIs](../concept/c_UsingSpecialCharactersInURIs.md)**  
A REST function URI or function variable may use special characters, such as pipe \(\|\) characters.

**Parent Topic:**[Outbound REST web service](../concept/c_OutboundRESTWebService.md)

