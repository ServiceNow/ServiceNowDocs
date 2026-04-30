---
title: Non-disclosure agreement requests in Legal Simple Contracts
description: Employees can submit legal requests for creating non-disclosure agreement \(NDA\) contracts with third parties such as vendors, customers, and partners. The legal department can manage and process these requested changes from a centralized location.
locale: en-US
release: yokohama
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Non-disclosure agreement requests in Legal Simple Contracts

Employees can submit legal requests for creating non-disclosure agreement \(NDA\) contracts with third parties such as vendors, customers, and partners. The legal department can manage and process these requested changes from a centralized location.

## Features

-   Contract templates with metadata and business rules for selecting the most relevant template for a request.
-   Complete self-service for creating standardized NDA contracts.
-   Requests to change the standardized contracts routed to the legal team.
-   Support for electronic signatures.
-   Electronic signature integrations with Adobe Acrobat Sign and Docusign.
-   Support for wet signature to enable effective collaboration between the signatories.
-   Document storage on the ServiceNow instance as well as external storage systems such as Box, Google Drive, and Microsoft OneDrive.
-   Legal contracts repository containing the metadata of signed contract documents.
-   Configurable system property to generate a certification of completion for an electronically signed non-disclosure agreement \(NDA\). For more information, see [Activate a system property to generate a certificate of completion](../task/configure-system-property-COC.md).

## Non-disclosure agreement contract request - Workflow

When a requester submits a legal request, an NDA contract document is created using a standard contract template based on the information from the request. The information from the request is inserted at the appropriate places in the template.

If needed, requesters can request specific changes in the generated NDA contract document. The legal department can manage and process these requested changes to make necessary revisions to the NDA contract document from a centralized location.

If the generated NDA document doesn’t require any changes, the requester can send it to the signatories for an electronic or manual signature. After all signatories have signed the contract document, it’s stored in the ServiceNow instance or an external storage system. The requester and legal department members can access the signed contract document from the Legal Contracts repository.

![Non-disclosure Agreement details](../image/LSD-NDA-wet-signature-view-details.png)

## Workflow for a non-disclosure agreement contract request

A sample workflow for a non-disclosure agreement contract request might progress as follows:

1.  Setting up the following items in the application:
    -   Multiple variations of NDA templates
    -   Template selection rule to choose the correct template based on the legal request
    -   Internal signatories for different templates
    -   E-signature integration - Adobe Acrobat Sign or Docusign
2.  Employee fills out the NDA intake request form.
3.  Employee previews the generated contract with metadata and sends it to the signatories.
4.  All signatories submit the required signatures.
5.  The signed contract is attached to the legal request record.
6.  A contract repository record is created with the metadata and signed contract.
7.  \(Optional\) The signed contract is moved to the configured storage and referenced in the contract repository section.

-   **[Submit a legal request for a NDA](../task/submit-legal-contract-request.md)**  
Submit a legal request for a non-disclosure agreement with third parties such as vendors, customers, or partners.
-   **[Work on a legal contract request](../task/work-on-legal-contract-request.md)**  
As a member of the legal contracts support team, review and revise a contract document as per the requested changes. Upload the revised document to the request and send the document to the requester from within the request.
-   **[Review and finalize the contract document](../task/finalize-contract-document-nda.md)**  
Review and finalize the contract document for sending it for signature.
-   **[Signature process for a legal request](lsd-signature-workflow.md)**  
You can require either an electronic or a wet \(manual\) signature for a legal request. The contract approval process differs depending on the signature type selected.
-   **[Add a manually signed contract](../task/upload-contract-document-for-wet-signature.md)**  
As a legal requester, on receiving the signed contract document from the signatories, add the digital version to the legal request record.

**Parent Topic:**[Legal Simple Contracts](../reference/legal-simple-contracts-landing-page.md)

