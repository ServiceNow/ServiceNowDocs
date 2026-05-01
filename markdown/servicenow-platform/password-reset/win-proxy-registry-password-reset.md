---
title: Configure registry keys on your proxy server
description: You can configure registry keys to enable the Password Reset Windows Application to use a proxy server.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Configure the Password Reset Windows Application to use a proxy server, Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure registry keys on your proxy server

You can configure registry keys to enable the Password Reset Windows Application to use a proxy server.

## Before you begin

Role required: Windows system administrator

## About this task

If you choose not to use the method described in this topic, there are other methods to configure a proxy server:

-   Configure an exception policy on your proxy server to allow unauthenticated access to the **service-now.com** domain. See [Configure an exception policy on your proxy server](win-proxy-exception-password-reset.md).
-   Configure all Windows clients that use the Password Reset Windows Application to pass valid credentials to the proxy server. See [Configure a proxy server using client credentials method](win-proxy-cfg-clients-password-reset.md).

## Procedure

1.  Open the Registry Editor on your Windows computer.

2.  Go to **Computer** &gt; **HKEY\_LOCAL\_MACHINE** &gt; **SOFTWARE** &gt; **Microsoft** &gt; **Windows** &gt; **CurrentVersion** &gt; **Authentication** &gt; **Credential Providers** &gt; **0780AF60-65C2-4718-942D-E0C56E89EF9B**.

3.  Set the following registry keys:

    **Note:** You can modify any of the listed string values.

    ```
    "ProxyServer"="<YourProxyName>:<PortNumber>"
    "ProxyEnable"="true"
    "ProxyUser"="<YourProxyUserName>"
    "ProxyPassword"="<YourProxyPassword>"
    "ProxyDomainName"="<YourProxyDomainName>"
    "ByPassProxyOnLocal"="false"
    ```

    -   ProxyServer: Set the proxy server name or IP address with port
    -   ProxyUser: User name associated with the credentials, in case proxy is enabled with basic authentication
    -   ProxyPassword: Password for the user name associated with the credentials
    -   ProxyDomainName: Domain name that verifies the credentials
    -   ByPassProxyOnLocal: Set to true if you want to bypass a proxy server for local calls.

**Parent Topic:**[Configure the Password Reset Windows Application to use a proxy server](win-config-proxy-server-password-reset.md)

