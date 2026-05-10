---
title: Configuring digital signature and encryption for emails
description: Configure emails that send a digital signature to verify you as an authentic sender and an email encryption to certify authentic recipients.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Emails, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configuring digital signature and encryption for emails

Configure emails that send a digital signature to verify you as an authentic sender and an email encryption to certify authentic recipients.

A digital signature verifies the email sender and assures recipients that the email came from a trusted source and wasn't altered. In the email composer for Configurable Workspace, you can select a check box to digitally sign outbound emails.

Encryption makes the email unreadable to anyone except the intended recipient. In the email composer for Configurable Workspace, you can select a check box to encrypt outbound emails.

## Digital signature and encryption configuration

To use digital signature or encryption for emails in Configurable Workspace, configure S/MIME for your instance. For information on S/MIME and instructions to configure S/MIME for emails, see [Setting up S/MIME for email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/smime-for-email-signing-and-encryption.md).

Configuring S/MIME for emails requires the following steps:

-   **[Import an S/MIME key pair](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/import-smime-key-pair.md)**

    Import an S/MIME key pair consisting of the private key and certificate to sign outbound emails or decrypt emails.

-   **[Upload a CA certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-ca-certificate.md)**

    Upload a digital CA \(Certificate Authority\) certificate to validate email certificates for secure communication.

-   **[Upload an email certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upload-email-certificate.md)**

    Upload an email certificate to validate a signature for inbound email or encrypt an outbound email or both for secure communication.

-   **[Enable S/MIME](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/enable-smime-for-outbound-and-inbound.md)**

    Configure S/MIME settings for inbound and outbound email.


