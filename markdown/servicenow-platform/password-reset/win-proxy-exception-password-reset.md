---
title: Configure an exception policy on your proxy server
description: You can configure an exception policy on your proxy server to allow unauthenticated access to the service-now.com domain.
locale: en-US
release: australia
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configure the Password Reset Windows Application to use a proxy server, Installing and configuring Password Reset Windows Application, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure an exception policy on your proxy server

You can configure an exception policy on your proxy server to allow unauthenticated access to the **service-now.com** domain.

## Before you begin

Role required: Windows system administrator

## Procedure

1.  On a machine in the network, back up the following registry key: `HKEY_USERS\.DEFAULT\Software\Microsoft\Windows\CurrentVersion\Internet Settings`

2.  Download and install the Sysinternals Suite from `https://technet.microsoft.com/en-us/sysinternals/bb842062.aspx`

3.  At the command prompt, navigate to the extracted `sysinternals` folder.

4.  Run the following command to launch Internet Explorer:

    `psexec -s -i "C:\Program Files\Internet Explorer\iexplore.exe"`

5.  On the Internet Explorer **Tools** menu, select **Internet options**.

6.  On the **Connections** tab, click **LAN settings**.

7.  In the **Proxy server** section, select **Use a proxy server for your LAN** and then fill in the **Address** field using the following format: `<proxy_server>:<port>`

8.  Click **OK** to close the **LAN Settings** page and then click **OK** to close **Internet options**.

9.  Export the following registry key to all clients that use the Password Reset Windows Application:`HKEY_USERS\.DEFAULT\Software\Microsoft\Windows\CurrentVersion\Internet Settings`


**Parent Topic:**[Configure the Password Reset Windows Application to use a proxy server](win-config-proxy-server-password-reset.md)

