---
title: Configure the IP address deny list
description: Prevent an IP address in your network from sending requests to your instance
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring Edge Encryption, Edge Encryption, Encryption]
---

# Configure the IP address deny list

Prevent an IP address in your network from sending requests to your instance

## Before you begin

Role required: security\_admin

Because the Edge Encryption proxy server resides in your network, it may be subject to vulnerability scans by your network software. To prevent IP scanner or other requests from being forwarded to your ServiceNow instance, you can add IP addresses, IP ranges, or network masks to a deny list. Any connection to the proxy server from a deny listed address is terminated and is not forwarded to your instance.

To place an IP address on a deny list, you must be logged in to your instance through the proxy server.

**Important:** Ensure that you understand your network topology before adding IP addresses in your network to a deny list. If an IP address is added to the deny list, any user with that IP address will be blocked from accessing the Edge Encryption proxy server.

## Procedure

1.  Navigate to **All** &gt; **Edge Encryption Configuration** &gt; **Maintenance** &gt; **Denylist IP Addresses**.

    The Encryption Proxy IP Denylists \[edge\_encryption\_ip\_blacklist\] list view opens.

2.  Click **New**.

3.  Complete the form.

<table id="table_l5k_rmz_y1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Proxy server

</td><td>

The Edge Encryption proxy server that is prevented from forwarding requests from addresses on the deny list.

</td></tr><tr><td>

IP, IP range, or net-mask

</td><td>

Requests from this IP address, range, or network mask are not forwarded to your ServiceNow instance. Example values include:-   IP address: 10.10.10.5
-   IP range: 10.10.10.1-15
-   Network mask: 10.10.10.0/24
 **Note:** You may use either IPv4 or IPv6 addresses

</td></tr><tr><td>

Active

</td><td>

Whether the record is active. Only IP addresses from active records are prevented from sending requests to the instance.

</td></tr><tr><td>

Description

</td><td>

Description of the deny list record.

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Repeat these steps for all other proxies for which an IP address should be denied.


## Result

The Edge Encryption proxy server terminates any connection from IP addresses, ranges, or network masks on the deny list and cannot forward the request to the instance.

**Parent Topic:**[Configuring Edge Encryption](../concept/edge-config.md)

