---
title: Publish an approved revision
description: Publish a document revision that has been approved.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a document, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Publish an approved revision

Publish a document revision that has been approved.

## Before you begin

Role required: document\_management\_admin

or

Role required: document\_management\_user

## About this task

Once a document has been created and edited, a specific revision can be submitted for draft review and final approval. After final approval, the document can be published.

Publish the approved revision from the Document Revisions list.

**Note:** Publishing documents to the Knowledge Base requires the Knowledge Document Plugin.

## Procedure

1.  Navigate to the document record.

2.  In the Document Revisions List, click the revision marked **Ready for Publishing**.

3.  Click **Publish Revision** to display the **Publish** dialog box.

    The revision number matches the latest revision number. If your standard is to change the revision number when the document is published, such as incrementing the version number to 1.1 or 1.0.1, the change can be made on this dialog box manually.

4.  Click **Publish**.

    The published revision is highlighted in green and the stage of previous revisions is automatically changed to Retired:

    **Note:** If the approval and publishing process is repeated, the published revision is retired when the new revision is published. Any workflows running against previous revisions are canceled when the document is published.


**Parent Topic:**[Create a document](../concept/c_CreateADocument.md)

