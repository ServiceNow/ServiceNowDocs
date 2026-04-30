---
title: Configure a MID Server for IPv6
description: A MID Server configured for IPv6 can connect to ServiceNow and use Discovery over IPv6 for specific addresses.
locale: en-US
release: yokohama
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Configure a MID Server for IPv6

A MID Server configured for IPv6 can connect to ServiceNow and use Discovery over IPv6 for specific addresses.

## Before you begin

Role required: admin

<table id="table_kzy_tbj_35b"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>## About this task

A pure IPv6 MID Server does not need to be configured for IPv6. It connects to IPv6 by default, and the **ecc\_agent** record for the MID Server is automatically populated with IPv6. Contact Support to ensure your instance is IPv6 enabled.

On a dual stack host, the MID Server defaults to using IPv4. The following procedure configures a dual stack MID Server to use IPv6. The following tables are automatically updated during upgrade to Tokyo to support IPv4 and IPv6:

-   **ecc\_agent**
-   **ecc\_agent\_router**
-   **ecc\_agent\_ip\_address**
-   **ecc\_agent\_command\_audit\_log**

When using Discovery over IPv6, the following requirements apply:

-   **Windows Discovery**

    Only WinRM is supported as of the Yokohama release. The requirements for WinRM over IPv6 are the same as IPv4. WinRM must be running on both the MID Server host and target, and the target must be configured as a trusted host on that MID Server.

-   **Unix Discovery**

    Only SNC SSH is supported as of the Yokohama release. No additional configuration is needed to use SNC SSH over IPv6. J2SSH and Maverick are not supported but, if their protocols are used over IPv6, the command is executed without guaranteeing the correct results. In that case, the following error message is reported in the MID Server logs: `IPv6 is currently not supported for MID Server using Maverick (J2SSH), however the command will be executed.`


## Procedure

1.  Navigate to the Java VM configuration wrapper in `agent/conf/wrapper-override.conf`.

2.  Open the file, then uncomment and change the following line of code to true:

    ```
    #wrapper.java.additional.109=-Djava.net.preferIPv6Addresses=false
    ```

    Change the previous line to read as follows:

    ```
    wrapper.java.additional.109=-Djava.net.preferIPv6Addresses=true
    ```

3.  Restart the MID Server.

    The MID Server is now configured to connect to the instance over IPv6.

    **Note:** For dual stack MID Servers, changing the wrapper does not affect the data populated in the **ecc\_agent** record, which is IPv4 by default.

4.  To update the **ecc\_agent** record to prefer IPv6 over IPv4, specify the following MID Server configuration parameter and set it to true: **mid.prefer\_ipv6\_addresses**.

5.  Restart the MID Server.

    The dual stack MID Server populates the relevant fields in the **ecc\_agent** record with IPv6 addresses. The tables **ecc\_agent\_router** and **ecc\_agent\_ip\_address** are populated with both IPv4 and IPv6 entries on a dual stack host.


