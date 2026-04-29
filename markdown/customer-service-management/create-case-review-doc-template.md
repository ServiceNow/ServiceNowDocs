---
title: Create a case digest document template
description: Create a template to use for generating case action summaries or post case review documents.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a case digest document template

Create a template to use for generating case action summaries or post case review documents.

## Before you begin

Role required: admin

Before creating a document template for case digests \(used in Case Action Summaries and Post Case Reviews\), ensure that the required plugins are active in your instance.

-   Case Digests \(`com.sn_csm_case_digest`\)
-   Outsourced for customer service \(`com.sn_csm_outsource`\)

**Note:** If the plugin is not active, contact your system administrator to activate it. The navigation menus and options described in this topic does not appear until the required plugins are active.

## About this task

Document templates identify the information to be included in case action summaries and post case review documents. Create a document template to select, organize, and format the content included in the generated documents. You can create a template or modify an existing template. Two document templates, **CAS Template** and **PCR Template**, are included with the Case Digests plugin.

## Procedure

1.  Navigate to **All** &gt; **Case Digest** &gt; **Administration** &gt; **Document Templates**.

2.  Select **New** to create a template.

    You can also modify an existing template by selecting the template name and opening the template form.

3.  Fill in the following fields on the CS Document Template form.

<table id="table_nbm_c44_bhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The template name.

</td></tr><tr><td>

Table Name

</td><td>

The table that contains the fields to include in the document template.-   Case Action Summary \[sn\_csm\_case\_digest\_cas\]
-   Post Case Review \[sn\_csm\_case\_digest\_pcr\]


</td></tr><tr><td>

Category

</td><td>

Select or create a category to organize your templates.

</td></tr><tr><td>

Header Image

</td><td>

Select to add an image file to use in the document header.

</td></tr><tr><td>

Footer Text

</td><td>

Text to include in the document footer.

</td></tr><tr><td>

Header Position

</td><td>

The position of the image within the header:-   Left align
-   Center align
-   Right align


</td></tr><tr><td>

Body

</td><td>

The content to include in the generated case action summary or post case review document. Add content by selecting fields from the table identified in the **Table Name** field. Selected fields are added to the text editor.

</td></tr><tr><td>

Internal content

</td><td>

The content in the case action summary that is for internal users only. This field is available if the Case Action Summary table is selected in the **Table name** field.

</td></tr></tbody>
</table>4.  Select **Submit** or **Update**.

5.  After creating the case digest template:

6.  Navigate to &gt; **All** &gt; **Case Digest** &gt; **Administration** &gt; **Configuration**.

7.  Open an existing configuration or create new and select the template you created.

8.  Select the template that you created in the **Document Template** field.

9.  Select **Save** to save the record.


**Related topics**  


[Create a case digest configuration](create-case-review-type.md)

