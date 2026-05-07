---
title: Configure the Password Reset Windows Application to use a proxy server
description: The Password Reset Windows Application supports the use of a proxy server. There are three options for configuring the proxy server.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [Installing and configuring Password Reset Windows Application, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure the Password Reset Windows Application to use a proxy server

The Password Reset Windows Application supports the use of a proxy server. There are three options for configuring the proxy server.

## Before you begin

Role required: Windows system administrator

## Procedure

1.  Use any one of the following configuration options to enable the Password Reset Windows Application to use a proxy server.

    |Options|Configuration|
    |-------|-------------|
    |**Option 1**|Configure registry keys. For more information, see [Configure registry keys on your proxy server](win-proxy-registry-password-reset.md).|
    |**Option 2**|Configure an exception policy on your proxy server to allow unauthenticated access to the **service-now.com** domain. For more information, see [Configure an exception policy on your proxy server](win-proxy-exception-password-reset.md).|
    |**Option 3**|Configure all Windows clients that use the Password Reset Windows Application to pass valid credentials to the proxy server. For more information, see [Configure a proxy server using client credentials method](win-proxy-cfg-clients-password-reset.md).|
    |**Option 4**|Configure the Proxy Auto-Configuration \(PAC\) file or Windows proxy auto detection \(WPAD\) using the Internet Explorer \(IE\) settings. For more information, see [Configure a proxy server using PAC file \(automatic configuration script method\)](win-proxy-server-pac-file-password-reset.md).|


-   **[Configure an exception policy on your proxy server](win-proxy-exception-password-reset.md)**  
You can configure an exception policy on your proxy server to allow unauthenticated access to the **service-now.com** domain.
-   **[Configure a proxy server using client credentials method](win-proxy-cfg-clients-password-reset.md)**  
If you cannot configure an exception policy, you must configure all Windows clients that use the Password Reset Windows Application to pass valid credentials to the proxy server.
-   **[Configure registry keys on your proxy server](win-proxy-registry-password-reset.md)**  
You can configure registry keys to enable the Password Reset Windows Application to use a proxy server.
-   **[Configure a proxy server using PAC file \(automatic configuration script method\)](win-proxy-server-pac-file-password-reset.md)**  
Configure the Proxy Auto-Configuration \(PAC\) file or Windows proxy auto detection \(WPAD\) using the Internet Explorer \(IE\) settings.

**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

