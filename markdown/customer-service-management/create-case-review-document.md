---
title: Create a post case review
description: Create a post case review document for a resolved case that captures the configured case information.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a post case review

Create a post case review document for a resolved case that captures the configured case information.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice\_manager, or admin

## About this task

You can create post case review documents for customer service product cases that are in the **Resolved** state. Creating a review document is a multi-step process that involves:

-   Creating a post case review record from a case.
-   Previewing the generated review document and making any corrections.
-   Requesting approval, if necessary.
-   Publishing the review document so that it is available to customers, internal stake holders, or both.

You can create one post case review document per case. If this document has already been created, the **Create Post Case Review** menu option is not available. You can view and edit the post case review document from the Related Records form section.

If a case is closed while the post case review is in progress, you can still update the **Additional comments** field on the Case form with the Post Case Review document link. When the case is closed, the system displays a message about the case closure on the Post Case Review form.

## Procedure

1.  Open a customer service case in the **Resolved** state.

2.  To create a post case review record, do one of the following:

    -   Agent Workspace: Click the More UI Actions icon \(![More UI Actions icon.](../image/agent-workspace-more-ui-actions-icon.jpg)\) and select **Create Post Case Review**.
    -   Platform interface: Click the form context menu icon and select **Create Post Case Review**.
3.  In the Post Case Review form, enter any necessary information in the following fields.

    Some information is copied from the Case form to the Post Case Review form, such as the short description and the resolution information.

<table id="table_o5s_msg_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically assigned post case review record number.

</td></tr><tr><td>

Case number

</td><td>

The case number from which this post case review record was created.

</td></tr><tr><td>

Assigned to

</td><td>

The agent assigned to the post case review record.

</td></tr><tr><td>

Commitment Date

</td><td>

The expected completion date of the post case review.

</td></tr><tr><td>

Assignment group

</td><td>

The group assigned to the post case review record.

</td></tr><tr><td>

Approval group

</td><td>

The group assigned to review and approve the post case review record. This field is visible if an approval workflow is selected in the case digest configuration.

</td></tr><tr><td>

Approval users

</td><td>

The users assigned to review and approve the post case review record. This field is visible if an approval workflow is selected in the case digest configuration.

</td></tr><tr><td>

Short description

</td><td>

Copied from the **Short description** field on the Case form.

</td></tr><tr><td>

Summary

</td><td>

A summary of the issue.

</td></tr><tr><td>

Symptoms

</td><td>

Specific symptoms or problems created by the issue.

</td></tr><tr><td>

Root Cause Analysis

</td><td>

Copied from the **Cause** field in the Resolution Information section on the Case form.

</td></tr><tr><td>

Solution Provided

</td><td>

Copied from the **Resolution notes** field in the Resolution Information section on the Case form.

</td></tr><tr><td>

Preventive Measures Taken

</td><td>

Any measures taken to prevent the issue from happening.

</td></tr><tr><td>

Work notes list

</td><td>

Internal users who receive a notification about this case when work notes are added.

</td></tr><tr><td>

Work notes

</td><td>

Information about how to resolve a customer service case, or steps taken to resolve it, if applicable.

</td></tr><tr><td>

Activities

</td><td>

Records all activity associated with this record.

</td></tr></tbody>
</table>4.  Click **Preview** to generate the review document and view it in the Preview Document pop-up window.

5.  Make any desired changes to the fields on the Post Case Review record and click **Preview** again.

    You can edit the content in the Post Case Review record if the state is **New** or **In Progress**. Clicking **Preview** creates a preview of the document with the latest record information.

6.  If approval is required, complete the following steps:

    1.  Add an **Approval group**.

    2.  Add one or more **Approval users**.

    3.  Click **Request Approval**.

    You can request approval for a post case review document before sharing it with customers or internal stake holders. When approval is requested, the status of the post case review moves to **Awaiting Approval** and the record is locked for edits.

    An email is sent to the approvers with a link to the post case review document. The approvers can either approve the document or suggest changes by adding them to the **Work notes** field on the Post Case Review record. The agent receives a notification when an approver approves the case review document or suggests changes.

    -   If the approver suggests changes, the agent can see the changes in the **Work notes** field.
    -   If the approver approves the document, the status of the post case review record changes to **Approved**.
7.  Click **Save**.

8.  Click **Publish to Case** to update the case with the Post Case Review document.

    The document is included as a link in the **Additional comments** field on the Case form. If the document is available to customers, the link is visible from the Customer and Consumer Service Portals.


