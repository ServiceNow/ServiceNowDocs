---
title: Import enterprise models and assets using AI assistance
description: Import enterprise models and assets with minimal human intervention by using AI-assisted import.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/import-data-ai-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 21
keywords: [AI-assisted import, column mapping, value mapping, bulk import]
breadcrumb: [Importing enterprise models and assets using AI assistance, Bulk import of your enterprise models and assets, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Import enterprise models and assets using AI assistance

Import enterprise models and assets with minimal human intervention by using AI-assisted import.

## Before you begin

**Important:** AI-assisted import supports simple and consumable models and assets only. If you want to import multi-component models and assets, use a manual import instead. For more information on manual imports, see [Manually import enterprise models and assets in the Enterprise Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/bulk-import-eam.md).

Enable and configure AI Search. AI Search is the search engine that enables you to query the Enterprise model classification \[sn\_ent\_model\_classification\] table when identifying and resolving model classification errors during the AI-assisted import process. For instructions on how to enable and configure AI Search, see [Enabling and configuring AI Search in ServiceNow AI Platform® applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/enable-configure-apps-ais.md).

Role required: You must have either the sn\_eam.enterprise\_admin role or a combination of the sn\_eam.asset\_import\_users and sn\_eam.asset\_manager roles.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **Bulk import** &gt; **AI assisted import**.

4.  Select **New**.

5.  On the form, fill in the fields.

    **Note:** At any point while you're defining the AI-assisted import details, you can view general import tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.

    |Field|Description|
    |-----|-----------|
    |Import name|Name of the AI-assisted import.|
    |Import config|Configuration that defines how and where your external enterprise model and asset data is imported into your ServiceNow instance. For example, you can define the Enterprise Asset Management tables that your data is added to. The default value is **Models and assets**.|
    |Import source file|Spreadsheet that you want to import external enterprise model and asset data from. You must select and attach a spreadsheet in the .xlsx format.|
    |Sheet name|Worksheet that you want to import external enterprise model and asset data from. This drop-down list automatically populates the name of each worksheet in the spreadsheet that you selected and attached in the **Import source file** field.|
    |Header row|Row number of the column headers in the selected worksheet. For example, if the column headers are in row 3, enter a value of `3`.|
    |Copy from template|Import template that you want to populate existing column and value mappings from.|

6.  Select **Next**.

    The import record is created. All data that you want to import from the source spreadsheet is uploaded into your ServiceNow instance.

    -   If you set the **Import config** field to **Create models** or **Models and assets**, the enterprise model import process begins. You're automatically redirected to the corresponding Column mapping page. Proceed to step 7.
    -   If you set the **Import config** field to **Create assets**, the enterprise asset import process begins instead. You're automatically redirected to the corresponding Column mapping page. Skip steps 7 to 14 and proceed directly to [step 15](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md).
7.  Define the column mappings that you want to apply to your imports.

    These mappings define the relationships between columns in your source spreadsheet and columns in the corresponding Enterprise Asset Management target tables.

    **Note:** Consider the following points when defining your column mappings:

    -   If you selected an import template in the **Copy from template** field of the New AI assisted import form, all column mappings from that template are populated automatically. If you did not select an import template, all column mappings are empty by default.
    -   The column mappings that you define manually take precedence over any mappings that you define autonomously.
    -   At any point while you're defining your column mappings, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.
    1.  Define column mappings either autonomously or manually.

<table id="table_cpf_vjd_vjc"><thead><tr><th>

Option for defining column mappings

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Define column mappings autonomously

</td><td>

Select **Auto map** in the Target fields list header.

 The auto-map runs, triggering the ServiceNow AI Lens skill. This skill analyzes the columns in your source spreadsheet and suggests mappings to columns in the corresponding Enterprise Asset Management target tables. Each suggestion is populated in the Target fields list and includes a confidence score from 0% to 100%. Higher scores indicate stronger matches.

 **Note:**

If you define any column mappings manually before running the auto-map, the ServiceNow AI Lens skill does not automatically override them with any AI-generated suggestions. You can replace an existing mapping with an AI-generated suggestion by manually removing the mapping before running the auto-map.

If you run the auto-map multiple times, the ServiceNow AI Lens skill automatically overrides all previous AI-generated suggestions.

</td></tr><tr><td>

Define column mappings manually

</td><td>

1.  In the Target fields and Source fields lists, locate the target and source columns that you want to map to each other.

**Note:** You can map multiple source columns to a single target column. You can also map a single source column to multiple target columns.

2.  Drag the source column from the Source fields list onto the **Source** field of the target column in the Target fields list.

Alternatively, select **+ Add** in the **Source** field to search for and select the source column that you want to map to the given target column.

The confidence score for the mapping is automatically set to 100%.

3.  Repeat step b for each source column that you want to map to the target column.
4.  Repeat steps a to c for each column mapping that you want to define.
 **Important:** You must define the mapping for each target column that is marked as required. All other column mappings are optional.

</td></tr></tbody>
</table>    2.  Review your column mappings to verify that they are accurate.

        Adjust any mappings as needed.

        **Note:** If you want to remove any mappings, use the following options:

        -   To remove the mapping between a target column and a specific source column, select the **X** next to the source column name in the **Source** field.
        -   To remove all mappings between a target column and its source columns, select the **X** in the **Source** field.
        -   To remove all column mappings, select **Clear all** in the Target fields list header.
    3.  Select **Save**.

    4.  Select **Confirm column mappings**.

        The column mappings are confirmed and you're automatically redirected to the Value mapping page.

        **Note:** The Value mapping page is accessible only after you have confirmed your column mappings.

8.  Define the value mappings that you want to apply to your imports.

    Source and target columns can contain choice lists and reference fields. When you map a source column to a target column, you can also map each choice list or reference field value that is supported by the source column to a matching value that is supported by the target column.

    **Note:** Consider the following points when defining your value mappings:

    -   You can define value mappings only for the column mappings that you defined and confirmed in [step 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md).
    -   You can define mappings for reference field values only if the original reference field tables are already populated with the relevant data.
    -   If you selected an import template in the **Copy from template** field of the New AI assisted import form, all value mappings from that template are populated automatically. If you did not select an import template, all value mappings are empty by default.
    -   The value mappings that you define manually take precedence over any mappings that you define autonomously.
    -   At any point while you're defining your value mappings, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.
    1.  Define value mappings either autonomously or manually.

        **Note:** If you don't want to define any value mappings, skip steps a to c and then proceed directly to step d.

        If you don't define some or any value mappings, the original values from your source spreadsheet are uploaded as-is. You must then resolve those values during the Review and import stage before you can import them.

<table id="table_ntt_dld_vjc"><thead><tr><th>

Option for defining value mappings

</th><th>

Procedure

</th></tr></thead><tbody><tr><td>

Autonomously define value mappings for all available column mappings

</td><td>

Select **Auto map all** in the Value mapping list header.

 The auto-map runs, triggering the ServiceNow AI Lens skill. This skill analyzes the choice list and reference field values in your source spreadsheet and suggests mappings to values in the corresponding Enterprise Asset Management target tables. Each suggestion includes a confidence score from 0% to 100%. Higher scores indicate stronger matches.

 **Note:**

If you define any value mappings manually before running the auto-map, the ServiceNow AI Lens skill does not automatically override them with any AI-generated suggestions. You can replace an existing mapping with an AI-generated suggestion by manually removing the mapping before running the auto-map.

If you run the auto-map multiple times, the ServiceNow AI Lens skill automatically overrides all previous AI-generated suggestions.

</td></tr><tr><td>

Autonomously define value mappings for a specific column mapping

</td><td>

1.  In the Value mapping list, locate the column mapping that you want to define value mappings for.
2.  Select **Auto map** next to the column mapping.

The auto-map runs, triggering the ServiceNow AI Lens skill. This skill analyzes the choice list and reference field values in your source spreadsheet and suggests mappings to values in the corresponding Enterprise Asset Management target tables. Each suggestion includes a confidence score from 0% to 100%. Higher scores indicate stronger matches.

**Note:**

If you define any value mappings manually before running the auto-map, the ServiceNow AI Lens skill does not automatically override them with any AI-generated suggestions. You can replace an existing mapping with an AI-generated suggestion by manually removing the mapping before running the auto-map.

If you run the auto-map multiple times, the ServiceNow AI Lens skill automatically overrides all previous AI-generated suggestions.

</td></tr><tr><td>

Define value mappings manually

</td><td>

1.  In the Value mapping list, expand the column mapping that you want to define value mappings for.
2.  Locate the source column value that you want to map a target column value to.
3.  In the corresponding drop-down list, select a matching target column value.

The confidence score for the mapping is automatically set to 100%.

4.  Repeat steps b and c for each value mapping that you want to define.


</td></tr></tbody>
</table>    2.  Review your value mappings to verify that they are accurate.

        Adjust any mappings as needed.

        **Note:** If you want to remove any mappings, use the following options:

        -   To remove all value mappings for a specific column mapping, select **Clear** next to the column mapping.
        -   To remove all value mappings for all available column mappings, select **Clear all** in the Value mapping list header.
    3.  Select **Save**.

    4.  Select **Confirm value mappings**.

        The value mappings are confirmed. The Enterprise Asset Management application uploads data from your source spreadsheet to the corresponding staging tables and then begins preparing the data for review. The Preparing your data for review dialog box opens, displaying status updates as the data preparation progresses.

        **Note:** Processing time varies based on the amount of data that the Enterprise Asset Management application must prepare. Larger amounts of data require longer processing times.

    5.  After all import data is prepared for review, select **Refresh** in the dialog box.

        You're automatically redirected to the Review and import page.

        **Note:** The Review and import page is accessible only after you have confirmed your value mappings and prepared all import data for review.

9.  Review your import data and resolve any resulting errors.

    Before you initiate the import, you can review the data that was uploaded from your source spreadsheet.

    The Enterprise Asset Management application also reviews this data to help identify errors, such as missing field values and unmatched references. If you defined column and value mappings for the import, the application reviews the data and identifies errors based on these mappings. If you didn't define some or any mappings, the application reviews the corresponding data as-is and identifies errors accordingly. You can review and resolve these errors as needed.

    **Note:** At any point while you're reviewing your import data or resolving your errors, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.

    1.  Review all import data by selecting **All Models** on the Review and Import page.

        The Total rows list opens, displaying all enterprise model data that was uploaded from your source spreadsheet.

    2.  Review and resolve your import data errors.

        1.  Review your import data errors through either the Total rows list or the Errors list.

            -   Total rows list: Displays all enterprise model data that was uploaded from your source spreadsheet, regardless of whether the enterprise models have any errors or not.

                You can open this list by selecting **All Models** on the Review and Import page.

            -   Errors list: Displays data for only the enterprise models that have errors.

                You can open this list by selecting **Errors** on the Review and Import page.

            Each error is highlighted in the Total rows and Errors lists. You can filter each list by error type by selecting the Filter by error group icon \[Omitted image "filters-tab-icon.png"\] Alt text: on the corresponding list header.

            Depending on the format that you want to view your data in, you can also toggle between the following list views:

            -   Original: Displays only string values for your enterprise model data. If you defined any value mappings, this list view displays all mapped values as strings. If you didn't define some or any value mappings, this list view displays the original string values from the source spreadsheet.

                You can toggle to this list view by selecting **Original** on the Total rows or Errors list header.

            -   Resolved: Displays choice, reference, or string values for your enterprise model data.

                -   If a choice or reference value is populated in the Original list view, the Resolved list view displays the resolved choice or reference \(sys\_id\) value. For example, the **Resolved manufacturer** column stores references from the target Companies \[core\_company\] table. These references match the values displayed in the Original list view.
                -   If a choice or reference value isn't populated in the Original list view, and there are no matching references in the target table, the corresponding fields in the Resolved list view remain empty. You must select the appropriate choice or reference field values manually.
                -   If any string values in your source spreadsheet correspond directly with string fields in a target table, this list view displays the original string values. For example, the **Model name** column displays the original model name string values from your source spreadsheet.
                You can toggle to this list view by selecting **Resolved** on the Total rows or Errors list header.

            **Note:** If the status of an enterprise model is unmapped or empty, the Enterprise Asset Management application automatically sets it to the default value of In production.

        2.  Automatically resolve errors for missing model categories and classifications.
            -   To resolve errors for missing model categories, select **Populate model category** in the Total rows or Errors list header.

                This option triggers the populate model category skill, which automatically populates missing model categories for your enterprise models.

                **Note:** You can populate missing model categories only for the enterprise models that you have uploaded the following data for:

                -   Manufacturer
                -   Model name or number
            -   To resolve errors for missing model classifications, select **Populate classification** in the Total rows or Errors list header. When the Select source for classification dialog box opens, search for and select a source to populate classifications from.

                This option triggers the populate classification skill, which automatically populates missing classifications for your enterprise models, based on the Enterprise Asset Management data model.

                **Note:** The populate classification skill uses AI Search to query the Enterprise model classification \[sn\_ent\_model\_classification\] table when populating missing model classifications. This table stores all available model classifications and their corresponding classification codes. Before AI Search can perform the query, it must index the table to make the data searchable. In most cases, AI Search indexes the table automatically. However, manual indexing is required under the following scenarios:

                -   The table has never been indexed.

                    This scenario can occur due to AI Search configuration issues or ServiceNow AI Platform issues. It can also occur if you enable and configure AI Search after installing the Enterprise Asset Management application.

                -   You insert a table record that uses a script with the `setWorkFlow()` method set to `false`.
                -   You import or side-load data from an XML file into the table.
                For instructions on how to index a table manually, [Perform a full table index or reindex for a single AI Search indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/index-single-source-ais.md).

                **Note:** You can populate missing classifications only for the enterprise models that you have uploaded the following data for:

                -   Manufacturer
                -   Model name or number
                -   Model category
        3.  Resolve all other errors manually by using either of the following options:
            -   To resolve your errors directly within the Total rows or Errors list, use the following steps:
                1.  Double-click a field value that you must update.

                    These field values are highlighted in the list.

                2.  When prompted, update the field value as needed.
                3.  Select **Apply**.
                4.  Repeat steps a to c for each field value that you must update.
            -   To resolve your errors through the Edit model record window, use the following steps:
                1.  Select the Edit icon \[Omitted image "edit-icon.png"\] Alt text: next to the error that you want to resolve.

                    The Edit model record window opens, indicating which field values you must update to resolve the error.

                2.  Update the field values as needed.
                3.  Select **Update**.
                4.  Repeat steps a to c for each error that you want to resolve.
        4.  Refresh the list of errors by selecting **Revalidate** in the Total rows or Errors list header.

            By refreshing the list, you can determine which errors you resolved successfully and which errors you must still resolve.

            **Note:** You're not required to resolve all errors before initiating the import. If you're unable to resolve an error, the corresponding enterprise model is excluded from the import. Only enterprise models without any errors are included.

10. When you're ready to import your data, select **Initiate Import**.

11. In the Confirm import dialog box, select **Confirm**.

    The import begins, initiating scheduled jobs to upload the data from your staging tables to the corresponding target tables. The Import in progress dialog box also opens, displaying status updates as the import progresses.

    **Note:** Processing time varies based on the amount of data that you're importing. Larger amounts of data require longer processing times.

12. After the import is complete, select **Refresh** in the dialog box.

    You're automatically redirected to the Summary page.

13. Review your import results.

    The Summary page contains various widgets that provide details about your enterprise model imports. Select any widget to view additional details.

    **Note:** At any point while you're reviewing your import results, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.

    |Widget|Description|
    |------|-----------|
    |Models rows|Enterprise models that appear in the source spreadsheet.|
    |Models inserts|Unique enterprise models that were imported into your ServiceNow instance.|
    |Models not imported|Enterprise models that were not imported into your ServiceNow instance.|

    **Note:** If you set the **Import config** field in the New AI assisted import form to **Create models**, skip steps 14 to 19 and proceed directly to [step 20](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md).

14. Select **Next**.

    The enterprise model import process is completed and then the enterprise asset import process begins. You're automatically redirected to the corresponding Column mapping page.

15. Repeat [step 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md) to define column mappings for your enterprise asset imports.

    **Note:**

    -   If you set the **Import config** field in the New AI assisted import form to **Create assets**, the **Model** column appears in the Target fields list. You can then define the column mapping to associate your enterprise assets with existing enterprise models.
    -   If you set the **Import config** field to **Models and assets**, the **Model** column doesn't appear in the Target fields list. In this scenario, enterprise models are also created during the import, so the Enterprise Asset Management application automatically associates each enterprise asset with a model that you have imported.
16. Repeat [step 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/import-data-ai-eam.md) to define value mappings for your enterprise asset imports.

17. Review your import data and resolve any resulting errors.

    Before you initiate the import, you can review the data that was uploaded from your source spreadsheet.

    The Enterprise Asset Management application also reviews this data to help identify errors, such as missing field values and unmatched references. If you defined column and value mappings for the import, the application reviews the data and identifies errors based on these mappings. If you didn't define some or any mappings, the application reviews the corresponding data as-is and identifies errors accordingly. You can review and resolve these errors as needed.

    **Note:** At any point while you're reviewing your import data or resolving your errors, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.

    1.  Review all import data by selecting **All Assets** on the Review and Import page.

        The Total rows list opens, displaying all enterprise asset data that was uploaded from your source spreadsheet.

    2.  Review and resolve your import data errors.

        1.  Review your import data errors through either the Total rows list or the Errors list.

            -   Total rows list: Displays all enterprise asset data that was uploaded from your source spreadsheet, regardless of whether the enterprise assets have any errors or not.

                Open this list by selecting **All Assets** on the Review and Import page.

            -   Errors list: Displays data for only the enterprise assets that have errors.

                Open this list by selecting **Errors** on the Review and Import page.

            Each error is highlighted in the Total rows and Errors lists. You can filter each list by error type by selecting the Filter by error group icon \[Omitted image "filters-tab-icon.png"\] Alt text: on the corresponding list header.

            Depending on the format that you want to view your data in, you can also toggle between the following list views:

            -   Original: Displays only string values for your enterprise asset data. If you defined any value mappings, this list view displays all mapped values as strings. If you didn't define some or any value mappings, this list view displays the original string values from the source spreadsheet.

                You can toggle to this list view by selecting **Original** on the Total rows or Errors list header.

            -   Resolved: Displays choice, reference, or string values for your enterprise asset data.

                -   If a choice or reference value is populated in the Original list view, the Resolved list view displays the resolved choice or reference \(sys\_id\) value. For example, the **Resolved location** column stores references from the target Locations \[cmn\_location\] table. These references match the values displayed in the Original list view.
                -   If a choice or reference value isn't populated in the Original list view, and there are no matching references in the target table, the corresponding fields in the Resolved list view remain empty. You must select the appropriate choice or reference field values manually.
                -   If any string values in your source spreadsheet correspond directly with string fields in a target table, this list view displays the original string values. For example, the **Serial number** column displays the original serial number string values from your source spreadsheet.
                You can toggle to this list view by selecting **Resolved** on the Total rows or Errors list header.

            **Note:** If the state and substate of an enterprise asset are unmapped or empty, the Enterprise Asset Management application automatically sets them to the following default values, based on whether the asset contains a mapped location or stockroom value:

            -   If the asset contains a mapped location value, the state is set to the default value of **In use**.
            -   If the asset contains a mapped stockroom value, the state and substate are set to the default values of **In stock** and **Available**.
            -   If the asset contains both a mapped location and stockroom value, the stockroom value takes precedence over the location value. The state and substate are set to the default values of **In stock** and **Available**.
            If an enterprise asset already has a state and substate, the existing values remain unchanged.

        2.  Resolve your errors using either of the following options:
            -   To resolve your errors directly within the Total rows or Errors list, use the following steps:
                1.  Double-click a field value that you must update.

                    These field values are highlighted in the list.

                2.  When prompted, update the field value as needed.
                3.  Select **Apply**.
                4.  Repeat steps a to c for each field value that you must update.
            -   To resolve your errors through the Edit asset record window, use the following steps:
                1.  Select the Edit icon \[Omitted image "edit-icon.png"\] Alt text: next to the error that you want to resolve.

                    The Edit asset record window opens, indicating which field values you must update to resolve the error.

                2.  Update the field values as needed.
                3.  Select **Update**.
                4.  Repeat steps a to c for each error that you want to resolve.
        3.  Refresh the list of errors by selecting **Revalidate** in the Total rows or Errors list header.

            By refreshing the list, you can determine which errors you resolved successfully and which errors you must still resolve.

            **Note:** You're not required to resolve all errors before initiating the import. If you're unable to resolve an error, the corresponding enterprise asset is excluded from the import. Only enterprise assets without any errors are included.

18. Repeat steps 10 to 12 to initiate and complete the import.

19. Review your import results.

    The Summary page contains various widgets that provide details about your enterprise asset imports. You can select any widget to view additional details.

    **Note:** At any point while you're reviewing your import results, you can view detailed tips and guidelines by selecting the Show guidelines panel icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual sidebar.

    |Widget|Description|
    |------|-----------|
    |Assets rows|Enterprise assets that appear in the source spreadsheet.|
    |Assets inserts|Unique enterprise assets that were imported into your ServiceNow instance.|
    |Assets not imported|Enterprise assets that were not imported into your ServiceNow instance.|

20. If you want to reuse your column and value mappings for future imports, select **Save as template** to save the completed import record as a template.

    When you create additional import records in the future, this template is available to select from in the **Copy from template** field of the New AI assisted import form.


## Result

Your enterprise models and assets are imported into your ServiceNow instance. They appear in the corresponding target tables in the Enterprise Asset Workspace.

**Parent Topic:**[Importing enterprise models and assets using AI assistance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/importing-data-ai-eam.md)

