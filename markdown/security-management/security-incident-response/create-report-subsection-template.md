---
title: Create a Report Subsection Template
description: Use the report subsection to further organize the section into multiple subsections and configure their alignment and position using the available types such as Text side panel, Primary, and Secondary.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure Major Security Incident status reports, Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a Report Subsection Template

Use the report subsection to further organize the section into multiple subsections and configure their alignment and position using the available types such as Text side panel, Primary, and Secondary.

## Before you begin

Role required: sn\_msi.workspace\_manager

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **MSI Administration** &gt; **Status Report Setup**.

    The MSI Status Report Setup page displays.

2.  In the Report Template section, select **Configure**.

3.  Open an existing report template and navigate to the respective Report sections list.

4.  In the Report sections list, open an existing Report section template.

5.  Navigate to **Report subsections** &gt; **New**.

    ![Sample Report subsection template](../image/msim-status-subsection.png "Create a Report subsection template") ![]( "Create a Report subsection template")

6.  On the Report subsection form, fill in the fields.

<table id="choicetable_mmr_gym_ysb"><thead><tr><th align="left" id="d162935e132">

Field

</th><th align="left" id="d162935e135">

Description

</th></tr></thead><tbody><tr><td id="d162935e141">

**Name**

</td><td>

Name of the Report template subsection. For example, Scope.**Note:** The existing subsections for the predefined reports are: Overview, Scope, Progress, Explanation.

-   **Overview**: Displays the overview as a subsection within the report.
-   **Scope**: Displays the visualization elements within the report such as the duration counters, incident impact, active teams, and active teams trend.
-   **Progress**: Displays the visualization elements within the report such as the Linked Security Incidents Graphs, Response Tasks Graph, and Collaboration Graphs.


</td></tr><tr><td id="d162935e170">

**Type**

</td><td>

The report subsection type. The available types are:-   **Primary**: This subsection spans the entire width of the page, and is rendered on top of all subsections within the section. There can be only one primary subsection within a section.
-   **Secondary**: This subsection spans the entire width of the page unless used with the text side panel.
-   **Text side panel**: This subsection accompanies the secondary panel and only supports the text.


</td></tr><tr><td id="d162935e197">

**Table**

</td><td>

Name of the report template table.

</td></tr><tr><td id="d162935e206">

**MSI report section template**

</td><td>

The MSI Report Template name for which you’re dividing the report into sections.

</td></tr><tr><td id="d162935e216">

**Order**

</td><td>

The order in which the report subsections will be rendered.

</td></tr><tr><td id="d162935e225">

**Icon**

</td><td>

Use the icon to indicate or highlight the section container on the report runtime configuration form.

</td></tr><tr><td id="d162935e234">

**Active**

</td><td>

Select the check box to create a report subsection for the selected template in the MSIM workspace.**Note:** If the check box is unselected, the MSI Manager can’t create a report subsection for this template in the MSIM workspace.

</td></tr><tr><td id="d162935e246">

**Editor - Content**

</td><td>

Define the template subsection content.

</td></tr></tbody>
</table>7.  Save and **Submit** the new report template section.


**Parent Topic:**[Configure Major Security Incident status reports](../concept/manage-status-reports-for-major-security-incident-management.md)

**Related topics**  


[Create a Report Template](create-report-template.md)

[Create a Report Section Template](create-report-section-template.md)

[Create Report Subsection Element template](create-report-subsection-element-template.md)

[Add system properties](../concept/adding-system-properties-to-your-status-reports.md)

