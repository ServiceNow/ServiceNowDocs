---
title: Setting up S/MIME for email
description: S/MIME is a protocol for sending digitally signed and encrypted emails to ensure the confidentiality, authenticity and integrity.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Email encryption - S/MIME protocol, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Setting up S/MIME for email

S/MIME is a protocol for sending digitally signed and encrypted emails to ensure the confidentiality, authenticity and integrity.

## Set up S/MIME for outbound mails \(signing and encryption\)

You can use S/MIME for outbound mails for the following purposes:

-   Digital signature
-   Encryption
-   Digital signature and encryption

To set up S/MIME, the admin must have the following:

-   email\_account\_admin and sn\_kmf.cryptographic\_manager roles
-   Key pair \(private key and public key\)
-   CA certificate
-   Email certificate

Upload the instance email account key pair and email certificates, and enable outbound S/MIME properties. For more information, see [Enable S/MIME](enable-smime-for-outbound-and-inbound.md).

If there are multiple recipients and some of the recipients do not have valid certificates, the email will be sent only to recipients with a valid certificate.

## Set up S/MIME for inbound mails \(sign verification and decryption\)

S/MIME for inbound mails can be used for the following:

-   Signature verification
-   Decryption
-   Signature verification and decryption

For information about enabling inbound S/MIME properties, see [Enable S/MIME](enable-smime-for-outbound-and-inbound.md).

If the system fails to decrypt a message, no inbound actions will run on the email and it is moved to the received-ignored status.

To set up the system to ignore inbound signed emails if the signature cannot be verified or is invalid, admins can create the **email.inbound.smime.ignore\_unverified\_emails** and set it to true.

For more information about key management and cryprographic module, see [Key Management Framework Reference](https://www.servicenow.com/docs/access?context=understanding-kmf&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **[Import an S/MIME key pair](../task/import-smime-key-pair.md)**  
Import an S/MIME key pair consisting of the private key and certificate to sign outbound emails or decrypt emails.
-   **[Upload a CA certificate](../task/upload-ca-certificate.md)**  
Upload a digital CA \(Certificate Authority\) certificate to validate email certificates for secure communication.
-   **[Upload an email certificate](../task/upload-email-certificate.md)**  
Upload an email certificate to validate a signature for inbound email or encrypt an outbound email or both for secure communication.
-   **[Enable S/MIME](enable-smime-for-outbound-and-inbound.md)**  
Configure S/MIME settings for inbound and outbound email.

**Parent Topic:**[Email encryption - S/MIME protocol](smime-inbound-outbound-mails.md)

**Related topics**  


[Activate S/MIME Email](../task/activate-smime-plugin.md)

