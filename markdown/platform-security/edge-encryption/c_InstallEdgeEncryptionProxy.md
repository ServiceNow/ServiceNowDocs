---
title: Installing Edge Encryption
description: You can install an Edge Encryption proxy manually or using the Edge Encryption interactive installer.
locale: en-US
release: yokohama
product: Edge Encryption
classification: edge-encryption
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Edge Encryption, Encryption]
---

# Installing Edge Encryption

You can install an Edge Encryption proxy manually or using the Edge Encryption interactive installer.

## Java requirements

The host machine installing or running the Edge Encryption proxy server must maintain a supported version of Java. Current supported versions are Java 17.0.3 or later in the 17.x version series.

**Note:** Java 11 is no longer be supported as of the Yokohama release. Upgrade your environment with the Edge Encryption proxy to Java 17 before you attempt to install Yokohama or later versions of the Edge Encryption proxy.

## Installing the proxy server

Installing Edge Encryption includes these steps.

-   Install the Edge Encryption proxy application on a server in your network using the interactive installer or the manual installer.
-   Generate the RSA key pair for digitally signing encryption configurations and encryption rules.
-   Install the Java Cryptography Extension \(JCE\), if you plan to use AES 256 encryption.
-   If you are using a secure SSL connection, obtain a server certificate and import it to the Java KeyStore.
-   Set up your keystore and encryption key.
-   If order preserving encryption types or encryption patterns are to be used, set up a MySQL database on a machine in your network.
-   Set the desired properties. Properties are located in the `edgeencryption.properties` configuration file.
-   Specify that a proxy server is a trusted source so that Edge Encryption can process requests coming from that proxy server.

## Accessing the proxy server

Once installation is complete, point each user's browser to an Edge Encryption proxy using the URL format: `<host>:<port>`. Values are determined by the [host and port properties](../reference/edge-encryption-proxy-server-properties.md) in the `edgeencryption.properties` file.

As an example with the following values:

|Property|Example value|
|--------|-------------|
|edgeencryption.proxy.host|hostname.mycompany.com|
|edgeencryption.proxy.http.port|8081|

A client will access the proxy server using the following address: `http://hostname.mycompany.com:8081/`.

**Note:** DNS settings and routing rules may be used. Host and port values are determined by your network administrator.

-   **[Request Edge Encryption](../task/t_InstallCloudEdge.md)**  
The Edge Encryption plugin \(com.glide.edgeencryption\) is available as a separate subscription.
-   **[Set up an Edge Encryption user account](../task/t_SetupEdgeEncryptionUser.md)**  
The Edge Encryption proxies connect to the instance as a user to obtain and update encryption configuration information. Create a user account for this purpose and give the edge\_encryption role to the user.
-   **[Download the Edge Encryption proxy server](../task/t_DownloadtheProxy.md)**  
Download the Edge Encryption proxy server application from your instance, and then copy the file to each computer that is to run the Edge Encryption proxy server.
-   **[Install the Edge Encryption proxy server using the interactive installer](../task/proxy-installer.md)**  
Install the Edge Encryption proxy server on a Windows or Linux computer using the interactive installer.
-   **[Install the Edge Encryption proxy server using the command line installer](../task/manual-proxy-install.md)**  
Manually install multiple Edge Encryption proxy servers in your network.
-   **[Authenticate an Edge Encryption proxy server](../task/authenticate-edge-proxy.md)**  
Specify that a proxy server is a trusted source so that Edge Encryption can process requests coming from that proxy server.
-   **[Stop the Edge Encryption proxy](../task/t_StoptheProxy.md)**  
You can stop an Edge Encryption proxy from the command line.
-   **[Uninstall the Edge Encryption proxy on Linux](../task/t_UninstalltheProxy.md)**  
You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.
-   **[Uninstall the Edge Encryption proxy on Windows](../task/t_UninstalltheProxyonWindows.md)**  
You can uninstall the Edge Encryption proxy. If you are upgrading the proxy, it is not necessary to shut down and uninstall the current version.
-   **[Set up multiple provider SSO with Edge Encryption](../task/SSO-edge.md)**  
Set up multiple provider SSO to enable logging in through the Edge Encryption proxy server URL or the instance URL. If you are implementing multiple provider single sign-on \(SSO\) with Edge Encryption enabled, some users might need to log in to your instance through the Edge Encryption proxy server, while other users might not.
-   **[Edge Encryption proxy server properties](../reference/edge-encryption-proxy-server-properties.md)**  
The `edgeencryption.properties` configuration file located in the `<installation directory>/conf/` folder contains properties used to configure your environment.
-   **[CyberArk integration with the Edge proxy server](cyberark-integration-edge-proxy.md)**  
Use CyberArk to store passwords in a centralized and secure digital vault to secure passwords that were previously stored in clear text and secured by file access, or that were previously encrypted via a second file.
-   **[Using a load balancer with the Edge proxy server](../reference/load-balancer-edge-proxy.md#)**  
You can use a load balancer to balance the load across the proxy servers in your Edge Encryption proxy setup. If the load balancer and proxy servers are using different ports, specify the host name and HTTPS port of the load balancer to enable users to view responses on their browser.

**Parent Topic:**[Edge Encryption](../reference/edge-encryption.md)

