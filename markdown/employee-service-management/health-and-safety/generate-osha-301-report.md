---
title: Generate an OSHA 301 form
description: Generate an OSHA 301 form for an injury or illness associated with a safety incident.
locale: en-US
release: xanadu
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Health and Safety Incident Management OSHA Content Pack, Health and Safety injury and illness reports, Health and Safety, Employee Service Management]
---

# Generate an OSHA 301 form

Generate an OSHA 301 form for an injury or illness associated with a safety incident.

## Before you begin

Ensure that the following conditions are met.

-   The Health and Safety Incident Management OSHA Content Pack \(com.snc.sn\_hs\_im\_osha\) application is installed on your ServiceNow instance.
-   The **Recordable** option is selected on the injury and illness report.

Role required: sn\_ohs\_im.compliance\_manager

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety Workspace**.

    The Health and Safety Workspace opens in a new tab of the browser window.

2.  Select the incident management icon \(![Incident Management icon.](../image/list-icon-hs.png)\) and navigate to the **Lists** tab.

3.  Open the injury an illness report from a safety incident or from the injury and illness list.

<table id="choicetable_smc_dfc_3bc"><thead><tr><th align="left" id="d628817e110">

Option

</th><th align="left" id="d628817e113">

Steps

</th></tr></thead><tbody><tr><td id="d628817e119">

**From a safety incident**

</td><td>

1.  In the **Safety Incidents** list, select **All**.
2.  In the list, select the incident that you want to generate the OSHA 301 form for.
3.  Select the **Report an incident** tab to open the playbook.
4.  In the **Add injury and illness** activity, select the injury and illness report to generate the OSHA 301 form for.


</td></tr><tr><td id="d628817e155">

**From an injury and illness list**

</td><td>

1.  In the **Injury / illnesses** list, open the report list. For example:
    -   For reports marked as recordable, select **Recordable**.
    -   For all reports, select **All**.
2.  In the list, open the injury and illness report that you want to generate the OSHA 301 form for.


</td></tr></tbody>
</table>4.  Review the injury and illness report and select the **Recordable** option.

    For more information, see [Injury and illness fields](../reference/hs-injury-illness-form.md).

5.  Select **Generate OSHA 301 form**.

6.  In the **Generate OSHA 301 form** dialog box, select the file format to generate the form in, for example, CSV or PDF.

7.  Select **Generate**.


## Result

-   The OSHA 301 form is generated using the saved template for OSHA 301 form and is available in the **Attachments** section of the incident.
-   The OSHA 301 template is automatically filled with the information available in the injury and illness report.

**Parent Topic:**[Health and Safety Incident Management OSHA Content Pack](../concept/generating-osha-forms.md)

