---
title: Lookup utility
description: Use the Lookup utility in a Virtual Agent topic to return a ServiceNow record query.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Assistant Designer utilities, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Lookup utility

Use the Lookup utility in a Virtual Agent topic to return a ServiceNow record query.

## Lookup utility properties

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

The name that identifies this Lookup utility node in the topic flow.

</td></tr><tr><td>

Variable name

</td><td>

The variable that stores the record returned by the script. The variable name is automatically created from the Node name property.

</td></tr><tr><td>

Table

</td><td>

The table used for the query.

</td></tr><tr><td>

Filter this table by using

</td><td>

The query to retrieve the record. Use the condition builder or a script to specify a query condition.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td class="sub-head" colspan="2">

Hide this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr></tbody>
</table>## Example Lookup utility

![Lookup utility properties include a node name, the table to query, and conditions to filter the results of the lookup.](../images/LookupExample.png "Lookup utility basic properties")

## Example Lookup script

```
(function execute(table) {

       var now_GR = new GlideRecord(table);
       gr.addEncodedQuery('active=true');
       gr.setLimit(1);
       gr.query();
       if(gr.next()) {
          return gr;
    }
})(table)

```

In this example, a table is queried for the first active record. The table to be queried is defined in the **Table** property found in the lookup utility control. The `setLimit()` method ensures that only a single record is returned from the database. If a record is found, it is returned. For more information on GlideRecord queries, see [Querying tables in script](https://www.servicenow.com/docs/access?context=c_UsingGlideRecordToQueryTables&version=australia&pubname=australia-api-reference&ft:locale=en-US) .

**Parent Topic:**[Assistant Designer utilities](va-utilities.md)

