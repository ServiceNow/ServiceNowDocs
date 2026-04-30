---
title: Import a key from a web service
description: Securely upload an external customer key onto your instance using import a key from a web service \(for example the key REST API\). Both symmetric and asymmetric public keys can be imported into a targeted KMF cryptographic module.Configure Key Management Framework import settings before importing a key.Upload your wrapped key into a cryptographic module using the import key from web service functionality. The example uses a symmetric key. Similar steps can be used to import an asymmetric key.
locale: en-US
release: xanadu
product: Platform Encryption
classification: platform-encryption
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Key Management Framework, Encryption]
---

# Import a key from a web service

Securely upload an external customer key onto your instance using import a key from a web service \(for example the key REST API\). Both symmetric and asymmetric public keys can be imported into a targeted KMF cryptographic module.

The key to be imported \(the target key\) must be encrypted with a wrapping key before it's uploaded into the instance’s target cryptographic module. This wrapping key is the public component of a public/private key pair, which must be present on the instance. The key is a pre-requisite before the wrapped target key can be uploaded via Import From Web Services.

These two separate procedures \(importing the wrapping key pair and importing the wrapped target key from a web service\) are detailed in the following documentation. This key pair must be generated and uploaded to be available in the instance’s internal Key Import cryptographic module.

**Note:** This example uses OpenSSL for key and certificate generation and the Postman API test tool to show REST API use. Substitute other comparable tools based on your company requirements.

**Parent Topic:**[Key Management Framework](../../encryption/concept/encryption.md)

## Import the wrapping / unwrapping key pair

Configure Key Management Framework import settings before importing a key.

### Before you begin

Role required: sn\_kmf.cryptographic\_manager

### About this task

This example uses OpenSSL for key and certificate generation. Substitute other comparable tools based on your company requirements.

### Procedure

1.  In your local environment, use the terminal to create a certificate.

    For example: `openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:4096 -keyout wrapping_private.key -out wrapping_public.crt`

    This certificate is a public component that contains a key. The certificate is used to wrap an AES symmetric key.

2.  In your local environment, use the terminal to create a keystore containing public cert \(with the wrapping key\), and private unwrapping key.

    For example:`openssl pkcs12 -export -in wrapping_public.crt -inkey wrapping_private.key -name "wrapping_key_alias" -out wrapping_keystore.p12`

3.  On your instance, navigate to **All** &gt; **Key Management** &gt; **Import Settings** &gt; **Key Import Settings**.

4.  In the Algorithm Definition section, verify the **Crypto Purpose** is set to `Asymmetric Key Unwrapping`.![Crypto purpose selection.](../image/import-web-cryptopurpose.png)

5.  Select an appropriate algorithm that aligns with asymmetric key material for the imported keystore.

    See [Cryptographic specification](cryptographic-purpose.md) for additional information.

6.  Select **Next**.

7.  In the **Lifecycle Definition** section, select **Next** to continue.

8.  In the **Key Origin** section, select either **Import from PKCS12** or **Import from BCFKS** in the **Origin** field.

    **Note:** If using the example keystore from step 1, select **Import from PKCS12**.

9.  Enter a **Key Alias** to identify the key.

    This alias should match the key alias \(or “friendly name”\) that was specified when generating the certificate or keystore to be uploaded. Continuing the example above, this would be `wrapping_key_alias`.

10. Select **Next**.

    The **Key Creation** section includes an **Import Key** link, which displays a dialog to upload the keystore. Continuing the example, this would be `wrapping_keystore.p12`.


## Import a wrapped key from a web service

Upload your wrapped key into a cryptographic module using the import key from web service functionality. The example uses a symmetric key. Similar steps can be used to import an asymmetric key.

### Before you begin

Role required: sn\_kmf.cryptographic\_manager \(module configuration\), sn\_kmf.cryptographic\_operator \(REST operation basic authentication\)

### About this task

KMF Import key endpoint access is required to complete the key import process.

This example uses OpenSSL to generate keys and certificates. You may substitute other comparable tools based on your requirements.

### Procedure

1.  Using the terminal on your local device, wrap your symmetric key using the Key Import module public key wrapping key.

    For example: `openssl pkeyutl -encrypt -pubin -inkey public_wrapping_key.pem -in symmetric_key.bin -pkeyopt rsa_padding_mode:oaep -pkeyopt rsa_oaep_md:sha256 -out wrapped_symmetric_key.txt`

    This example creates a wrapped key file named `wrapped_symmetric_key.txt`.

2.  Create a cryptographic module to be tied to the API.

    See or for additional information.

3.  Add a cryptographic specification with the following selections.

    -   **Crypto Purpose**: `Symmetric Data Encryption/Decryption`.
    -   **Key Origin**: `Import from web service` ![Key origin selected as import from web service.](../image/selectweborigin.png)

        See or for more information.

4.  Execute an `HTTP POST request` to the import from a web service REST endpoint.

<table id="choicetable_wgh_zgb_fqb"><thead><tr><th align="left" id="d78033e407">

Option

</th><th align="left" id="d78033e410">

Value/Format

</th></tr></thead><tbody><tr><td id="d78033e416">

**URL of the endpoint**

</td><td>

`https://<instance>/api/sn_kmf/key/import?cryptoSpecSysID=<sys_id_of_crypto_spec>`.

</td></tr><tr><td id="d78033e428">

**CryptoSpecSysID parameter**

</td><td>

The sys\_id of the newly created crypto specification.

**Tip:** Right-click the header of the crypto specification to copy the sys\_id.

</td></tr><tr><td id="d78033e448">

**Header-Content-Type**

</td><td>

Application/octet-stream.

</td></tr><tr><td id="d78033e457">

**Body**

</td><td>

Must contain a file attachment-binary and the public key to import \(wrapped\_symmetric\_key.txt\).

</td></tr><tr><td id="d78033e467">

**Import from web service REST endpoint**

</td><td>

Uses basic authentication of `<username/password>`.**Note:** Ensure that the designated user has the sn\_kmf\_cryptographic\_operator role.

</td></tr></tbody>
</table>    Successful import of the public key results in an HTTP response message with `Status 200`.

5.  Verify that the key successfully imported to the targeted cryptographic module.![Crypto specification module keys tab with successful key import.](../image/keyimportedfromwebservices.png)


