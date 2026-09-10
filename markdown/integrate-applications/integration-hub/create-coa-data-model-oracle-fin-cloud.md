---
title: Create the data model for the Oracle Financial Cloud spoke
description: Configure a chart of accounts structure data model in Oracle Financial Cloud so the Look up chart of accounts action in the Oracle Financial Cloud spoke can retrieve chart of accounts data.Create a BI Publisher report from the chart of accounts data model so the Look up chart of accounts action has a runnable report to call for chart of accounts structure data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/create-coa-data-model-oracle-fin-cloud.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-09-01"
reading_time_minutes: 4
breadcrumb: [Oracle Financial Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create the data model for the Oracle Financial Cloud spoke

Configure a chart of accounts structure data model in Oracle Financial Cloud so the **Look up chart of accounts** action in the Oracle Financial Cloud spoke can retrieve chart of accounts data.

## Before you begin

-   Oracle Financial Cloud must be accessible, and BI Publisher must be enabled for the instance.
-   The chart of accounts structures to be extracted must already be defined in General Ledger.
-   Role required: an Oracle Financial Cloud role with access to Reports and Analytics and permission to create BI Publisher data models.

## About this task

The **Look up chart of accounts** action retrieves chart of accounts structure data through a BI Publisher data model rather than a direct table query. Create the data model once per environment. The data model returns the chart of accounts structure code, segment definitions, and value set details for each ledger, filtered by an optional `P_LEDGER_NAME` parameter.

## Procedure

1.  Log in to Oracle Financial Cloud.

2.  Navigate to **Tools** &gt; **Reports and Analytics** &gt; **Browse Catalog**.

3.  Create the folder structure in this hierarchy: `Custom > ServiceNow > Data Model`.

4.  Click **New**, and select **Data Model**.

5.  From the **Data Model** page, select **SQL Query**.

6.  Enter a name for the query, and in the **Type of SQL** list, select **Standard SQL**.

7.  Paste the following SQL query, click **Validate SQL**, and click **OK**.

    ```
    SELECT   ta.structure_code coa_structure_code, ts.structure_instance_number coa_structure_id,
             gl.ledger_id, gl.NAME legder_name, gl.currency_code ledger_currency,
             b.segment_code, b.segment_identifier,
             b.sequence_number, b.NAME segment_name, b.column_name,
             vs.value_set_code, vs.value_data_type, vs.maximum_length, td.NAME segment_label
        FROM fnd_vs_value_sets vs, fnd_kf_segments_vl b, fnd_kf_structures_tl ta, fnd_kf_structures_b tb,
             fnd_kf_labeled_segments tc, fnd_kf_segment_labels_tl td, fnd_kf_str_instances_vl ts, gl_ledgers gl WHERE 1 = 1
         AND ta.application_id = 101   -- Application Id 101 is for General Ledger
         AND ta.structure_code = tb.structure_code AND tb.structure_id = tc.structure_id(+)
         AND tc.segment_label_code = td.segment_label_code(+) AND ta.LANGUAGE = 'US' AND td.LANGUAGE(+) = 'US'
         AND b.structure_id = tb.structure_id AND b.segment_code = tc.segment_code(+)
         AND b.default_value_set_id = vs.value_set_id AND gl.NAME = NVL (:p_ledger_name, gl.NAME)
         AND tb.structure_id = ts.structure_id AND ts.structure_instance_number = gl.chart_of_accounts_id
    ORDER BY gl.NAME, b.sequence_number
    ```

8.  On the **Add Parameter** page, confirm that the bind parameter `P_LEDGER_NAME` is detected.

9.  Select the checkbox to include the parameter, and click **OK**.

10. From the **Data Model** page, go to **Properties** &gt; **Data Sets**, and select the query to confirm the columns display as expected.

11. Select **Properties**, edit the group name if needed, and click **OK**.

12. Click the **Data** tab, enter a sample value for the `P_LEDGER_NAME` parameter, and view the sample data in tree or table format.

13. Click **Save as Sample Data**.

14. From the **Data Model** menu, go to **Parameters**, and select **Row Placement Order**.

15. Confirm that the row order matches `gl.NAME, b.sequence_number`, as defined in the SQL query's ORDER BY clause, and click **Save**.

    **Note:** This order must match the row order used later in the report definition.

16. When prompted for a save location, save the data model to `Custom > ServiceNow > Data Model`.

17. Name the data model `ServiceNow_COA_Structure_Extract_DM`.


## Result

The data model is saved to the BI Publisher catalog and is available as the data source for the **Look up chart of accounts** action's report extract.

## Create the BI Publisher report for the data model

Create a BI Publisher report from the chart of accounts data model so the **Look up chart of accounts** action has a runnable report to call for chart of accounts structure data.

### Before you begin

-   The `ServiceNow_COA_Structure_Extract_DM` data model must already be created and saved to `Custom > ServiceNow > Data Model` in Oracle Financial Cloud.
-   Role required: an Oracle Financial Cloud role with access to Reports and Analytics and permission to create BI Publisher.

### Procedure

1.  In BI Publisher, select **New**, and under **Published Reporting**, select **Report**.

2.  On the **Create Report** page, click **Use Data Model**.

3.  From **Create a report using an existing Data Model**, select `ServiceNow_COA_Structure_Extract_DM`, and click **Next**.

4.  On the following page, leave the default values, and click **Next**.

5.  Clear the **Show Grand Totals Row** checkbox at the bottom of the page.

6.  Drag and drop all required columns from the Data Source pane on the left into the layout area on the right, including every column needed for the extract.

7.  Click **Finish**.

8.  Save the report to `Custom > ServiceNow`, and name it `ServiceNow_Charts_of_Accounts_Structure_Extract_Report`.

9.  Run the report to confirm the data displays correctly, and enter a sample value for the bind parameter `P_LEDGER_NAME` if prompted.

10. Edit the report, go to the row placement settings, and confirm that the row order matches the order defined in the data model.

11. While editing the report, click **View as List**, and from **Output Formats**, select **Data \(XML\)** as the output format for the report, and set it as the default format.

    \[Omitted image "oracle-fin-cloud-spoke-coa-11.1.png"\] Alt text: Layout page for the report with Data \(XML\) set as the default format.

    \[Omitted image "oracle-fin-cloud-spoke-coa-11.2.png"\] Alt text: Output Formats list with the Data \(XML\) checkbox selected.

12. Save the report.


### Result

The report is saved to the BI Publisher catalog and produces chart of accounts structure output in the required format, ready for the **Look up chart of accounts** action to consume.

