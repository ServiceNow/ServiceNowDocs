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
breadcrumb: [Moveworks for Employee Center, Employee Center Integrations, Unified Employee Experience, Employee Service Management]
---

# Upload Java KeyStore certificate

Upload a Java KeyStore certificate and specify the password that's sent in Moveworks encrypted email.

## Before you begin

Ensure you have the encrypted email from Moveworks to set up secure connection.

**Note:** Follow the instructions available at [Contact Moveworks support](https://help.moveworks.com/docs/support#how-to-contact-moveworks-support) to receive encrypted email.

Role required: admin or OAuth admin

## About this task

Certificate authentication creates encrypted communication between your ServiceNow instance and the Moveworks platform. You must upload the JKS certificate file and configure the keystore password in both the certificate record and JWT key provider.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Search for **moveworks.jks** in the certificate list.

    ![Moveworks JKS](../images/mw-jks-key.png "Moveworks JKS certificate")

3.  Open the certificate record and upload the certificate file.

    1.  Select the **Attachment** option.
    2.  Upload your **moveworks.jks** file.
4.  Enter the password in the **Key Store Password** field.

    ![Validate Stores and certificates](../images/mw-jks-certificate.png "JKS password")

    **Note:** This password you receive from Moveworks team.

5.  Select **Validate Stores and Certificates**.

    The system validates the certificate with no errors and displays `Valid key_store` message.

    **Note:** [Contact Moveworks support](https://help.moveworks.com/docs/support#how-to-contact-moveworks-support) for troubleshooting.

6.  Navigate to **System Definition** &gt; **JWT Providers**.

    1.  Find the `Moveworks JWT Provider` entry in the list and open it.

    2.  Enter the same **Key Store Password** in the **Signing Key** field.

7.  Select **Save** or **Update**.


## Result

Certificate authentication is configured. JWT tokens can now be generated for secure communication between ServiceNow and Moveworks services.

## What to do next

Proceed to add bot ID to complete the Moveworks AI assistant setup.

**Related topics**  


[Moveworks for Employee Center reference](../reference/mw-ec-integration-reference.md)

