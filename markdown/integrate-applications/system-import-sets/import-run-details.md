---
title: Import run details
description: View detailed information about import set runs, individual rows in the import set, and import logs.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Data and Automation]
---

# Import run details

View detailed information about import set runs, individual rows in the import set, and import logs.

There are two ways to run or process an import set. The data displayed after the run varies slightly depending on which way you choose.

-   **Robust import set transformers**

    Separate the transform and processing functions, providing a more flexible alternative to transform maps. Robust import set transformers enable you to extract data from a source table into an intermediary data structure. You can transform the data as desired and then load that data to one or more target tables. Records are processed as batches to enhance performance. For more information, see [Robust Import Set Transformers](robust-import-set-transformers.md).

-   **Transform maps**

    Legacy method to map data from an import set staging table to a single target table. Transform maps combine the transform and processing functions into a single process. Each time you run a transform map, the system must load data from the import set staging table, transform it, and then insert it into a single target table. You can define multiple table mappings with multiple transform maps. For more information, see [Transform maps](../../../script/server-scripting/concept/c_CreatingNewTransformMaps.md).


After running the import, you can view the import history by navigating to the Import Set record and checking the tabs below the Related Links section. They cover the import set runs, import set rows, and import log.

## Import Set Runs

The **Import Set Runs** tab provides details about individual imports.

![An Import Set record showing the Import Set Runs tab.](../image/import-set-runs.png "Sample data for a completed import done with a robust import set transformer")

The following table provides more details about the fields in the image.

<table id="table_l3w_41n_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Started

</td><td>

Date and time the import started. Given in the time zone of the logged-in user.

</td></tr><tr><td>

State

</td><td>

State of the import. Options are:-   Cancelled
-   Cancel requested
-   Complete
-   Complete with errors
-   Did not complete
-   Running

</td></tr><tr><td>

Completed

</td><td>

Date and time the import finished. Given in the time zone of the logged-in user.

</td></tr><tr><td>

Run time

</td><td>

Total amount of time the import required to run.

</td></tr><tr><td>

Total

</td><td>

Total number of import set rows.

 For an import using a robust import set transformer, this field is the total number processed, ignored, skipped, and with errors.

 For an import using a transform map, this field is the total number inserted, updated, ignored, skipped, and with errors.

</td></tr><tr><td>

Inserts

</td><td>

Number of records inserted.

</td></tr><tr><td>

Updates

</td><td>

Number of records updated.

</td></tr><tr><td>

Processed

</td><td>

Number of records processed.

</td></tr><tr><td>

Ignored

</td><td>

Number of records ignored.

 An ignored record is one the user has specified should be ignored during an import. For example, you can identify records to ignore with the **ignore** variable in an onBefore script. For more information, see [Create Extract Transform Load \(ETL\) definitions](../task/create-etl-definitions.md).

</td></tr><tr><td>

Skipped

</td><td>

Number of records skipped.

 A skipped record is one that has been skipped by the system, due to an internal issue.

</td></tr><tr><td>

Errors

</td><td>

Number of errors encountered during the import.

</td></tr><tr><td>

Transform Map

</td><td>

If data is imported using a transform map, the associated map is shown here.

</td></tr><tr><td>

Robust Transformer

</td><td>

If data is imported using a robust import set transformer, the associated transformer is shown here.

</td></tr></tbody>
</table>## Import Set Rows

The **Import Set Rows** tab provides details about rows included in the import set run.

![An Import Set record showing the Import Set Rows tab.](../image/import-set-rows.png "Sample data for the three rows included in the import")

The following table provides more details about the fields in the image.

<table id="table_lgw_ccn_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date and time the import set row was created. Given in the time zone of the logged-in user.

</td></tr><tr><td>

Row

</td><td>

Number for the row. Numbering starts at zero.

</td></tr><tr><td>

State

</td><td>

State of the row import.

</td></tr><tr><td>

Target record

</td><td>

Record updated with the row.

 This field displays the target record only when the import is run with a transform map.

 For imports run with a robust import set transformer, you can view the target records by clicking the row record and checking the **Target record** field in the **Transform Target Rows** tab. For more information and an example, see the following section on Target records for robust import set transformers.

</td></tr><tr><td>

Error

</td><td>

Details for any errors encountered during the row import.

</td></tr><tr><td>

Comment

</td><td>

Comments from the transform script.

</td></tr><tr><td>

Transform Map

</td><td>

If data is imported using a transform map, the associated map is shown here.

</td></tr></tbody>
</table>## Target records for robust import set transformers

For imports using a robust import set transformer, you can view additional details by running the import in verbose mode. Verbose mode enables the following.

-   Greater detail in the import log. With verbose mode, the import log includes transform logs that show how transform operations are applied to records.
-   More information about each row's transform target rows. For each row in the **Import Set Rows** tab, clicking the row record opens the row in the import set table. In this view, you can see the transform target rows, import log, and import set row errors.

The **Transform Target Rows** tab displays the state, target record, import set run, and any error messages for each row. The first three fields are all links to the associated records, making it easier to find and track information for improved debugging. For more information on enabling verbose mode, see [Create a robust import set transformer](../task/create-robust-import-set-transformer.md).

![A row record showing the Transform Target Rows tab.](../image/transform-target-rows.png "Sample data showing the transform target row details for a row in the Computers import set table")

The following table provides more details about the fields in the image.

<table id="table_ibb_t2v_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State

</td><td>

State of the transform target row. Options are:-   Inserted
-   Updated
-   Error

</td></tr><tr><td>

Target record

</td><td>

Record updated with the row.

</td></tr><tr><td>

Import set run

</td><td>

Import Set record associated with the transform target row.

</td></tr><tr><td>

Error message

</td><td>

Text describing any errors encountered by the transform target row.

</td></tr></tbody>
</table>## Import Log

The Import Log tab displays the logs for the import set. It shows when each log was created, its level, the log message, and the source of the log. For details, see [Import logs](https://www.servicenow.com/docs/access?context=r_ImportLogs&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

