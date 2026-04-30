---
title: Map with transformation event scripts
description: Transformation events occur during the process of transforming an import set table onto a table.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Transform maps, Import sets, Imports, Creating integrations with applications]
---

# Map with transformation event scripts

Transformation events occur during the process of transforming an import set table onto a table.

These events modify the transformation behavior from any type of mapping specification. Transformation Event scripts modify the processing of the events at various stages of the transformation.

For example, the processing of a mapping operation defined using the [Mapping Assist Utility](../concept/c_MappingOptions.md) can be manipulated using the event scripts. There are a number of import set JavaScript objects that are accessible during these events. These objects represent tables or portions of tables. It is important to note that what these objects refer to varies depending on the context of the event in which they are referenced.

The following is a table of all of the transform events and their contextual variables.

**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

<table id="table_r1y_4rs_sq"><thead><tr><th>

Event name

</th><th>

Event Parameters

</th></tr></thead><tbody><tr><td>

onStart

</td><td>

When: The onStart event script is processed at the start of an import run, before any data rows are read.

 <table id="table_vjh_wrs_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onStart import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The first row of the source table, there is no data yet since the row has not been read.

</td></tr><tr><td>

import\_set

</td><td>

GlideRecord

</td><td>

The import set that is currently being transformed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

ignore

</td><td>

Boolean

</td><td>

When set to true, the entire transformation will be stopped and no further processing will occur.

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, has the same effect as the ignore flag of stopping the entire transformation, with an error message.

</td></tr></tbody>
</table> Example:

 ```
var info = "Starting Import Set Transformation Mapping operation using Data source, " 
+ map.table_source + " and Transform Map " + map.name + " on import set " + import_set.number;
log.info( info ); 

```

</td></tr><tr><td>

onComplete

</td><td>

When: The onComplete event script is processed at the end of an import run, after all data rows are read and transformed.

 <table id="table_hln_4ss_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onComplete import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The last row of the source import set table.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The last row of target table.

</td></tr><tr><td>

import\_set

</td><td>

GlideRecord

</td><td>

The import set that is currently being transformed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, will mark the current import set status to error after it completes.

</td></tr></tbody>
</table> Example:

 ```
// Create a myimport_completed event that can be reacted by an email notification or script action
// (there is already an import.finished event that the system will create at the end of an import)
var e = new GlideEvent("myimport_completed", import_set.sys_id, map.sys_id, "");
e.insert();
```

</td></tr><tr><td>

onBefore

</td><td>

When: The onBefore event script is processed at the start of a row transformation, before the source row is transformed into the target row.

 <table id="table_myd_kts_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onBefore import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The row of the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The row of the target table that is currently being processed.

</td></tr><tr><td>

import\_set

</td><td>

GlideRecord

</td><td>

The import set that is currently being transformed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Action returns a value of either "insert" or "update" indicating whether the current target row is about to be created or updated.

</td></tr><tr><td>

ignore

</td><td>

Boolean

</td><td>

When set to true, the current row transformation will be skipped and the remaining rows will be processed.If you have defined an onAfter script, the onAfter script runs for the current row even if the ignore flag is set to true.

</td></tr><tr><td>

status\_message

</td><td>

String

</td><td>

Defines a custom message to be sent in the &lt;status\_message&gt; XML response.

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, will halt the entire transformation for the current import set, with an error message.

</td></tr><tr><td>

error\_message

</td><td>

String

</td><td>

Defines a custom message to be sent in the &lt;error\_message&gt; XML response.

</td></tr></tbody>
</table> Example:

 ```
var name = source.u_name.toString();
var info = "Before the row is transformed, " + name;
log.info( info ); 
 
// Make sure a company name has been provided
var company = source.u_company.toString();
if(company.length == 0 ){
	ignore = true;
	info ="No company name, row ignored! " + name;
	log.info( info );
}
```

</td></tr><tr><td>

onAfter

</td><td>

When: The onAfter event script is processed at the end of a row transformation, after the source row has been transformed into the target row and saved.

 <table id="table_us2_m5s_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onAfter import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The row of the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The row of the target table that is currently being processed.

</td></tr><tr><td>

import\_set

</td><td>

GlideRecord

</td><td>

The import set that is currently being transformed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Action returns a value of either "insert" or "update" indicating whether the current target row was created or updated.

</td></tr><tr><td>

status\_message

</td><td>

String

</td><td>

Defines a custom message to be sent in the &lt;status\_message&gt; XML response.

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, will halt the entire transformation for the current import set, with an error message.

</td></tr><tr><td>

error\_message

</td><td>

String

</td><td>

Defines a custom message to be sent in the &lt;error\_message&gt; XML response.

</td></tr></tbody>
</table> Example:

 ```
if(source.new=="true"){
  gs.include('Cart');var bundle =new GlideRecord('sc_cat_item');
  bundle.addQuery('name','CONTAINS','comp');
  bundle.query();
  if(bundle.next()){
     var new_comp_cart = new Cart();
     var cart = new Cart();
     var item = cart.addItem(bundle);
     var rc = cart.placeOrder();
     log.info(rc.number);}}
```

</td></tr><tr><td>

onForeignInsert

</td><td>

When: The onForeignInsert event script is processed at the start of the creation of a related, referenced record, before the record is created.

 <table id="table_o4c_svs_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onForeignInsert import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The row of the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The row of the target table that is currently being processed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Action returns a value of either "insert" or "update" indicating whether the current target row is about to be created or updated.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Evaluates to the field name of the target record for which a foreign record that is about to be created.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Evaluates to the display value from the source record for which a foreign record is about to be created.

</td></tr><tr><td>

ignore

</td><td>

Boolean

</td><td>

When set to true, ignores the creation of a new foreign or related record.

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, rejects the entire transformation row, no data is saved for this row.

</td></tr></tbody>
</table> Example:

 ```
//Create an event.
var e = new GlideEvent("myimport_ForeignInsert", action, name, "");
e.insert();
```

</td></tr><tr><td>

onChoiceCreate

</td><td>

When: The onChoiceCreate event script is processed at the start of a choice value creation, before the new choice value is created.

 <table id="table_t4k_pws_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onChoiceCreate import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The row of the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The row of the target table that is currently being processed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Action returns a value of either "insert" or "update" indicating whether the current target row is about to be created or updated.

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Evaluates to the field name of the target record for which a choice value is about to be created.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Evaluates to the display value from the source record for which a choice is about to be created.

</td></tr><tr><td>

ignore

</td><td>

Boolean

</td><td>

When set to true, ignores the creation of a choice value.

</td></tr><tr><td>

error

</td><td>

Boolean

</td><td>

When set to true, rejects the entire transformation row, no data is saved for this row.

</td></tr></tbody>
</table> Example:

 ```
//Create an event
var e = new GlideEvent("myimport_ChoiceCreate", action, value, "");
e.insert();
```

</td></tr><tr><td>

onReject

</td><td>

When: The onReject event script is processed during the occurrence of a foreign record or choice creation, and the foreign record or choice is rejected ,the entire transformation row is not saved.

 <table id="table_q5k_4xs_sq"><thead><tr><th>

Import Set JS object

</th><th>

Type

</th><th>

Context in the onError import set event

</th></tr></thead><tbody><tr><td>

source

</td><td>

GlideRecord

</td><td>

The row of the source table that is currently being processed.

</td></tr><tr><td>

target

</td><td>

GlideRecord

</td><td>

The row of the target table that is currently being processed.

</td></tr><tr><td>

map

</td><td>

GlideTransformMap

</td><td>

Read-only information about the current transform map record.

</td></tr><tr><td>

action

</td><td>

String

</td><td>

Action returns a value of either "insert" or "update" indicating whether the current target row is about to be created or updated.

</td></tr><tr><td>

log

</td><td>

Function

</td><td>

The log object for the current import run. For example, log.info\(...\), log.warn\(...\), log.error\(...\).**Note:** To view the import logs, set the **glide.importlog.log\_to\_table** property to true. For more information, see [Import sets properties](../../../administer/import-sets/reference/r_ImportSetsProperties.md).

</td></tr></tbody>
</table> Example:

```
//Create an event
var e = new GlideEvent("myimport_onReject", action, "", "");
e.insert();
```

</td></tr></tbody>
</table>