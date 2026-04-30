---
title: REST message elements
description: An outbound REST message is composed of several elements, such as the endpoint and HTTP methods.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST, Outbound, Web services, API implementation, API implementation and reference]
---

# REST message elements

An outbound REST message is composed of several elements, such as the endpoint and HTTP methods.

A REST message contains the following elements:

<table id="table_ml1_pt1_5s"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Endpoint

</td><td>

The endpoint is the URL of the data to be retrieved, updated, or deleted. Every REST message must specify an endpoint.

</td></tr><tr><td>

Headers

</td><td>

HTTP headers in REST messages contain information about the request, such as the desired response format. A REST message may specify any number of headers.

</td></tr><tr><td>

Authentication settings

</td><td>

Authentication settings include which type of authentication to use, such as basic auth or OAuth, as well as the credentials to use.

</td></tr><tr><td>

HTTP methods

</td><td>

HTTP methods, such as GET, POST, or DELETE interact with the data at the endpoint. You can optionally override the parent REST message configuration in each HTTP method such as by specifying a different endpoint, authentication credentials, or headers.

 HTTP methods that send content, such as POST, include a message body detailing this content.

 A REST message may specify multiple HTTP methods. When sending a REST message, such as through a workflow activity or script, you must specify which HTTP method to use.

</td></tr></tbody>
</table>**Parent Topic:**[Outbound REST web service](../concept/c_OutboundRESTWebService.md)

