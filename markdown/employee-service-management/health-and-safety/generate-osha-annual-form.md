---
title: Generate an annual OSHA 300 Log or 300A Summary form
description: Generate an annual 300 Log or 300A Summary OSHA form for all OSHA recordable injuries and illnesses that happened in an establishment between January 1 and December 31 of a calendar year.
locale: en-US
release: yokohama
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Health and Safety Incident Management OSHA Content Pack, Health and Safety injury and illness reports, Health and Safety, Employee Service Management]
---

# Generate an annual OSHA 300 Log or 300A Summary form

Generate an annual 300 Log or 300A Summary OSHA form for all OSHA recordable injuries and illnesses that happened in an establishment between January 1 and December 31 of a calendar year.

## Before you begin

Ensure that the following conditions are met.

-   The Health and Safety Incident Management OSHA Content Pack \(com.snc.sn\_hs\_im\_osha\) application is installed on your ServiceNow instance.
-   The following fields are set in the incidents' injury and illness reports that should be included in the OSHA form.
    -   The **Recordable** option is selected. When you generate an OSHA form, only the recordable incidents are included.
    -   The **Establishment** field contains the establishment name.

Role required: sn\_ohs\_im.compliance\_manager

## About this task

The OSHA 300 Log and 300A Summary forms are generated per establishment per year.

For the PDF export format, the system uses the saved PDF templates for OSHA 300 and 300A forms and fills them with the values from the recordable injury and illness reports.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

2.  Select the incident management icon \(![Incident Management icon.](../image/list-icon-hs.png)\) and navigate to the **Lists** tab.

3.  In the **Lists** tab, under the **Injury / illnesses** list, open a report list.

    -   For reports marked as recordable, select **Recordable**.
    -   For all reports, select **All**.
4.  For the injury and illness reports, review the **Recordable** column.

5.  Select **Generate OSHA forms**.

6.  In the Generate OSHA form dialog box, fill in the fields.

<table id="table_ckg_ylq_dvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form type

</td><td>

Type of OSHA form.-   **OSHA 300 Log**: Log of all work-related injuries and illnesses.
-   **OSHA 300A Summary**: Summary of all work-related injuries and illnesses.


</td></tr><tr><td>

Establishment

</td><td>

Establishment to generate the form for.The form includes all OSHA recordable injuries and illnesses that happened in the selected establishment.

**Note:** In OSHA 300A form, the total hours worked by employees are auto-filled from the establishment's annual information. However, when the total hours information is not available for the selected year for this establishment, the system uses the default value from the Total hours worked system property in the report. For more information, see [Manage the list of establishments](manage-establishment-list.md).

</td></tr><tr><td>

File type

</td><td>

Type of the file the OSHA form is generated in—CSV or PDF.

</td></tr><tr><td>

Year

</td><td>

Calendar year to generate the form for.The form includes all OSHA recordable injuries and illnesses that happened between January 1 and December 31 of the selected calendar year.

</td></tr></tbody>
</table>7.  Select **Generate**.

8.  In the Generate OSHA form dialog box, select the OSHA form name link to download its PDF file.


## Result

-   The OSHA form is generated according to the selected form type and file type.
    -   If the selected file type is PDF, the system uses the saved OSHA 300 and 300A PDF templates and automatically populates them with values from recordable injury and illness reports.
    -   If the selected file type is CSV, the form is generated in CSV format.
-   The generated OSHA report contains all incidents, including the ones marked as sensitive, according to OSHA template. However, sensitive information is not disclosed in the form as incident details are not included.
-   The filled-in OSHA form is saved in the selected establishment.

## What to do next

You can view the saved OSHA form by navigating to the **Establishments** list. For more information, see [View a saved OSHA 300 and 300A form](view-osha-annual-forms.md).

**Parent Topic:**[Health and Safety Incident Management OSHA Content Pack](../concept/generating-osha-forms.md)

