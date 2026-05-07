---
title: Document Management lists
description: Lists are a collection of template documents you can use to create documents that are linked to other target records. Only users with the admin role can access lists.
locale: en-US
release: australia
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document Management lists

Lists are a collection of template documents you can use to create documents that are linked to other target records. Only users with the admin role can access lists.

## Document lists

A user with the admin role can create document lists and add multiple documents to a single list. Only users with the admin role can access lists.

## New hire onboarding

During new hire onboarding, employees must upload multiple documents such as ID, training certificates, and so on. Your organization can create documents as templates and group them under a list. Then when you reference this list to a target record, all the template documents under the list are created and linked to the target record.

![Document list form](../image/doc-list.png "Document List Entries")

## List entries

Lists entries are a mapping of a template document with a document list. Only template documents can be linked to a list, such as when documents have the **Template** option selected in the document record. The Document List Entries related list displays the list entries.

**Note:** Users can link only documents that they have access to.

-   **[Group document templates in a list for creating and linking documents to a target record](../task/create-doc-list.md)**  
Group document templates in a list to enable all the template documents in the list to automatically be created and linked to the target record when the list is referenced.
-   **[Add a document template to a document list](../task/add-list-entry-to-doc-list.md)**  
Add a template document to a document list that groups document templates for creating and linking to a parent record.
-   **[Create documents using document lists for a target table record](../task/create-documents-target-table-record.md)**  
You can create and reference documents on a target table record through the DocumentListService API.

**Parent Topic:**[Using Document Management](using-document-management.md)

**Related topics**  


[Group document templates in a list for creating and linking documents to a target record](../task/create-doc-list.md)

[Add a document template to a document list](../task/add-list-entry-to-doc-list.md)

