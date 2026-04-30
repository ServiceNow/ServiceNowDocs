---
title: HR document templates
description: HR Document Templates are used to create and modify reuseable HR documents.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [HR Documents, HR Service Delivery, Employee Service Management]
---

# HR document templates

**HR Document Templates** are used to create and modify reuseable HR documents.

**Important:**

Starting with the Zurich release, HR Document Templates is deprecated and no longer supported or available for new activation.

Use [Document Templates](document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Use HR document templates for documents that can be customized with dates, names, and signatures like:

-   Employee verification letters
-   Non-disclosure agreements
-   Offer letters
-   Educational reimbursement agreements

You can personalize HR document templates by mapping fields or using variables from the available tables to place data in fields. You can also capture multiple e-signatures in a document that automatically generates once all signatures are captured.

There are two types of HR **Document Templates**, both create PDF files, but are created and maintained differently:

1.  Document templates \(HTML\)
2.  PDF document templates

## Acknowledgement text

Within your document templates, you can capture the meaning of a signature. You can add acknowledgement text to your document templates that prompts the user to check a box when signing or providing credentials to a document.

## Document templates \(HTML\)

Document templates are created within the HR application and use variables to pre-fill information from tables into the document. You create how the document looks by defining the header, footer, images, placement of footer, and the text within the template. The base system provides default document templates that you can use to model your documents:

-   Employee Verification Letter in Canada
-   Employee Verification Letter in USA
-   Offer Letter Template
-   Education Agreement

Before you begin generating documents, configure the templates with your company logo and text. Obtain the following items and information to create or configure the predefined HR document templates.

-   A page of your company letterhead.
-   Copies of your current company employment verification letter and offer letter templates, if available.
-   The logo image to use in your header. The header image can be a maximum of 50 px high. If your letterhead includes a logo and text, ensure that the logo image includes the text, because you can only configure the image \(not text\) in the header.
-   The logo image to use in your footer, if applicable. The logo image can be a maximum of 15 pixels high. You can configure both an image and text in the footer.For best results, ensure that the image is optimized and a Scalable Vector Graphics \(SVG\) file.

**Important:** Usage of HR document templates with itext5 is no longer supported. Use HR document templates with itext7 instead.

To use HR document templates feature with itext7, the boolean property **itext7.pdf\_conversion** must be set to true in the Human Resources: Core \(sn\_hr\_core\) scope. This property has been set to true, by default, since the Paris release. If you are using the version of HR Document templates that has been released prior to the Paris release, create the **itext7.pdf\_conversion** property manually to switch to itext7.

## PDF document templates

PDF document templates originate from **Managed Documents** and use field mapping to pre-fill information from tables into the document. Before you customize a document:

-   The document must be a fillable PDF. See the Adobe home page and search for Convert existing forms to fillable PDFs to learn how to create fillable PDF documents [https://www.adobe.com/](https://www.adobe.com/).
-   The document must be uploaded and published.

The base system provides the default PDF document template as an example: Non-Disclosure Agreement \(Sample\).

## Generating documents

Both the **Document template** and **PDF document template** generate PDF documents that can be reviewed or printed and can require multiple signatures.

A common use case for generating a document from an HR case is when an employee requests an employment verification letter. For information on generating a PDF document from an HR case, see [HR document generation](DocumentGeneration.md).

**Related topics**  


[Managed Document features](https://www.servicenow.com/docs/access?context=r_ManagedDocumentFeatures&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

