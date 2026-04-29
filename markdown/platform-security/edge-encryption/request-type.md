---
title: Inspect the client request
description: Before creating a custom encryption rule, you must determine the format of the client request entering the Edge Encryption proxy server.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Define a custom encryption rule, Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Inspect the client request

Before creating a custom encryption rule, you must determine the format of the client request entering the Edge Encryption proxy server.

## Before you begin

Role required: admin

## About this task

Because encryption rules iterate over client requests and determine what, if anything, needs to be encrypted, you must understand the type of request you are creating a rule for. The format of the client request determines the structure of your encryption rule and the APIs available for use in the rule.

## Procedure

1.  Inspect the client request.

    Depending on the source of the request, the following tools are available to inspect the request and determine the format.

<table id="table_umt_q5y_rz"><thead><tr><th>

Source of request

</th><th>

Available tools

</th></tr></thead><tbody><tr><td>

Client browser

</td><td>

Use the developer console in your browser to inspect the client request. Useful tools include:

 -   [Firefox Network Monitor](https://developer.mozilla.org/en-US/docs/Tools/Network_Monitor)

-   [Chrome Network Panel](https://developers.google.com/web/tools/chrome-devtools/network-performance/resource-loading)

</td></tr><tr><td>

Third-party/external source

</td><td>

Use an HTTP protocol analyzer to inspect the request. Useful tools include:

 -   [Wireshark](https://www.wireshark.org/)
-   HTTP Scoop
 Alternatively, you can often use documentation for the external source to determine the format of the request.

</td></tr></tbody>
</table>2.  From the client request, inspect the packet and determine:

    -   The client request method
    -   The URL path of the request
    -   The URL parameters
    -   The POST parameters, if any
    -   The format of the request body, if included
    ![Example](../images/client-request.png)


## Result

Inspecting the request provides an understanding of the fields you need to filter for and iterate over in your encryption rule. To understand the fields in the request object, see [request](../concept/c_requestAPI.md#).

**Parent Topic:**[Define a custom encryption rule](../concept/c_EncryptionRules.md)

