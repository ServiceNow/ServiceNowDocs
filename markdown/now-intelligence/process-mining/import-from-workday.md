---
title: Import Workday or Salesforce data
description: Use the data available in Workday or Salesforce to optimize your processes and solve business problems. To use these datasets, you must first import them into ServiceNow environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/import-from-workday.html
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 4
breadcrumb: [Process Mining for Workday and Salesforce, Import external data, Process Mining, Platform Analytics]
---

# Import Workday or Salesforce data

Use the data available in Workday or Salesforce to optimize your processes and solve business problems. To use these datasets, you must first import them into ServiceNow® environment.

## Before you begin

Role required: sn\_process\_mining\_admin

## Procedure

1.  Create an audit table to store data.

    Audit table is a staging table that is created with the required columns to populate the external data.

    For detailed procedure, see [Create an audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-table.md).

2.  Add custom fields to the audit table.

    The custom fields form as breakdown filters when viewing the process graph. Without custom fields, there won't be any breakdown filters.

    For detailed procedure, see [Add custom fields to the audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/add-custom-field.md).

3.  Import data into the audit table.

    Create a Workday or Salesforce configuration record so Process Mining can pull audit log data from Workday or Salesforce and map it to the fields in ServiceNow®.

    Use this procedure to set up a new connection between Workday or Salesforce and Process Mining, define the initial data window, and map source fields to ServiceNow® fields.

    1.  Navigate to **All** &gt; **Process Mining** &gt; **External Data Set** &gt; **Connectors**.

        The Connector Configurations page is displayed.

        \[Omitted image "app-conn-config.png"\] Alt text: Connector configurations list

    2.  Select **New**.

        The Connector Configuration new record form is displayed.

        \[Omitted image "app-config-record.png"\] Alt text: New connector configuration record

    3.  Provide the details on the form.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration, for example Workday or Salesforce.

</td></tr><tr><td>

Type

</td><td>

Source app for this configuration.The available values are:

-   **Workday**: Select if you're trying to create a Workday configuration.
-   **Salesforce**: Select if you're trying to create a Salesforce configuration.


</td></tr><tr><td>

Subflow

</td><td>

Subflow for the selected **Type**.

</td></tr><tr><td>

Table

</td><td>

Table that stores the imported data. It is auto-populated.This is the table that is created in the [Create an audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-table.md) section.

</td></tr><tr><td>

Active

</td><td>

This is selected by default.This confirms that the connector configuration is active.

</td></tr><tr><td>

Fullpull

</td><td>

This is selected by default.This confirms that the entire data is pull from the source to the target. After the first import, this field is unchecked automatically. From the next time, when you import data, only the delta data is imported.

</td></tr><tr><td>

Import from date

</td><td>

Start date and time for the initial data import.

</td></tr><tr><td>

Domain

</td><td>

This is selected by default and can't be edited.

</td></tr><tr><td>

Action inputs

</td><td>

The type of action input you must provide. Currently, only query is available.In the **Value** field, provide the query. The query must include the name of the columns you must import.

For example:

```
SELECT  workdayID, businessProcessType, processHistory{process, cf_CF_IS_Subprocess, status, completedOn, dueDate, person} as processHistory FROM businessProcessTransactions
```

</td></tr></tbody>
</table>    4.  Save the record, and the select **Retrieve Field Mapping**.

        After you select **Retrieve Field Mapping**, the **Action Output** field is populated with column names of the source table.

    5.  Complete the field mapping in the **Field Mapping** area.

        The field names displayed are the ones you have created for the target table. Match them with the source target table fields from the **Action Output** field.

    6.  Select **Run Import Job**.

        The data import starts. The status is updated in the Connector Executions area.

        **Note:** If an import takes more than 24 hours, it gets automatically cancelled. This is managed by the sn\_po\_extdata.cancel\_job\_after\_seconds system property. For more information, see [Process Mining properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/components-installed.md).

        The Salesforce data is imported in batches. This is managed by the sn\_promin\_sf.salesforce\_data\_chunk\_size system property. For more information, see [Process Mining properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/components-installed.md).

    The data from the source is imported to your Process Mining audit table.

4.  Go to the **Import data** tab in Process Mining Workspace.

5.  Select **Import with another app**.

6.  Select **OK** on the notification message.

7.  Select **Yes, my data import is complete** check box.

8.  Select **Next**.

9.  On the next page, verify the data you’ve imported.

    Verify that the mandatory and custom fields have the value that you had specified in your source file.

10. Select **Edit your dataset** link if you want to import your dataset again or edit the imported dataset.

11. Select **Confirm and continue** after validating your data.

12. After you’ve validated your imported data, create a record table from the **Record Data** section.

13. Select an option under **How do you wish to add the record table?**.

    If your audit table has custom fields, then the two options are grayed out. By default, **Generate record data table** is selected.

14. Select **Create record**.

    After the record table is created, a tab opens displaying details of the audit and record tables.


## Result

The data is now completely imported to your process Mining instance. You can now create a project using this data to analyze improve your processes.

For information on creating a project, see [Create a project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/create-project.md). For information on managing an audit table, see [Managing an audit table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/managing-audit-table.md).

