---
title: Create Report Subsection Element template
description: Use subsection elements to further organize a subsection into multiple elements. Subsection elements help define visualizations, lists, free-form text more declaratively with filter options such as assignment groups and labels.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure Major Security Incident status reports, Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create Report Subsection Element template

Use subsection elements to further organize a subsection into multiple elements. Subsection elements help define visualizations, lists, free-form text more declaratively with filter options such as assignment groups and labels.

## Before you begin

Role required: sn\_msi.workspace\_manager

## Procedure

1.  Navigate to **Major Security Incident Management** &gt; **MSI Administration** &gt; **Status Report Setup**.

    The MSI Status Report Setup page displays.

2.  In the Report Template section, select **Configure**.

3.  Open an existing report template and navigate to the respective Report sections list.

4.  In the Report sections list, open an existing Report section template.

5.  In the Report section template list, open an existing Report subsection template.

6.  Navigate to **Report subsection elements** &gt; **New**.

    ![Sample Report subsection element template](../image/msim-status-subsection-element.png "Create Report subsection element template") ![]( "Create Report subsection element template")

7.  On the Report subsection elements form, fill in the fields.

<table id="choicetable_mmr_gym_ysb"><thead><tr><th align="left" id="d480765e138">

Field

</th><th align="left" id="d480765e141">

Description

</th></tr></thead><tbody><tr><td id="d480765e147">

**Name**

</td><td>

Name of the Report template subsection element. For example, Scope.**Note:** The existing subsections for the predefined reports are: Duration counters, Incident impact, Active Team, Active Team Trend.

-   **Duration Counters**: Displays the duration counter as a subsection element such as estimated time to resolve the incident within the status report.
-   **Incident impact**: Displays the visualization elements within the report such as the impacted assets, impacted locations, and impacted users.
-   **Active Team**: Displays the visualization elements within the report such as the number of active teams involved in closing the major security incident.
-   **Active Team Trend:** Depicts the active teams trend in a graphical representation.


</td></tr><tr><td id="d480765e181">

**Type**

</td><td>

The report subsection element type. The available types are:-   Free Form Text
-   Visualization
-   Custom
-   List


</td></tr><tr><td id="d480765e205">

**Table**

</td><td>

Name of the report template table.

</td></tr><tr><td id="d480765e214">

**Active**

</td><td>

Select the check box to create a report section for the selected template in the MSIM workspace.**Note:** If the check box is unselected, the MSI Manager can’t create a report section for this template in the MSIM workspace.

</td></tr><tr><td id="d480765e227">

**Show by default in the report**

</td><td>

Select this check box if you want to include the section within the report to quickly render the elements.

</td></tr><tr><td id="d480765e236">

**MSI Report Template**

</td><td>

The MSI Report Template name for which you’re dividing the report into sections.

</td></tr><tr><td id="d480765e245">

**Order**

</td><td>

The order in which the report sections will be rendered.

</td></tr><tr><td id="d480765e254">

**Description**

</td><td>

Provide a description to the subsection element type.

</td></tr></tbody>
</table>8.  Save and **Update** the new report template section.


-   **[Create a Free Form Type Element](create-free-form-type-element.md)**  
Create a free form element type to define the free form text more declaratively with filter options such as assignment groups and labels.
-   **[Create a Visualization Type Element](create-visualization-type-element.md)**  
Create a visualization element type to define the visualization elements more declaratively with filter options such as assignment groups and labels.
-   **[Create a List Type Element](create-list-type-element.md)**  
Create a list type element, which defines the related list elements more declaratively with filter options such as assignment groups and labels.
-   **[Create a Custom Type Element](create-a-custom-type-element.md)**  
Create a list type element, which defines the related list elements more declaratively with filter options such as assignment groups and labels.

**Parent Topic:**[Configure Major Security Incident status reports](../concept/manage-status-reports-for-major-security-incident-management.md)

**Related topics**  


[Create a Report Template](create-report-template.md)

[Create a Report Section Template](create-report-section-template.md)

[Create a Report Subsection Template](create-report-subsection-template.md)

[Add system properties](../concept/adding-system-properties-to-your-status-reports.md)

