---
title: How to automate signing requests using templates
description: Send Docusign signing requests using Docusign templates and information in your ServiceNow instance by creating flows in Flow Designer. For example, Send employee offer .
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Docusign eSignature Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# How to automate signing requests using templates

Send Docusign signing requests using Docusign templates and information in your ServiceNow instance by creating flows in Flow Designer. For example, `Send employee offer` .

## Before you begin

Role required: admin

-   Request Integration Hub subscription
-   Activate Docusign eSignature spoke
-   [Set up Docusign eSignature spoke using JWT grant](setup-docusign-jwt.md#) or [Set up Docusign eSignature spoke using authorization code grant](setup-docusign-authorization-code.md#)

## About this task

**Note:** Customize flows based on your requirements.

## Procedure

1.  In Docusign, create document templates and specify recipient roles, for example, `Candidate` and `Manager`.

    The system retrieves other recipient details such as name and email, when the flow is triggered.

2.  In Workflow Studio, create a new flow.

3.  Specify **TRIGGER** to initiate the flow.

4.  Specify one of the following actions to be performed during the flow and provide recipient details:

    -   **Create Draft Envelope from Template**
    -   **Get Recipient ID by Role Name**
    -   **Add Recipient to Envelope**
    -   **Get Recipient ID by Role Name**
    -   **Add Recipient to Envelope**
    -   **Get Field ID**
    -   **Set Field Value**
    -   **Send Envelope**
    -   **Get Field Value**
5.  Pause the flow until the specified document is signed or rejected by selecting the **Wait for Signature from Docusign** action.

    -   The selected document or Embedded Signing URL is sent to the recipients for signing. While signing the document, the recipient details are auto-populated.
    -   An envelope record is created in the **Envelopes** table. The Envelope status and other details are updated.

