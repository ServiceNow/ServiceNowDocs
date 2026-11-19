---
title: Run an import
description: You can manually run an import to immediately import data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/system-import-sets/t\_RunImport.html
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Run an import

You can manually run an import to immediately import data.

## Before you begin

Role required: admin

## Procedure

1.  From a Transform Map, click **Transform**.

    When the import completes, you see a link to go to the target table containing your imported records. The amount of time that it takes to run an import varies depending on the number of records you import. It might take as long as several hours for very large import operations \(tens of thousands of records\).

2.  Click **View the imported data** to see the loaded import set table.

3.  Click **Create transform map** to create a new transform map to transform the data in the import set table to its target table.

4.  Click **Run import** to execute an existing transform map for the loaded data.


## Result

Three things to note at this point:

-   The spreadsheet is imported, and a new table is created to hold the data.
-   Within that table, the imported records are designated with their own Set value.
-   A new module is created in the System Import Sets application for the new table.

**Parent Topic:**[Importing data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/system-import-sets/c_ImportDataUsingImportSets.md)

