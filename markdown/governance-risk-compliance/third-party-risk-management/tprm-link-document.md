---
title: Link documents to a TPRM record
description: Use the Document Management system to link documents to assessments, engagements, issues, and tasks for traceability in Third-party Risk Management \(TPRM\).
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [TPRM, document management, link document, document references, traceability]
breadcrumb: [Document Management system, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Link documents to a TPRM record

Use the Document Management system to link documents to assessments, engagements, issues, and tasks for traceability in Third-party Risk Management \(TPRM\).

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

Linking documents ensures reusability and traceability across the TPRM life cycle. A single document can be referenced by multiple records such as assessments, engagements, issues, and tasks. Duplicate references aren’t allowed.

If you want to link a document directly to a third-party, engagement, or assessment record instead of the document record, navigate to that specific record and add the document reference to the **Documents** related list. For example, **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Third-parties** &gt; **All Engagements** select the engagement record you want, open the **Documents** related list, and select **Link documents**.

**Note:**

-   If the selected record already has the document linked, the system displays an error and prevents duplicate references.
-   If permissions restrict linking, request access from the document owner or administrator.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Documents** &gt; **All Documents**.

2.  Select the document record that you want to add a document reference link to.

3.  Open the **Document References** tab.

4.  Select **New** to add a reference.

5.  Choose the record type \(Assessment, Engagement, Issue, or Task\) and select the specific record.

6.  Select **Submit** to save the reference.


## What to do next

After linking the document, perform the following tasks:

-   Verify that the reference appears in the **Document References** list.
-   Confirm that the link rolls up to the associated third-party record for traceability. The linked document should be visible from the **Documents** related list of the Third-party record.
-   Confirm permissions enable relevant users to view linked documents.

