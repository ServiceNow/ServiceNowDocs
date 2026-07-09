---
title: Signatory roles
description: Signatory roles define how each participant interacts with a contract document during the signature workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cncore-signatory-roles.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 3
keywords: [signatory role, signer, viewer, receiver, approver, signatory status]
breadcrumb: [Reference, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Signatory roles

Signatory roles define how each participant interacts with a contract document during the signature workflow.

## Signatory role types

**Note:** Signatory roles apply to Docusign electronic signature integrations. Signatory roles are available only for signature block-based contract templates. The **Signatory role** field is not displayed for participant-based templates.

|Role|Description|
|----|-----------|
|**Signer**|Signs the contract document. This is the default role for all signatories.|
|**Viewer**|Views the contract document during the electronic signature workflow. Does not sign the document.|
|**Receiver**|Receives a copy of the signed contract document after all signatories have completed their actions.|
|**Approver**|Approves the contract document in the electronic signature tool before signing begins.|

## Role availability by signature type

The following table describes field availability for each role across signature types.

|Role|Electronic signature|Wet signature|Offline signature|
|----|--------------------|-------------|-----------------|
|**Signer**|Available|Available|Available|
|**Viewer**|Available|Inactive|Inactive|
|**Receiver**|Available|Inactive|Inactive|
|**Approver**|Available|Inactive|Inactive|

**Note:** When you switch the signature type from electronic signature to wet signature or offline signature, signatories with Viewer, Receiver, or Approver roles become inactive. These signatories no longer appear in the Signatories tab. If you switch back to electronic signature, these signatories are reactivated and appear again in the Signatories tab.

## Signatory task statuses

The following table describes signatory task statuses in a contract request.

|Status|Description|
|------|-----------|
|**Not started**|The signature request has not been sent to the signatory.|
|**Pending**|The signature request has been sent and is awaiting action from the signatory.|
|**Completed**|The signatory has signed the contract document.|
|**Declined**|The signatory has declined the contract document.|

## System property

<table id="table_property"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

Enable signatory roles for DocuSign

 `sn_cm_core.enable_docusign_signature_roles`

</td><td>

Controls the visibility of the **Role** field in internal signatory rules, and the **Signatory Role** field in the Employee Center portal and Contract Workspace.To enable this property, see [Enable signatory roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-enable-signatory-roles.md).

</td><td>

`false`

</td></tr></tbody>
</table>**Parent Topic:**[Contract Management Pro reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-ref.md)

**Related topics**  


[Components installed with Contract Management Pro]()

[Components installed with Contract Workspace]()

[Components installed with Analytics Pack for Contract Management Pro]()

[Contract request State and Contract document status in Contract Management Pro]()

[Clause Variation form]()

[Contract Configuration form]()

[Properties installed to configure expiry notifications]()

[Properties installed to configure contracts integrations]()

[Expiring Contracts Condition form fields]()

[Action assignment form]()

[UFX Add on Event mapping form]()

[Obligation form]()

[Obligation Management notifications]()

[Contract Management Pro glossary]()

[Contract Management solutions]()

