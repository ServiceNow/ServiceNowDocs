---
title: Document approval
description: During the approval process, the approver approves or rejects the document. A document goes through the approval process after the review process.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a document, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document approval

During the approval process, the approver approves or rejects the document. A document goes through the approval process after the review process.

## Approval workflow

After the document has been reviewed, submit the document for approval. If the document does not have an approver, the approval process is omitted.

When the document is Active, the workflow Document Management Default is used to manage approvals:

![Default workflow](../image/MDOCworkflow.png "Document Management Default workflow")

If the approver rejects the document, the author and owner are notified and the document review is cancelled. The author, owner, and approver should discuss what changes need to be made to the document. When the document is ready, a new review can be initiated.

If the final approver approves the document, the author and the owner are notified. Once final approval is successful, the document stage changes to Ready for Publishing in the Document Revisions list:



## Process modification for multiple approvers

If there are multiple approvers, the approval process works in sequence and multiple approvers can be assigned to a single sequence. For example:

-   Sequence 1: approvers A and B
-   Sequence 2: approvers C and D
-   Sequence 3: approver E

Because the sequences take place in ascending chronological order, approvers A and B receive the approval request first \(approvers C, D, and E are not part of the process yet\). Similar to the review process, the first approver to act within a sequence dictates what happens to the document. If approver A acts first and rejects the document, the approval process stops and the state is set to Cancelled. Approver B's status is changed to No Longer Required. If approver A acts first and approves the document, the process stops and approver B's status is changed to No Longer Required. Then, the document moves to approval sequence 2. After at least one approver in each sequence approves the document, the author and the owner are notified that the document has been approved.

**Parent Topic:**[Create a document](../concept/c_CreateADocument.md)

