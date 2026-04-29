---
title: How to automate on-demand signing requests
description: Send Docusign on-demand signing requests using information in your ServiceNow instance by creating flows in Flow Designer.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# How to automate on-demand signing requests

Send Docusign on-demand signing requests using information in your ServiceNow instance by creating flows in Flow Designer.

## Before you begin

-   Request Integration Hub subscription
-   Activate Docusign spoke
-   Role required: admin
-   [Set up Docusign eSignature spoke using JWT grant](setup-docusign-jwt.md#) or [Set up Docusign eSignature spoke using authorization code grant](setup-docusign-authorization-code.md#)

## About this task

**Note:** Customize flows in Flow Designer based on your requirements.

## Procedure

1.  In Workflow Studio, create a flow.

2.  Specify **TRIGGER** to initiate the flow.

3.  Specify one of the following actions to be performed during the flow:

    -   **Send Adhoc Signature Request To User**
    -   **Send Adhoc Signature Request To Users - Inline**
4.  To pause the flow until the specified document is signed or rejected, select the **Wait for Signature from Docusign** action.

5.  Perform one of the following set of actions:

    -   To send an embedded signing URL, select **Use Embedded Signing**, and **Embedded Signing Recipient \[User\]**.
    -   To send a document for signing, provide details regarding Docusign account, PDF document, recipient, email, and envelope expiry.
    -   The selected document or Embedded Signing URL is sent to the recipients for signing. While signing the document, the recipient details are auto-populated.
    -   An envelope record is created in the **Envelopes** table. The Envelope status and other details are updated.

