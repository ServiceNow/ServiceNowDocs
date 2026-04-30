---
title: Document Templates configurations
description: Use Document Templates configurations to generate table of contents and page numbers on a PDF document that is generated from an HTML template.Create a TOC configuration to generate Table of Contents in a PDF document that is generated from an HTML document.Create a page number configuration to automatically generate page numbers in a PDF document that is generated from an HTML document.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using Document Templates: HR Service Delivery use case, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Document Templates configurations

Use Document Templates configurations to generate table of contents and page numbers on a PDF document that is generated from an HTML template.

**Note:** Only if the **com.snc.pdfgenerator.html2pdf.api.version** property is set to 2 \(default\), the Table of Contents and Page number configuration features are available to use. If the **com.snc.pdfgenerator.html2pdf.api.version** property is set to 1, the Table of Contents and Page number configuration features are not available to use.

**Parent Topic:**[Using Document Templates: HR Service Delivery use case](using-doc-templates.md)

**Related topics**  


[Document template categories](document-types-document-templates.md)

[Document Templates of type HTML](document-templates-flow-html.md)

[Document Templates of type PDF \(Advanced forms\)](document-templates-PDF-flow.md)

[Work on a document task](../task/work-doctemp-tasks.md)

[Document generation methods](generate-pdf-doctemp.md)

[Document tasks generation](../task/task-mapped-participants.md)

## Create a TOC configuration in Document Templates

Create a TOC configuration to generate Table of Contents in a PDF document that is generated from an HTML document.

### Before you begin

Role required: sn\_doc.writer

### Procedure

1.  Navigate to **Document Templates** &gt; **Document Configuration** &gt; **Table of Contents Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_jrv_4hz_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Table of Contents configuration.

</td></tr><tr><td>

Title

</td><td>

Table of Contents title that appears in the generated document.

</td></tr><tr><td>

Type

</td><td>

Table of Contents is displayed in a list view in the generated PDF document.

</td></tr><tr><td>

Heading numbering

</td><td>

Format in which you want the page numbers of the headings to be displayed. The values are:-   None
-   Decimal


</td></tr><tr><td>

Table leader

</td><td>

Gap between the heading and page number. Table leader helps to correlate a section or a heading with its page number. The values are:-   None
-   Dotted


</td></tr><tr><td>

Clickable

</td><td>

Enable or disable clickable links inside the generated Table of Contents.

</td></tr><tr><td>

Show page numbers

</td><td>

Option to display page numbers on the generated PDF document.**Note:** This option makes the page number configuration field on the document template mandatory.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the TOC configuration is created.

</td></tr><tr><td>

Start numbering after table of contents

</td><td>

Option to begin page numbers after TOC ends.**Note:**

-   This field appears only when the **Show page numbers** field is enabled.
-   This field overrides the **Start numbering from page** field in page number configuration.


</td></tr></tbody>
</table>4.  Click **Submit**.


## Create a page number configuration in Document Templates

Create a page number configuration to automatically generate page numbers in a PDF document that is generated from an HTML document.

### Before you begin

Role required: sn\_doc.writer

### Procedure

1.  Navigate to **Document Templates** &gt; **Document Configuration** &gt; **Page Number Configurations**.

2.  Click **New**.

3.  On the form, fill in the fields:

<table id="table_jrv_4hz_vrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of page number configuration.

</td></tr><tr><td>

Page number format

</td><td>

Format in which page numbers are displayed on the generated PDF document: **Decimal**

</td></tr><tr><td>

Start numbering from page

</td><td>

Page from which you want the numbering to begin.**Note:** The value in this field is overridden by the **Start numbering after table of contents** in TOC configuration.

</td></tr><tr><td>

Application

</td><td>

Application scope in which the page number configuration is created.

</td></tr><tr><td>

Position

</td><td>

Vertical position of the page number: **Header** or **Footer**

</td></tr><tr><td>

Horizontal alignment

</td><td>

Horizontal alignment of the page number: **Left**, **Center**, or **Right**

</td></tr></tbody>
</table>4.  Click **Submit**.


