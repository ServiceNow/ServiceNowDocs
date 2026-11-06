---
title: Approval field mapping
description: Approval fields, events, and rules in Transaction Manager \(TM\) and how they map to the quote table. Use these names to check or troubleshoot your Advanced Approvals configuration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/r\_approval\_field\_mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 2
keywords: [approval fields, Advanced Approvals, Transaction Manager, quote table, field mapping]
breadcrumb: [Advanced Approval Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Approval field mapping

Approval fields, events, and rules in Transaction Manager \(TM\) and how they map to the quote table. Use these names to check or troubleshoot your Advanced Approvals configuration.

## Approval fields

|Field|Description|Type|
|-----|-----------|----|
|**Approval State** \(`txn.approvalState`\)|Approval state of the transaction. The Cancel Approval event updates this field to recalled or rejected.|Text|

## Field mapping

|Transaction Manager field|Quote table column|Default value|Notes|
|-------------------------|------------------|-------------|-----|
|`txn.approvalState`|Not mapped to the Quote table|Empty|Access modifiable: No. Conditions for inclusion: NOW Only - Approvals. Needed for approvals. This field maps to the Quote table only if a reason is identified.|
|`txn.stage`|State \(`state`\)|`draft`|Existing field. A separate field holds the approval state. Included in the TXN-Quote sync. Not shown in the Transaction Manager UI.|

## Approval events

|Event|Variable name|Description|
|-----|-------------|-----------|
|Preview Approval|`txn.approval.preview`|System event that previews the approval conditions.|
|Request Approval|`txn.approval.request`|System event that submits an approval request.|
|Cancel Approval|`txn.approval.cancel`|System event that recalls or rejects an approval request. Updates `txn.approvalState` to recalled or rejected.|
|Approve Approval|`txn.approval.approve`|System event that approves an approval request.|
|View Approval|`txn.approval.view`|System event that shows the approval status and history.|

## Approval rules

<table><thead><tr><th>

Rule

</th><th>

Variable name

</th><th>

Description

</th><th>

Error message

</th></tr></thead><tbody><tr><td>

Validate Approval Submission

</td><td>

`txn.approval.validateSubmission` \(also listed as `txn.validateApprovalSubmission`\)

</td><td>

Checks that the approval state in Transaction Manager matches the submitted state confirmed by the approval engine.

</td><td>

Error occurred during submission of approval request. Please try again. We couldn't submit this transaction for approval. Please try again. If the issue continues, contact your administrator.

</td></tr><tr><td>

Validate Approval Completion

</td><td>

`txn.approval.validateCompletion` \(also listed as `txn.validateApprovalCompletion`\)

</td><td>

Checks that the approval state in Transaction Manager matches the approved state confirmed by the approval engine.

</td><td>

Error occurred during submission of approval. Please try again. This transaction can't be marked as approved yet, the approval is still in progress.

</td></tr><tr><td>

Validate Approval Revision

</td><td>

`txn.approval.validateRevision` \(also listed as `txn.validateApprovalRevision`\)

</td><td>

Checks that the approval state in Transaction Manager matches the recalled or rejected state confirmed by the approval engine.

</td><td>

Error occurred during recall or reject. Please try again. This transaction is currently under approval and can't be edited. Please recall the approval request first.

</td></tr></tbody>
</table>## Components added by the approval blueprint

Importing the approval blueprint adds the following components:

-   System events: Preview, Request, Approve, Cancel/Reject, and View.
-   Integrations: data flow between the microservices and the approval system.
-   Rules: Validate Approval Submission, Validate Approval Completion, and Validate Approval Revision.
-   Rule groups: Approval Submission, Approval Completion, and Approval Revision.
-   Field: Approval state.

## Related list support

|Related list|Support|Notes|
|------------|-------|-----|
|Approvals tab|Not supported|The approvals slideout is accessible through a header event. No action needed.|

## Tenant setting

The Approvals tenant setting seeds the system objects that Advanced Approvals needs.

**Parent Topic:**[Advanced Approval Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/advanced-approval-management-reference.md)

