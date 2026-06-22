---
title: Configure the AES 256-bit encryption key
description: After you configure the AES 128-bit key through the Edge proxy installer, you can optionally configure an AES 256-bit encryption key to encrypt your data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/edge-encryption/configure-256-key.html
release: zurich
product: Edge Encryption
classification: edge-encryption
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Install the Edge Encryption proxy server using the interactive installer, Installing Edge Encryption, Edge Encryption, Encryption]
---

# Configure the AES 256-bit encryption key

After you configure the AES 128-bit key through the Edge proxy installer, you can optionally configure an AES 256-bit encryption key to encrypt your data.

## Before you begin

Role required: admin

## About this task

The encryption key is either a plain text file inside the `/keys` directory or a secret key inside a keystore. If you use a keystore for your AES 128-bit and AES 256-bit encryption keys, both keys must use the same keystore. If you don’t want to configure an AES 256-bit encryption key, select **Skip** to continue installing the proxy server.

If you’re updating an SSL certificate on an Edge proxy server, see [Update SSL certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/update-ssl-certificate.md).

## Procedure

1.  Select the encryption key location.

<table id="choicetable_ech_hb2_hfb"><thead><tr><th align="left" id="d64074e93">

Option

</th><th align="left" id="d64074e96">

Description

</th></tr></thead><tbody><tr><td id="d64074e102">

**File Store**

</td><td>

Use a file to store a single encryption key. You can use an existing file in the `/keys` directory, or you can generate a new file. To generate a new file, enter an alias and select **Generate**. A file containing an encryption key is created.**Note:** This choice designates both the storage location and the encryption key. If you select **File Store**, select **Next** and go to [step 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/configure-256-key.md).

</td></tr><tr><td id="d64074e130">

**Create New Java KeyStore**

</td><td>

Create a keystore to store the encryption key.

</td></tr><tr><td id="d64074e139">

**Java KeyStore File**

</td><td>

Store the encryption key in an existing Java KeyStore file.

</td></tr></tbody>
</table>2.  Select **Next**.

3.  Select or create the encryption key.

<table id="choicetable_x1n_4b2_hfb"><thead><tr><th align="left" id="d64074e166">

Option

</th><th align="left" id="d64074e169">

Description

</th></tr></thead><tbody><tr><td id="d64074e175">

**New Key**

</td><td>

Create an encryption key and alias.**Note:** You must use lowercase letters and numbers for the alias name \(key name, key alias\), according to Java KeyStore requirements. To find out more about the keytool utility, see the [Java SE Documentation](http://docs.oracle.com/javase/6/docs/technotes/tools/windows/keytool.html).

</td></tr><tr><td id="d64074e191">

**Use Existing Key**

</td><td>

Use an existing encryption key in the selected keystore.

</td></tr><tr><td id="d64074e200">

**Import Existing Key**

</td><td>

Import an encryption key from a different keystore.

</td></tr></tbody>
</table>4.  Select **Next**.

5.  If you want to use AES 256-bit encryption, see [Configure the AES 256-bit encryption key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/configure-256-key.md).

6.  To use AES 256-bit encryption, you must also configure the AES 256-bit default encryption key on the instance.

    Do this by navigating to the instance and defining a default key. See [Configure encryption keys on the instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/t_RotateEncryptionKeys.md). Ensure that the key alias, size, and type match the requirements defined in the installer.

7.  After the key is configured on the instance, return to the installer and select **Next**.


**Parent Topic:**[Install the Edge Encryption proxy server using the interactive installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/proxy-installer.md)

**Previous topic:**[Configure the AES 128-bit encryption key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/configure-128-key.md)

**Next topic:**[Update SSL certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/edge-encryption/update-ssl-certificate.md)

