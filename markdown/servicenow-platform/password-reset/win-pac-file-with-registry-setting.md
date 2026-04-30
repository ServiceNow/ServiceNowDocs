---
title: PAC file with registry setting
description: In this proxy configuration, the Proxy Auto-Configuration \(PAC\) file can be configured in Password Reset Windows Application registry settings.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a proxy server using PAC file \(automatic configuration script method\), Configure the Password Reset Windows Application to use a proxy server, Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# PAC file with registry setting

In this proxy configuration, the Proxy Auto-Configuration \(PAC\) file can be configured in Password Reset Windows Application registry settings.

The name of the registry setting enables the proxy via PAC file is **UseProxyAutoConfigScript**. The PAC script location \(URL\) can be provided in the **ProxyServer** setting. The reference configuration is provided as shown in the following image:![PAC registry settings](../image/pac-registry-settings2.png)

## Registry setting to configure proxy via PAC

-   ProxyEnable – &lt;true&gt;

    Enables the proxy on application level.

-   ProxyServer – &lt;PAC file URL&gt;

    Initialize the PAC file location here.

-   UseProxyAutoConfigScript – &lt;true&gt;

    If set to true, it indicates that the address provided in the **ProxyServer** registry setting is PAC script.


## How it works

The PAC file provided in the **ProxyServer** registry setting is used to get the actual target proxy server address for a URL \(In this case, the ServiceNow instance\) based on the PAC file script configuration. The PAC file script must return a valid Proxy server address for a provided ServiceNow URL to make the application work.

The target proxy address is cached for a URL in the machine. The caching behavior is applicable for the browsers as well. The ServiceNow® Password Reset Windows Application behaves the same as the Internet Explorer browser. That is, if the URL is accessible via a browser, then it's accessible via the app as well.

**Note:** It is not necessary to configure the proxy setting in Internet Explorer as the APP is reading the PAC file script via a registry.

**Parent Topic:**[Configure a proxy server using PAC file \(automatic configuration script method\)](../task/win-proxy-server-pac-file-password-reset.md)

