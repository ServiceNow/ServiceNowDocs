---
title: TableUtils - Global
description: The TableUtils script include provides shortcuts for accessing table related information.Creates an instance of a TableUtils class.Drops a database table.Drops a database table and cleans up references to the table.Drops a database table, all of it's extended tables, and cleans up references to the tables.Returns the base table name from which the table was extended.Returns the list of tables that extend a table, includes the base table.Returns a list of all classes participating in the hierarchy of the specified table.Returns the table hierarchy.Returns a list of tables that extend a table.Determines if a table has been extended.Determines if a table is a base class, meaning it has no parents and has extensions.Determines if the table has no parents and no extensions.Checks to see if a table exists.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# TableUtils- Global

The TableUtils script include provides shortcuts for accessing table related information.

This class is available to server-side scripts.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## TableUtils - TableUtils\(String tableName\)

Creates an instance of a TableUtils class.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name|

```
var tu = new TableUtils("incident");
```

## TableUtils - drop\(String tableName\)

Drops a database table.

**Note:** Use with extreme caution. Dropping a table permanently deletes the table and all its data. If the table is extended, use dropTableAndExtensions.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to drop|

|Type|Description|
|----|-----------|
|void| |

```
var tu = new TableUtils();
tu.drop("table_that_will_be_lost_forever");
```

Output:

```
dropping table table_that_will_be_lost_forever
Starting cache flush
Cache flush complete
TABLE DROP: admin dropped table table_that_will_be_lost_forever
```

## TableUtils - dropAndClean\(String tableName\)

Drops a database table and cleans up references to the table.

**Note:** Use with extreme caution. Dropping a database table permanently deletes the table and all its data. If the table is extended, use dropTableAndExtensions.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Name of the table to drop|

|Type|Description|
|----|-----------|
|void| |

```
var tu = new TableUtils();
tu.dropAndClean("table_that_will_be_lost_forever");
```

Output:

```
dropping table table_that_will_be_lost_forever
Starting cache flush
Cache flush complete
TABLE DROP: admin dropped table table_that_will_be_lost_forever
*** Script: removing gauges for table_that_will_be_lost_forever
*** Script: removing forms for table_that_will_be_lost_forever
*** Script: removing styles for table_that_will_be_lost_forever
*** Script: removing forms sections for table_that_will_be_lost_forever
*** Script: removing lists for table_that_will_be_lost_forever
*** Script: removing related lists for table_that_will_be_lost_forever
*** Script: removing references to table_that_will_be_lost_forever
*** Script: removing dictionary entries for table_that_will_be_lost_forever
Background message, type:info, message: Table deleted
```

## TableUtils - dropTableAndExtensions\(String tableName\)

Drops a database table, all of it's extended tables, and cleans up references to the tables.

**Note:** Use with extreme caution. Dropping a database table permanently deletes the table and all of its data.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table to drop|

|Type|Description|
|----|-----------|
|void| |

```
var tu = new TableUtils();
tu.dropTableAndExtensions("table_that_will_be_lost_forever");
```

Output:

```
dropping table parent_table_that_will_be_lost_forever
Starting cache flush
Cache flush complete
TABLE DROP: admin dropped table ext_table_that_will_be_lost_forever
removing gauges for ext_table_that_will_be_lost_forever
removing forms for ext_table_that_will_be_lost_forever
removing styles for ext_table_that_will_be_lost_forever
removing forms sections for ext_table_that_will_be_lost_forever
removing lists for ext_table_that_will_be_lost_forever
removing related lists for ext_table_that_will_be_lost_forever
removing references to ext_table_that_will_be_lost_forever
removing dictionary entries for ext_table_that_will_be_lost_forever
Background message, type:info, message: Table deleted
dropping table parent_table_that_will_be_lost_forever
Starting cache flush
Cache flush complete
TABLE DROP: admin dropped table parent_table_that_will_be_lost_forever
removing gauges for parent_table_that_will_be_lost_forever
removing forms for parent_table_that_will_be_lost_forever
removing styles for parent_table_that_will_be_lost_forever
removing forms sections for parent_table_that_will_be_lost_forever
removing lists for parent_table_that_will_be_lost_forever
removing related lists for parent_table_that_will_be_lost_forever
removing references to parent_table_that_will_be_lost_forever
removing dictionary entries for parent_table_that_will_be_lost_forever
Background message, type:info, message: Table deleted
```

## TableUtils - getAbsoluteBase\(\)

Returns the base table name from which the table was extended.

**Note:** For any table under the cmdb\_ci hierarchy, this method returns cmdb\_ci and not cmdb, which is the actual base table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Base table name|

```
var table = new TableUtils("cmdb_ci_server");
gs.print(table.getAbsoluteBase());
```

Output: cmdb\_ci

## TableUtils - getAllExtensions\(\)

Returns the list of tables that extend a table, includes the base table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|A list of tables that extend the table, includes the base table.|

```
var table = new TableUtils("task");
gs.print(table.getAllExtensions());
```

Output:

```
[task, incident, issue, kb_submission, sysapproval_group, change_request, change_request_imac, sc_task, 
problem, sc_req_item, ticket, ast_transfer_order, planned_task, change_task, change_phase, sc_request]
```

## TableUtils - getHierarchy\(\)

Returns a list of all classes participating in the hierarchy of the specified table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|A list of all classes in the specified table's hierarchy.|

```
var table = new TableUtils("cmdb_ci_server");
gs.print(table.getHierarchy());
```

Output: \[cmdb\_ci\_server, cmdb\_ci\_computer, cmdb\_ci\_hardware, cmdb\_ci, cmdb\_ci\_mainframe, cmdb\_ci\_linux\_server, cmdb\_ci\_mainframe\_lpar, cmdb\_ci\_esx\_server, cmdb\_ci\_unix\_server, cmdb\_ci\_solaris\_server, cmdb\_ci\_hpux\_server, cmdb\_ci\_aix\_server, cmdb\_ci\_osx\_server, cmdb\_ci\_netware\_server, cmdb\_ci\_win\_server\]

## TableUtils - getTables\(\)

Returns the table hierarchy.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|A list of table names in the parent hierarchy.|

```
// Get the hierarchy of tables
var table = new TableUtils("cmdb_ci_computer");
var tableArrayList = table.getTables();

// Use the j2js method to convert the Java ArrayList to JavaScript
gs.include("j2js");
var tableArray = j2js(tableArrayList);

// Write the value of each element in the JavaScript array
var i = 0;
while ( i < tableArray.length ) {
gs.print("Table with index " + i + ": " + tableArray[i]);
i++;
}

```

Output:

```
Table with index 0: cmdb_ci_computer
Table with index 1: cmdb_ci_hardware
Table with index 2: cmdb_ci
Table with index 3: cmdb
```

## TableUtils - getTableExtensions\(\)

Returns a list of tables that extend a table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|ArrayList|A list of table names that extend the table.|

This example shows that 58 tables in this instance extend the Computer \[cmdb\_ci\_computer\] table. \(Output condensed below.\)

```
// Get the tables that extend the table
var table = new TableUtils("cmdb_ci_computer");
var tableArrayList = table.getTableExtensions();
 
// Use the j2js method to convert the Java ArrayList to JavaScript
gs.include("j2js");
var tableArray = j2js(tableArrayList);
 
// Write the value of each element in the JavaScript array
var i = 0;
while ( i < tableArray.length ) {
  gs.print("Table with index " + i + ": " + tableArray[i]);
  i++;
}
```

Output:

```
Table with index 0: cmdb_ci_mainframe_hardware
Table with index 1: cmdb_ci_handheld_computing
Table with index 2: cmdb_ci_ucs_blade
Table with index 3: cmdb_ci_storage_switch
Table with index 4: cmdb_ci_server
Table with index 5: cmdb_ci_hmc_server
…
Table with index 56: cmdb_ci_pc_hardware
Table with index 57: cmdb_ci_ucs_rack_unit
```

## TableUtils - hasExtensions\(\)

Determines if a table has been extended.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the table has extensions.|

```
var table = new TableUtils("cmdb_ci_server");
gs.print(table.hasExtensions());
```

Output:

```
true
```

## TableUtils - isBaseClass\(\)

Determines if a table is a base class, meaning it has no parents and has extensions.

For example, Task is a base class since it is not extended from another table and has tables extended from it. Sys\_user is not a base class because it has no parents, but does not have extensions.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_l5p_w1w_4t" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether a table is a base class table meaning it has no parents but has extensions.Valid values:

-   true: Table is a base class.
-   false: Table is not a base class.

</td></tr></tbody>
</table>```
var table = new TableUtils("task");
gs.print("Task is base class: " + table.isBaseClass());
 
var table = new TableUtils("sys_user");
gs.print("User is base class: " + table.isBaseClass());
```

Output:

```
 Task is base class: true
User is base class: false
```

## TableUtils - isSoloClass\(\)

Determines if the table has no parents and no extensions.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the table has no parent and no table is extended from it.|

```
var table = new TableUtils("task");
gs.print("task is solo class: " + table.isSoloClass());
 
var table = new TableUtils("cmdb_ci_win_server");
gs.print("cmdb_ci_win_server is solo class: " + table.isSoloClass());
 
var table = new TableUtils("sys_user");
gs.print("sys_user is solo class: " + table.isSoloClass());
```

Output:

```
task is solo class: false
cmdb_ci_win_server is solo class: false
sys_user is solo class: true
```

## TableUtils - tableExists\(\)

Checks to see if a table exists.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the table exists.|

```
var table = new TableUtils("my_table");
gs.print("Does 'my_table' exist? " + table.tableExists());
```

Output: Does 'my\_table' exist? false

