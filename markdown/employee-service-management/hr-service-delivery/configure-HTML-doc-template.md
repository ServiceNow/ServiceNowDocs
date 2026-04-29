---
title: Configure an HTML document template
description: Create or modify the document template with your unique company logo and audience criteria.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Document Templates of type HTML, Configuring Document Templates, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Configure an HTML document template

Create or modify the document template with your unique company logo and audience criteria.

## Before you begin

Role required: sn\_hr\_core.admin and Delegated developer

## About this task

Configure an HTML document template 

## Procedure

1.  Navigate to **All** &gt; **Document Templates** &gt; **All Document Templates**.

2.  Select **New**.

3.  Select **HTML Document Template**.

4.  On the form, fill in the fields.

<table id="table_dvm_fm3_zhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the document template.

</td></tr><tr><td>

Table

</td><td>

Table associated with the type of template. The table determines the available variables that can be used.**Note:** Tables appear based on the application scope that is selected.

</td></tr><tr><td>

Category

</td><td>

Document category in which the template is added.

</td></tr><tr><td>

User criteria

</td><td>

Audience criteria for this document. For example, you can create a letter intended for only Canadian employees.**Note:** When defining conditions like case sensitivity or null values, see API [GlideFilter - Scoped, Global](https://www.servicenow.com/docs/access?context=c_GlideFilterScopedAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Body

</td><td>

Text in the template.To insert variables, place your cursor in the desired location and select the variable. Available variables are listed under **Fields**.

Document template styles are applied to regular text fields, and not for rich description fields. A rich description field preserves its own HTML formatting and style and is not overridden by the document template formatting and style.

Use the formatting tools in the **Body** to apply formatting options, such as bold, italic, underline, font styling. The body is a place holder for HTML text and tokenized variables.

 **Note:**

-   Jelly and CSS Styling are not supported.
-   You can also use [Document template scripts](../concept/document-template-scripts.md) to dynamically change the text in the HTML body.


</td></tr><tr><td>

Start date

</td><td>

Date starting which the HTML document template is valid. **Start date** helps in maintaining multiple versions of same template.**Note:** Start date must be before the end date.

</td></tr><tr><td>

End date

</td><td>

Date until which the HTML document template is valid. **End date** helps in maintaining multiple versions of same template.By default, if the values in **Start date** and **End date** are empty it will imply that the template will always be valid.

If you specify an end date, you must also specify a start date.

</td></tr><tr><td>

Template date format

</td><td>

Format in which you want the date to appear when an agent previews the document, generates the attachment, or initiates document tasks for participants.**Note:**

-   When signing using a ServiceNow application or the AdobeSign application: If no value is selected in **Template date format**, the value specified in the **template\_date\_format** system property is considered. If both **Template date format** and **template\_date\_format** system property are empty, the value in the Date format field from the agent's user profile is considered.
-   When signing using a DocuSign application: The date format selected in Signing settings in the DocuSign application is considered over **Template date format** in the configured HTML template in a ServiceNow instance.


</td></tr><tr><td>

Template language

</td><td>

Language in which you want dynamic tokens to be translated when an agent previews the document, generates the attachment, or initiates document tasks for participants. The **Template language** field is also used for full template translation.**Note:**

-   Template language is a mandatory field. The default language is none.
-   Translation feature is available only when language plugins are installed on the instance.


</td></tr><tr><td>

Select variables

</td><td>

List of variables that can be used in the body of the template. Variables pull information from the selected table to customize the template.Offsets are supported for date variables. Offsets extend or subtract days, weeks, or months from a date used in a template.

Valid date offset variables are:-   + \(plus\)
-   - \(minus\)
-   d \(days\)
-   w \(weeks\)
-   m \(months\)
 Examples:

-   Offer letter \(five days after the stated date\): Your offer is valid until $\{Date +5d\}.
-   Benefits for terminated employee \(two weeks from termination date\): Your benefits end effective $\{subject\_person.hr\_profile.employment\_end\_date +2w\}.
 **Note:** Only variables that you have access appear.

</td></tr><tr><td>

Signing type

</td><td>

Option to specify the application that is used for signing the document. For example, ServiceNow Sign, DocuSign or AdobeSign.**Note:** Signing types are available only when the respective integration plugins are installed.

</td></tr><tr><td colspan="2">

**Header**

</td></tr><tr><td>

Header image

</td><td>

Image to be displayed in the header. You can add your company logo using this feature.**Note:** Supported file types are: JPEG, JPEG2000, GIF, PNG, BMP, WMF, TIFF, and JBIG2.

</td></tr><tr><td>

Header image position

</td><td>

Position where you want the header image to appear : left, right, or center.

</td></tr><tr><td>

Header image height

</td><td>

Height of the image in the header. **Important:**

-   The height and width of the image is scaled proportionally based on the value that you specify.
-   Ensure that the height of the image is lesser than the value specified in the **Page size** field, otherwise, the image is cropped.


</td></tr><tr><td colspan="2">

**Footer**

</td></tr><tr><td>

Footer image

</td><td>

Image to be displayed in the footer.**Note:** Supported file types are: JPEG, JPEG2000, GIF, PNG, BMP, WMF, TIFF, and JBIG2.

</td></tr><tr><td>

Footer image height

</td><td>

Height of the image in the footer. **Important:**

-   The height and width of the image is scaled proportionally based on the value that you specify.
-   Ensure that the height of the image is lesser than the value specified in the **Page size** field, else, the image is cropped.


</td></tr><tr><td>

Footer image position

</td><td>

Position where you want the footer image to appear: left, right, or center.

</td></tr><tr><td>

Footer text

</td><td>

Text to be displayed in the footer. For example, you can add proprietary and confidential statements.

</td></tr><tr><td>

Footer text position

</td><td>

Position where you want the footer image to appear: left, right, or center.

</td></tr><tr><td>

Vertical alignment

</td><td>

Vertical alignment of the footer text with the footer image.

</td></tr><tr><td colspan="2">

**Page**

</td></tr><tr><td>

Page size

</td><td>

Size of the page that can be selected from the list such as Letter, A4, or Legal.

</td></tr><tr><td>

Custom font

</td><td>

Custom font from the PDF Generation Font Families table.**Important:** Make sure that you use the custom font family in the CSS of the HTML body.

</td></tr><tr><td>

Top/Bottom margin

</td><td>

Space from the top of the page until the starting of the HTML content or space from the bottom of the page until the ending of the HTML content.

</td></tr><tr><td>

Left/Right margin

</td><td>

Space from the left of the page until the starting of the HTML content or space from the right of the page until the ending of HTML content.

</td></tr></tbody>
</table>5.  Place the mouse in the desired location in the body of the template and select the **Insert Date** button to insert date variables.

    You can use the button multiple times to add different types of dates based on the variables you choose.

6.  Select **Add blocks**.

    1.  To add an existing document block to the template, in Search blocks, type in the name of an existing document block, select the document block, and select **Insert**.
    2.  To add a new document block to the template, click **Create New Block**. For more information, see [Create document blocks in Document Templates](create-doc-blc.md).
7.  To automatically generate Table of Contents \(TOC\) and page numbers in the document that is generated from an HTML template, perform the following steps:

    1.  In the **Table of Contents** field, select the TOC configuration that you want to apply on the HTML template.
    2.  In the **Page number** field, select the page number configuration that you want to apply on the HTML template.
    3.  Select **Insert Table of Contents** and insert the Table of Contents macro in the required position in the body of the HTML template.

        **Note:** The Table of Contents macro will not be displayed if the TOC configuration is not selected in the **Table of Contents** field.

8.  To translate content in templates using Localization Framework, select **Translate**.

    For more information, see [Use Localization Framework for Document Templates](doc-lzt-fm.md).

9.  To save your document and remain on the **HTML Document Template** form, click **Save**.

10. To save and return to the All Document Templates list, select **Submit**.


