---
title: Upload and parse a Microsoft Word document that includes content controls
description: As a contract configurator, after adding the content controls to the Microsoft Word document to be used for the contract template using the Microsoft Word Add-in for ServiceNow Contracts, upload the document to the ServiceNow instance.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Upload and parse a Microsoft Word document that includes content controls

As a contract configurator, after adding the content controls to the Microsoft Word document to be used for the contract template using the Microsoft Word Add-in for ServiceNow Contracts, upload the document to the ServiceNow instance.

## Before you begin

Add metadata, signatory details, and content controls for the clauses before uploading the document. The uploaded document is parsed for the content controls and data populated into the ServiceNow instance. For more information, see [Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the document in which you have included content controls in Microsoft Word.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  In the add-in login screen, enter the credentials of the ServiceNow instance from which you downloaded the manifest file.

4.  Select **Proceed to select a document**.

5.  In the Select Attachment screen, select **Attach file** and select the same file that includes the content controls.

    If the file name of the document you are uploading and the one uploaded in the contract template are different, you are asked to confirm proceeding with the upload.

6.  Select **Upload and parse document** to replace the existing document in the contract template with the one you are uploading and parse the content controls in the ServiceNow instance.


## What to do next

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md).

**Parent Topic:**[Creating a contract template using Microsoft Word add-in for ServiceNow Contracts](../concept/cncore-setup-ct-add-in.md)

**Related topics**  


[Create a contract template to contain content controls](cncore-create-ct-word-addin.md)

[Add document content controls using Microsoft Word add-in for ServiceNow Contracts](cncore-add-contrl-wrd-addin.md)

[Complete clause mapping to build a clause library](cncore-clause-map-addin.md)

[Add conditions for a contract table mapping](cncore-add-filter-table-map.md)

