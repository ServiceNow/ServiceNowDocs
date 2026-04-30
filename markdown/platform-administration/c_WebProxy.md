---
title: Web proxy
description: Several properties support Web proxy configuration.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# Web proxy

Several properties support Web proxy configuration.

**Note:** Set these properties in the System Properties `[sys_properties]` table.

<table id="table_iyk_qll_cr"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

glide.http.proxy\_host

</td><td>

Specify the proxy server hostname or IP address. -   Type: string
-   Default value: none

</td><td>

proxy.company.com, 192.168.34.54

</td></tr><tr><td>

glide.http.proxy\_port

</td><td>

Specify the port number for the proxy server. -   Type: string
-   Default value: none

</td><td>

8080, 9100

</td></tr><tr><td>

glide.http.proxy\_username

</td><td>

Specify the username used to authenticate the proxy server. -   Type: string
-   Default value: none

</td><td>

proxyuser

</td></tr><tr><td>

glide.http.proxy\_password

</td><td>

Specify the password used to authenticate the proxy server. -   Type: string
-   Default value: none

</td><td>

password

</td></tr><tr><td>

glide.email.override.url

</td><td>

Set the URL to use in emailed links in place of the instance URL. The URL should end with `nav_to.do`.-   Type: string
-   Default value: instance URL

</td><td>

https://servicenow.customerdomain.com/production/nav\_to.do

</td></tr></tbody>
</table>-   **[NTLM authentication](../reference/r_NTLMAuthentication.md)**  
NTLM is the most complex of the authentication protocols supported by a basic web server.
-   **[Proxy servers for SOAP clients](c_ProxyServersForSOAPClients.md)**  
Administrators can specify separate proxy settings for SOAP clients, such as the MID Server or ODBC Driver.
-   **[Bypass the proxy server](../reference/r_BypassTheProxyServer.md)**  
Administrators can configure the instance to bypass the proxy server for specific URLs or URL patterns.

**Parent Topic:**[Basic system configuration](../../core-configuration/concept/p_CoreConfigurationOverview.md)

