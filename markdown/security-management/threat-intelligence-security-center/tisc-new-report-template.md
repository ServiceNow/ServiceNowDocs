---
title: Create Report Template
description: Create a customized case report template to standardize how case information is documented and presented in your organization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-new-report-template.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [About Report Templates in TISC, Administer, Threat Intelligence Security Center, Security Operations]
---

# Create Report Template

Create a customized case report template to standardize how case information is documented and presented in your organization.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Threat Intelligence Security Center** &gt; **Administration**.

2.  Select **Reports** &gt; **Report Template**.

    This section displays the templates available in the base system and published templates. You can pick any desired template for you to work with the reports.

    **Note:** You can also delete the templates, if required.

3.  Select **New**.

4.  Enter the name and description of the template.

5.  Select **Save**.

    The Template Content section displays.

    **Note:** When you create a report template, it is in draft state. Other users cannot view the template until it is complete.

6.  Expand the **Template Contents** to insert the desired fields in the Template body.

    **Note:**

    -   You can define the template body and select required variables for the template editor section. Templates support Rich Text Editor \(RTE\) functions including indentation, font size, tables, images, and formatting.
    -   You can insert images by copying and pasting them directly into the template. When you add an image, the system uploads it as an attachment.
    -   You can upload images up to 698 pixels. Larger images are automatically resized. This size restriction helps PDF reports display properly and prevents image truncation.
7.  Add the required elements of the case.

8.  Select **Save Content** to save the contents of your new report template.

9.  Select **Preview** to preview your report format and also to see how a report is generated when you generate any case report.

    **Note:**

    -   **Case Fields**: When you modify report templates, preview the added contents. For example, to add a Short description field, select it from Case fields to add it as a template variable. When generating a report, the case short description appears in the report.
    -   **Records**: You can add related case records that display as case artifacts. For example, you can add malicious observables from the observables related list. These related records are displayed in the table format
    -   **Scripts**: To display report date and time, add **Current Date Time** scripts to include Report Created Date and Time.
    -   **MITRE ATT&amp;CK**: This displays the MITRE card associated techniques in your report.
    After adding required case-related fields to your report template, publish the template.

10. Select **Publish** to publish the template.

    A confirmation message is displayed whether you want to publish the report template.

    **Note:** When you publish a report template, it is set to available to all users. If the template is set to outdated, you can disable it to hide it from users. Re-enable the published report to make it visible to users again.

11. Select **Delete** to delete the report template in case if you don't want that report template.

    To rename your report template, select **Edit** and modify the desired fields.


