---
title: Configure an HR PDF document template
description: Create or modify custom HR PDF document templates with your unique criteria. PDF document templates originate from Managed Documents and are either a fillable PDF with mapped fields or a standard PDF with an inline signature.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Configure an HR PDF document template

Create or modify custom HR PDF document templates with your unique criteria. PDF document templates originate from Managed Documents and are either a fillable PDF with mapped fields or a standard PDF with an inline signature.

## Before you begin

Role required: sn\_hr\_core.manager

## About this task

**Important:**

Starting with the Xanadu release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](../concept/document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](../concept/migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

With PDF document templates, you can take an existing document and reuse it with custom information from an HR case or any available table. For example, you can take a fillable PDF document from Managed Documents, and map fields to customize the document each time it is used.

The document must be a fillable PDF to map the fields to a table. See the Adobe home page and search for fillable PDF to learn how to create fillable PDF documents [https://www.adobe.com/](https://www.adobe.com/).

**Note:** Fillable PDFs presented to an employee does not save any data populated by the employee \(except for signatures\). Fillable PDFs are only used for mapping fields to a table.

Documents are uploaded and accessed from the Managed Documents application in the Documents \[dms\_document\] table. Documents are required to be published as a document revision before it can be accessed.

The base system provides the Non-Disclosure Agreement document template as an example of a PDF document template.

**Note:** See . [Managed Document features](https://www.servicenow.com/docs/access?context=r_ManagedDocumentFeatures&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or on an existing PDF document template to edit it.

    When you select **New**, the HR Document Templates list appears.

3.  Select **PDF Document Template**.

    **Note:** To know the differences between the types of document template, see [HR document templates](../concept/c_HRDocumentTemplates.md).

4.  Fill in the fields on the form.

<table id="table_xm3_tm3_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR PDF document template.

</td></tr><tr><td>

Table

</td><td>

Select the table associated with the type of template. The table determines the available fields that can be mapped.**Note:** Only tables that you have access to appear.

</td></tr><tr><td>

Document type

</td><td>

Select the document type the template applies to. Click **New** from **HR Document Type** to create a document type.

 A document type is required when you want a list of documents to appear in the HR case form. HR criteria works with this field to narrow the list of documents you want available for an HR case.

 See [Using document types with HR document templates](../concept/DocumentTypes.md).

 **Note:** When creating a document type, the **Value** auto-populates from the name you enter \(all lower case and underscores\).

</td></tr><tr><td>

Active

</td><td>

Option to activate the HR PDF document template for use.

</td></tr><tr><td>

Document revision

</td><td>

Select the document and revision the PDF document template is based on. Documents listed originate from Managed Documents.

 **Note:** User group and document owner determine what revisions are available to view or select.

</td></tr><tr><td>

HR criteria

</td><td>

Select the audience criteria for this document. For example, you can create a letter intended for only Canadian employees. The HR criteria narrows the number of users for the template.

**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

PDF Preview

</td><td>

Appears after saving or selecting an existing PDF template.Click to view a preview of the template.

**Note:** Using style tags for text alignment is not supported. Use spaces to align your text.

</td></tr></tbody>
</table>5.  Click **Submit** or **Save** to save your PDF document template.

    The **Mark Signatures** button appears at the top menu bar. Click to map where signatures are required in the template. A preview of the PDF document template appears to define a signature block.

    The **Parse PDF** related link appears. When there are fields on the template that can be mapped, the **Parse PDF** link appears under **Related Links**.

6.  Click **Parse PDF** if it appears under **Related Links** to view the fields that can be mapped.

    The AcroForm PDF determines which fields can be mapped and the table selected determines what information you can have populated in those fields. ![Click the Parse PDF related link.](../image/hr-pdf-doc-template-parse-pdf.png)

    The **PDF Template Mappings** list appears. Click the fields of the PDF to map them to fields on the table selected. You can customize your document with pre-filled information from the table. See [Add or modify a PDF template mapping](PDFTemplateMapping.md). After creating or editing the field mappings, the PDF Preview button appears.

7.  Click **Update**.


