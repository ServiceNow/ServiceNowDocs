---
title: Reference for Document Templates
description: Reference topics provide additional information about Document Templates.Several types of components are installed with activation of the Document Templates plugin, including tables and user roles
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Reference for Document Templates

Reference topics provide additional information about Document Templates.

## Components installed with Document Templates

Several types of components are installed with activation of the Document Templates plugin, including tables and user roles

Demo data is available for this feature.

### Roles installed

<table id="table_el3_mnl_fsb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Document templates reader \[sn\_doc.reader\]

</td><td>

-   Provides read-only permission to document templates.
-   Can only view the Table of Contents and Page number configurations in a configured HTML template.

</td><td>

None

</td></tr><tr><td>

Document templates writer\[sn\_doc.writer\]

</td><td>

-   Provides read and write permissions to document templates.
-   Can add the Table of Contents and Page number configurations to an existing HTML template or a new HTML template.

</td><td>

-   sn\_doc.reader
-   doc\_toc\_config\_writer
-   doc\_page\_number\_config\_writer

</td></tr><tr><td>

Document templates administrator\[sn\_doc.admin\]

</td><td>

Provides read, write, and delete permissions to document templates.

</td><td>

sn\_doc.writer

</td></tr></tbody>
</table>### Tables installed

<table id="table_kl3_mnl_fsb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PDF Template Mapping\[sn\_doc\_pdf\_template\_mapping\]

</td><td>

Table to store the fields mappings of a PDF document template.

</td></tr><tr><td>

HTML Template\[sn\_doc\_html\_template\]

</td><td>

Table to store HTML document templates.

</td></tr><tr><td>

PDF Template\[sn\_doc\_pdf\_template\]

</td><td>

Table to store PDF document templates.

</td></tr><tr><td>

Participant\[sn\_doc\_participant\]

</td><td>

Table to store the details defined for participants.

</td></tr><tr><td>

Document Task\[sn\_doc\_task\]

</td><td>

Table to store document template tasks.

</td></tr><tr><td>

Document Task Note\[sn\_doc\_task\_note\]

</td><td>

Table to store the details of review notes.

</td></tr><tr><td>

Document Template\[sn\_doc\_template\]

</td><td>

Base table for PDF Template and HTML Template tables.

</td></tr><tr><td>

Document Template Category\[sn\_doc\_template\_category\]

</td><td>

Table to store document template categories.

</td></tr><tr><td>

Document Template Script\[sn\_doc\_template\_script\]

</td><td>

Table to store document template scripts.

</td></tr><tr><td>

Table of Contents Configurations\[doc\_toc\_config\]

</td><td>

Table to store TOC configurations that are used in an HTML template.**Note:** This table is available by default with ServiceNow Platform. However, the menu shortcuts to navigate to this table are available with the Document Templates application only.

</td></tr><tr><td>

Page Number configurations \[doc\_page\_number\_config\]

</td><td>

Table to store page number configurations that are used in an HTML template.**Note:** This table is available by default with ServiceNow Platform. However, the menu shortcuts to navigate to this table are available with the Document Templates application only.

</td></tr></tbody>
</table>