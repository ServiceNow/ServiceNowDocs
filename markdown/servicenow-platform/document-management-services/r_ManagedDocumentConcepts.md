---
title: Managed Document concepts
description: The following concepts explain Managed Documents: Managed Document, Document Collection, Document Revisions, and Document Parameters.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Features, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Managed Document concepts

The following concepts explain Managed Documents: Managed Document, Document Collection, Document Revisions, and Document Parameters.

<table id="table_uhs_bfn_vq"><thead><tr><th>

Concept

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Managed Document

</td><td>

The **Document \[dms\_document\]** table contains the documents controlled through the managed documents process.

</td></tr><tr><td>

Document Collection

</td><td>

The **Document Collection \[dms\_collection\]** table allows related documents to be grouped together.

</td></tr><tr><td>

Document Revisions

</td><td>

Because managed documents must have clear records of individual versions of a document, revisions \(including the file\) are attached to the primary document record through a related list. Document revisions are controlled to keep a standard naming scheme and consistent version numbers. Once a document revision is ready, it can be submitted for review.

</td></tr><tr><td>

Document Parameters

</td><td>

**Important:** Parameters do not control application or document security. Parameters only organize documents, they do not affect who can access documents. To grant access to the Managed Documents application, you can assign a role. To grant access to a specific document, set user and group permissions.

 Each document can be associated with predefined parameters. The parameters can help with grouping documents.

-   Type: Defines the type of document being controlled. Documents of the same type use the same controls.
-   Classification: Defines document restriction level, such as public, restricted, or confidential.
-   Audience: Defines the groups with access to the document, such as internal or external.
-   Name Formats: Defines the format of document names, ensuring that documents of the same type have the same name scheme assembled from name components.
-   Name Components: Defines the document values used in the name formats.
-   Approval Rules: Defines the approvals the document must have before it can be published.

</td></tr></tbody>
</table>**Parent Topic:**[Managed Document features](r_ManagedDocumentFeatures.md)

