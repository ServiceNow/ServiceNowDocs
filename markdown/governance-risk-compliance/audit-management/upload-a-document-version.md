---
title: Upload a version of a document
description: Upload a new version of a document when you need to change its content. You can optionally send the new version for review and approval before it publishes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/upload-a-document-version.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Document version workflow, Using Document Management System in Audit Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Upload a version of a document

Upload a new version of a document when you need to change its content. You can optionally send the new version for review and approval before it publishes.

## Before you begin

Role required: sn\_audit\_ws.auditor, sn\_audit\_ws.supervisor

## About this task

For more information on the states a version moves through, see [Document version and approval workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/document-version-approval-workflow.md).

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**, and open the record that has the document you want to update.

2.  Select the **Documents** panel, and select the document.

3.  Select **Track versions**.

    The list of existing versions for the document appears.

4.  Select **New version**.

5.  Attach the updated file, and enter a description for the version.

6.  To require review and approval before the version publishes, add a reviewer and one or more approvers.

    For the steps, see [Set reviewers and approvers for a document version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/audit-management/set-reviewers-and-approvers-for-a-document.md).

7.  Save the version.

    The version is created in the **Draft** state.

8.  Select **Submit**.

    If you added a reviewer or an approver, the version moves to **Awaiting review** or **Awaiting approval**. If you didn't add a reviewer or an approver, the version publishes immediately and the previous version is retired.


