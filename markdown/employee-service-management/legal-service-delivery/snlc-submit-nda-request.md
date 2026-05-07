---
title: Submit a legal request for a non-disclosure agreement
description: Submit a legal request for a non-disclosure agreement \(NDA\) with third parties such as vendors, customers, or partners.
locale: en-US
release: australia
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Non-disclosure agreement requests, Use, Contract Management Pro for Legal Service Delivery, Integration with ServiceNow applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Submit a legal request for a non-disclosure agreement

Submit a legal request for a non-disclosure agreement \(NDA\) with third parties such as vendors, customers, or partners.

## Before you begin

-   The contract type must be active.
-   Role required:
    -   sn\_lg\_ops.legal\_user and sn\_cm\_core.contract\_user

## Procedure

1.  Access the non-disclosure agreement intake form.

<table id="choicetable_vvd_bng_hxb"><thead><tr><th align="left" id="d392380e85">

Method

</th><th align="left" id="d392380e88">

Actions

</th></tr></thead><tbody><tr><td id="d392380e94">

**__Employee Center__**

</td><td>

1.  Navigate to **All** &gt; **Employee Center**.
2.  Select **Legal** &gt; **Browse all Legal** from the header.
3.  Search for and open the **Non-disclosure agreement** request item.


</td></tr><tr><td id="d392380e139">

**__Legal Service Portal__**

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

Requested For

</td><td>

User for whom you want to submit a legal request. This field is visible only when you are a legal fulfiller with the sn\_lg\_cnt.contract\_fulfiller role.

</td></tr><tr><td>

Contract party type

</td><td>

Category of the third party entity with whom the contract has to be signed.

</td></tr><tr><td>

Purpose of the contract

</td><td>

Purpose of the agreement. Example: Non-disclosure agreement for new business investments.

</td></tr><tr><td>

Company

</td><td>

Legal name of the third party with whom you are making an agreement.If the company name isn’t listed, select the **\[Company not listed\]** option and enter the name in the **New company legal name** field.

</td></tr><tr><td>

Address

</td><td>

Mailing address of the third party.

</td></tr><tr><td>

Country

</td><td>

Country of the third party.

</td></tr><tr><td>

Contract start date

</td><td>

Start date of the contract period.

</td></tr><tr><td>

Contract end date

</td><td>

End date of the contract period.

</td></tr><tr><td>

External signatory details

</td><td>

List of people from the selected third party who should sign the agreement.

</td></tr><tr><td>

Signature type

</td><td>

Type of signature.-   Electronic signature: The signatory electronically signs the contract.
-   Wet signature: The signatory manually signs the physical version of the contract.
The default signature type is Electronic Signature.

</td></tr></tbody>
</table>3.  Modify the list of signatories.

    -   To add a signatory, select **Add** and provide the signatory's details.

    -   To modify a signatory's information, select the Edit row icon \(![Edit row icon.](../../legal-digital-forensics/image/rename-icon.png)\) on the signatory's row and update the details.

    -   To remove a signatory, select the Remove row icon \(![Remove row icon.](../../legal-digital-forensics/image/delete-icon.png)\) on the signatory's row.

4.  Select **Submit**.

5.  Modify the request details or manage signatories by selecting **Actions** and then selecting **Edit Request**.

    This option is available only if the request state is Draft or Work in progress. For more information, see [Modify a non-disclosure agreement legal request](snlc-modify-nda-req.md).


## Result

-   A legal request is submitted and a contract request is created for generating contract documents.
    -   If there are no validation errors, a contract request is created in the Work in progress state.
    -   If there is a validation error due to incorrect signatory information, a contract request is created in Draft state.
-   If a contract template rule or contract configuration is not available, a contract request will not be created. The contract configurator should correct the configuration to trigger contract request creation. The legal request remains in Draft state.
-   Version 1.0 of a contract document is generated and listed in the **Contract Document** tab of the contract request.
-   The contract document generation process involves:
    -   Using the correct contract template based on contract template rules.
    -   Replacing the metadata with data from the request.
    -   Replacing the signatory information.
    -   Placing the content of the clauses in the contract document according to the clause variation rules.
-   Internal signatories based on the template are also populated in the generated document. For more information, see [Define an internal signatory rule](../../contract-mgmt-pro/task/cncore-define-internal-signers-rule.md).

    **Note:**

    -   If more signatories have been added in the request than are needed for the contract as defined in the contract template, only the default number of signatories are necessary for signing the contract. Other signatories are marked as Not Considered.
    -   If fewer signatories are included in the request than are required for the contract, you can add more signatories.
    A record for each external signatory is created in the Signer \[sn\_cm\_core\_signer\] table.


For more information on how to view and track a legal request, see [View and track non-disclosure agreement requests as a legal user](snlc-view-legal-req-details.md).

**Parent Topic:**[Non-disclosure agreement requests](../concept/snlc-request-nda-1.md)

