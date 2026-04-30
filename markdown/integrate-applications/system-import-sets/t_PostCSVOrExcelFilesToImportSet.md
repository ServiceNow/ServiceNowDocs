---
title: Post CSV or Excel files directly to an import set
description: An administrator can post CSV or Excel files directly to instance.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Post CSV or Excel files directly to an import set

An administrator can post CSV or Excel files directly to instance.

## Before you begin

Role required: import\_set\_loader

## About this task

The `sys_import.do` target lets you dynamically upload a CSV or Excel file into the import set table specified by the **sysparm\_import\_set\_tablename** parameter. You must specify a name that matches an existing import set table name. If the import set table does not exist, pre-create it by performing a manual import. The **sysparm\_transform\_after\_load=true** parameter causes the CSV transform to be executed immediately, if a transform map exists.

You can upload a file using POST to the following URL \(replace placeholders with desired values\):

```
https://<instance>.service-now.com/sys_import.do?sysparm_import_set_tablename=<table_name>&sysparm_transform_after_load=<true>
```

**Important:** The body of the POST must contain the file as a multi-part attachment.

-   **[Posting a CSV file - Perl and Java examples](../reference/r_PerlExample.md)**  
An example using Perl to post a CSV file with basic auth credentials and Java Apache HttpClient class to post a CSV file with basic auth credentials.

**Parent Topic:**[Importing data using import sets](../concept/c_ImportDataUsingImportSets.md)

