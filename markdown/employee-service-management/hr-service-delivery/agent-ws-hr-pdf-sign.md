---
title: E-signature in HR Service Delivery Agent Workspace
description: When working on an HR case or HR task, you can use e-signature to sign documents that require signatures.Depending on the case or situation, you can electronically sign a document.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using the HR Service Delivery Agent Workspace, HR Service Delivery Agent Workspace \(Classic\), HR Service Delivery, Employee Service Management]
---

# E-signature in HR Service Delivery Agent Workspace

When working on an HR case or HR task, you can use e-signature to sign documents that require signatures.

When an employee creates a case requesting an employment verification letter, you can:

-   Preview the document.
-   Use e-signature to sign it.
-   Generate the document.

Previewing a document ensures you sign the correct document. This step is useful if you have multiple employment verification letters.

E-signature provides multiple methods to sign. You can choose to type your name or use your mouse to draw your signature. For more information, see [Sign and generate a document in HR Service Delivery Agent Workspace](agent-ws-hr-pdf-sign.md#).

You can optionally require a user to check an acknowledgment box before the signature is accepted.

Generating the document combines the document template with your signature and creates an attachment to the case. If you use Employee Document Management, you can move the attachment to your document repository for storage.

**Note:** For more information, see [Configure an e-signature template](https://www.servicenow.com/docs/access?context=configure-e-signature-configuration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Sign and generate a document in HR Service Delivery Agent Workspace

Depending on the case or situation, you can electronically sign a document.

### Before you begin

Role required: sn\_hr\_core.case\_writer

### Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **HR Agent Workspace**.

2.  Locate and open an HR case.

    Ensure that the state of the case is **Work in Progress**.

3.  Select the **Sign Document** button.

    ![HR case - Sign Document button](../reference/images/agent-ws-hr-pdf-3.png)

4.  Preview the document.

    Ensure it is the correct document for the case.![HR case - Sign document](../reference/images/agent-ws-hr-pdf-4.png)

5.  You have two choices on how to sign the document.

    1.  Select **Type signature** to type your signature.

    2.  Or, select **Draw signature** to draw your signature using your mouse.

6.  Select Generate to attach your signature to the document.

    ![HR case - Generate document](../reference/images/agent-ws-hr-pdf-5.png)

7.  Select the ![Attachment icon](../image/attach-icon.png) Attachments icon.

    ![HR case - Attachments](../reference/images/agent-ws-hr-pdf-6.png)

    The document moves to Attachments in the contextual side panel. If your company uses Employee Document Management \(EDM\), you can move the document to the EDM repository. For more information on EDM, see [Create or upload employee documents using HR Service Delivery Agent Workspace](agent-ws-hr-edm.md#).


