---
title: Review and approve document versions
description: Examine document versions submitted for review and authorize them to move forward in the approval workflow as a reviewer or approver.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_review\_and\_approve\_documents.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [document review, document approval, reviewer task, approver task, document workflow, authorization package]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Review and approve document versions

Examine document versions submitted for review and authorize them to move forward in the approval workflow as a reviewer or approver.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_user

In general, any role with write access to the record can add, edit, or modify the docs.

**Note:** You can add documents only when the record is in an active state. Inactive records don't allow changes to linked documents.

-   You have been assigned as a reviewer or approver for a document linked to an authorization package, boundary, or engagement
-   A document version has been submitted for review or approval

## About this task

When a document version is submitted for approval, assigned reviewers and approvers receive task notifications. Your role determines what you do:

-   Reviewers examine the document, provide feedback, and move it to the approval stage
-   Approvers authorize the document for publication after the review is completed

Document versions progress forward through the following states:

-   Draft: The document is being prepared and has not been submitted for review. Only you can edit a draft version.
-   Awaiting Review: The document has been submitted and is waiting for assigned reviewers to examine it.
-   Awaiting Approval: Reviewers have completed their review, and the document is now waiting for assigned approvers to authorize it.
-   Ready for Publishing: Approver has approved the document.
-   Published: All approvals are complete and the document is now the active version.
-   Retired: A newer version has been published, and this version has been replaced. Retired versions remain available for historical reference but can't be edited.

All reviewer and approver tasks appear in the **My tasks** page.

## Procedure

1.  In the CAM Workspace, select **Tasks** in the left sidebar.

2.  Under **My pending tasks**, select **Document version approvals** to view all your pending document review tasks.

    A list appears showing all documents awaiting your review or approval. The list includes the document name, current state, version number, who created it, and when.

3.  Select on a task row to open it and view details about the document version you need to review or approve.

4.  In the task details, select the document link or attachment to download and review the file.

5.  When you're ready to proceed, change the **State** field to indicate your decision:

    -   Approved: The document version meets all requirements and can proceed. Reviewers move the document to awaiting approval. Approvers authorize it for publication.
    -   Rejected: The document has issues that must be addressed before proceeding. The document owner receives notification and can submit a revised version.
    -   Canceled: Stop the current approval process without completing the review.
    -   No Longer Required: The approval is no longer needed \(for example, the engagement has been closed or the document has been superseded\).
6.  Select **Save** to submit your review or approval decision.

    Your review or approval decision is recorded and submitted. The document version moves to the next state in the workflow. For example, if you selected Canceled or No Longer Required, the approval process stops and the document remains in its current state.


**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

