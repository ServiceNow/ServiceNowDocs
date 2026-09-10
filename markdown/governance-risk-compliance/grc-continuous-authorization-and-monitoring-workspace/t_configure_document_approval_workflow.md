---
title: Configure document approval workflows
description: Set up reviewers and approvers for linked documents to establish a formal approval workflow before a document version becomes active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_configure\_document\_approval\_workflow.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-08-28"
reading_time_minutes: 2
keywords: [document approval, document versioning, approval workflow, authorization package, reviewer, approver]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Configure document approval workflows

Set up reviewers and approvers for linked documents to establish a formal approval workflow before a document version becomes active.

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

## About this task

When you link a document, you can establish an approval workflow to track how the document moves through review and sign-off stages. By configuring reviewers and approvers, you create a controlled process where:

-   Reviewers examine the document and provide feedback
-   Approvers authorize the document for publication
-   All reviewers and approvers receive task notifications

**Important:** If you don't configure reviewers or approvers, a new document version automatically moves to Published state, without requiring review.

## Procedure

1.  In the authorization package or engagement, open the **Documents** side panel.

2.  Select the menu icon next to the document you want to configure, then select **Send for approval**.

    The **Send for approval** dialog opens. Note that you configure approval settings before uploading a new version, not after.

3.  In the **Reviewer** section, select **New** to add reviewers.

    1.  Choose how to assign the reviewer:

        -   **Role:** Assign to all users who hold a specific role \(for example, "Auditor"\)
        -   **User:** Assign to a specific individual
        -   **Group:** Assign to a group of users
        -   **Condition:** Assign based on criteria \(for example, "owner matches current user"\)
    2.  Enter the reviewer name, role, or condition, then select **Save**.

    3.  Repeat to add multiple reviewers if needed.

4.  In the **Approver** section, select **New** to add approvers using the same assignment options.

    If you have multiple approvers, configure the **Sequence** to determine the order in which they receive approval tasks. A lower sequence number approves first.

5.  Select **Save** to store the approval workflow configuration.


## Result

Your approval workflow is now configured and active. The system records your reviewer and approver assignments, and they're notified of their roles.

When you create a new version of the document, the workflow will activate:

1.  You upload a new version and select **Submit**
2.  The document state changes to `Awaiting Review`
3.  Assigned reviewers receive a task to review the document
4.  Once all reviewers complete their review, the state changes to Awaiting Approval
5.  Assigned approvers receive a task to approve or reject the document
6.  Once all approvers approve, a **Publish** action becomes available
7.  Select **Publish** to make the document active. The previous version is automatically marked as `Retired`

Throughout this workflow, all reviewers and approvers can track the document state and provide feedback through the **Tasks** list in the CAM Workspace.

**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

