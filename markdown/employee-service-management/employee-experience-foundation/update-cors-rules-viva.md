---
title: Allow cross-domain requests to REST APIs
description: Allow cross-domain requests to REST APIs from a browser-based application in a different domain by creating a record in CORS rules through the Microsoft Viva Connections Integration application scope.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Employee Center for Microsoft Viva Connections, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Allow cross-domain requests to REST APIs

Allow cross-domain requests to REST APIs from a browser-based application in a different domain by creating a record in CORS rules through the Microsoft Viva Connections Integration application scope.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **CORS Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_zxz_qzb_gyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the CORS rule.

</td></tr><tr><td>

Application

</td><td>

Application containing the associated CORS record. This field is automatically set to Employee Center for Microsoft Viva Connections.

</td></tr><tr><td>

REST API

</td><td>

The REST API this CORS rule applies to. Enter `Microsoft VIVA Integration [sn_now_ms_viva/viva]`.

</td></tr><tr><td>

Domain

</td><td>

The domain that this CORS rule applies to. Enter `https://{tenantName}.sharepoint.com`. For example, https://nowhkconnect.sharepoint.com.This CORS rule is evaluated against requests from the specified domain. You can specify a domain pattern or an IP address.

</td></tr><tr><td>

Max age

</td><td>

The number of seconds to cache the client session. After an initial CORS request, further requests from the same client within the specified time do not require a preflight message. If you do not specify a value, the default value of 0 indicates that all requests require a preflight message.

</td></tr><tr><td>

HTTP Methods tab

</td><td>

The HTTP methods allowed.Only the selected methods can be called from the specified domain. The available methods are:

-   **GET**
-   **POST**
-   **PUT**
-   **PATCH**
-   **DELETE**


</td></tr><tr><td class="sub-head" colspan="2">

HTTP Headers tab

</td></tr><tr><td>

Exposed headers

</td><td>

List of headers that the browser is allowed to access from the request.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Configuring Employee Center for Microsoft Viva Connections](../concept/configure-viva.md)

