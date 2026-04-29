---
title: Configure a proxy server using PAC file \(automatic configuration script method\)
description: Configure the Proxy Auto-Configuration \(PAC\) file or Windows proxy auto detection \(WPAD\) using the Internet Explorer \(IE\) settings.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Password Reset Windows Application to use a proxy server, Installing and configuring Password Reset Windows Application, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a proxy server using PAC file \(automatic configuration script method\)

Configure the Proxy Auto-Configuration \(PAC\) file or Windows proxy auto detection \(WPAD\) using the Internet Explorer \(IE\) settings.

## Before you begin

Role required: Windows system administrator

## About this task

The Password Reset Windows Application internal classes automatically pick the configuration that is done using **Use automatic configuration script** at the Internet Explorer level. If you configure the proxy at Internet Explorer, level all the changes done at a remote proxy level are applicable in the Password Reset Windows Application as well.

## Procedure

1.  On the Internet Explorer Tools menu, select **Internet options**.

2.  On the **Connections** tab, click **LAN settings**.

    ![Internet options](../image/Internet-options.png)

3.  Select the **Use automatic configuration script** check box.

    ![Use automatic configuration script](../image/lan.png)

4.  In the **Address** field, enter the PAC file location on the network.

5.  Click **OK**.


-   **[PAC file with registry setting](../reference/win-pac-file-with-registry-setting.md)**  
In this proxy configuration, the Proxy Auto-Configuration \(PAC\) file can be configured in Password Reset Windows Application registry settings.

**Parent Topic:**[Configure the Password Reset Windows Application to use a proxy server](win-config-proxy-server-password-reset.md)

