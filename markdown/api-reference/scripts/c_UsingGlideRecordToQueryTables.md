---
title: Querying tables in script
description: Using methods in the GlideRecord API, you can return all records from a table, return records from a table that satisfy specific conditions, or return records that include a string from a single table or from multiple tables in a text index group.Describes the operators that can be used within an addQuery\(\) request.These examples demonstrate how to perform various GlideRecord queries.
locale: en-US
release: australia
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Server-side scripting, Scripting, API implementation, API implementation and reference]
---

# Querying tables in script

Using methods in the GlideRecord API, you can return all records from a table, return records from a table that satisfy specific conditions, or return records that include a string from a single table or from multiple tables in a text index group.

Query tables using the GlideRecord API. For API reference, see [GlideRecord - Scoped](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## Return all records from a table

To query a table, first create a GlideRecord object. To create a GlideRecord, create the following in script:

```
var target = new GlideRecord('incident');
```

Creating a GlideRecord creates a `target` variable which is a GlideRecord object for the incident table.

To process all records from the incident table, add the following script:

```
target.query(); // Issue the query to the database to get all records 
while (target.next()) { 
  // add code here to process the incident record 
}
```

This script issues the query\(\) to the database. Each call to next\(\) would load the next record for processing.

## Return records from a table that satisfy query conditions

Most of the time, you want to retrieve a specific record or a specific set of records, and you have some criteria \(query conditions\) that define the records you want to obtain. For example, say that you want to obtain all the incident records that have a priority value of 1. Here is the code that would accomplish that.

```
var target = new GlideRecord('incident'); 
target.addQuery('priority',1);
target.query(); // Issue the query to the database to get relevant records 
while (target.next()) { 
  // add code here to process the incident record 
}
```

Notice that the example script includes `target.addQuery('priority', 1);`. This line indicates that you only want the records where the **priority** field is equal to 1. In general, most queries that you want to perform are equality queries; queries where you want to find records with a field equal to a value. For this reason, you do not need to provide an equality operator. However, lets say you wanted to find all incidents where the **priority** field is greater than 1. In this case, you would provide the operator that you want to apply to the query.

```
var target = new GlideRecord('incident') ; 
target.addQuery('priority','>',1);
target.query(); // Issue the query to the database to get relevant records 
while (target.next()) { 
  // add code here to process the incident record 
}
```

## Return records from a table that include a string

Use the `'123TEXTQUERY321'` reserved name to search for string matches in all fields on a table. For example, this script returns records from the Incident table with field values that include the 'email' string.

```
var now_GR = new GlideRecord('incident');
gr.addQuery('123TEXTQUERY321', 'email');
gr.query();
```

`'123TEXTQUERY321'` is a reserved option for the **name** parameter in the `addQuery()` method. You can use this option in an encoded query string. For example, instead of `gr.addQuery('123TEXTQUERY321', 'email');`, you can use `gr.addEncodedQuery('123TEXTQUERY321=email')`.

String search is case-insensitive. The system returns the same results whether you search for `email`, `Email`, or `EMAIL`.

**Note:** Before you can query using a string search, you must configure text indexing \(and optionally search attributes\) for the table you want to search. For more information, see [Configure a single table for indexing and searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/configure-single-table-for-indexing.md).

## Return records from multiple tables in a text index group that include a string

Use the `'123TEXTINDEXGROUP321'` reserved name to search for a string in a table from a text index group. This option returns results with relevancy scores computed using the text index group's settings.

**Note:** You can only query one table in the text index group at a time. Use this option when you want to issue multiple single-table queries and merge their results, ordering them by relevancy score. The advantage of this option is that search result relevancy scores for the individual table queries are normalized consistently for all tables in the text index group.

For example, this script returns records from the Knowledge table that include the keyword 'email', with relevancy scores computed for the 'portal' index group.

```
var now_GR = new GlideRecord('kb_knowledge');
gr.addQuery('123TEXTQUERY321', 'email');
gr.addQuery('123TEXTINDEXGROUP321', 'portal');
gr.query();
```

You can create a similar query for each additional table in the 'portal' index group that you want to search, and then merge the individual queries' results, displaying the results with the highest relevancy scores first. Because all of these search queries use the same text index group search settings, the relevancy scores for their results are all normalized consistently. If you searched the same set of tables without using the `gr.addQuery('123TEXTINDEXGROUP321', 'portal')` method, the individual queries' relevancy scores would be normalized differently and would not be a useful basis for sorting the merged result set.

`'123TEXTINDEXGROUP321'` is a reserved option for the **name** parameter in the `addQuery()` method. You can use this option in an encoded query string. For example, instead of `gr.addQuery('123TEXTINDEXGROUP321', 'portal');`, you can use `gr.addEncodedQuery('123TEXTINDEXGROUP321=portal')`.

Multi-table string search is case-insensitive. The system returns the same results whether you search for `email`, `Email`, or `EMAIL`.

**Note:** Before you can query tables in an index group, you must configure text indexing and search attributes for those tables and include them in the index group. For more information, see [Configure multiple tables for indexing and searching](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/index-multiple-tables.md). All tables in the index group must use the V4 indexing format.

**Parent Topic:**[Server-side scripting](c_ServerScripting.md)

## Available JavaScript operators

Describes the operators that can be used within an addQuery\(\) request.

<table id="table_pc2_kqj_2p"><thead><tr><th>

Field

</th><th>

Definition

</th><th>

addQuery

</th></tr></thead><tbody><tr><td>

=

</td><td>

Field must be equal to value supplied.

</td><td>

addQuery\('priority', '=', 1\);

</td></tr><tr><td>

&gt;

</td><td>

Field must be greater than value supplied.

</td><td>

addQuery\('priority', '&gt;', 1\);

</td></tr><tr><td>

&lt;

</td><td>

Field must be less than value supplied.

</td><td>

addQuery\('priority', '&lt;', 3\);

</td></tr><tr><td>

&gt;=

</td><td>

Field must be equal or greater than value supplied.

</td><td>

addQuery\('priority', '&gt;=', 1\);

</td></tr><tr><td>

&lt;=

</td><td>

Field must be equal or less than value supplied.

</td><td>

addQuery\('priority', '&lt;=', 3\);

</td></tr><tr><td>

!=

</td><td>

Field must not equal the value supplied.

</td><td>

addQuery\('priority', '!=', 1\);

</td></tr><tr><td>

STARTSWITH

</td><td>

Field must start with the value supplied. The example shown on the right returns all records where the *short\_description* field starts with the text Error.

</td><td>

addQuery\('short\_description', 'STARTSWITH', 'Error'\);

</td></tr><tr><td>

CONTAINS

</td><td>

Field must contain the value supplied somewhere in the text. The example shown on the right returns all records where the *short\_description* field contains the text Error anywhere in the field.**Note:** The LIKE operation is not supported. Administrators must use CONTAINS in the query.

</td><td>

addQuery\('short\_description', 'CONTAINS', 'Error'\);

</td></tr><tr><td>

IN

</td><td>

Takes a map of values that allows commas, and gathers a collection of records that meet some other requirement. Behaves as `Select * from <table> where short_description IN ('Error', 'Success', 'Failure')`, which is identical to `Select * from <table> where short_description='Error'`. For example, to query all variable values that belong to a specific Activity, use the **IN** clause, and store their sys\_ids in a map, or comma-separated list. Then query the variable value table and supply this list of sys\_ids.

</td><td>

addQuery\('short\_description', 'IN', 'Error,Success,Failure'\);

</td></tr><tr><td>

ENDSWITH

</td><td>

Field must terminate with the value supplied. The example shown on the right returns all records where the *short\_description* field ends with text Error.

</td><td>

addQuery\('short\_description', 'ENDSWITH', 'Error'\);

</td></tr><tr><td>

DOES NOT CONTAIN

</td><td>

Selects records that do NOT match the pattern in the field. This operator does not retrieve empty fields. For empty values, use the operators "is empty" or "is not empty."The example shown on the right returns all records where the *short\_description* field does not have the word "Error."

</td><td>

addQuery\('short\_description', 'DOES NOT CONTAIN', 'Error'\);

</td></tr><tr><td>

NOT IN

</td><td>

Takes a map of values that allows commas, and gathers a collection of records that meet some other requirement. Behaves as: `Select * from <table> where short_description NOT IN ('Error')`.

</td><td>

addQuery\('short\_description', 'NOT IN', 'Error,Success,Failure'\);

</td></tr><tr><td>

INSTANCEOF

</td><td>

Special operator that retrieves only records of a specified "class" for extended tables. The code example on the right, shows how to retrieve all configuration items that are classified as computers.

</td><td>

addQuery\('sys\_class\_name', 'INSTANCEOF', 'cmdb\_ci\_computer'\);

</td></tr></tbody>
</table>For additional information on the operators that are available for filters and queries, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

There are also some special methods that you can use to search for data that is NULL or NOT NULL. To search for all incidents where the *short\_description* field has not been supplied \(is null\), use the following query:

```
var target = new GlideRecord('incident'); 
target.addNullQuery('short_description');
target.query(); // Issue the query to the database to get all records 
while (target.next()) { 
  // add code here to process the incident record 
}
```

To find all incidents in which a *short\_description* has been supplied, use the following query:

```
var target = new GlideRecord('incident'); 
target.addNotNullQuery('short_description');
target.query(); // Issue the query to the database to get all records 
while (target.next()) { 
  // add code here to process the incident record 
}
```

For more information on the GlideRecord API and its available methods, see [GlideRecord](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

## GlideRecord query examples

These examples demonstrate how to perform various GlideRecord queries.

### query

```
var rec = new GlideRecord('incident');
rec.query(); 
while(rec.next()) { 
  gs.print(rec.number + ' exists'); }
```

### update

```
var rec = new GlideRecord('incident');
rec.addQuery('active',true);
rec.query(); 
while(rec.next()) { 
  rec.active = false;
  gs.print('Active incident ' + rec.number = ' closed');
  rec.update(); }
```

### insert

```
var rec = new GlideRecord('incident');
rec.initialize();
rec.short_description = 'Network problem'; 
rec.caller_id.setDisplayValue('Joe Employee'); 
rec.insert();
```

### delete

```
var rec = new GlideRecord('incident');
rec.addQuery('active',false);
rec.query(); 
while(rec.next()) { 
  gs.print('Inactive incident ' + rec.number + ' deleted');
  rec.deleteRecord(); }
```

### Querying Service Catalog Tables

You cannot directly query the variables of the Service Catalog Request Item table \[sc\_req\_item\]. Instead, query the Variable Ownership table, \[sc\_item\_option\_mtom\], by adding two queries, one for the variable name and another for the value. The query returns the many-to-many relationship, which you can dot-walk to the requested item. The following example finds the request items that have the variable *item\_name* with a value of *item\_value* and displays the request item numbers:

```
var now_GR = new GlideRecord('sc_item_option_mtom');
gr.addQuery('sc_item_option.item_option_new.name','item_name');
gr.addQuery('sc_item_option.value','item_value');
gr.query();
 
while(gr.next()) {
  gs.addInfoMessage(gr.request_item.number); }
```

For additional information see [GlideRecord](../../../app-store/dev_portal/API_reference/glideRecordScoped/concept/c_GlideRecordScopedAPI.md#).

