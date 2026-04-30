---
title: Configure an HR document template \(HTML\)
description: Create or modify HR document templates with your unique company logo and audience criteria. Document templates are created within the HR application and use variables to pre-fill information from tables to create reusable HR documents.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [HR document templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Configure an HR document template \(HTML\)

Create or modify HR document templates with your unique company logo and audience criteria. Document templates are created within the HR application and use variables to pre-fill information from tables to create reusable HR documents.

## Before you begin

Role required: sn\_hr\_core.manager and sn\_hr\_le.admin

## About this task

**Important:**

Starting with the Yokohama release, HR Document Templates is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported.

Use [Document Templates](../concept/document-templates-overview.md) that provides the latest experience for this functionality. For migration guidelines, see [Migrating from HR Document Templates to Document Templates](../concept/migration-hrdt-dt.md#).

For deprecation details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

HR document templates customize HR documents to match the service and subject person.

The base system provides examples of employment verification letters, educational reimbursement agreements, and an offer letter.

Body text is defined and formatted with TinyMCE and can merge or include user and table variables during document generation. The PDF generator does not support some of the HTML elements.

**Note:** The example offer letter only appears when the **Human Resources Scoped App: Lifecycle Events** is activated.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Document Templates**.

2.  Click **New** or on an existing document template to edit it.

    When you select **New**, the HR Document Templates list appears.

3.  Select **Document Template**.

    **Note:** To know the differences between the types of document template, see [HR document templates](../concept/c_HRDocumentTemplates.md).

4.  Fill in the fields on the form.

<table id="table_dvm_fm3_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the HR document template.

</td></tr><tr><td>

Table

</td><td>

Select the table associated with the type of template. The table determines the available variables that can be used.**Note:** Only tables that you have access to appear.

</td></tr><tr><td>

Document type

</td><td>

Select the document type the template applies to. Click **New** from **HR Document Type** to create a document type.

 A document type is required when you want a list of documents to appear in the HR case form. **HR criteria** works with this field to narrow the list of documents you want available for an HR case.

 See [Using document types with HR document templates](../concept/DocumentTypes.md).

 **Note:** When creating a document type, the **Value** auto-populates from the name you enter \(all lower case and underscores\).

</td></tr><tr><td>

Header image

</td><td>

Select to add an image in the header. You can add your company logo using this feature.**Note:** Supported file types are: JPEG, JPEG2000, GIF, PNG, BMP, WMF, TIFF, and JBIG2.

</td></tr><tr><td>

Header image position

</td><td>

Select where you want the header image to appear.

</td></tr><tr><td>

HR criteria

</td><td>

Select the audience criteria for this document. For example, you can create a letter intended for only Canadian employees. The HR criteria narrows the number of users for the template.

**Note:** When defining conditions like case sensitivity or null values, see API[GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Body

</td><td>

Enter and format the text to comprise the body of the template.To insert variables, place your cursor in the desired location and click the variable. Available variables are listed under **Fields**.

 Use the formatting tools in the **Body** to apply formatting options, such as bold, italic, underline, font styling.

 The body is a place holder for HTML text and tokenized variables. When the PDF is generated, the variables are resolved before sending it to the PDF Generator \[com.snc.pdf\_generator\] plugin.

 **Note:** Currently, there is no support for style tags to align text left or right. Space indentation must be used. Jelly and CSS Styling are not supported.

</td></tr><tr><td>

Select variables

</td><td>

A list of variables that can be used in the body of the template. Variables pull information from the selected table to customize the template.Offsets are supported for date variables. Offsets extend or subtract days, weeks, or months from a date used in a template.

Valid date offset variables are:-   + \(plus\)
-   - \(minus\)
-   d \(days\)
-   w \(weeks\)
-   m \(months\)
 Examples:

-   Offer letter \(five days after stated date\): Your offer is valid until $\{Date +5d\}.
-   Benefits for terminated employee \(two weeks from termination date\): Your benefits end effective $\{subject\_person.hr\_profile.employment\_end\_date +2w\}.
 **Note:** Only variables that you have access to appear.

</td></tr><tr><td>

Footer image

</td><td>

Select to add an image in the footer.The original height of your image should not exceed 170 pixels. Scale your image by 30% or ensure the image height is less than 50 pixels in order for the image to be clear and visible.

 **Note:** Supported file types are: JPEG, JPEG2000, GIF, PNG, BMP, WMF, TIFF, and JBIG2.

</td></tr><tr><td>

Footer image position

</td><td>

Select where you want the footer image to appear.

</td></tr><tr><td>

Footer text

</td><td>

Enter text. For example, you can add proprietary and confidential statements.

</td></tr><tr><td>

Page size

</td><td>

Select the page size from the choice list.**Note:** A4 is 8.3 x 11.7 inches or 210 x 297 millimeters.

</td></tr></tbody>
</table>5.  Place the cursor in the desired location in the body of the template and click the **Insert Date** or **Insert Signature** buttons to insert these variables.

    You can use these buttons multiple times to add different types of dates or signatures based on the variables you choose.

6.  Click **Save** to save your document and remain on the **HR Document Template** form or click **Submit** to save and return to the **HR Document Templates** list.

7.  Review the look of the generated document by impersonating an employee and submitting the associated catalog item.

    Impersonate the user assigned to work on the case to generate the letter within the HR case. Continue editing and testing the document template until you are satisfied with the generated PDF.

    TinyMCE provides rich text creation that the PDF generator does not support. Non-supported HTML elements are:

    **Note:** The following HTML elements are NOT supported:

    -   Vertical alignment.
    -   Page breaks.
    -   Table-specific color \(text color is supported\).
    -   Custom spacing between blocks of text or images.
    -   Custom column width in HTML tables.
    -   Custom column alignment in HTML tables.
    -   Custom border styling in HTML tables.
    -   CSS text manipulation \(\)including CSS based font tags\).
    -   Inline styling.
    -   Background images.
    See [Editing functions in the TinyMCE editor](https://www.servicenow.com/docs/access?context=r_EditingFunctions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


**Related topics**  


[Configure an HR criteria record](../concept/hr-criteria.md#)

