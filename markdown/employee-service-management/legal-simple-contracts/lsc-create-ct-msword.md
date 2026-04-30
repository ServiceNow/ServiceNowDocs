---
title: Create a Microsoft Word legal contract template
description: Create a legal contract template in Microsoft Word format that can be used to generate a standard contract with predefined content when an employee submits a contract request.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure legal contract templates of type Microsoft Word, Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create a Microsoft Word legal contract template

Create a legal contract template in Microsoft Word format that can be used to generate a standard contract with predefined content when an employee submits a contract request.

## Before you begin

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Select **New**.

3.  Select **Word Document Template**.

4.  On the Word Template New Record form, fill in the fields.

    For a description of the field values, see [Word Template New Record form](../reference/lsc-word-tmple-rec-form.md).

5.  Extract the content marked by the supported content controls from the imported document by selecting **Parse Document**.

    The supported content controls are:

    -   **field** - Indicates metadata
    -   **signature\_** - Indicates a signature
    -   **sign\_date\_** - Indicates the signing date
    For more information on the supported content controls and tagging guidelines, see [Add content controls in a Microsoft Word document](lsc-cont-contr-word-tmplt.md).

    The content controls derived from the documentare listed in the Template mappings related list.

6.  Select **Save**.


## Result

The contract template is saved in the Draft state.

**Parent Topic:**[Configure legal contract templates of type Microsoft Word](lsc-configure-ct-msword.md)

**Related topics**  


[Add content controls in a Microsoft Word document](lsc-cont-contr-word-tmplt.md)

[Create and configure participants for legal contract template](lsc-add-config-participants-msword.md)

[Update contract template mappings for legal contract template](lsc-template-map-msword.md)

[Publish a contract template](lsc-publish-word-template.md)

