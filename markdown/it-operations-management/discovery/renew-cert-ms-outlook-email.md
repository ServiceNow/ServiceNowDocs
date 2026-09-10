---
title: Renew certificates via email
description: Certificate renewal notifications are sent to users configured in the Certificate notification policy table via email 60 days before a certificate expires or after a certificate expires.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/renew-cert-ms-outlook-email.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "0256-02-23"
reading_time_minutes: 1
breadcrumb: [Certificate alerts and notifications, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Renew certificates via email

Certificate renewal notifications are sent to users configured in the **Certificate notification policy** table via email 60 days before a certificate expires or after a certificate expires.

## Before you begin

-   You must have certificate CSR information to paste or in a .csr or .pem format. If you don’t have one, you can instruct the system to generate a new one or use a previous one.
-   Role required: pki\_admin or admin

## Procedure

1.  Open the email and select Renew through email.

    Opening the link triggers a new email. It’s the request to renew the certificate.

2.  Open the renewal email.

3.  Add the CSR in one of the following ways:

    -   Attach a CSR file in .csr or .pem format.
    -   Paste the CSR directly.
    -   To generate a new CSR, replace the text in the subject line called &lt;Renewal Option&gt; with the text `AUTO-CSR`.

        **Note:** This generates a new CSR and the private key is stored securely in your vault.

    -   To use the previous CSR, replace the text in the subject line called &lt;Renewal Option&gt; with the text `RP-CSR`.

        **Note:** The system reuses the CSR from the previous certificate request.

4.  Select **Send**.

    Your manager receives an email notification for final approval or rejection of the certificate renewal.

5.  To approve the certificate renewal request, select **Click here to approve** in the email.


## Result

The certificate renewal is complete.

**Parent Topic:**[Certificate alerts and notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/cert-inventory-mgmt-workflow.md)

