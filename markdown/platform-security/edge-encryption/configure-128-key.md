---
title: Configure the AES 128-bit encryption key
description: After you configure the HTTPS certificate through the Edge Encryption proxy installer, configure the AES 128-bit encryption key to encrypt your data.
locale: en-US
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure the AES 128-bit encryption key

After you configure the HTTPS certificate through the Edge Encryption proxy installer, configure the AES 128-bit encryption key to encrypt your data.

## Before you begin

Role required: admin

## About this task

The encryption key is either a plain text file inside the `/keys` directory or a secret key inside a keystore. If you use a keystore for your AES 128-bit and AES 256-bit encryption keys, they must both use the same keystore.

If you are updating an SSL certificate on an Edge proxy server, see [Update SSL certificate](update-ssl-certificate.md).

## Procedure

1.  Select the encryption key location.

<table id="choicetable_hj2_b1p_gfb"><thead><tr><th align="left" id="d133265e93">

Option

</th><th align="left" id="d133265e96">

Description

</th></tr></thead><tbody><tr><td id="d133265e102">

**File Store**

</td><td>

Use a file to store a single encryption key. You can use an existing file in the `/keys` directory, or you can generate a new file. To generate a new file, enter an alias and click **Generate**. A file containing an encryption key is created.**Note:** This choice designates both the storage location and the encryption key. If you select **File Store**, click **Next** and go to [step 5](configure-128-key.md#configure-key-on-instance).

</td></tr><tr><td id="d133265e130">

**Create New Java KeyStore**

</td><td>

Create a keystore to store the encryption key.

</td></tr><tr><td id="d133265e139">

**Java KeyStore File**

</td><td>

Store the encryption key in an existing Java KeyStore file.

</td></tr></tbody>
</table>2.  Click **Next**.

3.  Select or create the encryption key.

<table id="choicetable_trt_g1p_gfb"><thead><tr><th align="left" id="d133265e166">

Option

</th><th align="left" id="d133265e169">

Description

</th></tr></thead><tbody><tr><td id="d133265e175">

**New Key**

</td><td>

Create an encryption key and alias.**Note:** You must use lowercase letters and numbers for the alias name \(key name, key alias\), per Java KeyStore requirements. To find out more about the keytool utility, see the [Java SE Documentation](http://docs.oracle.com/javase/6/docs/technotes/tools/windows/keytool.html).

</td></tr><tr><td id="d133265e191">

**Use Existing Key**

</td><td>

Use an existing encryption key in the selected keystore.

</td></tr><tr><td id="d133265e200">

**Import Existing Key**

</td><td>

Import an encryption key from a different keystore.

</td></tr></tbody>
</table>4.  Click **Next**.

5.  Configure the key on the instance according to the requirements defined in your installer.

    To configure the key on the instance, navigate to the instance and define a default key. See [Configure encryption keys on the instance](t_RotateEncryptionKeys.md). Ensure that the key alias, size, and type match the requirements defined in the installer.



6.  Once the key is configured on the instance, return to the installer and click **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](proxy-installer.md)

**Previous topic:**[Configure the HTTPS certificate](configure-cert.md)

**Next topic:**[Configure the AES 256-bit encryption key](configure-256-key.md)

