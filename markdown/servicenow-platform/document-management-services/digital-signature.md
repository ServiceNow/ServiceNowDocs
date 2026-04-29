---
title: Digital signature for PDF documents using CAC or PIV smart cards
description: Use digital signatures to make the document signing experience seamless and to eliminate manual intervention by using your Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) smart card.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Digital signature for PDF documents using CAC or PIV smart cards

Use digital signatures to make the document signing experience seamless and to eliminate manual intervention by using your Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) smart card.

## CAC or PIV cards

The Common Access Card \(CAC\) and Personal Identification Verification \(PIV\) are smart cards used for general identification and authentication of user access. CAC and PIV hold a unique digital certificate and user information such as a photograph, personal identification number \(PIN\), and signature to identify each user.

## Sign PDF documents

ServiceNow enables you to integrate with Adobe, as well as configure and use PIV or CAC smart cards as an authenticator for digital signing of PDF documents. This integration provides the flexibility to use PIV or CAC cards to safeguard critical and valuable assets.

The Adobe Acrobat Reader desktop application enables you to digitally sign a PDF with CAC or PIV smart cards.

**Note:** You should do the following to digitally sign a PDF with CAC or PIV smart cards:

-   Install Adobe Acrobat Reader on your desktop.
-   Configure your Google Chrome or Mozilla Firefox browser to open downloaded PDFs in Adobe Acrobat Reader.

## Document template for digital signature

Digital signing for documents is configured with a document template. You must define document templates and signing workflows for digital signature using smart cards to generate and send auto-filled documents to be signed by different participants.

To configure digital signing for CAC or PIV smart cards, the following must be done:

-   Use [Document Templates](https://www.servicenow.com/docs/access?context=document-templates-overview&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) to create and upload a PDF document
-   Set up certificates in the sys\_ca\_certificate table
-   Set up a map certificate in the sys\_user\_certificate table
-   [Review the **com.snc.pdfsigning.validation.method** property](../reference/property-value-cac-piv-signing.md)
-   Sign and review the PDF document

-   **[Install Document Template integration with digital signatures using a smart card](../task/install-document-template-digital-signatures.md)**  
You can install the Document Template integration with Digital Signatures using Smart Cards application \(com.sn.dt-digital-signature-smart-card-integration\) if you have the admin role.
-   **[Set up a document template for signing documents using a CAC or PIV smart card](../task/create-document-template.md)**  
Set up a document template for PDF using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card. Set up certificates to automate and simplify the process of filling, reviewing, and signing a document online.
-   **[Sign document templates for PDF documents using CAC or PIV smart card](../task/sign-pdf-documents-cac-piv.md)**  
Use the PDF document template to initiate digital signing, review, and generate a filled PDF document using a Common Access Card \(CAC\) or Personal Identification Verification \(PIV\) card.
-   **[Review the digitally signed document](../task/review-signed-documents.md)**  
Review the digitally signed PDF document to either approve or reject it.

**Parent Topic:**[Using Document Management](using-document-management.md)

