---
title: Add a new Health and Safety related document
description: Add and store documents Health and Safety related documents so that they can be easily and appropriately referenced in related records.
locale: en-US
release: zurich
product: Health and Safety Core
classification: health-and-safety-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Health and Safety Core, Health and Safety, Employee Service Management]
---

# Add a new Health and Safety related document

Add and store documents Health and Safety related documents so that they can be easily and appropriately referenced in related records.

## Before you begin

Role required: sn\_ohs\_im.document\_writer

## About this task

-   The ServiceNow® Document Management \(com.snc.platform\_document\_management\) plugin is installed with Health and Safety applications and enables you to manage your safety documents. For information on document management, see [Document repository](https://www.servicenow.com/docs/access?context=doc-mgt-view-documents-repo&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   All Health and Safety documents are stored in the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table. The previous **Standards and Documents** list and its associated table \[sn\_ohs\_im\_document\] have been deprecated. To access your existing safety documents, migrate them from the deprecated table into the new Health and Safety document \[sn\_ohs\_im\_document\_v2\] table. For more information, see [Migrate existing safety documents to the Document library](../../hs-core/task/hs-migrate-sync-existing-safety-document-docs-library.md).

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the configuration icon \(![Configuration icon](../../hs-risk-management/image/icon-config.png)\).

3.  In the **Configuration** tab, select **Health and Safety document library** and then **All**.

4.  Select **New**.

    To edit an existing document, open the one that you want to edit.

5.  On the form, fill in the fields.

    For information on the document field descriptions, see [Create a document record](https://www.servicenow.com/docs/access?context=create-new-doc&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

6.  In the Access Settings section, select the document access settings.

    For information on access settings, see [Document security and access](https://www.servicenow.com/docs/access?context=document-access-settings&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

7.  Select **Save**.

    The **Versions**, **Reviewers**, and **Approvers** tabs appear for this document.

8.  In the **Reviewers** tab, select **New** to add a reviewer for this document.

9.  In the **Approvers** tab, select **New** to add an approver the document.

    If there're multiple approvers added for a document, it is sent to approvers in ascending order based on the sequence number entered. If two approvers have the same sequence number, only one approver's approval is needed to move on to the next approver in the sequence.

    For information on advanced approval rules and process, see [Document approval and publish process](https://www.servicenow.com/docs/access?context=document-review-approval&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

10. In the **Versions** tab, select **New** to upload a version of this document.

    For information on field descriptions, see [Health and Safety document version form](../reference/hs-document-form.md).

11. If a reviewer and approver have been added for this document, select the version and then select **Submit Version** to it for review and approval.


## Result

-   The document is listed in the **Health and Safety document library** list under **Configuration** and is saved in the Health and Safety document \[sn\_ohs\_im\_document\_v2\] table.
-   The document is available to be referenced in Health and Safety records such as **Documents** tab on the Contractor company form when uploading documents related to the company or its workers.

**Parent Topic:**[Using Health and Safety Core](../../hs-core/concept/using-hs-core.md)

