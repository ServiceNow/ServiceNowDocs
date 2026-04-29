---
title: Install the Edge Encryption proxy server \(interactive installer\)
description: Install the Edge Encryption proxy on a Windows or Linux computer.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Install the Edge Encryption proxy server \(interactive installer\)

Install the Edge Encryption proxy on a Windows or Linux computer.

## Before you begin

Role required: admin

## Procedure

1.  [Download the Edge Encryption proxy server installer](t_DownloadtheProxy.md).

2.  Open the Edge Encryption proxy installer.

    **Note:** If installing on a Windows machine, you must run the installer as Administrator.

    1.  To run the installer as Administrator on a Windows machine, right-click the Command Prompt and select **Run as administrator**.

    2.  From the command line, navigate to the directory that contains the downloaded .jar file.

    3.  Run the following command: `java -jar <file name>.jar`.

    ![ServiceNow Edge Encryption proxy installer](../images/Madrid-Edge-Installer-1.png "ServiceNow Edge Encryption proxy installer")

3.  To install a new proxy server, select **Install New**.

    If a proxy is already installed, you can run the installer to:

    -   **Verify Installation**: Perform tests to detect and fix issues in a previous installation.
    -   **Reinstall Existing**: Perform tests to detect and fix issues in a previous installation and view or modify existing settings.
4.  Configure the **Installation Location** and **Target ServiceNow Instance**.

    1.  Click **Browse** to select an installation location or manually enter an installation path.

    2.  Enter the URL of the target ServiceNow instance.

        Include the protocol and port number.

        `https://example.servicenow.com:443`

    3.  Enter the user name and password for a user with the edge\_encryption role on the target ServiceNow instance.

5.  Click **Next**.

6.  Configure the **Connection Settings** and **Proxy Settings**.

<table id="table_lrb_pz4_2z"><thead><tr><th>

Setting

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Proxy Host

</td><td>

Fully qualified domain name of the machine on which you are installing the proxy server.**Note:** Click **Detect FQDN** to look up the machine's fully qualified domain name and auto-populate the **Proxy Host** field.

 Along with the port, this property defines the URL used by the client to access the proxy server.

</td></tr><tr><td>

HTTP Port

</td><td>

Port on the proxy for HTTP communication.

</td></tr><tr><td>

HTTPS Port

</td><td>

Port on the proxy for HTTPS communication.

</td></tr><tr><td>

Proxy Name

</td><td>

Name of the proxy and the service. The proxy name must be unique.

</td></tr><tr><td>

Proxy Poll Interval

</td><td>

Poll interval in seconds. With the default setting, it takes 5 seconds for the proxy to learn of encryption configuration changes. Larger values cause the instance to take longer to detect proxies that have come online. **Note:** Changing the default setting of the Proxy Poll Interval can result in detection delays when a proxy comes online.

</td></tr><tr><td>

Proxy Keep-Alive Ping Interval

</td><td>

Time in seconds between pings issued by the proxy to the instance. Pings are issued periodically to verify connectivity between the proxy and the instance. The default value is 10. The minimum value is 5.

</td></tr></tbody>
</table>7.  Click **Install**.

    The Edge Encryption proxy server installs. The installation may take a few minutes.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Next topic:**[Configure CyberArk properties protection](configure-cyberark-prop-protection.md)

