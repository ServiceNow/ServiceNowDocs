---
title: Document versions
description: In the ServiceNow Document Management application, documents display as versions in the record. You view these versions as a related list within the document record. A document can have many versions.
locale: en-US
release: yokohama
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Document repository, Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document versions

In the ServiceNow® Document Management application, documents display as versions in the record. You view these versions as a related list within the document record. A document can have many versions.

The term "document" refers to the container record that holds document information such as its name, description, type and other metadata. While the document record doesn’t contain the actual document file, it does contain versions in the record, which you can open, update, and track.

Use the Attachment icon \(![Attachment icon.](../image/attachment-icon.png)\) to add documents to a record.

Alternatively, you can provide the link to a document in the URL field. You then access the actual documents by selecting the versions in the related list.

## Document version review and approval

All approver and reviewer users have read access to the documents that they’re approving.

A document can have a reviewer or multiple reviewers and no approvers and vice versa. Users with admin and platform\_document\_management\_admin roles​ have the option to create approval and review rules.

Document owners have the option to:

-   Initiate approval and review workflow​ for a document version.
-   Publish the approved version.
-   See the activity stream of the approval and review workflow.
-   Track the document **Version State**.

For multiple document versions, the latest reviewed and approved version gets published and the previous versions are retired.

-   **[Create a document version](../task/create-doc-version.md)**  
Create a document version for each document.

**Parent Topic:**[Document repository](doc-mgt-view-documents-repo.md)

**Related topics**  


[Create a document record](../task/create-new-doc.md)

[Download a document](../task/downloading-a-document.md)

[Share a document link](../task/share-document-link.md)

[Modify a shared link access](../task/modify-access-shared-link.md)

[Delete a document link](../task/delete-document-link.md)

[Delete documents](../task/delete-a-doc.md)

