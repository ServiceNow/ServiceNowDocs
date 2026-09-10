---
title: Set reviewers and approvers for a document version
description: Configure a reviewer and one or more approvers on a document version before you submit it, so the version is reviewed and approved before it publishes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/set-reviewers-and-approvers-for-a-document.html
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
breadcrumb: [Document version workflow, Using Document Management System in Audit Workspace, Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Set reviewers and approvers for a document version

Configure a reviewer and one or more approvers on a document version before you submit it, so the version is reviewed and approved before it publishes.

## Before you begin

Role required: sn\_audit\_ws.supervisor, sn\_audit.manager

## Procedure

1.  From the Documents panel, select the document, then select **Track versions**.

2.  Select the version that is in the **Draft** state.

3.  In the **Reviewer** field, select the role, user, group, or condition that must review the version.

4.  In the **Approvers** field, add one or more roles, users, groups, or conditions that must approve the version.

5.  If you added more than one approver, set the sequence in which they must approve the version.

6.  Select **Save**.

    When you submit the version, it moves to **Awaiting review**, then to **Awaiting approval** once the reviewer completes their review.


