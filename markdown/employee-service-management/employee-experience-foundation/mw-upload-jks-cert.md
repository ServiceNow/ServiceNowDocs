---
title: Upload Java KeyStore certificate
description: Upload a Java KeyStore certificate and specify the password that's sent in Moveworks encrypted email.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Moveworks for Employee Center, Unified Employee Experience, Employee Service Management]
---

# Upload Java KeyStore certificate

Upload a Java KeyStore certificate and specify the password that's sent in Moveworks encrypted email.

## Before you begin

Ensure you have the encrypted email from Moveworks to set up secure connection.

You can generate a self-signed JWT certificate \(valid for 2 years\) for use with Moveworks for Web. For more information, see [JWT Certificate Generation Guide \(Mac and Windows\)](https://docs.moveworks.com/ai-assistant/ai-assistant-web-surfaces/moveworks-for-web/moveworks-for-web-installation-servicenow#jwt-certificate-generation-guide-mac--windows)

**Note:** You must've purchased Moveworks and implemented it for the self-signing to work.

Role required: admin or OAuth admin

## About this task

Certificate authentication creates encrypted communication between your ServiceNow instance and the Moveworks platform. You must upload the JKS certificate file and configure the keystore password in both the certificate record and JWT key provider.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Search for **moveworks.jks** in the certificate list.

    ![Moveworks JKS](../images/mw-jks-key.png "Moveworks JKS certificate")

3.  Open the certificate record and upload the certificate file.

    1.  Select the **Manage Attachments** \(![](../../workplace-central/images/attachment-icon.png)\) icon.
    2.  Upload your **moveworks.jks** file.
4.  Enter the password in the **Key Store Password** field.

    ![Validate Stores and certificates](../images/mw-jks-certificate.png "JKS password")

    **Note:** This password you receive from Moveworks team.

5.  Select **Validate Stores and Certificates**.

    The system validates the certificate with no errors and displays `Valid key_store` message.

    **Note:** [Contact Moveworks support](https://help.moveworks.com/docs/support#how-to-contact-moveworks-support) for troubleshooting.

6.  Navigate to **System Definition** &gt; **JWT Providers**.

    1.  In the Signing configuration field, verify if `Moveworks JWT Provider` is selected.

    2.  Select the info icon \(![preview icon](../../wsd-reservation-management/image/info-icon.png)\).

    3.  Select **Open Record** in the pop-up.

    4.  In the Moveworks JWT key window, enter the same **Key Store Password** in the **Signing Key** field.

7.  Select **Save** or **Update**.


## Result

Certificate authentication is configured. JWT tokens can now be generated for secure communication between ServiceNow and Moveworks services.

## What to do next

Proceed to add bot ID to complete the Moveworks AI assistant setup.

**Related topics**  


[Moveworks for Employee Center reference](../reference/mw-ec-integration-reference.md)

