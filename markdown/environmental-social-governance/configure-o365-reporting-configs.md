---
title: Set up Microsoft 365 reporting configuration
description: Set up the Microsoft 365 reporting configuration records to specify the data points and reports that you want to import in to a Microsoft Word document for disclosure reporting purposes.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Integrating Microsoft 365 with ServiceNow reporting, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Set up Microsoft 365 reporting configuration

Set up the Microsoft 365 reporting configuration records to specify the data points and reports that you want to import in to a Microsoft Word document for disclosure reporting purposes.

## Before you begin

Role required: \(per product\)

-   In Environmental, Social, and Governance Management: sn\_esg\_msoff\_intg.admin
-   In Audit Management: sn\_audit.admin

## About this task

Data is imported into a Microsoft Word document for disclosure reporting purposes. When creating these Microsoft Word disclosures, you must specify which tables, reports, and data visualizations from your ServiceNow instance must be used to import data into your Microsoft Word document. You can also specify the columns from a table from which you want to import data. Only those reports that are either created by or shared with the ESG administrator are available for selection.

## Procedure

1.  Navigate to once of the following locations:

    -   **All** &gt; **Environmental, Social, and Governance** &gt; **Microsoft 365 Reporting Integration** &gt; **Reporting Configurations**
    -   **All** &gt; **Audit** &gt; **Audit report** &gt; **Reporting Configurations**
2.  From the Microsoft 365 reporting configurations list, select **New**.

3.  On the Microsoft 365 reporting configuration form, fill in the fields.

<table id="table_lh1_zzx_5vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Business domain

</td><td>

Domain from where the configuration is created. This field is automatically set to ESG.

</td></tr><tr><td>

Reporting item

</td><td>

Name of the configuration. For example, if you want to get data about your ESG goals in your word document, you can provide a name such as `My ESG goals`.

</td></tr><tr><td>

Source type

</td><td>

Source from which you want to fetch the data. The choices are as follows:-   **Table**: Select this option when you want to import data from a table.
-   **Report**: Select this option if you want to import data from a predefined report or chart. For more information on how to create a report, see [Create a report with Analytics Q&amp;A](https://www.servicenow.com/docs/access?context=t_CreateYourOwnReport&version=xanadu&pubname=xanadu-now-intelligence&section=create-report-nlq&ft:locale=en-US).
-   **Data visualization**: Select this option if you want to import data from a data visualization in the Performance Analytics library. For more information, see [Overview of data visualization types](https://www.servicenow.com/docs/access?context=data-visualization-type-overview&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).
 **Note:** Only list reports, pivot reports, multi-level pivot reports, horizontal and vertical bar charts, and pie charts are available for selection. Stacked bar charts and grouped bar charts are not supported.

</td></tr><tr><td>

Source table

</td><td>

Source table to fetch data from. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Filter

</td><td>

Filter conditions to filter the records. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Columns

</td><td>

Column from the table whose values are to be inserted. This field only appears when **Table** is selected from the **Source type** field.

</td></tr><tr><td>

Source report

</td><td>

Available report to be inserted in the disclosure report. This field only appears when **Report** is selected from the **Source type** field.

</td></tr><tr><td>

Active

</td><td>

Option to indicate if the record is active. Only active records are available for selection in the document.

</td></tr><tr><td>

Track configuration

</td><td>

Option to track any changes made to the data inserted using configuration and log those changes in the log table.

</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Add additional reporting configuration filters to the reporting configuration. These filters help to fetch the data into your Microsoft Word disclosure report. For more information, see [Add additional reporting configuration filters for a Microsoft 365 configuration record](add-additional-reporting-filters.md).

-   **[Configure a business domain role](configure-business-domain-roles.md)**  
Configure the business domain roles so that users of a particular domain can select the domain for which they want to import the data. Only those users who are added during the configuration are able to view the domain on the Microsoft Word document.

**Parent Topic:**[Integrating Microsoft 365 with ServiceNow reporting](../concept/integrating-o365-with-servicenow.md)

