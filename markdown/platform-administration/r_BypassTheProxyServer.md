---
title: Bypass the proxy server
description: Administrators can configure the instance to bypass the proxy server for specific URLs or URL patterns.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Web proxy, Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Bypass the proxy server

Administrators can configure the instance to bypass the proxy server for specific URLs or URL patterns.

Typically, internal addresses do not need a proxy server for SOAP communications.

<table id="table_b2k_y4l_cr"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

glide.http.proxy\_bypass\_list

</td><td>

Specify the semicolon-separated list of addresses that bypass the proxy server. Use an asterisk as a wildcard character to specify all or part of an address. -   Type: string
-   Default value: none
-   Location: System Properties `[sys_properties]` table

</td><td>

127.0.0.1;\*.internal.com;localhost

</td></tr></tbody>
</table>**Parent Topic:**[Web proxy](../concept/c_WebProxy.md)

