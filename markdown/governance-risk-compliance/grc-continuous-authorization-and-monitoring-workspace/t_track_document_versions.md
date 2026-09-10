---
title: Create, manage, and submit document versions for approval
description: Create and manage document versions to maintain a complete history of changes as a document evolves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_track\_document\_versions.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [document versioning, version history, document versions, authorization package, published version, retired version, draft version]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Create, manage, and submit document versions for approval

Create and manage document versions to maintain a complete history of changes as a document evolves.

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

-   You have linked a document to an authorization package, boundary, or engagement
-   The authorization package or engagement must be in an active, editable state
-   You must have edit permissions on the document

## About this task

Document versioning tracks how a linked document changes over time. All linked documents maintain a version history at the instance level, visible to all users who have access to the document.

**Note:** Document versions progress forward only. You can't roll back to a previous version or revert a published document to draft state. If you need to undo changes, you must create a version with the corrected content.

## Procedure

1.  In the authorization package or engagement, open the **Documents** side panel.

2.  Locate the document you want to version, then select the menu icon next to it.

3.  Select **Track Versions** to view the complete version history.

    A version history panel opens, showing all versions of the document with their current state, creation date, and who created them. The most recent version appears first.

4.  To create a new version in **Track Versions** dialog, select **Create New Version**.

    Alternatively, select **Expand View**, navigate to Versions tab, and then select **New** to create a version.

5.  In the **Create New Version** dialog, select **Upload attachment** and add the new document version.

6.  In **Notes** field, add notes describing the changes.

    Notes help other users understand what changed between versions.

7.  Select **Save Version** to create the version.

    If no approval workflow is configured, the new version is immediately published and the previous version is marked as retired. If an approval workflow exists, the new version enters Draft state and waits for submission.

8.  If the document has an approval workflow configured, select Submit icon in the Track dialog.

    Alternatively, select the menu icon next to the document in the Document panel and select **Send for approval** to trigger the approval process.

    The document state changes to Awaiting Review, and assigned reviewers receive task notifications.

9.  After all reviewers and approvers complete their tasks, in Track Versions dialog, select the Publish icon to publish the version.

    Publishing a version automatically retires all previous versions. The published version becomes the active document that all linked records reference.


**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

