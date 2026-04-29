---
title: Create and configure participants for legal contract template
description: Add and configure participants that act as placeholder for users who will be assigned as signers of a contract document.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure legal contract templates of type Microsoft Word, Legal contract templates, Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Create and configure participants for legal contract template

Add and configure participants that act as placeholder for users who will be assigned as signers of a contract document.

## Before you begin

A Microsoft Word document must have been uploaded and parsed to provide template mappings for the contract template. For more information, see [Create a Microsoft Word legal contract template](lsc-create-ct-msword.md).

Role required: sn\_lg\_contracts.contracts\_config

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Simple Contracts Admin** &gt; **Contract Templates**.

2.  Open a contract template.

3.  In the Participants related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_lld_cps_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique display name of the mapped participant. **Note:** The length of the name should be equal to or less than the length allocated in the Word document template for a signer.

</td></tr><tr><td>

Order

</td><td>

Order in which the signature request will be initiated for the participant.

</td></tr><tr><td>

Signer

</td><td>

User field from the list of fields that are populated from the Signer \[sn\_lg\_contracts\_signer\] table.**Note:** You can select only the highlighted user fields.

The user in the mapped field is automatically added as a signatory in the document.

</td></tr></tbody>
</table>5.  Select **Submit**.


**Parent Topic:**[Configure legal contract templates of type Microsoft Word](lsc-configure-ct-msword.md)

**Related topics**  


[Add content controls in a Microsoft Word document](lsc-cont-contr-word-tmplt.md)

[Create a Microsoft Word legal contract template](lsc-create-ct-msword.md)

[Update contract template mappings for legal contract template](lsc-template-map-msword.md)

[Publish a contract template](lsc-publish-word-template.md)

