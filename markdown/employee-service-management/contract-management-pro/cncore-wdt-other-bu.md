---
title: Configure document templates for standard letters or documents
description: Create Word Document Templates to create standard letters or documents that can be signed by configured participants.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure document templates for standard letters or documents

Create Word Document Templates to create standard letters or documents that can be signed by configured participants.

## Document template flow

Document templates can be used by business units other than Legal to generate standard documents. For example, you can use the Word Document Templates feature to generate a standard response template.

The following flow describes how you can use a Microsoft Word document template from configuring the template through attaching the signed Microsoft Word document to a case.

-   Set [Content controls in Word Document Templates](../concept/cncore-wdt-doc-contentctrl.md).
-   [Configure a Microsoft Word document template](cncore-wdt-config-word-doc.md).
-   [Create participants for document templates](cncore-wdt-create-participant.md)
-   Insert signatures.
-   Publish the Microsoft Word document template.
-   [Document tasks generation](../../human-resources/task/task-mapped-participants.md).
    -   An internal ServiceNow user receives a document task for signing the Microsoft Word document. An external user receives the Microsoft Word document for signing via an email.
    -   After all the document tasks are completed, the work notes are updated and the signed PDF document is added as an attachment to the case.

-   **[Content controls in Word Document Templates](../concept/cncore-wdt-doc-contentctrl.md)**  
Word Document Templates supports content controls that act as placeholder for the content.
-   **[Configure a Microsoft Word document template](cncore-wdt-config-word-doc.md)**  
Upload a word document and add participants with whom you require signatures.
-   **[Create participants for document templates](cncore-wdt-create-participant.md)**  
Define actions and the order of actions for participants. The type of action and order are considered while initiating document tasks.

**Parent Topic:**[Configure Contract Management Pro](../concept/cncore-config-cmpro.md)

**Related topics**  


[Install Contract Management Pro](cncore-install-cmpro.md)

[Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

[Configure contract templates for a contract request](../concept/cncore-document-templates.md)

[Add and configure contract request functionality](../concept/cncore-uptake-steps.md)

[Configuring Contract Workspace with UI Builder components](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure Obligation Management notifications](cncore-config-ob-mgmt-notf.md)

