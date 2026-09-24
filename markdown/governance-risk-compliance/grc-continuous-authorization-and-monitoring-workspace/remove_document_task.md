---
title: Remove a document from a record
description: Remove a document from the current record by unlinking it from the record, or delete it permanently from ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/remove\_document\_task.html
release: brazil
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [document, remove, unlink, delete, Documents component]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Remove a document from a record

Remove a document from the current record by unlinking it from the record, or delete it permanently from ServiceNow.

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

In general, any role with write access to the record can remove documents.

## About this task

When you remove a document, you choose whether to unlink it from the current record only, or delete it permanently from ServiceNow.

Unlinking keeps the document available for other records. Deleting removes it from ServiceNow entirely and from all records where it was linked.

## Procedure

1.  On the document card, select the more actions menu \(**⋮**\).

2.  Select **Remove**.

    The remove dialog opens and presents your options.

3.  Select one of the following options:

    -   **Unlink the document from this record** — Removes the document from the current record only. The document stays in the ServiceNow platform and remains linked to other records.
    -   **Delete document from ServiceNow** — Permanently removes the document from ServiceNow and from all records it was linked to. This action cannot be undone.
    If you lack the permission, only **Unlink the document from this record** is available.

    When you remove a folder, the same dialog appears. Deleting a folder also removes all documents inside it. Unlinking a folder removes it from the current record only; documents in the folder remain in the Document Management System.

4.  Select **Remove**.

5.  If you selected **Delete document from ServiceNow**, confirm the permanent deletion in the confirmation dialog.

    This step appears only for deletions. The confirmation reminds you that this action can't be reversed.


**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

