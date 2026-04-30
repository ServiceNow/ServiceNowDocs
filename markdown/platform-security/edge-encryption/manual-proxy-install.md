---
title: Install the Edge Encryption proxy server using the command line installer
description: Manually install multiple Edge Encryption proxy servers in your network.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Installing Edge Encryption, Edge Encryption, Encryption]
---

# Install the Edge Encryption proxy server using the command line installer

Manually install multiple Edge Encryption proxy servers in your network.

## Before you begin

Roles required: security\_admin on your ServiceNow instance and local administrator on the host machine.

If order preserving encryption types or encryption patterns are to be used, set up a MySQL database on a machine in your network if not already present.

**Note:** If using Unbound Technology encryption keys with Edge Encryption, install the proxy server using the command line installer on the Unbound client machine. The Edge Encryption proxy server must run on the same machine as the Unbound technology client.

## About this task

First, set up a single Edge Encryption proxy server. After your first proxy server is successfully running, add additional proxy servers for one instance to ensure an optimal environment. See [Sizing your Edge Encryption environment](../concept/edge-environment-size.md) to determine the number of additional proxy servers needed.

1.  [Install the Edge Encryption proxy server \(command line installer\)](install-edge-linux-windows.md)  
Install an Edge Encryption proxy on a 64-bit Windows or Linux computer.
2.  [Create and configure the RSA key pair for the digital signature](t_SetUpAKeyPair.md)  
Create an RSA key pair that the proxy server can use to create the digital signature for signing changes to the encryption properties and configuration.
3.  [Import and configure the certificate for secure SSL connection](t_SetUpSecureSSLConnection.md)  
To use a secure SSL connection, import a server certificate and add it to the Java KeyStore.
4.  [Set up a keystore and encryption keys](set-up-keystore.md)  
Set up the keystore and encryption keys used by the Edge Encryption proxy server.
5.  [Configure encryption keys on the instance](t_RotateEncryptionKeys.md)  
Edge Encryption provides the tools to manage encryption keys without taking the proxy offline.
6.  [Configure additional properties in the Edge Encryption properties file](set-props.md)  
After installing the Edge Encryption proxy server in your network and setting up your keystore and keys, configure the additional Edge Encryption properties.
7.  [Configure a web proxy](t_SetUpWebProxyProperties.md)  
If your network uses a web proxy, you can set up the Edge Encryption proxy to use the web proxy.
8.  [Set the proxy server initial memory limit and upper bound memory limit](increase-memory.md)  
Set the initial memory limit and upper bound memory limit to specify how much memory the proxy server can consume. Set these limits to avoid performance issues in your Edge Encryption implementation.
9.  [Start the Edge Encryption proxy](t_RuntheProxy.md)  
After an Edge Encryption proxy is installed and configured, you can start the proxy from the command line.
10. [Obfuscate passwords in the properties file](t_SetUpPasswordEncryption.md)  
Obfuscate passwords in the `edgeencryption.properties` file to be able to share the properties file without revealing clear text passwords.
11. [Manually add an additional proxy](t_AddAdditionalProxies.md)  
After the first Edge Encryption proxy is properly configured and tested, you can set up additional proxies on a Linux or Windows machine. Installing multiple proxies on the same machine is not recommended.

**Parent Topic:**[Installing Edge Encryption](../concept/c_InstallEdgeEncryptionProxy.md)

