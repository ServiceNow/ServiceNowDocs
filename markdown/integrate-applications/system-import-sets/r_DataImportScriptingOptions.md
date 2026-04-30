---
title: Scheduled data import scripting options
description: Multiple JavaScript objects are available in the Scheduled Data Import Pre script and Post script fields.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Schedule a data import, Importing data using import sets, Import sets, Imports, Workflow Data Fabric]
---

# Scheduled data import scripting options

Multiple JavaScript objects are available in the Scheduled Data Import **Pre script** and **Post script** fields.

<table id="table_DataImportScriptingOptions"><thead><tr><th>

Object

</th><th>

Description

</th><th>

Example

</th></tr></thead><tbody><tr><td>

cancel

</td><td>

Set this object to true to stop the import action.

</td><td>

Use the **Pre script** field to evaluate the conditions of the import and determine whether to cancel the import process. To cancel the import process, use the following call:```
cancel = true;
```

</td></tr><tr><td>

import\_set

</td><td>

Get the GlideRecord object for the new import set. This variable allows you to query the following columns from the sys\_import\_set table:-   number
-   sys\_id
-   state
-   table\_name

</td><td>

If you want to use information from the import set, you can specify one of the properties of the import\_set variable.```
var x = import_set.number;
```

</td></tr><tr><td>

data\_source

</td><td>

GlideRecord of the data source to be used for the scheduled import.

</td><td>

Typically, you define the data source with the Scheduled Data Import record. If you want to access this data source or modify the data source in certain conditions, you can use the following.```
data_source.import_set_table_name = 'new_set_from_scheduler';
data_source.update();
```

</td></tr></tbody>
</table>**Parent Topic:**[Schedule a data import](../task/t_ScheduleADataImport.md)

