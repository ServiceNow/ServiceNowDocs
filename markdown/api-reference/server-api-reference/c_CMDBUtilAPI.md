---
title: CMDBUtil - Global
description: The CMDBUtil API provides utility methods for creating and managing table relationships in the Configuration Management Database \(CMDB\) and managing CMDB baselines.Applies proposed changes in a task\_ci record that represent an update set for all CIs associated with the task.Generates the XML for proposed changes diff, and adds it to the corresponding task\_ci record.Bootstraps the environment by creating the database, creating the system dictionary table, and having the system dictionary table describe itself.Creates a CI relationship between fields.Gets all the child tables of the specified table as a comma-separated list.Gets all the records in the CMDB View \[cmdb\_view\] table.Gets a list of all the parents of a table.Determines whether a CI class is defined in the Business Rule Exclusion Lists \[cmdb\_business\_rule\_exclusions\] table. Use this method in an advanced condition to prevent a business rule from executing on excluded CI classes.Wraps the call to RelationshipEventProcessor\(\), which processes any changes to CI relationships.Wraps the call to RelationshipEventProcessor\(\), which processes any changes to CI relationships, with the specified type and triplet.Deletes the specified CI relationship.Changes the parent of the given table to the new parent.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CMDBUtil- Global

The CMDBUtil API provides utility methods for creating and managing table relationships in the Configuration Management Database \(CMDB\) and managing CMDB baselines.

CMDBUtil is a JavaScript-accessible ScriptableObject. The CMDBUtil API has dynamic and static methods. You access dynamic methods by creating a SNC.CMDBUtil object. You access static methods by using SNC.CMDBUtil global object to call the methods.

This example creates a CMDBUtil object.

```
var cu = new SNC.CMDBUtil();
cu.baselineProposedChangesGenDIFF(current, action.get('sysparm_changeset'));
```

This example calls a static method.

```
var output = SNC.CMDBUtil.getAllChildrenOfAsCommaList('cmdb_ci_computer');
```

Use these methods to manage CMDB table relationships and baselines.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CMDBUtil - baselineProposedChangesApplyChanges\(GlideRecord proposedChanges\)

Applies proposed changes in a task\_ci record that represent an update set for all CIs associated with the task.

This is a dynamic method.

|Name|Type|Description|
|----|----|-----------|
|proposedChanges|GlideRecord|The collection of proposed changes in the change request \(CHG\).|

|Type|Description|
|----|-----------|
|void| |

```
//Where current is a GlideRecord and action is the current UI action
var base = new SNC.CMDBUtil();
base.baselineProposedChangesApplyChanges(current);
```

## CMDBUtil - baselineProposedChangesGenDiff\(GlideRecord current, String changeSet\)

Generates the XML for proposed changes diff, and adds it to the corresponding task\_ci record.

This is a dynamic method.

|Name|Type|Description|
|----|----|-----------|
|current|GlideRecord|The GlideRecord that contains the collection of proposed changes.|
|changeSet|String|The sysid of the task\_ci record that represents the change set to use.|

|Type|Description|
|----|-----------|
|void| |

```
//Where current is a GlideRecord and action is the current UI action
var base = new SNC.CMDBUtil();
base.baselineProposedChangesGenDIFF(current, action.get('sysparm_changeset'));
```

## CMDBUtil - bootstrap\(String dictFile\)

Bootstraps the environment by creating the database, creating the system dictionary table, and having the system dictionary table describe itself.

This is a static method.

|Name|Type|Description|
|----|----|-----------|
|dictFile|String|The file name including path, of the dictionary to load.|

|Type|Description|
|----|-----------|
|void| |

## CMDBUtil - createCIRelationship\(String tableName, String parent, String child, String parentField, String childField\)

Creates a CI relationship between fields.

<table id="table_a1b_4kc_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Optional. The name of the relationship target table.Default: CI Relationship \[cmdb\_rel\_ci\] table.

</td></tr><tr><td>

parent

</td><td>

String

</td><td>

Sys\_id of the parent CI record in the Configuration Items \[cmdb\_ci\] table.

</td></tr><tr><td>

child

</td><td>

String

</td><td>

Sys\_id of the child CI record in the Configuration Items \[cmdb\_ci\] table.

</td></tr><tr><td>

parentField

</td><td>

String

</td><td>

The parent relationship label listed in the CI Relationship Type \[cmdb\_rel\_type\] table.

</td></tr><tr><td>

childField

</td><td>

String

</td><td>

The child relationship label listed in the CI Relationship Type \[cmdb\_rel\_type\] table.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Sys\_id of the new record listed in the CI Relationship \[cmdb\_rel\_ci\] table.|

The following example shows how to create a CI relationship between the parent CI contains field and the child CI contained\_by field. The relationship is listed in the CI Relationship \[cmdb\_rel\_ci\] table.

```
var base = new SNC.CMDBUtil();
base.createCIRelationship('<parent_ci_sys_id>', '<child_ci_sys_id>, 'Contains', 'Contained by');
```

## CMDBUtil - getAllChildrenOfAsCommaList\(String baseTable\)

Gets all the child tables of the specified table as a comma-separated list.

This is a static method.

|Name|Type|Description|
|----|----|-----------|
|baseTable|String|The base table name.|

|Type|Description|
|----|-----------|
|String|A comma-separated list of sys\_ids of tables extending the base table.|

```
//Where cmdv_ci_computer is a table.
var output = SNC.CMDBUtil.getAllChildrenOfAsCommaList('cmdb_ci_computer');
gs.print(output);
```

## CMDBUtil - getCMDBViews\(\)

Gets all the records in the CMDB View \[cmdb\_view\] table.

This method is dynamic.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|List of the records in the CMDB View \[cmdb\_view\] table.|

The following example shows how to list the CMDB views.

```
var util = new SNC.CMDBUtil(); 
var cmdbViews = util.getCMDBViews();
gs.info(cmdbViews);

// Note that the output in the example is type: java.util.ArrayList
// To convert to JS Array, use ArrayUtils (add these lines preceding gs.info):
// var arrUtil = new global.ArrayUtil();
// var arrViews = arrUtil.convertArray(cmdbViews);
```

Output:

```
[View 3, View 1, View 2, Another view]
```

## CMDBUtil - getTables0\(String tableName\)

Gets a list of all the parents of a table.

This method is a static method.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|The table name.|

|Type|Description|
|----|-----------|
|Array|List of tables that are parents of the specified table.|

The following example shows how to list the parent tables of the Server \[cmdb\_ci\_server\] table.

```
var gr = new GlideRecord('incident');

// Querying the incident table
gr.addQuery('number','INC0000005'); 
gr.query();


if(gr.next()){
  // Find the list of parent tables for Configuration item field of this Incident
  var ciParent = SNC.CMDBUtil.getTables0(gr.cmdb_ci.sys_class_name); 
  gs.print("Parent Tables for the Configuration Item '" + gr.cmdb_ci.name + "' belonging to the CMDB Class '"+ gr.cmdb_ci.sys_class_name+ "' are: \n" + ciParent);
}
```

Output:

```
Parent Tables for the Configuration Item 'ApplicationServerPeopleSoft' belonging to the CMDB Class 'cmdb_ci_server' are: 
[cmdb_ci_server, cmdb_ci_computer, cmdb_ci_hardware, cmdb_ci, cmdb]
```

## CMDBUtil - isExcludedFromBR\(String className\)

Determines whether a CI class is defined in the Business Rule Exclusion Lists \[cmdb\_business\_rule\_exclusions\] table. Use this method in an advanced condition to prevent a business rule from executing on excluded CI classes.

For example, the Create Asset on insert business rule uses this method in the advanced condition to prevent the rule from creating assets for CI classes such as cmdb\_ci\_qualifier, cmdb\_ci\_endpoint, cmdb\_ci\_storage\_volume, and cmdb\_ci\_vcenter\_datastore\_disk. Define classes for exclusion in the Business Rule Exclusion Lists \[cmdb\_business\_rule\_exclusions\] table.

|Name|Type|Description|
|----|----|-----------|
|className|String|Name of the class to check for exclusion.|

|Type|Description|
|----|-----------|
|Boolean|True if the class is defined in the Business Rule Exclusion Lists \[cmdb\_business\_rule\_exclusions\] table; otherwise, false.|

```
//Returns true if the cmdb_ci_endpoint class is defined 
//in the Business Rule Exclusion Lists table
var exclusion = SNC.CMDBUtil.isExcludedFromBR("cmdb_ci_endpoint");

//Advanced condition that prevents business rules from executing on 
//classes in the Business Rule Exclusion Lists table
(!SNC.CMDBUtil.isExcludedFromBR(current.getTableName()))
```

## CMDBUtil - processCIChange\(GlideRecord event, GlideRecord target\)

Wraps the call to RelationshipEventProcessor\(\), which processes any changes to CI relationships.

This is a dynamic method.

|Name|Type|Description|
|----|----|-----------|
|event|GlideRecord|The event record.|
|target|GlideRecord|The target record.|

|Type|Description|
|----|-----------|
|void| |

## CMDBUtil - processRelChange\(GlideRecord event, GlideRecord current, String relType, String triplet\)

Wraps the call to RelationshipEventProcessor\(\), which processes any changes to CI relationships, with the specified type and triplet.

This is a dynamic method.

|Name|Type|Description|
|----|----|-----------|
|event|GlideRecord|The event record|
|current|GlideRecord|The current record, which is either the relation record or a user record if the current process is a deletion.|
|relType|String|The type of relation that changed.|
|triplet|String|The child, parent, and class name from the relation that changed.|

|Type|Description|
|----|-----------|
|void| |

## CMDBUtil - removeCIRelationship\(String tableName, String parentField, String childField, String parentDesc, Object childDesc\)

Deletes the specified CI relationship.

This is a dynamic method.

<table id="table_a1b_4kc_3v" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Optional. Table nameDefault: CI Relationship \[cmdb\_rel\_ci\] table

</td></tr><tr><td>

parentField

</td><td>

String

</td><td>

Parent field

</td></tr><tr><td>

childField

</td><td>

String

</td><td>

Child field

</td></tr><tr><td>

parentDesc

</td><td>

String

</td><td>

Parent relationship descriptor

</td></tr><tr><td>

childDesc

</td><td>

Object

</td><td>

Child relationship descriptor

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

This code example shows how to remove every relation type 'Depends on::Used by' for the specified parent.

```
var cu = new SNC.CMDBUtil();
var parentSysID = '27d18f6fc0a8000b00ad14d4929d1b45';
var parentDesc = 'Depends on';
var childDesc = 'Used by'
 
// Get records with parent equal parentSysID
var relation = new GlideRecord('cmdb_rel_ci');
relation.addQuery('parent', parentSysID);
relation.query();
while(relation.next()){
    // Remove every relation of type: 'Depends on::Used by' for the parent
    // If the relation type does not exist, it inserts this relation type into [cmdb_rel_type].
    cu.removeCIRelationship('cmdb_rel_ci', parentSysID, relation.child.getValue('sys_id'), parentDesc, childDesc)
}
```

## CMDBUtil - reParentTable\(String table, String oldParent, String newParent\)

Changes the parent of the given table to the new parent.

|Name|Type|Description|
|----|----|-----------|
|table|String|The table to re-parent.|
|oldParent|String|The old parent.|
|newParent|String|The new parent.|

<table id="table_hdq_m5c_3v" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates if the parent change is successful.

 Valid values:

-   true: Parent change was successful.
-   false: Parent change wasn't successful.

</td></tr></tbody>
</table>To recreate the following example, use the code provided to create a custom table. Next create a record and check it in the task table. The custom table created extends from the Task table, which means it has successfully re-parented. The code isn't intended to be directly used via copy and paste. To show output, the custom table was created before running the code.

```
/*
  Before running the code in the background Script Make Sure 'Record For Rollback' is unchecked.

  This API CMDBUtil.reParentTable changes the parent of the table but will not allow the OOB tables to change the parent it works only in the custom table. Hence this script contains the creation of the custom table.
  API CMDBUtil.reParentTable has 3 parameters (Table, Old Parent , New Parent);
  We can make the Parent as Null as well by using this (Table, Old Parent, '');

  The code in this example shows how to create a custom table without any extension.
  Then creating a record and then again creating a record and checking in the task table after it gets extended to the task table.

  If the code returns false means the record is not present in the task table as it is not extended. It returns true only when the record is found in the task table after the table is extended.

*/

/* Run the following code to create the custom table without an extension
createCustomTable('u_custom_table','Custom Table'); // Creating a custom Table (don't create if you have one)
var CreatedRecord = CreateCustomRecord('u_custom_table'); // Creating a record in the custom table
gs.print(CheckRecord('u_custom_table'));  // Checking of the record in the task table by passing the Class Name (A.K.A your custom Table)

var getParentTables = new SNC.CMDBUtil.reParentTable('u_custom_table','','task'); // Extending the custom table to task table . This Works only when the table is extendable
var CreatedRecordAfter = CreateCustomRecord('u_custom_table'); // Creating a record in the custom table
gs.print(CheckRecord('u_custom_table'));  // Checking of the record in the task table by passing the Class Name (A.K.A your custom Table)
*/

// If the custom Table is already created, run this. (Do not run these 4 lines when creating the table)
gs.print(CheckRecord('u_custom_table')); //Checking of the record in the task table by passing the Class Name (A.K.A your custom Table)
var getParentTables = new SNC.CMDBUtil.reParentTable('u_custom_table','','task'); //Extending the custom table to task table . This Works only when the table is extendable
var CreatedRecordAfter = CreateCustomRecord('u_custom_table'); //Creating a record in the custom table
gs.print(CheckRecord('u_custom_table'));  //Checking of the record in the task table by passing the Class Name (A.K.A your custom Table)


function createCustomTable(Name, Label)
{
  var customTable = new GlideRecord('sys_db_object');
  customTable.initialize();
  customTable.name=  Name ;
  customTable.label= Label ;
  customTable.is_extendable= true;
  customTable.insert();
}

function CreateCustomRecord(customTableName)
{
  var customTable = new GlideRecord(customTableName);
  customTable.initialize();
  return customTable.insert();
}

function CheckRecord(customTableName)
{
  var task =new GlideRecord('task');
  task.addQuery('sys_class_name', customTableName);
  task.query();

  if(task.next())
  {
    return true;
  }

  return false;
}
```

Output:

```
*** Script: true
*** Script: true
```

