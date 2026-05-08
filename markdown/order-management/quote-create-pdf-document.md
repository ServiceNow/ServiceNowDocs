---
title: Create a quote PDF document
description: In Quote Management, sales agents can create a PDF of a quote that can be sent to customers for review and signatures.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Quote Management, Configure, price, quote apps, Use, Sales Customer Relationship Management]
---

# Create a quote PDF document

In Quote Management, sales agents can create a PDF of a quote that can be sent to customers for review and signatures.

## Before you begin

Create a quote PDF document

Role required: sales\_agent

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Quotes** &gt; **All**.

3.  Select the quote that you’re working with.

4.  On the **Details** tab, go to **Quote Document Details** and fill in the fields.

<table id="choicetable_sbm_qvt_pdc"><tbody><tr><td id="d92790e102">

**Document template**

</td><td>

A document template is required to create a quote document PDF. A standardized template is included with the base system. Select the template that you want. See [Set up PDF document templates](quote-mgt-setup-pdf-document-templates.md) for more information about how to create customized templates.

</td></tr><tr><td id="d92790e121">

**External signer**

</td><td>

Option that enables you to have the quote document signed by someone outside the organization. See [Set up PDF document signers](quote-mgt-configure-pdf-document-signers.md) for more details on how to set up external signers. When you select **Send for signature**, the external signer's email address is used to send an email through Docusign for review and electronic signature.

</td></tr><tr><td id="d92790e148">

**Internal signer**

</td><td>

Option that lets you select an internal signer for the quote. When you select **Send for signature**, the internal signer's email address is used to send an email using Docusign for review and signature.

See [Set up PDF document signers](quote-mgt-configure-pdf-document-signers.md) for more details about how to set up an internal signer.

</td></tr></tbody>
</table>5.  Select **Save**.

6.  In the Quote form, select **Generate Document**.

    The PDF document is generated and appears in the **Attachment** side window.

7.  Select the attachment icon to ![](../../../reuse/icons/product-icons/paperclip-outline-24.svg) open the attachments window.

8.  Select the actions icon ![](../image/icon-three-dots.png) and choose an action for your PDF document.

    |Choice|Description|
    |------|-----------|
    |**Download**|Agents can download a document that enables them to send is a different way.|
    |**Remove**|This option deletes the document.|
    |**Rename**|This choice enables agents to rename the document.|
    |**Send for signature**|Agents use this option to send the document for signatures. The document is sent to the signers indicated on the Quote details tab under Quote document.|

    A message appears indicating that the PDF document was generated.

9.  To view the generated PDF, select the PDF in the attachments window.![](../image/quote-attachment-window-pdf.png)


**Parent Topic:**[Using Quote Management](../concept/quote-mgmt-using.md)

