---
title: Sign document templates for PDF documents using CAC or PIV smart card
description: Use the PDF document template to initiate digital signing, review, and generate a filled PDF document using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Digital signature for PDF documents using CAC or PIV smart cards, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Sign document templates for PDF documents using CAC or PIV smart card

Use the PDF document template to initiate digital signing, review, and generate a filled PDF document using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card.

## Before you begin

Adobe Acrobat Reader must be installed on your desktop.

A document template must be set up for signing documents. For more information, see [Set up a document template for signing documents using a CAC or PIV smart card](create-document-template.md).

Role required: none

## About this task

## Procedure

1.  Initiate the PDF document signing process with a custom implementation using script.

    For more information, see [Using Document Templates: Custom use case](https://www.servicenow.com/docs/access?context=doc-temp-gen&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

    **Note:** HR cases can skip this step as custom implementation using scripts is for cases related to non-HR applications.

2.  Sign the PDF document in Service Portal.

    -   To navigate through the Employee Center, navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
    -   To navigate through My Document Tasks, navigate to**Self-Service** &gt; **My Document Tasks**.
3.  Select the document task that is assigned to you.

4.  Review the PDF document and select **Sign Document** to sign the document or **Reject** to reject the document.

    The signed document opens as a PDF document in Adobe Acrobat Reader.

5.  Go to the sign location to click and select the mapped certificate or Digital ID file.

6.  Enter the password for the Digital ID file, select **Sign**, and save the signed copy.

7.  In the PDF document, select send to send the signed PDF document.

    The signed document is uploaded to the document task for verification.

8.  Go to the **My Document Tasks** and select the document, review and select **Validate Document** to validate the document or select **Reject** to reject the document.

    The signature is successfully captured and authenticated after document validation.


**Parent Topic:**[Digital signature for PDF documents using CAC or PIV smart cards](../concept/digital-signature.md)

