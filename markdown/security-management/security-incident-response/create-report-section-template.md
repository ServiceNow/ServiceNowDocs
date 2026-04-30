---
title: Create a Report Section Template
description: A report can further be divided into various sections. Use the Report section to break down the report into multiple sections and reorganize them in order.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Major Security Incident status reports, Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a Report Section Template

A report can further be divided into various sections. Use the Report section to break down the report into multiple sections and reorganize them in order.

## Before you begin

Role required: sn\_msi.workspace\_manager

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **MSI Administration** &gt; **Status Report Setup**.

    The MSI Status Report Setup page displays.

2.  In the Report Template section, select **Configure**.

3.  Open an existing report template.

4.  Navigate to **Report sections** &gt; **New**.

    The new report section page displays.

    ![Sample Report section template](../image/msim-status-section.png "Create a Report section template") ![]( "Create a Report section template")

5.  On the Report section template form, fill in the fields.

<table id="choicetable_mmr_gym_ysb"><thead><tr><th align="left" id="d170300e121">

Field

</th><th align="left" id="d170300e124">

Description

</th></tr></thead><tbody><tr><td id="d170300e130">

**Name**

</td><td>

Name of the Report template section. For example, Summary.

</td></tr><tr><td id="d170300e139">

**Table**

</td><td>

Name of the report template table.

</td></tr><tr><td id="d170300e148">

**Active**

</td><td>

Select the check box to create a report section for the selected template in the MSIM workspace.**Note:** If the check box is unselected, the MSI Manager can’t create a report section for this template in the MSIM workspace.

</td></tr><tr><td id="d170300e160">

**MSI report template**

</td><td>

The MSI Report Template name for which the report is divided into sections.

</td></tr><tr><td id="d170300e170">

**Order**

</td><td>

The order in which the report sections will be rendered.

</td></tr><tr><td id="d170300e179">

**Icon**

</td><td>

Use the icon to display system icons in the report.

</td></tr><tr><td id="d170300e188">

**Hint**

</td><td>

Use the hint text to guide the report creation. Within the report, the hint text is displayed under the section title.

</td></tr><tr><td id="d170300e197">

**Editor - Body**

</td><td>

Define the template section body. You can define the section body by selecting the custom tokens or variables from the editor.

</td></tr></tbody>
</table>6.  Save and **Submit** the new report template section.


**Parent Topic:**[Configure Major Security Incident status reports](../concept/manage-status-reports-for-major-security-incident-management.md)

**Related topics**  


[Create a Report Template](create-report-template.md)

[Create a Report Subsection Template](create-report-subsection-template.md)

[Create Report Subsection Element template](create-report-subsection-element-template.md)

[Add system properties](../concept/adding-system-properties-to-your-status-reports.md)

