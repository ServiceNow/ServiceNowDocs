---
title: Enable S/MIME
description: Configure S/MIME settings for inbound and outbound email.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/enable-smime-for-outbound-and-inbound.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up S/MIME, Email encryption, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable S/MIME

Configure S/MIME settings for inbound and outbound email.

## Enable S/MIME for Inbound and Outbound emails

You can configure email properties from the Email Properties page through the **System Mailboxes** or **System Properties** module.

Email properties are available from either of these modules:

-   **System Mailboxes** &gt; **Email Properties**
-   **System Properties** &gt; **Email Properties**

## Outbound S/MIME configuration

For encryption, you must upload the email certificate for the recipients in PEM format and the CA certificates for the issuing authority. For more information, see [Upload an email certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-email-certificate.md) and [Upload a CA certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-ca-certificate.md).

For signing, you must upload the email account key pair in P12 format. For more information, see [Import an S/MIME key pair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/import-smime-key-pair.md).

<table id="table_uvv_2my_vtb"><thead><tr><th>

Configuration

</th><th>

Related property

</th></tr></thead><tbody><tr><td>

Digitally sign your outbound emails.

</td><td>

email.outbound.smime.signing.enabled

</td></tr><tr><td>

Send a public certificate in the outbound email.

</td><td>

email.outbound.smime.signing.send\_public\_cert

</td></tr><tr><td>

Encrypt message contents and attachments.

</td><td>

email.outbound.smime.encryption.enabled

</td></tr><tr><td>

Encryption algorithm. Select **AES-CBC** or **AES-GCM**.**Note:** Before selecting AES-GCM, check whether GCM is supported by the client for S/MIME.

</td><td>

email.outbound.smime.encryption.algo

</td></tr></tbody>
</table>## Inbound S/MIME configuration

For decryption, you must upload the email certificate for the recipients in PEM format and the CA certificates for the issuing authority. For more information, see [Upload an email certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-email-certificate.md) and [Upload a CA certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-ca-certificate.md).

For signature verification, you must upload the email account key pair in P12 format. For more information, see [Import an S/MIME key pair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/import-smime-key-pair.md).

|Configuration|Related property|
|-------------|----------------|
|Verify the signature for inbound emails.|email.inbound.smime.verify\_sign|
|Decrypt inbound emails.|email.inbound.smime.decrypt|

## Enable S/MIME for email notification form

To digitally sign or encrypt your emails, go to **All** &gt; **Email** &gt; **Notifications**, select **New** and select the **Digitally sign your emails** check box for digitally signing emails and **Encrypt emails** check box for email encryptions.

\[Omitted image "smime-email-form.png"\] Alt text: Enable S/MIME for email notification form

For more information, see [Create an email notification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateANotification.md).

## Enable S/MIME for email client

In the compose email form, select the **Digitally sign your emails** check box for digitally signing emails and **Encrypt emails** check box for email encryptions.

\[Omitted image "enable-smime-email.png"\] Alt text: Enable S/MIME for email client

**Parent Topic:**[Setting up S/MIME for email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/smime-for-email-signing-and-encryption.md)

**Related topics**  


[Import an S/MIME key pair]()

[Upload a CA certificate]()

[Upload an email certificate]()

