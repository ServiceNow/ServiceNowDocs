---
title: Post incident review report
description: The Post Incident Review \(PIR\) reports feature enables you to set up and download the post incident review reports using the Post Incident Review tab.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Manage post incident activities, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Post incident review report

The Post Incident Review \(PIR\) reports feature enables you to set up and download the post incident review reports using the Post Incident Review tab.

The security admin can create and configure the report templates and map those templates to the security incident using the report configuration. A security analyst can then view or download the report after the security incident is resolved and the status is updated to Review state.

A PDF report is generated and attached to the security incident when the incident is moved to the Closed state after successful configuration.

**Note:** The reports feature is applicable and supported from Orlando Patch9.

To customize your post incident review reports, you must do the following configuration.

1.  **Report Templates**: Customize and configure the following report template features to add additional information on the report:
    1.  Timeline
    2.  Branding
    3.  Template Scripts
2.  **Report Configuration**

This section describes the configuration procedure:

## Report Templates

Use  the  Report  Templates  section to create primary and additional report templates that are applied  to  the security incidents  to  generate  the  Post Incident Review  report. You can format  and  configure  the report based on your requirements. The templates also helps you to include the assessment details in the template.

Following are a few optional steps that can be performed while building the template:

1.  Configuring the branding information.
2.  Setting up the page size and page margin.
3.  Adding any security incident related fields \(both custom and standard\).
4.  Using the following predefined custom tokens:  
    1.  **$sessionUser**: returns  the logged in username
    2.  **$date**:  returns  the current date
    3.  **$if\_not\_null\_start &amp; $if\_not\_null\_end**: if these tags are used against any fields then the tags are displayed only if the value exists.  For example:  
        -   **$\{if\_not\_null\_start:problem\}**
        -   **Problem Category: $\{problem.category\}**
        -   **$\{if\_not\_null\_end:problem\}**
5.  Including the related list data using the template scripts. For more information, see the section below on **Template Scripts**.
6.  Including the timeline information using the Timeline Filters. For more information, see the section below on **Timeline**.
7.  Managing and formatting the template content such as attachments, tables, and images.

**Note:** The enhanced report template toolbar features are available only from the Paris release version.

Report templates key points:

1.  The images attached to the report template are displayed on the Post Incident Review report only when they’re included in the  sys\_attachment  table. 

    **Note:** Images selected from the db\_image table won’t be displayed on the post incident review report.

2.  Videos aren’t supported in the post incident review report.
3.  The URLs in the PDF are non-clickable. To enable the URLs non-clickable \(.\) is denoted as \(dot\).
4.  The report isn’t generated if the size of the report template exceeds 50MB. 
5.  The font family selected for the report template content won’t be applied to the PDF if it isn’t supported by the PDF generator.

    **Note:** If the corresponding font is not there, the PDF generator identifies the closest alternative font and then generates the PDF.

6.  If you provide higher page margin values, generate post incident review report is failed. For example, Top and Bottom margin &gt; 450  and Left and Right margin &gt; 450.
7.  If a large text is included in the report template without spaces, then the text may be truncated. Preview the text and modify it accordingly.

The security admin can preview the report using the **Preview Report** button available on the Report Template page.

**Note:**

**Select a Security incident to preview a report with this template** option and select **Preview Report**.

## Branding

You can add the branding template name, header  and  footer image, header and footer text, generate page numbers, and include the branding record in the report template after it’s created.

The following is a sample  branding report format:

Report template branding key points:

1.  The maximum size allowed for the header and footer image is 5MB. If the size exceeds more than the specified limit, then an error message, ‘Image format cannot be recognized’ is displayed in the security incident.
2.  The footer text length is limited to 100 characters.
    1.  If the footer image text and report content are overlapped while previewing, you must change the branding record.
    2.  If the footer text contains a URL link, then it may overlap on to the footer image. Preview and correct it as required.

## Timeline

Timeline configuration enables you to create and modify the timeline filters as required. You can  filter  the activity types that should be included in the report, configure if the child tasks should be included or excluded in the report, and configure if the images should be included or excluded in the report.

If you want to use and populate any timeline configuration, you must add the tag as mentioned below: **$\{timeline:timeline name\}**. Two  sample timeline  configurations  as an example are  provided  in the set up that are used in  the  Phishing Report template and Default Report template.  You can modify and reuse the configurations. 

## Template Scripts

Use the template scripts to include the related lists data, date and time stamp, and any other data that aren’t directly dot-walkable. The following is an example:

**Construct a template script to display the related list on report template**:

1.  To prepare the related list data, call PostIncidentReportUtils.fetchRelatedListDataForReport method.
2.  To represent the step1 data in the table format and style, call the ReportTemplateUtil.constructTablefunction method.

If you want to use and populate any template script, then you must add the tag template script tag as **$\{template\_script:script name\}**.

Following are a few sample template scripts provided to configure and modify your post incident reports.

|Script name|Description|
|-----------|-----------|
|formatted\_current\_date|Returns the current local date and time in the DDMMYYYY 00.00 AM or PM format. For example, 21 Jan 2021 3:51 PM PST.|
|si\_affected\_users|Returns the affected users from the related list in a tabular form.|
|si\_assessments|Returns the post incident assessment results in a tabular form.|
|si\_associated\_phish\_emails|Returns the associated phishing emails from the related list in a tabular form.|
|si\_associated\_phish\_headers|Returns the associated phishing headers from the related list in a tabular form.|
|si\_business\_criticality|Returns color coded business criticality value.|
|si\_malicious\_observables|Returns the malicious observables from the related list in a tabular form.|
|si\_observables|Returns the observables from the related list in a tabular form.|
|si\_priority|Returns color coded priority value.|
|si\_response\_tasks|Returns the response tasks from the related list in a tabular form.|
|si\_time\_to\_identify|Returns the duration spent in Draft and Analysis state.|
|si\_time\_to\_resolve|Returns the time to resolve the incident.|

Report template scripts key points:

1.  If a related list is added with more than five columns, the table data is truncated during the PDF generation.  Each column minimum width is set to 124px.
2.  If a template script is unable to load the content in the report template due to technical issues, an error message is displayed on the report, ‘Error while evaluating the template script’ and the security admin must evaluate the correctness of the script to resolve the issue.
3.  si\_assessments: By default, all the assessment categories are added to the report. The security admin can filter  the data by modifying the template script as required. Add the **categories: sys\_id1,  sys\_id2;** parameter to filter the data.
4.  Time to resolve and time to identify scripts: Use the definition records that are part of the metric-related list. If the definition records are unavailable  for the security incident, then create or add those definition records to populate the values for the two fields.

**Note:**

By default, the Security Admin doesn’t have access to view the version records  of any table. You must add an admin role to access the version records and revert to the previous version.

## Report Configuration

Use the Report Configuration section to set up the conditions and apply the report templates to  the  Security Incidents. You can add one primary report and one or more additional report templates to the same condition.

The following is an example condition that is provided to apply the Phishing Report template to the Phishing category incidents and  the other  one to apply the Default Report template to all the security incidents.   The Default Report template would be applied to the security incidents  if the conditions aren’t met.

## Procedure to turn off the new implementation

1.  Deactivate the following business rules:
    1.  Generate PIR PDF
    2.  Create Knowledge On Closure New
2.  Activate the following business rules:
    1.  Generate PIR when in Review and Close
    2.  Create Knowledge On Closure
    3.  \[Regen PIR on closure/cancel/delete\]
3.  Activate the UI rule, **Hide PIR field when empty**.
4.  Go to the form layout in the security incident form. Under **Post Incident Review** section:
    1.  Remove PIR report picker from the PIR section
    2.  Add the Post Incident Report field to the PIR section

## Configure Post Incident Review \(PIR\) report properties for child security incidents

You have an option to configure the following two PIR report properties for child security incidents:

-   **sn\_si.generate\_pir\_report\_for\_child\_si**
-   **sn\_si.include\_child\_si\_timeline\_in\_pir**

**Note:** Users with the administrator \[admin\] role can view the properties. Users with the Security administrator \[sn\_si.admin\] role can modify them.

<table id="table_q34_gsf_jzb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

sn\_si.generate\_pir\_report\_for\_child\_si

</td><td>

Option to enable the generation of Post Incident Review \(PIR\) reports for child security incidents.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: Navigate to All &gt; System Properties &gt; All Properties.

</td></tr><tr><td>

sn\_si.include\_child\_si\_timeline\_in\_pir

</td><td>

Option to include the timeline of the child security incidents in the parent Security Incident's PIR report.-   **Type**: true \| false
-   **Default value**: false
-   **Location**: Navigate to All &gt; System Properties &gt; All Properties.

</td></tr></tbody>
</table>