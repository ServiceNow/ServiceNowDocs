---
title: NTLM authentication
description: NTLM is the most complex of the authentication protocols supported by a basic web server.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Web proxy, Basic system configuration, Get started, Administer the ServiceNow AI Platform]
---

# NTLM authentication

NTLM is the most complex of the authentication protocols supported by a basic web server.

NTLM is the most complex of the authentication protocols supported by a basic web server such as [HttpClient](http://hc.apache.org/httpclient-3.x/). It is a proprietary protocol designed by Microsoft with no publicly available specification. Early versions of NTLM were less secure than Digest authentication due to faults in the design. However, these were fixed in a service pack for Windows NT 4 and the protocol is now considered more secure than Digest authentication.

NTLM authentication requires that an instance of NTCredentials be available for the domain name of the server or the default credentials. Since NTLM does not use the notion of realms, HttpClient uses the domain name of the server as the name of the realm. Also, the username provided to the NTCredentials should not be prefixed with the domain:

-   Correct: adrian
-   Incorrect: DOMAIN\\adrian

There are some significant differences in the way NTLM works compared with basic and digest authentication. These differences are generally handled by HttpClient. However, having an understanding of these differences can help you avoid problems when using NTLM authentication.

-   NTLM authentication works almost exactly the same as any other form of authentication in terms of the HttpClient API. The only difference is that you need to supply NTCredentials instead of UsernamePasswordCredentials \(NTCredentials actually extends UsernamePasswordCredentials so you can use NTCredentials right throughout your application, if needed\).
-   The realm for NTLM authentication is the domain name of the computer being connected. This can be troublesome because servers often have multiple domain names. Only the domain name that HttpClient connects to, as specified by the HostConfiguration, is used to look up the credentials. While initially testing NTLM authentication, it is best to pass the realm in as null, which is used as the default.
-   NTLM authenticates a connection and not a request. So you need to authenticate every time a new connection is made and keeping the connection open during authentication is vital. For this reason, NTLM cannot be used to authenticate with both a proxy server and the web server, nor can NTLM be used with HTTP 1.0 connections or web servers that do not support HTTP keep-alives.

**Note:** Set these properties from the System Properties `[sys_properties]` table.

<table id="table_tm2_2nl_cr"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Examples

</th></tr></thead><tbody><tr><td>

glide.http.proxy\_ntusername

</td><td>

Specify the username used to authenticate the proxy server with NTLM authentication. -   Type: string
-   Default value: none

</td><td>

username

</td></tr><tr><td>

glide.http.proxy\_ntpassword

</td><td>

Specify the password used to authenticate the proxy server with NTLM authentication. -   Type: string
-   Default value: none

</td><td>

password

</td></tr><tr><td>

glide.http.proxy\_nthost

</td><td>

Specify the hostname used to authenticate the proxy server with NTLM authentication. -   Type: string
-   Default value: none

</td><td>

nthost

</td></tr><tr><td>

glide.http.proxy\_ntdomain

</td><td>

Specify the domain used to authenticate the proxy server with NTLM authentication. -   Type: string
-   Default value: none

</td><td>

DOMAIN

</td></tr></tbody>
</table>**Parent Topic:**[Web proxy](../concept/c_WebProxy.md)

