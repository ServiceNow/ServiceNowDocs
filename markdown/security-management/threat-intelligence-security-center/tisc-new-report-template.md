---
title: Create a new Report Template
description: Create a new case report template according to your business needs of your organization.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [About Report Templates in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Create a new Report Template

Create a new case report template according to your business needs of your organization.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Reports** &gt; **Report Template**.

    This section displays the templates available in the base system, and also the published templates. You can pick any desired template for you to work with the reports.

    **Note:** From this section you can also delete the templates, if required.

3.  Click **New**.

4.  Fill in the details as appropriate.

<table id="choicetable_dzs_2xx_ghc"><thead><tr><th align="left" id="d159642e101">

Field

</th><th align="left" id="d159642e104">

Description

</th></tr></thead><tbody><tr><td id="d159642e110">

**Name**

</td><td>

Name of the report template.

</td></tr><tr><td id="d159642e119">

**Report Category**

</td><td>

Select the desired option from the drop down list. The available report categories are:1.  **Case Reports**: Case Reports allow users to generate and curate reports based on data associated with specific cases.
2.  **Intelligence Reports**: Intelligence Reports allow users to curate reports using data available across the entire Threat Intelligence Library.


</td></tr><tr><td id="d159642e140">

**Description**

</td><td>

Enter a short description for the report template.

</td></tr></tbody>
</table>5.  Click **Save**.

    The Template Content section displays.

    **Note:** Whenever you create a new report template, the template will be in the draft state which means that the template creation is work in progress and any other user will not be able to view the report template until it is complete.

6.  Expand the **Template Contents** to insert the desired fields in the Template body.

    **Note:**

    -   For the Intelligence Reports, in the Template Content section, no substitution variables are available for selection. Only the **current date time script** is supported and this is the only script that can be used.
    -   The template that you're editing allows you to define the template body and select the required variables to add to the template editor section. The templates are supported with Rich text editor \(RTE\) so that you can control various functions available such as indentation, font size, create tables, add images, and various other formatting capabilities.
    -   You can also insert images to your report templates, for that you need to copy and paste the image directly to the template. When add an image then that image is uploaded as an attachment.
    -   You can upload or attach an image which is up to 698 pixels, if the image is above the defined size then it will be automatically adjusted to the original size. This restriction of pixel size will help the PDF report generation to display in a proper format and the images doesn't get truncated in the report.
7.  Add the required elements.

8.  Click **Save Content** to save the contents of your new report template.

9.  Click **Preview** to preview your report format and also to see how a report is generated when you generate any case report.

    **Note:**

    -   **Case Fields**: Whenever you modify your report template\(s\), preview the contents added to the template. For example, when you are generating a case report and you would want to add a field called Short description then you can select that field from the Case fields, then that field is added as a variable in the report template. When a report is generated for the analyst then whatever is the case short description that description will be displayed in the report.
    -   **Records**: Within the report template, you can also add the related records of that particular case which are displayed as the artifacts of the case. For example, if you would want to see any malicious observables in the report from the observables related lists, you can add it to your report template. These related records are displayed in the table format
    -   **Scripts**: Whenever you would want to see the date and time of the report then you can add the **Current Date Time** scripts to your report template, and this will add the Report Created Date and Time.
    -   **MITRE ATT&amp;CK**: This displays the MITRE card associated techniques in your report.
    After you add all the required Case related fields to you report template, you need publish your report template.

10. Click **Publish** to publish the template.

    A confirmation message is displayed whether you want to publish the report template.

    **Note:** When you publish a report template then this template is enabled for all the users. In case if it is outdated, and you want to restrict the report viewing for the users then you can disable the published report, which means the report template will be hidden for the users. You need to re enable the published report for the users to see and use it until then it will be hidden from viewing.

11. Click **Delete** to delete the report template in case if you don't want that report template.

    If you want to rename your report template, click **Edit** and modify the desired fields.


