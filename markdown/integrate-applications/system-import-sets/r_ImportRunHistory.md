---
title: Import run history
description: The import history gives status information about individual import operations.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Creating integrations with applications]
---

# Import run history

The import history gives status information about individual import operations.

**Note:** Functionality described here requires the **Admin** role.

## Run import utility

The Run Import utility is used to run an import operation using an existing Transform Map and Import Set table.

![](../image/ImportHistoryRecord.png "Import History Record")

Error Codes are related to a transformation. Not all errors produce error codes. If an error code does exist, it is in the \[sys\_import\_set\_row\_error\] table error code field.

**Error Codes**

-   **100** Reference field value rejected.
-   **200** Choice field value rejected.
-   **300** List reference field rejected.
-   **800** Invalid target record or field.
-   **900** Transform script error.

**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

