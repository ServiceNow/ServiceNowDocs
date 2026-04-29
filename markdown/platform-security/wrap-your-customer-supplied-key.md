---
title: Wrap your customer-supplied key
description: Wrap your symmetric data encryption key with an ephemeral public wrapping key before you can upload it to your instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Customer-supplied keys for Field Encryption Enterprise, Configuring Field Encryption, Field Encryption, Encryption]
---

# Wrap your customer-supplied key

Wrap your symmetric data encryption key with an ephemeral public wrapping key before you can upload it to your instance.

## Before you begin

Role required: security\_admin and sn\_kmf.cryptographic\_manager or sn\_kmf.admin

You must have a symmetric data encryption key in a `.bin` to use these steps. For instructions on this process, see [Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md).

**Important:** Your symmetric data encryption key must be in a binary format \(.BIN\). If another format is used, the following error message:

`Token failed validation. Please reattach the unmodified token.`

## About this task

To modify optional properties that control the size, padding algorithm, and validity period of the key, see [Configure properties for customer-supplied key](configure-properties-for-customer-supplied-key.md).

You must have a cryptographic tool to wrap your key. The example in this document uses OpenSSL 1.1. For more information on OpenSSL, see details at [https://www.openssl.org](https://www.openssl.org). If you’re using other cryptographic tools, such as LibreSSL or GnuTLS, refer to the documentation for those products for similar steps.

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Field Encryption** &gt; **Field Encryption Experience**.

2.  Select**View module details** from the **Field Encryption modules overview** to open the field encryption module that you’ve previously created.

    **Note:** If you haven't created a field encryption module yet, you can create one using the steps in [Configure Field Encryption modules](configure-fe-modules.md).

3.  In the **Cryptographic Specification** section, select **Manage Specification Settings**.

4.  Select the **Next** button until you reach the **Key Origin** section.

5.  Verify that the **Origin** field has a value of **Upload customer supplied key**.

    If that value can't be selected, refer to steps 3–5 in [Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md).

6.  In the **Key Alias** field, create an alias.

    Your key uses this alias once it's uploaded.

7.  Select **Next**.

8.  Select the link in the **Download wrapping key** field.

    A `token_publickey` file downloads to your computer. Don’t rename this file.

9.  On your local machine, unzip and open the `token_publickey` folder.

    You should see an import token file \(.txt\) and a public key file \(.PEM\) in this folder.

10. Move your symmetric data encryption key that you generated into this folder.

11. Copy the name of the `token_publickey` file to your clipboard.

12. Open a terminal session and navigate to the `token_publickey` folder.

13. Enter the following command:

    **Important:** Replace any bracketed text \(&lt;&gt;\) with your specific file names and information. Use the following key wrapping command examples table as a guide.

    `openssl pkeyutl -encrypt -pubin -inkey publickey_<keyname>. PEM -in <keyname.bin> -out wrapped_key_material -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256`

<table id="table_ahy_fxk_f2c"><thead><tr><th>

Directions

</th><th>

Command

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Input the publickey\_&lt;keyname&gt;.PEM

</td><td>

`openssl pkeyutl -encrypt -pubin -inkey publickey_<keyname>.PEM`

</td><td>

`openssl pkeyutl -encrypt -pubin -inkey publickey_567898643ffff.PEM`

</td></tr><tr><td>

Input the name of your symmetric data encryption key

</td><td>

`-in <keyname.bin>`

</td><td>

`-in mykey.bin`

</td></tr><tr><td>

Enter the &lt;-out&gt; command and specify whether the wrapped key material should use 256-bit encryption

</td><td>

`-out wrapped_key_material -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256`

</td><td>

NA

</td></tr></tbody>
</table>
## What to do next

Now that your key is wrapped, you can upload it to your instance using the procedure in .

**Parent Topic:**[Configure Customer-supplied keys for Field Encryption Enterprise](fe-config-customer-supplied-keys.md)

