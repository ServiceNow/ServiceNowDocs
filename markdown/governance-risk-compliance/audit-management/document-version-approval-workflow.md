---
title: Document version and approval workflow
description: Every new version of a document in the Documents panel can go through an optional review and approval workflow before it is published and replaces the previous version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/document-version-approval-workflow.html
release: australia
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Using Document Management System in Audit Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Document version and approval workflow

Every new version of a document in the Documents panel can go through an optional review and approval workflow before it is published and replaces the previous version.

When you upload a new version of a document from the Documents panel, the version moves through the following states:

|State|Description|
|-----|-----------|
|Draft|The new version is uploaded but not yet submitted.|
|Awaiting review|The version is submitted and is waiting for the assigned reviewer to review it. This state occurs only if a reviewer is configured for the version.|
|Awaiting approval|The reviewer has completed their review and the version is waiting for the assigned approver, or the next approver in sequence, to approve it. This state occurs only if one or more approvers are configured for the version.|
|Published|The version is published and becomes the current version of the document. The previously published version is automatically retired.|
|Retired|An earlier version that was replaced when a newer version was published. Retired versions remain available for reference but cannot be edited or republished.|

If you don't add a reviewer or an approver before you submit a version, the version publishes immediately and retires the previous version.

## Reviewers and approvers

Before you submit a new version, you can add one reviewer and one or more approvers on the version. When you add more than one approver, you set the sequence in which they must approve the version, for example, first approver, second approver, and so on. Reviewers and approvers act on a version from the **Document version approval** item on their task list. For the steps, see [Set reviewers and approvers for a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/set-reviewers-and-approvers-for-a-document.md) and [Approve or reject a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/approve-or-reject-a-document-version.md).

## Rollback is not supported

**Note:** After a version is published, you cannot roll back to a previous version. To make changes to a published document, upload a new version.

