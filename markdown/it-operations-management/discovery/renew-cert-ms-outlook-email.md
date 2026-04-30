---
title: Renew a certificate via MS Outlook email notification
description: A user receives a notification via email 60 days before a certificate expires. A task is made to manually renew the certificate. This notification is sent directly to your email. In this email, you can take direct action to renew the certificate.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-23"
reading_time_minutes: 1
breadcrumb: [Configure for MS Outlook email notification certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Renew a certificate via MS Outlook email notification

A user receives a notification via email 60 days before a certificate expires. A task is made to manually renew the certificate. This notification is sent directly to your email. In this email, you can take direct action to renew the certificate.

## Before you begin

Before you begin: You need your certificate CSR. It can be the raw CSR info, or a .csr or .pem file. If you don’t have one, you can instruct the system to use a previous one.

Role required: pki\_admin or admin

## Procedure

1.  Select “Renew through email,” in the email itself.

    **Note:** Once you click the link, a new email will appear. It’s the request to renew the certificate. To renew, choose one of four changes to the email and send it.

2.  Add your CSR in one of the following ways:

    1.  Attach a CSR file in .csr or .pem format and select **send**.

    2.  Paste the CSR directly and select **send**.

    3.  Replace the text in the subject line called &lt;Renewal Option&gt; with the text AUTO-CSR and select send.

        **Note:** This will generate a new CSR where the private key is stored securely in your vault.

    4.  Replace the text in the subject line called &lt;Renewal Option&gt; with the text RP-CSR and select **send**.

        **Note:** The system will reuse a previous CSR from an older certificate request.

3.  Select **click here to approve** or **click here to reject** in the following email notification.

    **Note:** Once you send the email request to renew your certificate, you will immediately receive an email notification asking you to give final approval or to reject the certificate renewal.


## Result

Upon approval, you will have a renewed certificate.

