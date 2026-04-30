---
title: Migrating from HR Document Templates to Document Templates
description: Review these guidelines to successfully migrate from HR Document Templates to Document Templates. Document Templates provides the latest experience of HR Document Templates functionality with additional features and capabilities.Follow the steps for migrating HR Document template \(HTML\) to Document template \(HTML\).Follow the steps for migrating HR Document template \(PDF\) to Document Template \(PDF\).
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Migrating from HR Document Templates to Document Templates

Review these guidelines to successfully migrate from HR Document Templates to Document Templates. Document Templates provides the latest experience of HR Document Templates functionality with additional features and capabilities.

**Important:**

Starting with the Xanadu release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

Review the following details to understand the key offerings and differences between HR Document Templates and Document Templates.

<table id="table_zcy_f2n_vbc"><thead><tr><th>

Table/Feature

</th><th>

HR Document Templates

</th><th>

Document Templates

</th></tr></thead><tbody><tr><td>

Template

</td><td>

HR Document Template\[sn\_hr\_core\_document\_template\]

</td><td>

Document Template\[sn\_doc\_template\]

</td></tr><tr><td>

Document Type/Category

</td><td>

Document Type \[sn\_hr\_core\_document\_type\]

</td><td>

Category\[sn\_doc\_template\_category\]

</td></tr><tr><td>

Criteria

</td><td>

HR Criteria \[sn\_hr\_core\_criteria\]

</td><td>

User Criteria \[user\_criteria\]

</td></tr><tr><td>

PDF template mappings

</td><td>

PDF Template Mapping\[sn\_hr\_core\_pdf\_template\_mapping\]

</td><td>

Template Mapping \[sn\_doc\_pdf\_template\_mapping\]

</td></tr><tr><td>

Participants

</td><td>

Participants are not supported.You must directly map user fields in HTML template body or PDF template mappings.

</td><td>

Participants are supported. Participant details are stored in the Participant \[sn\_doc\_participant\] table. You must map participants for signing in HTML body and PDF template mappings.For an HTML template, see [Create participants for an HTML document template](../task/create-participants-html.md).

For a PDF template, see [Create participants for a PDF document template](../task/create-participant.md).

</td></tr><tr><td>

HTML Template Translation

</td><td>

-

</td><td>

SupportedSee [Use Localization Framework for Document Templates](../task/doc-lzt-fm.md)

</td></tr><tr><td>

HTML template blocks

</td><td>

-

</td><td>

SupportedSee [Document blocks in Document Templates](doc-block-temp.md).

</td></tr><tr><td>

HTML template scripts

</td><td>

-

</td><td>

SupportedSee [Document template scripts](document-template-scripts.md).

</td></tr><tr><td>

HTML template TOC

</td><td>

-

</td><td>

SupportedSee [Create a TOC configuration in Document Templates](doc-template-configs.md#).

</td></tr><tr><td>

User action

</td><td>

Only one action type is supported: Signing

</td><td>

Different action types are supported \(Fill, Review and Signing\) based on the template type.For an HTML template, see **Action type** in [Create participants for an HTML document template](../task/create-participants-html.md).

For a PDF template, see **Action type** in [Create participants for a PDF document template](../task/create-participant.md).

</td></tr><tr><td>

Tasking

</td><td>

Tasking is done through HR tasks.

</td><td>

Tasking is done through document tasks based on configured participants.

</td></tr><tr><td>

Signing type

</td><td>

For HTML, only ServiceNow signing is supported.For PDF, all three signing types are supported: ServiceNow Sign, DocuSign, and AdobeSign.

</td><td>

For both HTML and PDF, all three signing types are supported: ServiceNow Sign, DocuSign, and AdobeSign.**Note:**

-   Template must be created in ServiceNow.
-   Only signing is supported in external system.
-   Templates that are created in DocuSign or AdobeSign are not supported in the Document Templates application.

</td></tr><tr><td colspan="3">

**HR case fields to be used in case template**

</td></tr><tr><td>

Document template

</td><td>

PDF template \(pdf\_template\)

</td><td>

Document template \(document\_template\).

</td></tr><tr><td>

Document type/category

</td><td>

Document type \(document\_type\)

</td><td>

Document template category \(document\_template\_category\)

</td></tr><tr><td colspan="3">

**HR service configuration**

</td></tr><tr><td>

Case option

</td><td>

Automatically create draft document

</td><td>

Automatically Initiate Document tasks

Automatically initiate document tasks based on participant configuration. See [Document generation methods](generate-pdf-doctemp.md).

</td></tr></tbody>
</table>## Migrate HR Document template \(HTML\) to Document Template

Follow the steps for migrating HR Document template \(HTML\) to Document template \(HTML\).

### Before you begin

Role required: admin

### Procedure

1.  Create a document template category in the Category \[sn\_doc\_template\_category\] table \(if HR Document template has a document type associated with it\).

2.  Navigate to **Document Template** &gt; **HTML template**.

3.  Click **New**.

4.  Fill in the form fields, such as Name, Table, Category, Body, Language, similar to HR Document template and save it.

    If there is any signature token \(Signature token: $\{signature\}, $\{&lt;-user\_field-&gt;.signature\}\) in HTML body, remove it and save the template.

5.  If HR document template has HR criteria associated with it, select the corresponding user criteria in the new document template.

6.  Find participants based on signature tokens in old HR document template body, and create participant records in the **Participant** related list in the new Document Templates.

    After a participant is created, add the signature token by clicking **Insert signature**. In the legacy HR Document Templates body, signature token is supported in the format $\{&lt;-user\_field-&gt;.signature\} while in new Document Templates body, signature token is supported in the format $\{signature:&lt;-participant\_user\_name-&gt;\}.

7.  Publish the template by clicking **Publish**.

8.  Update the case template to use the new document template or category.

    See the HR case fields in the Functionality and Table Comparison: HR Document Templates and Document Templates table in [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).


## Migrate HR Document template \(PDF\) to Document Template

Follow the steps for migrating HR Document template \(PDF\) to Document Template \(PDF\).

### Before you begin

Role required: admin

### Procedure

1.  Create a document template category in the Category \(sn\_doc\_template\_category\) table \(if HR Document template has a document type associated with it\).

2.  Navigate to **Document Template** &gt; **PDF template**.

3.  Click **New**.

4.  Fill in the form fields, such as Name, Table, Category, and Language, similar to that of HR Document Templates.

5.  If HR document template has HR criteria associated with it, select the corresponding user criteria in the new document template.

6.  Select **Attachment type** as **Select from document revision**, and add **Document revision** used in the HR document template.

7.  Select the corresponding signing type and **Save**.

8.  Click the **Parse PDF** related link.

    Template mapping records are created. Update the mapping fields.

9.  Create a participant record with action type **Sign** for each user who needs to sign the document.

    **Note:** This step is required only when legacy HR Document Template has PDF Template mapping record with Document field type as **Signature**.

10. Publish the template by clicking **Publish**.

11. Update the case template to use the new document template or category.

    For more information, see the HR case fields in the Functionality and Table Comparison: HR Document Templates and Document Templates table in [Migrating from HR Document Templates to Document Templates](migration-hrdt-dt.md#).


