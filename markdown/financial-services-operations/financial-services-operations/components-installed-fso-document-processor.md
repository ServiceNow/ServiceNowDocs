---
title: Components installed with Financial Services Document Processor
description: Several types of components are installed with installation of the Document Processor application, including tables and user roles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Components installed with Financial Services Document Processor

Several types of components are installed with installation of the Document Processor application, including tables and user roles.

## Roles installed

<table id="table_itl_4d3_htb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Document Processor admin

 \[sn\_doc\_processor.admin​\]

</td><td>

This role gives access to all document entities and grants admin privileges. This application-specific system administrator role can:-   Grant document processor roles
-   Delete document verification tasks

</td><td>

sn\_doc\_processor.agent

</td></tr><tr><td>

Document processor agent

\[sn\_doc\_processor.agent​\]

</td><td>

-   Can view document verification tasks if they have access to parent record document verification tasks.
-   Can submit, verify, and reject document verification tasks.

</td><td>

-   canvas\_user
-   sn\_docintel.extraction\_agent
-   sn\_docintel.creation\_agent

</td></tr><tr><td>

Document processor collector

\[sn\_doc\_processor.collector​\]

</td><td>

-   Can view document verification tasks if they have access to parent record document verification tasks.
-   Can submit document verification tasks.
-   Can request deferment of and exception for document verification tasks.

</td><td>

canvas\_user

</td></tr><tr><td>

Document processor viewer

\[sn\_doc\_processor.viewer\]

</td><td>

Can view document verification tasks if they have access to parent record document verification tasks.

</td><td>

 

</td></tr></tbody>
</table>## Tables installed

<table id="table_mtl_4d3_htb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Document Category

 \[sn\_doc\_processor\_category\]

</td><td>

Stores all document categories that are configured for all workflows across Financial Services Operations applications.

</td></tr><tr><td>

Document Type

\[sn\_doc\_processor\_type\]

</td><td>

Stores all defined document types.

</td></tr><tr><td>

Category Type

\[sn\_doc\_processor\_m2m\_category\_type\]

</td><td>

Stores all defined document category types.

</td></tr><tr><td>

Attribute

\[sn\_doc\_processor\_attribute\]

</td><td>

Stores all defined document attributes.

</td></tr><tr><td>

Document List Definition

\[sn\_doc\_processor\_list\]

</td><td>

Stores all document lists.

</td></tr><tr><td>

Document List Item Definition

\[sn\_doc\_processor\_list\_item\]

</td><td>

Stores all defined document list items.

</td></tr><tr><td>

Document Verification

\[sn\_doc\_processor\_verification\_task\]

</td><td>

Stores all tasks for document verification requests for all Financial Services Operations applications. This table extends the Task \[task\] table.

</td></tr><tr><td>

Extracted Value

\[sn\_doc\_processor\_extracted\_value\]

</td><td>

Stores all extracted values for documents processed through OCR.

</td></tr><tr><td>

Document

\[sn\_doc\_processor\_document\]

</td><td>

Stores all documents.

</td></tr></tbody>
</table>