---
title: Complete mapping and upload Microsoft Word document that includes content controls
description: As a contract configurator, after adding the content controls to the Microsoft Word document to be used for the contract template using the Microsoft Word Add-in for ServiceNow Contracts, upload the document to the ServiceNow instance.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create templates in Microsoft Word, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Complete mapping and upload Microsoft Word document that includes content controls

As a contract configurator, after adding the content controls to the Microsoft Word document to be used for the contract template using the Microsoft Word Add-in for ServiceNow Contracts, upload the document to the ServiceNow instance.

## Before you begin

Add metadata, signatory details, and content controls for the clauses before uploading the document. The uploaded document is parsed for the content controls and data populated into the ServiceNow instance. For more information, see [Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the document in which you have added content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  In the add-in login screen, enter the credentials of the ServiceNow instance from which you downloaded the manifest file.

4.  Select the contract template for which you want to upload the document.

5.  Select **Complete mapping and upload**.

    ![Complete mapping and upload](../image/cmpro-upload-doc.png "Complete mapping and upload")

6.  On the confirmation screen, select **Complete mapping**.

    The contract document is uploaded and the content controls are parsed. The ServiceNow instance is updated with the data from the contract document.


## What to do next

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md).

**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Create a contract template to contain content controls](cncore-create-ct-word-addin.md)

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md)

