---
title: Add and configure signature blocks using Microsoft Word add-in for ServiceNow Contracts
description: Add and configure signature blocks in contract templates to define signatories, placeholders for signatures, and other metadata in the contract document. Signature blocks are automatically added in the contract document based on the number of signatories specified in the contract request.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring signatories in Contract template using Microsoft Word add-in, Add document content controls using Microsoft Word add-in for ServiceNow Contracts, Creating a contract template using Microsoft Word add-in for ServiceNow Contracts, Configure contract templates, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Add and configure signature blocks using Microsoft Word add-in for ServiceNow Contracts

Add and configure signature blocks in contract templates to define signatories, placeholders for signatures, and other metadata in the contract document. Signature blocks are automatically added in the contract document based on the number of signatories specified in the contract request.

## Before you begin

The Microsoft Word add-in for ServiceNow Contracts must be configured. For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md).

An active contract template must exist in the Draft or Editing state where the **Signature blocks** option is selected. For more information, see [Create a contract template to contain content controls](cncore-create-ct-word-addin.md).

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the document in which you want to map the tables using Microsoft Word add-in.

2.  From the Microsoft Word ribbon, select the ServiceNow Contracts add-in.

3.  On the login screen, enter the credentials of the ServiceNow instance for which the Microsoft Word add-in is configured.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  On the add-in screen in the **Templates** tab, select the contract template to which you want to add the signature metadata.

5.  In the **Signatory** tab, select **Add signatory**.

6.  In the Signatory type section, set the signature type as internal or external, and select **Next**.

    **Note:** You can create one internal signature block and one external signature block.

7.  Define the signature block in the Microsoft Word document.

    1.  Select a placeholder in the Microsoft Word document.

    2.  Select the signature tag.

    3.  Select **Next**.

8.  Insert the items you want to display in the signature block.

    When adding content controls for a signature block, set the font color of the content control tags to match the document’s background color.

    1.  Place the cursor within the signature block.

    2.  Select the tag for the metadata you want to add.

        You can add the following metadata:

        -   Signature
        -   Name
        -   Title
        -   Date
        -   Email
9.  Select **Complete**.

    The signatory fields—such as Name, Title, and Email—are not pre-filled in the contract document before it is sent for signature. These fields will be populated by the electronic signature provider when the signatory access the document to sign it.

10. View the signatory details by navigating to the **Template Mappings** related list of the Contract template form.


## What to do next

Define an internal signatory rule to automatically add signatory details in contract documents using the template. For more information, see [Define an internal signatory rule](cncore-define-internal-signers-rule.md).

**Parent Topic:**[Configuring signatories in Contract template using Microsoft Word add-in](../concept/cncore-config-sign-addin.md)

**Related topics**  


[Add and configure participants for a contract using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-add-signatory.md)

