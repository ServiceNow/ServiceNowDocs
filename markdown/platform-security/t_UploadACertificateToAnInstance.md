---
title: Uploading a certificate to an instance
description: Add a certificate to the instance from the Certificates module.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Certificates, Encryption]
---

# Uploading a certificate to an instance

Add a certificate to the instance from the Certificates module.

## Upload a certificate to an instance

Upload a certificate to an instance.

## Before you begin

Role required: admin

## About this task

When a certificate is updated on the ADFS server, you must also upload an updated certificate to the instance.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Specify a unique name for the certificate.|
    |**Expiration notification**|\[Optional\] Select whether you want to send a notification when the certificate is about to expire.|
    |**Active**|Select whether the instance should use this certificate for secure communications and signing requests.|
    |**Short Description**|\[Optional\] Enter a text description of the certificate such as the requester or server name.|
    |**Format**|Select the certificate format. The instance supports the PEM and DER formats.|
    |**Type**|Select the certificate container. The instance recognizes certificates from trust stores, Java keystore, and PKCS\#12 keystores.|
    |**PEM Certificate**|Enter the base-64 encoded PEM-formatted text containing the DER certificate. The instance decodes the certificate to populate the **Valid from**, **Expires**, **Expires in days**, **Issuer**, and **Subject** fields.|

4.  Select **Submit**.

    During the upload, the module extracts and displays the certificate's read-only properties in these fields:

    -   Valid from date
    -   Expiration date
    -   Issuer
    -   Subject of the certificate
5.  Select **Validate Stores/Certificates** to check if the certificate is correct.

    If the instance encounters any errors with the certificate or keystore, it displays an error message.


-   **[Uploading a trusted server certificate](t_UploadATrustedServerCertificate.md)**  
By uploading the service provider's trusted server certificate, the instance ensures it is connecting to a valid and secure service.

**Parent Topic:**[Certificates](../concept/c_Certificates.md)

**Related topics**  


[Exploring Certificates](../concept/exploring-certificates.md)

[Generating an LDAP client certificate](t_GenerateAnLDAPClientCertificate.md)

