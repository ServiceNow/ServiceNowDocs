---
title: Set up a SafeNet KeySecure keystore
description: If you are using a SafeNet keystore, copy a set of libraries into the proxy distribution directory.If you use a SafeNet NAE server for key storage with Edge, before upgrading the proxy from Kingston or lower to London or higher, you must copy Gemalto SafeNet client ProtectApp JAR files and add new properties.
locale: en-US
release: xanadu
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up a keystore and encryption keys, Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set up a SafeNet KeySecure keystore

If you are using a SafeNet keystore, copy a set of libraries into the proxy distribution directory.

## Before you begin

Role required: admin

You must install and set up the SafeNet keystore before performing this step. Secure a license with [Thales](https://www.thalesgroup.com) in order to download the libraries.

**Note:** For IngrianNAE version 8.12, you must also download the `commons-collections.jar` file

## About this task

**Note:** On Linux, file paths use a forward slash \(/\).

## Procedure

1.  Change to the `<installation directory>/conf/` directory, and open the `edgeencryption.properties` file.

2.  Enter the properties for the [SafeNet keystore](../reference/edge-encryption-proxy-server-properties.md).

    **Note:** You may configure SafeNet keystore using with username/password authentication or client certificate authentication, but not a combination of both.

    An example for a SafeNet keystore using username and password authentication.

    ```
    edgeencryption.nae.retries = 3
    edgeencryption.nae.enabled = true
    edgeencryption.nae.server = url
    edgeencryption.nae.port = 9000
    edgeencryption.nae.protocol = ssl
    edgeencryption.nae.keystore.path = keystore/safenet_truststore
    edgeencryption.nae.keystore.password = password
    edgeencryption.nae.user = safenet_user
    edgeencryption.nae.password = safenet_password
    ```

    An example for a SafeNet keystore using client certificate authentication. This authentication method eliminates the need to store the SafeNet server username and password in the properties file.

    ```
    edgeencryption.nae.retries = 3
    edgeencryption.nae.enabled = true
    edgeencryption.nae.server = url
    edgeencryption.nae.port = 9000
    edgeencryption.nae.protocol = ssl
    edgeencryption.nae.keystore.path = keystore/safenet_clientcert
    edgeencryption.nae.keystore.password = password
    edgeencryption.nae.client.certificate = cert_name
    ```

3.  Add or create a key in the SafeNet keystore.

    You add the key name \(alias\) on the instance when you assign default keys.

4.  Save and close the `edgeencryption.properties` file.


**Parent Topic:**[Set up a keystore and encryption keys](set-up-keystore.md)

## Upgrade from Kingston or lower to London or higher

If you use a SafeNet NAE server for key storage with Edge, before upgrading the proxy from Kingston or lower to London or higher, you must copy Gemalto SafeNet client ProtectApp JAR files and add new properties.

### Before you begin

Role required: admin

### About this task

**Note:** On Linux, file paths use a forward slash \(/\).

### Procedure

1.  Copy the following files from `<installation directory>/lib` to the `<installation directory>/nae directory`:

    -   `commons-collections<version>.jar`
    -   `ingrianlog4j-api-<version>.jar`
    -   `ingrianlog4j-core-<version>.jar`
    -   `ingrianNAE-<version>.jar`
2.  On the current version \(not upgraded\) of the proxy, update the `<installation directory>/conf/edgeencryption.properties` file by adding the following two properties:

    -   **edgeencryption.ekm.provider.classname** = `com.snc.edgeencryption.encryption.CloudEdgeNaeKeyProvider`
    -   **edgeencryption.thirdparty.vendor.library.path** = `<directory path to the directory where you copied the jar files in step 1>`

        **Note:** **edgeencryption.thirdparty.vendor.library.path** for Java 11.

3.  Save the changes.

4.  Proceed with the upgrade to London or higher.


