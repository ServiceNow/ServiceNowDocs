---
title: Import run history
description: The import history gives status information about individual import operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/system-import-sets/r\_ImportRunHistory.html
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Import run history

The import history gives status information about individual import operations.

**Note:** Functionality described here requires the **Admin** role.

## Run import utility

The Run Import utility is used to run an import operation using an existing Transform Map and Import Set table.

\[Omitted image "ImportHistoryRecord.png"\] Alt text:

Error Codes are related to a transformation. Not all errors produce error codes. If an error code does exist, it is in the \[sys\_import\_set\_row\_error\] table error code field.

**Error Codes**

-   **100** Reference field value rejected.
-   **200** Choice field value rejected.
-   **300** List reference field rejected.
-   **800** Invalid target record or field.
-   **900** Transform script error.

**Parent Topic:**[Importing data using import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/c_ImportDataUsingImportSets.md)

