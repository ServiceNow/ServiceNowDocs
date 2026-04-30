---
title: GlideTableHierarchy - Scoped
description: The GlideTableHierarchy API provides methods for handling information about table relationships.Instantiates a GlideTableHierarchy object.Returns an array of strings containing all tables that extend the current table and includes the current table.Returns the parent class.Returns an array of strings containing all classes in the hierarchy of the current table.Returns the table's name.Returns the top level class in the hierarchy.Returns an array of strings of the table names in the hierarchy.Returns an array of strings containing all tables that extend the current table.Returns true if this is a base class.Returns true if this table is not in a hierarchy.Returns true of this class has been extended.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideTableHierarchy- Scoped

The GlideTableHierarchy API provides methods for handling information about table relationships.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideTableHierarchy - GlideTableHierarchy\(String tableName\)

Instantiates a GlideTableHierarchy object.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The name of the table.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.getTables());
```

Output:

```
incident,task
```

## GlideTableHierarchy - getAllExtensions\(\)

Returns an array of strings containing all tables that extend the current table and includes the current table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of strings containing the tables in the hierarchy that includes the current table.|

```
var table = new GlideTableHierarchy("task"); 
gs.info(table.getAllExtensions());
```

Output: Line breaks added for clarity.

```
task,sc_task,problem_task,change_phase,sc_req_item,kb_submission,
release_phase,problem,ticket,sm_task,hr_task,change_task,change_request,
change_request_imac,incident,release_task,vtb_task,sm_order,hr_case,
sysapproval_group,sc_request
```

## GlideTableHierarchy - getBase\(\)

Returns the parent class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The parent class.|

```
var table = new GlideTableHierarchy("cmdb_ci_server"); 
gs.info(table.getBase());
```

Output:

```
cmdb_ci_computer
```

## GlideTableHierarchy - getHierarchy\(\)

Returns an array of strings containing all classes in the hierarchy of the current table.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|Array|An array of strings of the classes in the hierarchy.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.getHierarchy());
```

Output:

```
incident,task
```

## GlideTableHierarchy - getName\(\)

Returns the table's name.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|The table's name.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.getName());
```

Output:

```
incident
```

## GlideTableHierarchy - getRoot\(\)

Returns the top level class in the hierarchy.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the root class.|

```
var table = new GlideTableHierarchy("cmdb_ci_server"); 
gs.info(table.getRoot());
```

Output:

```
cmdb
```

## GlideTableHierarchy - getTables\(\)

Returns an array of strings of the table names in the hierarchy.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of strings containing the names of tables in the hierarchy.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.getTables());
```

Output:

```
incident,task
```

## GlideTableHierarchy - getTableExtensions\(\)

Returns an array of strings containing all tables that extend the current table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|An array of strings containing the tables that extend the current table.|

```
var table = new GlideTableHierarchy("task"); 
gs.info(table.getTableExtensions());
```

Output: Line breaks added for clarity

```
sc_task,problem_task,change_phase,sc_req_item,kb_submission,release_phase,problem,
ticket,sm_task,hr_task,change_task,change_request,change_request_imac,incident,
release_task,vtb_task,sm_order,hr_case,sysapproval_group,sc_request
```

## GlideTableHierarchy - isBaseClass\(\)

Returns true if this is a base class.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the current table has no parent and has extensions.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.isBaseClass());
```

Output:

```
false
```

## GlideTableHierarchy - isSoloClass\(\)

Returns true if this table is not in a hierarchy.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the current table has no parent and no extensions.|

```
var table = new GlideTableHierarchy("sys_user"); 
gs.info(table.isSoloClass());
```

Output:

```
true
```

## GlideTableHierarchy - hasExtensions\(\)

Returns true of this class has been extended.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the current table has extensions.|

```
var table = new GlideTableHierarchy("incident"); 
gs.info(table.hasExtensions());
```

Output:

```
false
```

