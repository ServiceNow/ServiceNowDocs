---
title: Create or request a new document
description: Once an administrator has set parameters for the Managed Documents application, you can create or request new documents.
locale: en-US
release: yokohama
product: Document Management Services
classification: document-management-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Create a document, Managed Documents, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create or request a new document

Once an administrator has set parameters for the Managed Documents application, you can create or request new documents.

## Before you begin

Role required: document\_management\_admin

or

Role required: document\_management\_user

## Procedure

1.  Navigate to **All** &gt; **Managed Documents** &gt; **Create New**.

2.  Complete the following fields:

<table id="table_cst_nmw_kq"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Number

</td><td>

An identifying number for the document. Automatically generated using number maintenance.

</td></tr><tr><td>

Name

</td><td>

A name for the document. Note that the name for the document is combined with other naming components \(as defined by the [name format](../reference/r_DefiningNameFormats.md)\) to create the names for each document revision.

</td></tr><tr><td>

Requested by

</td><td>

The person asking that the document be created or updated.

</td></tr><tr><td>

Owner

</td><td>

The approver of the document request. Also responsible for setting completion date with requesters and authors.

</td></tr><tr><td>

Reviewers

</td><td>

The user or users who review the document and provide feedback to owners and authors.

</td></tr><tr><td>

Department

</td><td>

The department responsible for the document.

</td></tr><tr><td>

Type

</td><td>

The document purpose. This is a choice list derived from the [type parameters](../reference/r_DefiningDocumentParameters.md).

</td></tr><tr><td>

Classification

</td><td>

The document classification, based on security, audience, and confidentiality. This is a choice list derived from the [classification parameters](../reference/r_DefiningClassifications.md).**Note:** This does not drive any functionality.

</td></tr><tr><td>

Audience

</td><td>

The document readers, such as external or internal. This is a choice list derived from the [audience parameters](../reference/r_DefiningAudiences.md).**Note:** This does not drive any functionality.

</td></tr><tr><td>

State

</td><td>

The current status of the document in the editing and publication process.

</td></tr><tr><td>

Checked out by

</td><td>

The user who currently has the document checked out.

</td></tr><tr><td>

Description

</td><td>

A short description of the document.

</td></tr><tr><td class="sub-head" colspan="2">

Revision Settings

</td></tr><tr><td>

Name format

</td><td>

The format for the name of each individual revision of the document. For more information, see [name format](../reference/r_DefiningNameFormats.md).

</td></tr><tr><td>

Revision format

</td><td>

A choice between the two digit \(0.x\) or the three digit \(0.0.x\) revision format.

</td></tr><tr><td>

Auto increment revision

</td><td>

If selected, the revision number automatically increments each time the document is revised.

</td></tr></tbody>
</table>    The User Permissions related list determines which users have rights to view and contribute to the document:

<table id="table_ivj_rpw_kq"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

User

</td><td>

A reference to a user who is entitled to read but not contribute to a document.

</td></tr><tr><td>

Type

</td><td>

A choice list describing how the user can interact with the document. Options are:-   Reader - The user can read the document versions.
-   Editor - The user can upload new versions.
-   Owner - The user can edit the document.


</td></tr></tbody>
</table>    The Group Permissions related list determines which groups have rights to view and contribute to the document:

<table id="table_fwz_xpw_kq"><thead><tr><th>

Field

</th><th>

Input value

</th></tr></thead><tbody><tr><td>

Group

</td><td>

A reference to a group of users who are entitled to read and contribute to the document.

</td></tr><tr><td>

Type

</td><td>

A choice list describing how group members can interact with the document. Options are:-   Reader - Group members can read the document versions.
-   Editor - Group members can upload new versions.
-   Owner - Group members can edit the document.


</td></tr></tbody>
</table>
-   **[Specify an approver](t_SpecifyAnApprover.md)**  
You can specify approvers for a document record after you save it.

**Parent Topic:**[Create a document](../concept/c_CreateADocument.md)

