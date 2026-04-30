---
title: Set up a keystore and encryption keys
description: Set up the keystore and encryption keys used by the Edge Encryption proxy server.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set up a keystore and encryption keys

Set up the keystore and encryption keys used by the Edge Encryption proxy server.

## Before you begin

Role required: security\_admin

## Procedure

1.  Carefully determine the appropriate type of keystore to use based on your organization's needs.

<table id="table_sj1_jpd_wz"><thead><tr><th>

Supported keystore

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**File store**

</td><td>

Keys are stored in a file in a file system accessed by the Edge Encryption proxy server. Because encryption keys stored in a file are not encrypted, it is your responsibility to protect these files.

</td></tr><tr><td>

**Java KeyStore**

</td><td>

A Java KeyStore:-   Stores keys in a Java JCEKS KeyStore.
-   Is password protected and more secure than storing keys in a file in the file system.
-   Can store multiple keys. A key alias represents each key, making it easier to manage multiple keys.
 The Edge Encryption proxy ships with the Java JCEKS KeyStore file named `keystore.jceks` in the `keystore` directory. This keystore file contains the ServiceNow public key used to validate encryption rules signed by ServiceNow.

</td></tr><tr><td>

**Enterprise Key Management \(EKM\)**

</td><td>

**SafeNet KeySecure** Keys are stored and retrieved with SafeNet KeySecure key management.

 You must secure a license with [Gemalto](http://www.gemalto.com), download the libraries, and install the SafeNet KeySecure keystore on a host machine in your network before configuring the keystore on the Edge Encryption proxy server.

 **Unbound Technology**

 The base64-encoded wrapped encryption key is stored as text file on the Edge Encryption proxy server. The Unbound Technology implementation \(previously Dyadic Security\) maintains control of the wrapping key.

 The Edge Encryption proxy server must run on the same machine as the Unbound technology client.

</td></tr></tbody>
</table>    **Note:** If using a keystore other than the base system Java JCEKS KeyStore, you must import the ServiceNow public key into your keystore. The public key alias is **servicenow**.

2.  Set up the keystore and encryption keys in your local network.


-   **[Set up a Java KeyStore keystore](t_JavaKeyStoreSetUp.md)**  
You can use a Java KeyStore keystore to store encryption keys.
-   **[Set up a SafeNet KeySecure keystore](t_SetUpNAEKeyStore.md#)**  
If you are using a SafeNet keystore, copy a set of libraries into the proxy distribution directory.
-   **[Set up Unbound Technology keys](unbound-key-install.md)**  
Use Unbound Technology \(previously Dyadic Security\) keys with Edge Encryption by storing the base64-encoded wrapped encryption key as text file on the Edge Encryption proxy server and providing the wrapping key alias. The Unbound Technology implementation maintains control of the wrapping key.
-   **[Create an encryption key stored in a file](t_CreateAFileStoreKeyStore.md)**  
You can use a simple text file as a keystore. Each file holds a single encryption key.

**Parent Topic:**[Install the Edge Encryption proxy server using the command line installer](manual-proxy-install.md)

**Previous topic:**[Import and configure the certificate for secure SSL connection](t_SetUpSecureSSLConnection.md)

**Next topic:**[Set up a Java KeyStore keystore](t_JavaKeyStoreSetUp.md)

