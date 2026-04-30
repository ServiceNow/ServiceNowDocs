---
title: Wrap your customer-supplied key
description: Wrap the symmetric key to use for encryption with the downloaded public key.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-12-27"
reading_time_minutes: 2
breadcrumb: [Using customer supplied keys with Column Level Encryption Enterprise, Using Column Level Encryption, Column Level Encryption, Encryption]
---

# Wrap your customer-supplied key

Wrap the symmetric key to use for encryption with the downloaded public key.

## Before you begin

**Note:** This procedure describes options that are available with KMF base system and options to be used with Column Level Encryption Enterprise functionality. Column Level Encryption Enterprise functionality is available only when the com.glide.now.platform.encryption plugin is active. See [Activate Column Level Encryption Enterprise](../../now-platform-encryption/task/activate-platform-encryption.md) for more information on obtaining Column Level Encryption Enterprise.

Some of the steps in this document require the use of a cryptographic tool installed on your local device. The examples in this task use the OpenSSL tool. For more information on this tool see [https://www.openssl.org](https://www.openssl.org). If you are using other cryptographic tools, such as LibreSSL or GnuTLS, refer to the documentation for those products for similar steps.

-   Modify optional properties that control the size, padding algorithm, and validity period of the key. See [Configure properties for customer-supplied keys](../concept/customer-supplied-keys.md).
-   You must have your symmetric key \(.BIN\) for encryption.

    **Important:** Your key must be in binary format. If another format is used, a `Token failed validation. Please reattach the unmodified token.`error message displays.

-   You must have a cryptographic tool to wrap your key. This example uses OpenSSL 1.1.


Role required: sn\_kmf.cryptographic\_manager or sn\_kmf.admin

## Procedure

1.  Navigate to **All** &gt; **Key Management Framework** &gt; **Cryptographic Modules** &gt; **All**.

2.  Select the cryptographic module that you created for the customer supplied key from the Crypto Specifications related list.

3.  You will be directed to the **Key Creation** step.

4.  If you have not previously downloaded the wrapping key, click the link to download the `token_publickey<id>.zip` file and save it to the same location as your key.

    **Note:** Do not rename the downloaded `token_publickey<id>` file.

5.  Unzip the file to your local network.

    The zip file contains two files, an import token and a public key `.PEM` certificate. Wrap your symmetric key with the public key to encrypt it.

6.  Copy the name of the `token_publickey`file to your clipboard.

7.  From a command line, use the copied `token_publickey` file name to open the folder of the unzipped files as a placeholder for the wrapped key.

8.  Edit this script by replacing the examples with the names of your crypto files.

    ```
    "downloads user.name$ cd `token_publickey_<token>`
    openssl pkeyutl -encrypt -pubin -inkey `publickey_<keyname>.PEM`
    -in `<keyname.bin>`
    -out wrapped_key_material -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha<128 or 256> "
    ```

    Review the key wrapping commands in the following table for more information.

<table id="table_azx_3yk_snb"><thead><tr><th>

Directions

</th><th>

Command

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Open the file directory where you downloaded the wrapping token.

</td><td>

```
cd
```

</td><td>

`cd token_publickey123456789`

</td></tr><tr><td>

Paste the name of the `publickey.PEM` certificate.

</td><td>

```
openssl pkeyutl -encrypt -pubin -inkey
```

</td><td>

`publickey_586798643ffff.PEM`

</td></tr><tr><td>

Paste the name of your key here.

</td><td>

```
-in
```

</td><td>

`mykey.bin`

</td></tr><tr><td>

Enter the &lt;-out&gt; command and specify if the key is 128 bit or 256 bit.

</td><td>

```
-out wrapped_key_material -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256
```

</td><td>

N/A

</td></tr></tbody>
</table>9.  Run the command.

    A system message displays `token_publickey_<keynumber>`. The key will be generated and a `wrapped_key_material` file added to the directory.

10. Upload the wrapped key.


## What to do next

Return to [Configure and upload your customer supplied key](../../key-management-framework/task/upload-customer-supplied-key.md) to upload your wrapped key.

**Parent Topic:**[Using customer supplied keys with Column Level Encryption Enterprise](../concept/csk-landing.md)

