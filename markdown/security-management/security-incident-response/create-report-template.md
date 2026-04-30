---
title: Create a Report Template
description: Create various report templates, which can be applied to the major security incidents and generate a status report. You can add standard and custom Major Security Incident Response form fields to the report template that are dot-walkable. In addition, you can format and configure the report based on your requirements using sections, subsections, and its elements.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Major Security Incident status reports, Managing MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a Report Template

Create various report templates, which can be applied to the major security incidents and generate a status report. You can add standard and custom Major Security Incident Response form fields to the report template that are dot-walkable. In addition, you can format and configure the report based on your requirements using sections, subsections, and its elements.

## Before you begin

Role required: sn\_msi.workspace\_manager

## About this task

You can define report components to your report templates and provide additional information. Create visualized data to track the scope and progress metrics, add related list data, preview, and generate or share the status reports.

## Procedure

1.  Navigate to **All** &gt; **Major Security Incident Management** &gt; **MSI Administration** &gt; **Status Report Setup**.

    The MSI Status Report Setup page displays.

2.  In the Report Template section, select **Configure**.

3.  Select **New** to create a report template.

4.  On the Report template form, fill the fields.

<table id="choicetable_fll_jgw_wsb"><thead><tr><th align="left" id="d38667e102">

Field

</th><th align="left" id="d38667e105">

Description

</th></tr></thead><tbody><tr><td id="d38667e111">

**Name**

</td><td>

Name of the report template.

</td></tr><tr><td id="d38667e120">

**Branding information**

</td><td>

Select the branding information of your report template such as logo, header, and footer text. For example, Default branding record.

</td></tr><tr><td id="d38667e129">

**Report Type**

</td><td>

Type of status report. The status report can be in one of the following types:-   PDF
-   Email


</td></tr><tr><td id="d38667e146">

**Table**

</td><td>

Name of the report template table.

</td></tr><tr><td id="d38667e156">

**Top/Bottom Margin**

</td><td>

Define the top and bottom margin indentations required while generating the report.

</td></tr><tr><td id="d38667e165">

**Left/Right Margin**

</td><td>

Define the left and right margin indentations required while generating the report.

</td></tr><tr><td id="d38667e174">

**Page Size**

</td><td>

The page size of your report template. For example, the default size is A4.

</td></tr><tr><td id="d38667e183">

**Active**

</td><td>

Select the check box for the MSI Manager to generate a report from the template that was created from the **Reports Template** section.**Note:** If the check box is cleared, then the MSI Manager can't create a report for that specific report template type in the MSIM workspace.

</td></tr><tr><td id="d38667e198">

**First page header editor**

</td><td>

Allows you to define the template body. Select the required variables to add to the template editor section.

</td></tr></tbody>
</table>    ![Create a Report Template](../image/msim-status-report-template-config.png "Create a Report Template") ![]( "Create a Report Template")

5.  **Submit** the new report template record.

    A new report template is created under the Reports Templates page.


-   **[Add Branding to your Report Templates](add-branding-to-your-report-templates.md)**  
Add branding to your reports. You can add header and footer image, header and footer text. You can include this branding information in any of the report template types that you want to create other than the two predefined reports.
-   **[Use Visualizations in Report Templates](using-widgets-in-your-report-templates.md)**  
Use report widgets to define and include User Interface Builder \(UIB\) elements such as data visualizations in the MSIM status reports.
-   **[Use Reports Lists in Report Templates](using-reports-lists-in-your-report-templates.md)**  
Use report lists to define and include the related list artifacts to generate lists in the PDF based on your configured MSI list records.
-   **[Use Template Scripts in your Report Templates](using-template-scripts-in-your-report-templates.md)**  
Create a script to include the related lists data, date operations, and any other data that aren’t directly dot-walkable.
-   **[Preview the Report Template](preview-status-reports.md)**  
Use the Preview functionality to preview your design-time report template to generate and share the report with other stakeholders during run time from the Major Security Incident Management workspace.

**Parent Topic:**[Configure Major Security Incident status reports](../concept/manage-status-reports-for-major-security-incident-management.md)

**Related topics**  


[Create a Report Section Template](create-report-section-template.md)

[Create a Report Subsection Template](create-report-subsection-template.md)

[Create Report Subsection Element template](create-report-subsection-element-template.md)

[Add system properties](../concept/adding-system-properties-to-your-status-reports.md)

[Create and distribute MSIM Status Reports](creating-and-distributing-major-security-incident-status-reports.md)

