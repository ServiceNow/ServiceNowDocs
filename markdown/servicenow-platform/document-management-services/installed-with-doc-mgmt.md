---
title: Components installed with Document Management
description: Several types of components are installed with activation of the Document Management plugin, including tables and user roles.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [References, Document Management, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Document Management

Several types of components are installed with activation of the Document Management plugin, including tables and user roles.

Demo data is available for this feature.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Admin

</td><td>

Provides Create, Read, Update, and Delete access to the document and its related tables.

 Admin users have access to List and List Entries modules.

</td><td>

platform\_document\_management\_admin

</td></tr></tbody>
</table><table id="table_mlt_4ky_gsb"><thead><tr><th>

Role Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dm\_sharing\_levels\_user

</td><td>

This role contains the following roles:

 -   dm\_user\_role\_read
-   dm\_user\_group\_read
-   dm\_user\_criteria\_read

 Provides the ability to share documents at all levels \(group, role, and user criteria\).

</td></tr><tr><td>

dm\_user\_role\_read

</td><td>

Provides read access to the user role table and the ability to share documents based on user roles.

</td></tr><tr><td>

dm\_user\_group\_read

</td><td>

Provides read access to the User Group table and the ability to share documents based on user groups.

</td></tr><tr><td>

dm\_user\_criteria\_read

</td><td>

Provides read access to the User Criteria table and the ability to share documents based on user criteria.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ds\_document

</td><td>

Stores document records containing document metadata.

</td></tr><tr><td>

ds\_document\_version

</td><td>

Stores document versions containing the actual document file or URL to the file.

</td></tr><tr><td>

ds\_document\_references

</td><td>

Stores references between document records and other records.

**Note:** The records can be from any other table and record on the platform

 Supports a many-to-many relationship between documents and target records.

</td></tr><tr><td>

ds\_document\_lists

</td><td>

Stores document lists, which are a collection of template documents used to create and link documents to other records.

</td></tr><tr><td>

ds\_document\_list\_entry

</td><td>

Stores mappings between template documents and document lists.

</td></tr><tr><td>

ds\_document\_user\_can\_access\_mtom

</td><td>

Stores permissions provided to users to access documents as a Reader, Writer, or Owner.

</td></tr><tr><td>

ds\_document\_ug\_can\_access\_mtom

</td><td>

Stores permissions provided to user groups to access documents as a Reader, Writer, or Owner.

</td></tr><tr><td>

ds\_document\_ur\_can\_access\_mtom

</td><td>

Stores permissions provided to user roles to access documents as a Reader, Writer, or Owner.

</td></tr><tr><td>

ds\_document\_uc\_can\_access\_mtom

</td><td>

Stores permissions provided to user criteria to access documents as a Reader, Writer, or Owner.

</td></tr><tr><td>

ds\_document\_permalink

</td><td>

Stores the permalink and expiration date for the document.

</td></tr></tbody>
</table>**Note:** The Documents \[ds\_document\] and Versions \[ds\_document\_version\] tables can be extended.

**Parent Topic:**[References](../concept/reference-document-management.md)

**Related topics**  


[Document Management roles](document-management-roles.md#)

[Domain separation and Document Management](../concept/domain-separation-document-services.md)

