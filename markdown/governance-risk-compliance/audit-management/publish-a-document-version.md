---
title: Publish a document version
description: Publish an approved document version to set it as the current version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/publish-a-document-version.html
release: brazil
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Document version workflow, Using Document Management System in Audit Workspace, Audit Workspace overview, Audit Management, Governance, Risk, and Compliance]
---

# Publish a document version

Publish an approved document version to set it as the current version.

## Before you begin

Role required: sn\_audit\_ws.supervisor, sn\_audit.manager

## About this task

The **Publish** action is available on a version only after every configured approver has approved it. See [Document version and approval workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/document-version-approval-workflow.md).

## Procedure

1.  From the Documents panel, select the document, then select **Track versions**.

2.  Select the version that is in the **Awaiting approval** state and has been approved by every approver.

3.  Select **Publish**.

    The version state changes to **Published** and becomes the current version of the document. The previously published version is automatically retired. You cannot roll back to the retired version.


