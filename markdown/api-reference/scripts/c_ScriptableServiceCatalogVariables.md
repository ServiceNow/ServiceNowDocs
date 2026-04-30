---
title: Scriptable service catalog variables
description: You can use scripting to reference any request item variable from a table in scoped and non-scoped environment.
locale: en-US
release: yokohama
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Scriptable service catalog variables

You can use scripting to reference any request item variable from a table in scoped and non-scoped environment.

An example of a variable reference follows.

```
current.variables.<variable_name>
```

Where current refers to the current record, and *&lt;variable\_name&gt;* is the name of your variable.

**Note:** In order to reference a variable from JavaScript, it must have a name.

When a variable is part of a variable set, you can reference it as current.variables.&lt;variable\_name&gt; or current.variables.&lt;variable\_set\_name&gt;.&lt;variable\_name&gt;.

Variable set is also a first-class citizen in Service Catalog. Like variables, a variable set has read, write, and create roles. If roles are provided for a variable set, the roles are applicable for the variables within the set. Roles of an individual variable are overridden by the roles of the variable set.

## Print a variable

```
var original = current.variables.original_number;
gs.print(original);

```

## Set a variable

```
current.variables.name = "Auto-Generated:" + current.variables.asset_tag;
```

## Create an inventory item with fields set from variables

```
doCreation(); 

function doCreation ( ) { 
var create = current.variables.create_item; 
if (create == 'true') { // we want to create an asset 
  var computer = new GlideRecord('cmdb_ci_computer');
  computer.initialize();
  computer.asset_tag = current.variables.asset_tag;
  computer.serial_number = current.variables.serial_number;
  computer.name = current.variables.name;
  computer.manufacturer = current.variables.company;
  computer.insert(); } }
```

## Get GlideElementVariable of variables and variable sets associated with a GlideRecord

```
now_GR.variables
```

## Get the name value pair of variables associated with a GlideRecord

```
now_GR.variables.getVariableValue();
```

## Get a list of GlideElementVariable for variables within a task record

```
now_GR.variables.getElements();
```

## Get a list of GlideElementVariable for variables \(including multi-row variable set\) within a task record

```
now_GR.variables.getElements(true);
```

**Note:** The getElements\(\) method returns all the variables present on the given task record except for the formatter variables like label, break, container end, container split, and so on.

## APIs for GlideElementVariable

-   now\_GR.variables.&lt;var\_name&gt;.isMultiRow\(\): Get whether the GlideElementVariable is a multi-row variable set or a variable.
-   now\_GR.variables.&lt;var\_name&gt;.getQuestion\(\): Get the Question object for a variable. Applicable only for a variable \(isMultiRow\(\) is false\) and not for a multi-row variable set.
-   now\_GR.variables.&lt;var\_name&gt;.getLabel\(\): Get the label of the GlideElementVariable. For a variable, the label of the variable is returned. For multi-row variable set, the title of the variable set is returned.
-   now\_GR.variables.&lt;var\_name&gt;.canRead\(\): Get whether the user can view a variable or multi-row variable set.
-   now\_GR.variables.&lt;var\_name&gt;.canWrite\(\): Get whether the user can edit a variable or multi-row variable set.
-   now\_GR.variables.&lt;var\_name&gt;.getDecryptedValue\(\): Get the decrypted value for a masked variable. Applicable only for a masked variable.
-   now\_GR.variables.&lt;var\_name&gt;.getRows\(\): Get the list of row objects for a multi-row variable set. Applicable only for a multi-row variable set \(isMultiRow\(\) is true\).
-   now\_GR.variables.&lt;var\_name&gt;.getRowCount\(\): Get the number of rows for multi-row variable set. Applicable only for a multi-row variable set \(isMultiRow\(\) is true\).

## Example to access variables of GlideRecord for the Task table

```
var now_GR = new GlideRecord('sc_req_item'); 
if (now_GR.get('635a1f5387320300e0ef0cf888cb0b73')) { 
    var variables = now_GR.variables.getElements(); 
    for (var i=0;i<variables.length;i++) { 
        var question = variables[i].getQuestion(); 
        gs.log(question.getLabel() + ":" + question.getValue()) 
    } 
}
```

## Example to access a multi-row variable set of GlideRecord for the Task table

```
var now_GR = new GlideRecord('sc_req_item');
now_GR.get('02c38dcd87013300e0ef0cf888cb0bb2');

var vars = now_GR.variables.getElements(true);

for (var i=0; i<vars.length; i++) {
    var now_V = vars[i];
    if (now_V.isMultiRow()) {
        var rows = now_V.getRows();
        for (var j=0; j<now_V.getRowCount(); j++) {
            var row = rows[j];
            var cells = row.getCells();
            for (var k=0; k<cells.length; k++) {
                var cell = cells[k];
                gs.info(cell.getLabel() + ":" + cell.getCellDisplayValue())
            }
        }
    }
}
```

## Multi-row variable set

<table id="table_xz2_tnk_b2b"><thead><tr><th>

Operation

</th><th>

Usage

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Table operations

</td></tr><tr><td>

Return JSON array value as String

</td><td>

```
now_GR.variables.table_var
```

</td></tr><tr><td>

Set value of a multi-row variable set

</td><td>

```
now_GR.variables.table_var = <val>
```

 **Note:** An array of ordered \(key, value\) pairs is also applicable as input.

</td></tr><tr><td>

Get value of column, var1, of a multi-row variable set

</td><td>

```
now_GR.variables.table_var.var1
```

</td></tr><tr><td>

Set value of a variable set, var1

</td><td>

```
now_GR.variables.table_var.var1 = <val>
```

 **Note:** An array of ordered \(key, value\) pairs is also applicable as input.

</td></tr><tr><td class="sub-head" colspan="2">

Row operations

</td></tr><tr><td>

Get the current row count

</td><td>

```
now_GR.variables.table_var.getRowCount()
```

</td></tr><tr><td>

Returns the row specified by the variable "i" - getRow\(&lt;int&gt; i\)

</td><td>

```
var row = now_GR.variables.table_var.getRow(<int> i);
```

</td></tr><tr><td>

Get the cell value for a question column mapped to &lt;var\_name&gt;

</td><td>

```
row.<var_name>
```

</td></tr><tr><td>

Set the cell value for a question column mapped to &lt;var\_name&gt;

</td><td>

```
row.setCellValue('<var_name>',value)
```

</td></tr><tr><td>

Set the cell value for a question column mapped to &lt;var\_name&gt;

</td><td>

```
row.<var_name> = value
```

</td></tr><tr><td>

Add an empty row at the end of the table and return a scriptable object

</td><td>

```
var row = now_GR.variables.table_var.addRow()
```

</td></tr><tr><td>

Delete a row

</td><td>

```
row.deleteRow()
```

</td></tr></tbody>
</table>## Notes and limitations

-   //Single column of table\_Var
-   now\_GR.variables.table\_var.var1
-   now\_GR.variables.table\_var.var1 = &lt;val&gt;

1.  You can only set a variable in a before business rule. Variables set in an after rule are not written to the database.
2.  There is nothing in place to prevent namespace collision with variables. Creating two variables named computer\_speed would result in only one of them showing up; the second one would overwrite the first one.
3.  Date/time variables use the same time zone formatting and storage rules as all other dates in the system. They are stored internally in GMT, but translated into the user's local time zone and format for display.

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

