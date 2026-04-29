---
title: Create an encryption key stored in a file
description: You can use a simple text file as a keystore. Each file holds a single encryption key.
locale: en-US
release: australia
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up a keystore and encryption keys, Install the Edge Encryption proxy server using the command line installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Create an encryption key stored in a file

You can use a simple text file as a keystore. Each file holds a single encryption key.

## Before you begin

Role required: admin

## About this task

This step creates both the key storage and the encryption key.

**Note:** The name of the key file must match the key alias specified in the encryption keys table in the instance. See [Configure encryption keys on the instance](t_RotateEncryptionKeys.md).

## Procedure

1.  Create a file in the `/keys` folder of the proxy server installation directory.

2.  Add the encryption key to the file.

<table id="choicetable_sm3_f1b_tt"><tbody><tr><td id="d215133e88">

**AES 128**

</td><td>

Place the encryption key, exactly 16 bytes, into the file.

</td></tr><tr><td id="d215133e97">

**AES 256**

</td><td>

Place the encryption key, exactly 32 bytes, into the file.

</td></tr></tbody>
</table>3.  Update the `edgeencryption.properties` file.

    1.  Change to the `<installation directory>/conf/` directory.

    2.  Open the `edgeencryption.properties` file.

    3.  Enter the properties for the [file store](../reference/edge-encryption-proxy-server-properties.md).

    4.  Save and close the file.


**Parent Topic:**[Set up a keystore and encryption keys](set-up-keystore.md)

