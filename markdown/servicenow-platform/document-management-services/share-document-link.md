---
title: Share a document link
description: Create and control document sharing based on classification for shared links with public access.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document repository, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Share a document link

Create and control document sharing based on classification for shared links with public access.

## Before you begin

Role required: owner or writer

## About this task

The **Share document** button is visible only when the document has a valid default version.

## Procedure

1.  Navigate to **All** &gt; **Documents** &gt; **Documents**.

2.  Select the record that you want to share the document link for.

3.  In the record, select **Share** to share the document link.

    **Note:** To restrict the creation and sharing of permalinks based on document classifications go to the system property **com.snc.documents.permalink.allowed\_classification** and add the classification type under the property value.

4.  For Link Validity, select **Permanent** to keep the link permanently, or select **Expire Link On**, and select the link expiry date.

    **Note:** If a classification that was previously allowed for permalink creation becomes restricted then a new permalink cannot be created for documents if the classification is changed to restricted. But existing permalinks will continue to function until they have reached their expiry date or are explicitly deleted.

5.  Select the copy link icon \(![Copy link icon.](../image/icon-copy.png)\) to copy and share the document link to download the document.

    **Important:** The permalink generated can be accessed publicly irrespective of the document classification.

6.  Select **Done**.


**Parent Topic:**[Document repository](../concept/doc-mgt-view-documents-repo.md)

**Related topics**  


[Create a document record](create-new-doc.md)

[Document versions](../concept/document-mgt-versions.md)

[Download a document](downloading-a-document.md)

[Modify a shared link access](modify-access-shared-link.md)

[Configure document permissions](../concept/document-configuration.md)

[Delete a document link](delete-document-link.md)

[Delete documents](delete-a-doc.md)

