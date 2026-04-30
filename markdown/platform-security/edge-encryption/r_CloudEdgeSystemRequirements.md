---
title: Edge Encryption system requirements
description: You can run the Edge Encryption proxy application on servers or virtual machines that run on Microsoft Windows or Linux operating systems. For optimum performance, ensure that your configuration meets these requirements.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Planning for Edge Encryption, Edge Encryption, Encryption]
---

# Edge Encryption system requirements

You can run the Edge Encryption proxy application on servers or virtual machines that run on Microsoft Windows or Linux operating systems. For optimum performance, ensure that your configuration meets these requirements.

## Java requirements

The host machine installing or running the Edge Encryption proxy server must maintain a supported version of Java. Current supported versions are Java 11.0.6 or later in the 11.x version series

**Note:** Java 8 is no longer be supported as of the Utah release. Upgrade your environment with the Edge Encryption proxy to Java 11 before you attempt to install the Utah version of the Edge Encryption proxy.

**Note:** Java does not automatically allow unlimited strength keys. You must specifically enable the use of AES 256-bit encryption.

## Support for OpenJDK

The ServiceNow AI Platform supports OpenJDK version 11.

## Proxy server minimum configuration

A proxy server requires this minimum configuration:

-   4 GB of RAM per proxy server \(6 GB is recommended for most deployments\).

    **Note:** The proxy server host requires at least 1 GB of RAM more than the proxy server. The proxy server host needs the extra 1 GB for operating system services. For example, if you configure a proxy server to use 4 GB of RAM, you must install at least 5 GB of RAM on the proxy server host.

    Because the proxy server requires at least 4 GB of memory, 32-bit JREs and 32-bit operating systems are no longer supported starting with the London release.

-   3 or more GHz CPU \(4-core CPU preferred for optimum performance\).
-   Multiple proxy servers behind a load balancer. The number of proxy servers you need depends on the number of application nodes, the number of simultaneous users, and the number of servers needed for failover. See [Sizing your Edge Encryption environment](../concept/edge-environment-size.md) for more information.
-   Ability to run concurrently with other services, depending on the server utilization and resource availability.

## Proxy server supported systems

The following systems are supported:

<table id="table_nj1_mhn_gfb"><thead><tr><th>

Supported System

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Windows Server 2012, 2012-R2, 2016, and 2019 editions

</td><td>

-   Virtual machines or physical hardware
-   64-bit systems

</td></tr><tr><td>

Linux

</td><td>

-   Virtual machines or physical hardware
-   64-bit systems

 On 64-bit Linux systems, you must install the 32-bit [GNU C library](http://www.gnu.org/software/libc/) \(glibc\). The installation command for CentOS is `yum install glibc.i686`.

</td></tr></tbody>
</table>## Proxy server version requirements

Keep your Edge Encryption proxy version in sync with your ServiceNow instance version \(same major release, for example Tokyo\). To eliminate downtime during the upgrade process, the Edge Encryption proxy is backwards compatible. However it is important to upgrade as soon as possible to avoid ensure users can access new features and important bug fixes.

## Proxy server connection requirements

The proxy server that runs the Edge Encryption application must be able to communicate with machines in your network. Make sure that the proxy server has these network privileges:

|Network Privilege|Description|
|-----------------|-----------|
|Firewall access|Configure any firewalls between the proxy server and the client devices to allow a connection. If your network uses a DeMilitarized Zone \(DMZ\) to add an extra layer of security to your Local Area Network \(LAN\), and if your network security protocols limit port access from within the network to the DMZ, you might have to deploy a proxy server to a machine within the DMZ.|
|Network access|Configure each client to enable the proxy server to connect with it. If network security prevents you from configuring new machines that can connect to the clients, install the proxy server on an existing machine with connection privileges.|
|Instance access|Ensure that the proxy server has network access to the instance. Make sure that you configure the proxy server network to allow traffic over TCP port 443.|
|Network account|Install the proxy server with either a local or domain administrator.|

## Order-preserving and tokenization database system requirements

Order-preserving encryption and encryption patterns require that you configure an Oracle MySQL database for the Edge Encryption proxy server. Order-preserving encryption allows any comparison operation to be directly applied on encrypted data, without first decrypting the data. Encryption patterns let you replace string patterns with tokens \(called tokenization\) before they are sent to and stored in the database. Because of the size of the MySQL database, use a dedicated proxy server to run the order-preserving and tokenization database.

The minimum database system requirements include:

<table id="table_rl3_zhn_gfb"><thead><tr><th>

MySQL Database

</th><th>

Requirement

</th></tr></thead><tbody><tr><td>

Version

</td><td>

MySQL database versions 5.7 and 8.0**Note:** MySQL versions 5.5 and 5.6 are no longer tested and have reached the end of support.

</td></tr><tr><td>

OS

</td><td>

64-bit systems

</td></tr><tr><td>

CPU

</td><td>

2 or more GHz CPU \(4-core CPU preferred for optimum performance\)

</td></tr><tr><td>

RAM

</td><td>

16 GB

</td></tr><tr><td>

Disk

</td><td>

Storage Area Network \(SAN\) or local storage \(RAID 10 recommended\)

</td></tr><tr><td>

Size

</td><td>

Determined by the number of potential records multiplied by the record size. See [Calculate the order-preserving and tokenization database size](../task/size-db.md).

</td></tr><tr><td>

Configuration

</td><td>

High availability cluster. If you are unsure of how to configure your MySQL server, contact [MySQL](https://www.mysql.com/) for configuration information.

</td></tr></tbody>
</table>**Parent Topic:**[Planning for Edge Encryption](../concept/c_EdgeEncryptionPlanning.md)

