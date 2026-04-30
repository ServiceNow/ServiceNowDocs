---
title: Create an Automation Discovery report
description: Create an Automation Discovery report to analyze your records for automation opportunities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-10-29"
reading_time_minutes: 1
breadcrumb: [Automation Discovery, Platform Analytics]
---

# Create an Automation Discovery report

Create an Automation Discovery report to analyze your records for automation opportunities.

## Before you begin

Role required: admin, nlu\_admin, or sn\_auto\_discovery.DiscoveryAuthor

## About this task

**Important:** Starting with the Zurich release, Automation Discovery is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported in Zurich. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Procedure

1.  Navigate to **All** &gt; **Automation Discovery** &gt; **Automation Discovery Reports**.

2.  Select **New Report**.

    ![New report form in Automation Discovery.](../images/new_auto_disc_report_form.png)

3.  Fill in the form fields.

<table id="table_adv_3fk_bpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Data source**

</td><td>

Type of records that you want to analyze.Default is **Incident \(incident\)**.

</td></tr><tr><td>

**Filter by**

</td><td>

Criteria for selecting the records you want to analyze.

</td></tr><tr><td>

**Field to Analyze**

</td><td>

Field on the data tables that you want Automation Discovery to analyze.

</td></tr><tr><td>

**Taxonomy**

</td><td>

Model to run the data against. The default is **ITSM**, which supports English, French, German, Japanese, and Spanish. The **Predictive AIOps** taxonomy supports only English. Select the check box to use the same taxonomy to group unmatched records together.

</td></tr><tr><td>

**Frequency**

</td><td>

How often the report runs with the given conditions. Default is **Run Once**.

You can choose to continuously run a report after adding opportunities to your model to check the improvement.

</td></tr><tr><td>

**Recipient list**

</td><td>

Users to receive the report via email.

</td></tr><tr><td>

**Report name**

</td><td>

Name of the report.

</td></tr></tbody>
</table>    **Note:** The **\# of records** number provides an estimate of how many records meet your criteria.

4.  Select **Run Report**.

    Your report appears at the top of the list on the **Discovery Reports** page. The page lists the **Status** of your report. After the analysis completes, you can select the report to view the results.


