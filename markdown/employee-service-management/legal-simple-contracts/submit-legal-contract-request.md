---
title: Submit a legal request for a NDA
description: Submit a legal request for a non-disclosure agreement with third parties such as vendors, customers, or partners.
locale: en-US
release: australia
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Non-disclosure agreement requests in Legal Simple Contracts, Requests, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a legal request for a NDA

Submit a legal request for a non-disclosure agreement with third parties such as vendors, customers, or partners.

## Before you begin

Role required: sn\_lg\_ops.legal\_user

## Procedure

1.  Access the non-disclosure agreement intake form.

<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d225333e71">

Option

</th><th align="left" id="d225333e74">

Description

</th></tr></thead><tbody><tr><td id="d225333e80">

**Using __Employee Center__**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**
2.  Select **Legal** &gt; **Browse all Legal** from the header.
3.  Search for and open the **Non-disclosure agreement** request item.


</td></tr><tr><td id="d225333e123">

**Using __Legal Service Portal__**

</td><td>

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Service Portal**
2.  Select **Service Catalog**.
3.  Search for and open the **Non-disclosure agreement** request item.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_contract_request_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Is this for a Vendor, Customer, or Partner?

</td><td>

Category of the third party.

</td></tr><tr><td>

Purpose of the Agreement

</td><td>

Purpose of the agreement. Example: Non-disclosure agreement for new business investments.

</td></tr><tr><td>

Company legal name

</td><td>

Legal name of the third party with whom you are making an agreement.If the company name isn’t listed, select **\[Company not listed\]** option and enter the name in the **New company legal name**.

</td></tr><tr><td>

Address

</td><td>

Mailing address of the third party.

</td></tr><tr><td>

Country

</td><td>

Country of the third party.

</td></tr><tr><td>

Start date

</td><td>

Start date of the agreement period.

</td></tr><tr><td>

Signature type

</td><td>

Type of signature.-   Electronic signature: The signatory digitally signs the contract.
-   Wet signature: The signatory manually signs the physical version of the contract.
The default signature type is Electronic Signature.

</td></tr><tr><td>

External signatory details

</td><td>

List of people from the selected third party who would sign the agreement.

</td></tr></tbody>
</table>3.  Modify the list of signatories.

    -   To add a signatory, select **Add** and provide the signatory's details.

    -   To modify a signatory's information, select the Edit row icon \(![Edit row icon.](../../legal-digital-forensics/image/rename-icon.png)\) on the signatory's row and update the details.

    -   To remove a signatory, select the Remove row icon \(![Remove row icon.](../../legal-digital-forensics/image/delete-icon.png)\) on the signatory's row.

4.  Select **Submit**.

    -   A legal request for generating a contract document for non-disclosure agreement is created in the New state.
    -   A contract document in the Document Ready status is generated with data from the request using a contract template based on the contract template rules. Internal signatories based on the template are also populated in the generated document. For more information, see [Configure a rule for selecting a legal contract template](configure-legal-contract-template-rules.md).

        **Note:**

        -   If more signatories have been added in the request than are needed for the contract as defined in the contract template, only the default number of signatories are necessary for signing the contract. Other signatories are marked as Not Considered.
        -   If fewer signatories are included in the request than are required for the contract, you can add more signatories.
        In either case, you can submit a change request to update the number of signatories as required for your contract.

    -   A record for each external signatory is created in the Signer \[sn\_lg\_contracts\_signer\] table.
    For more information on how to view and track a legal request, see [View and track legal request details](../../legal-request-management/task/view-legal-request-details.md).

5.  If you need changes in the generated document, submit a change request to the legal department.

    For more information, see [Review and finalize the contract document](finalize-contract-document-nda.md).

6.  Modify the request details or manage signatories by selecting **Actions** and then selecting **Edit Request**.

    This option is available only if the request state is New and the document status is Document Ready. For more information, see [Modify a legal request](update-legal-contract-request-tpc.md).

7.  When the contract document is finalized, send it to the signatories for getting it signed.

    For more information, see [Review and finalize the contract document](finalize-contract-document-nda.md).


**Parent Topic:**[Non-disclosure agreement requests in Legal Simple Contracts](../concept/legal-request-nda.md)

