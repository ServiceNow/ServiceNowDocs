---
title: Remove a document from a record
description: Remove a document from an engagement, control test, or evidence record in the Documents panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/remove-a-document-from-a-record.html
release: brazil
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-09-16"
reading_time_minutes: 1
breadcrumb: [Using Document Management System in Audit Workspace, Audit Workspace overview, Audit Management, Governance, Risk, and Compliance]
---

# Remove a document from a record

Remove a document from an engagement, control test, or evidence record in the Documents panel.

## Before you begin

Role required: sn\_audit\_ws.auditor or sn\_audit\_ws.supervisor

## About this task

You can remove a document only while the parent record is open. When an engagement or control test moves into a closed state, the Documents panel becomes read-only and the **Remove** action isn't available. For more information, see [Using Document Management System in Audit Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/manage-documents-panel.md).

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Audit Workspace**, and open an engagement, control test, or evidence record.

2.  Select the **Documents** panel.

    The Documents panel displays the documents and folders linked to the record.

3.  Select the document that you want to remove.

4.  Select **Remove**.

    A confirmation pop-up is displayed.

5.  Select **Remove** in the pop-up.

    Removing a document unlinks it from this record only. The document isn't deleted, and any other records it's linked to aren't affected. An entry that includes the document name is added to the work notes of the record.

    The document no longer appears in the Documents panel for this record.


