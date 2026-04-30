---
title: Create a Custom Type Element
description: Create a list type element, which defines the related list elements more declaratively with filter options such as assignment groups and labels.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create Report Subsection Element template, Configure Major Security Incident status reports, Manage MSIM status reports, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a Custom Type Element

Create a list type element, which defines the related list elements more declaratively with filter options such as assignment groups and labels.

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

7.  Fill in the report subsection elements form with the required details as explained in [Create Report Subsection Element template](create-report-subsection-element-template.md).

8.  Navigate to the Report Subsection element Type field, and select the **Custom** option.

    This displays the **Custom content** section.

9.  On the Custom content form, fill in the fields.

<table id="choicetable_dyq_gmn_ysb"><thead><tr><th align="left" id="d398718e146">

Field

</th><th align="left" id="d398718e149">

Description

</th></tr></thead><tbody><tr><td id="d398718e155">

**Dynamic content**

</td><td>

Enter the dynamic content such as the template scripts.

</td></tr><tr><td id="d398718e164">

**Run time configurable**

</td><td>

Select this check box if the custom element type is run time configurable.

</td></tr><tr><td id="d398718e173">

**Runtime config UX App Route**

</td><td>

Enter the Runtime configuration UX App Route value when a UIB page is created with the required configuration experience.**Note:** This field appears only when the **Run time configurable** option is selected.

</td></tr></tbody>
</table>
## The following is an example of the report template subsection element type for a Technical Status Report

![Report template subsection element type for a Technical Status Report](../image/custom-element-type.png "Report subsection element type")

**Parent Topic:**[Create Report Subsection Element template](create-report-subsection-element-template.md)

