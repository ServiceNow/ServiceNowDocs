---
title: Create a document record
description: Use the Document Management system to create document records in Third-party Risk Management.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-10-21"
reading_time_minutes: 2
keywords: [TPRM, document management, create document, version document, link document, manage permissions]
breadcrumb: [Document Management system, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Create a document record

Use the Document Management system to create document records in Third-party Risk Management.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

-   Any user with access to the Vendor Management Workspace can create a document.
-   If you have the TPR Assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role, you automatically have write access to all documents.
-   If you’re the document creator, you also have write access regardless of your role.
-   If you aren’t the creator and don’t have the TPR Assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role you only have read access to the document.

For more information on setting document permissions, see [Define document sharing permissions](tprm-doc-share-permissions.md).

## About this task

The document management system in TPRM enables you to create, version, and reference documents. This ensures that all relevant parties have access to the necessary documents and that the document life cycle is properly managed.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **All Documents**.

2.  Create a document record by selecting **New**.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create new document form](../reference/tprm-create-new-document-form.md).

4.  Select **Submit** to save the document record.


## What to do next

After submitting the document record, complete the following tasks to finalize the document setup:

-   Add a version by uploading a document file. Only one attachment is allowed per version. For more information, see [Create a document version](tprm-create-document-version.md).
-   Define who can view, edit, or manage the document using the sharing permissions field. For more information, see [Define document sharing permissions](tprm-doc-share-permissions.md).
-   Link reference records by associating the document with relevant records such as assessments, engagements, issues, or tasks to enable roll-up and traceability. For more information, see [Link documents to a TPRM record](tprm-link-document.md).

