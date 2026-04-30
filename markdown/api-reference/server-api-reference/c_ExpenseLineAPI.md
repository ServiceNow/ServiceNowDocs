---
title: ExpenseLine - Global
description: The ExpenseLine script include is used by various cost management processes and can also be used for generating expense line \(fm\_expense\_line\) records from your own server-side scripts.Constructor for ExpenseLine object.Creates a new expense line record.Used internally by the createExpense method to process CI relationships when the expense source is a cmdb\_ci record.Identifies the source rate card or distribution cost that was the source of expense line generation.Defines the description of an expense.Sets the parent field on the expense line.Flags the expense as recurring by setting the recurring field to true.Sets a value for the expense line summary\_type field.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ExpenseLine- Global

The ExpenseLine script include is used by various cost management processes and can also be used for generating expense line \(fm\_expense\_line\) records from your own server-side scripts.

This script include requires the Cost Management \(com.snc.cost\_management\) plugin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ExpenseLine - ExpenseLine \(GlideRecord source, Number amount, String description\)

Constructor for ExpenseLine object.

|Name|Type|Description|
|----|----|-----------|
|source|GlideRecord|GlideRecord identifying the source of the expense|
|amount|Number|Decimal number identifying the amount of the expense|
|description|String|\(Optional\) Description of the expense.|

|Type|Description|
|----|-----------|
|ExpenseLine object|The ExpenseLine object just instantiated.|

```
//get some random CI to be used as an expense source
        var ci = new GlideRecord("cmdb_ci_server");
        ci.query();
        ci.next();
        
        //create expense line
        var exp = new ExpenseLine(ci, 234.56, "Test expense line");
```

## ExpenseLine - createExpense\(\)

Creates a new expense line record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Boolean|True if the expense line was successfully created.|

```
//get some random CI to be used as an expense sourcevar ci =new GlideRecord("cmdb_ci_server");
ci.query();
ci.next();
 
//create expense line
var exp =new ExpenseLine(ci,234.56,"Test expense line");
exp.setSummaryType("run_business");
var success = exp.createExpense();

```

## ExpenseLine - processCIParents\(\)

Used internally by the createExpense method to process CI relationships when the expense source is a cmdb\_ci record.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|void| |

## ExpenseLine - setCostSource\(GlideRecord costSource\)

Identifies the source rate card or distribution cost that was the source of expense line generation.

This is not the source \(CI, task\) of the expense.

|Name|Type|Description|
|----|----|-----------|
|costSource|GlideRecord|GlideRecord of CI rate card cost, distribution cost, or task rate card. This is generally only used for system-generated expense lines.|

|Type|Description|
|----|-----------|
|void| |

## ExpenseLine - setDescription\(String description\)

Defines the description of an expense.

|Name|Type|Description|
|----|----|-----------|
|description|String|Description of expense.|

|Type|Description|
|----|-----------|
|void| |

## ExpenseLine - setParent\(GlideRecord expense\)

Sets the parent field on the expense line.

This is generally only used by the system when generating indirect expenses such as business service aggregated expenses.

|Name|Type|Description|
|----|----|-----------|
|expense|GlideRecord|Parent expense line record.|

|Type|Description|
|----|-----------|
|void| |

## ExpenseLine - setRecurring\(Boolean recurring\)

Flags the expense as recurring by setting the recurring field to true.

Expense lines are set to false by default so there is no need to call setRecurring\(false\).

|Name|Type|Description|
|----|----|-----------|
|recurring|Boolean|Set to true to identify expense line as a recurring expense.|

|Type|Description|
|----|-----------|
|void| |

## ExpenseLine - setSummaryType\(String summaryType\)

Sets a value for the expense line summary\_type field.

|Name|Type|Description|
|----|----|-----------|
|summaryType|String|Typically you would set this to a value already specified in the expense line summary type field choice list.|

|Type|Description|
|----|-----------|
|void| |

```
//get some random CI to be used as an expense sourcevar ci =new GlideRecord("cmdb_ci_server");
ci.query();
ci.next();
 
//create expense line
var exp =new ExpenseLine(ci,234.56,"Test expense line");
exp.setSummaryType("run_business");
```

