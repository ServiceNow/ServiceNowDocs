---
title: Verify outbound network access for a private relay
description: Verify that the relay host machine can reach each Reverse Tunnel gateway host on the data port and the admin port.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/verify-relay-outbound-access.html
release: brazil
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [verify, Reverse Tunnel, private relay, ports, firewall]
breadcrumb: [Configure, Reverse Tunnel, Workflow Data Fabric]
---

# Verify outbound network access for a private relay

Verify that the relay host machine can reach each Reverse Tunnel gateway host on the data port and the admin port.

## Before you begin

-   The private relay must be registered with the instance, and gateways must appear in the **Gateways** field of the relay record.
-   Outbound firewall rules must permit the relay host machine to connect to each gateway host on its data port and admin port. For the purpose of each port, see [Reverse Tunnel architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/reverse-tunnel-architecture.md).
-   PowerShell on a Windows host machine or a terminal on a Linux host machine must be available.

Role required: sn\_zc\_tunnel.relay\_manager

## About this task

Each check tests the connection to a host and port and reports whether the connection succeeded. The check doesn't send data. The commands use `Test-NetConnection` on Windows and netcat \(`nc`\) on Linux, but you can use a different connectivity tool.

The relay connects to multiple gateway hosts, so each gateway host requires two checks, one for the data port and one for the admin port.

## Procedure

1.  Navigate to **All** &gt; **Private Relay** &gt; **Relays**.

2.  Open the relay record.

3.  Open each gateway record in the **Gateways** field and note the **Controller**, **Data Port**, and **Admin Port** values.

    The Controller value is the gateway host. Use only the hostname, without the `https://` prefix.

4.  Open a command shell on the relay host machine.

    -   On Windows, open PowerShell.
    -   On Linux, open a terminal.
5.  For each gateway host, test the connection on the data port and the admin port.

    **Note:** Replace *gateway-host* with the hostname from a Controller value. If the data port or admin port values in the record differ from 4281 and 4290, use the values from the record.

    On Windows, run the following commands:

    ```
    Test-NetConnection -ComputerName <gateway-host> -Port 4281
    Test-NetConnection -ComputerName <gateway-host> -Port 4290
    ```

    On Linux, run the following commands:

    ```
    nc -zv <gateway-host> 4281
    nc -zv <gateway-host> 4290
    ```

    For example, a relay with two gateway hosts requires the following commands:

    Windows:

    ```
    Test-NetConnection -ComputerName <gateway-host-1> -Port 4281
    Test-NetConnection -ComputerName <gateway-host-1> -Port 4290
    Test-NetConnection -ComputerName <gateway-host-2> -Port 4281
    Test-NetConnection -ComputerName <gateway-host-2> -Port 4290
    ```

    Linux:

    ```
    nc -zv <gateway-host-1> 4281
    nc -zv <gateway-host-1> 4290
    nc -zv <gateway-host-2> 4281
    nc -zv <gateway-host-2> 4290
    ```

6.  Review the output of each command.

    Each command reports whether the connection succeeded or failed.

    On Windows, a successful check ends with `TcpTestSucceeded : True`, as in the following example:

    ```
    ComputerName     : gateway-host.example.com
    RemoteAddress    : 192.0.2.50
    RemotePort       : 4281
    InterfaceAlias   : Ethernet
    SourceAddress    : 192.0.2.15
    TcpTestSucceeded : True
    ```

    On Linux, a successful check returns a message similar to the following example:

    ```
    Connection to gateway-host.example.com 4281 succeeded!
    ```


## Result

If every command reports success, the relay host machine can reach all gateway hosts.

If a command doesn't report success, the connection to that hostname and port failed. A failed connection can have several causes, including a missing or incorrect outbound firewall rule. Share the hostname and port with your network administrator.

## What to do next

Register backend services to the relay. For details, see [Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/connect-customer-relay.md).

