---
title: Link documents to Knowledge articles
description: Manage a document and access the latest version of the document from an article by linking the document to a Knowledge article.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Knowledge Document plugin, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Link documents to Knowledge articles

Manage a document and access the latest version of the document from an article by linking the document to a Knowledge article.

## Before you begin

Your administrator must have activated the following plugins:

-   Knowledge Document plugin \(com.snc.knowledge\_document\)
-   Knowledge Management Advanced plugin \(com.snc.knowledge\_advanced\)

The document is already uploaded and published. For more information, see [Upload a document](t_UploadADocument.md) and [Publish an approved revision](t_PublishAnApprovedRevision.md).

You must have contribute access to the Knowledge Base within which the article linked to the document is stored.

If a Knowledge article is already linked to the document, you must have contribute access to the article.

Role required: document\_management\_user and knowledge

## About this task

You can link the initial or revised version of a document to a Knowledge article. The document appears as an attachment to the linked article. Revising a document doesn't automatically update the document attached to the linked Knowledge article. Therefore, every time you revise a document, you must again link the revised document to the Knowledge article.

**Note:**

As the owner of a document or an administrator, you can link the document to a published article. If the article is checked out by another user, you can't link the document to the associated article, unless the article is published.

A managed document can only be linked to one article.

## Procedure

1.  Navigate to **Managed Documents** &gt; **Documents** &gt; **All**.

2.  Click the document.

3.  In the Knowledge Settings related list, fill in the fields.

<table id="table_jp1_44s_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Behavior

</td><td>

Process performed when the **Link to Knowledge** related link is clicked. A behavior is one of the following types:

 -   **Always create record**: A new Knowledge article is created and linked with the latest published revision of the document as an attachment.
-   **Update existing record**: The linked Knowledge article is updated with the latest published revision of the document as an attachment. If no Knowledge articles exist for the document, a new Knowledge article is created.
 **Note:** Once you select a behavior setting for a document, you can't modify it later when revising the document.

</td></tr><tr><td>

Knowledge Base

</td><td>

Knowledge Base in which the Knowledge article is stored. You can associate a Knowledge article with one Knowledge Base only. If you are using an article template, you can modify this value only if the template is available in the other Knowledge Base.

</td></tr><tr><td>

Type

</td><td>

Article template to create a Knowledge article using defined fields and values. **Note:** when a Knowledge article is created, the **Type** field becomes read-only.

</td></tr><tr><td>

Valid to

</td><td>

Date that the article expires. Adds valid to date information to the same field in the Knowledge article.

</td></tr><tr><td>

Short description

</td><td>

A few words or short phrase describing the Knowledge article. Adds the short description to the same field in the Knowledge article.

</td></tr></tbody>
</table>4.  Click the **Link to Knowledge** related link.

5.  In the information message that is displayed, click the message link to view the Knowledge article.


## Result

The uploaded document is added as an attachment to a Knowledge article. Depending on the **Behavior** field value specified in the Knowledge settings related list, the Knowledge article is created or updated with the document.

**Parent Topic:**[Knowledge Document plugin](../concept/c_KnowledgeDocument.md)

