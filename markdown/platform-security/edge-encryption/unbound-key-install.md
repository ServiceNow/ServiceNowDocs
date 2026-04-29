---
title: Set up Unbound Technology keys
description: Use Unbound Technology \(previously Dyadic Security\) keys with Edge Encryption by storing the base64-encoded wrapped encryption key as text file on the Edge Encryption proxy server and providing the wrapping key alias. The Unbound Technology implementation maintains control of the wrapping key.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a keystore and encryption keys, Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Set up Unbound Technology keys

Use Unbound Technology \(previously Dyadic Security\) keys with Edge Encryption by storing the base64-encoded wrapped encryption key as text file on the Edge Encryption proxy server and providing the wrapping key alias. The Unbound Technology implementation maintains control of the wrapping key.

## Before you begin

Role required: security\_admin

In your Unbound Technology implementation, identify both the wrapping key and the wrapped key. Use the RSA/ECB/OAEPWITHSHA-256ANDMGF1PADDING algorithm for wrapping and padding. Export the wrapped key in base64-encoded text format. Save the file using the key alias as the name with no file extension.

**Note:** If using Unbound Technology encryption keys with Edge Encryption, install the proxy server using the command line installer on the Unbound client machine. The Edge Encryption proxy server must run on the same machine as the Unbound technology client.

## Procedure

1.  Add the wrapped encryption key in base64-encoded text format to the `<proxy-installation-directory>/keys` directory.

    The name of the file must be the key alias with no file extension.

2.  Update the `edgeencryption.properties` file.

    1.  Change to the `<proxy-installation-directory>/conf` directory.

    2.  Open the `edgeencryption.properties` file.

    3.  Enter the File store properties and set the value of **edgeencryption.keyfile.directory** to `keys`.

        This property directs the proxy server to look for the encryption key in the `<Java-home-directory>/keys` directory.

        For more information on Edge Encryption properties, see [Edge Encryption proxy server properties](../reference/edge-encryption-proxy-server-properties.md).

    4.  Uncomment the properties for the Dyadic provider configuration and set the value of **edgeencryption.ekm.provider.rsa.wrapping.key.alias** to the wrapping key alias in your Unbound implementation.

    5.  Save and close the file.


## What to do next

Add the encryption key alias to the instance. The encryption key alias is the file name of the wrapped encryption key added to the `<proxy-installation-directory>/keys` directory. For example, if the file in the directory is named `myunboundkey`, add this name to the **Key alias** field. See [Configure encryption keys on the instance](t_RotateEncryptionKeys.md).

**Parent Topic:**[Set up a keystore and encryption keys](set-up-keystore.md)

