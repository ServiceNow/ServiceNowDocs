---
title: ExpenseAllocation - Global
description: The ExpenseAllocation script include is used by various cost management processes and can also be used for generating custom expense allocation records \(fm\_expense\_allocation\) from scripted expense allocation rules.Called when you create a new ExpenseAllocation object.Creates an expense allocation \(fm\_expense\_allocation\) record referencing the parameters provided during instantiation and this method.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ExpenseAllocation- Global

The ExpenseAllocation script include is used by various cost management processes and can also be used for generating custom expense allocation records \(fm\_expense\_allocation\) from scripted expense allocation rules.

This script include requires the Cost Management \(com.snc.cost\_management\) plugin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ExpenseAllocation - ExpenseAllocation\(GlideRecord expense, GlideRecord rule\)

Called when you create a new ExpenseAllocation object.

This is not needed if scripting advanced allocation rules. This object is already available as the *allocation* variable.

|Name|Type|Description|
|----|----|-----------|
|expense|GlideRecord|GlideRecord identifying the source of the expense.|
|rule|GlideRecord|GlideRecord identifying the rule to use in allocating the expense line.|

|Type|Description|
|----|-----------|
|ExpenseAllocation object|The ExpenseAllocation object just created.|

```
var allocation=new ExpenseAllocation(expenseGlideRecord, ruleGlideRecord);
```

## ExpenseAllocation - createAllocation\(GlideRecord target, Number amount\)

Creates an expense allocation \(fm\_expense\_allocation\) record referencing the parameters provided during instantiation and this method.

|Name|Type|Description|
|----|----|-----------|
|target|GlideRecord|GlideRecord target of the allocation, for example a cost center record to allocate an expense to Decimal amount - the amount of the allocation.|
|amount|Number|The amount of the allocation.|

|Type|Description|
|----|-----------|
|Boolean|True if the expense allocation was successfully created.|

```
var allocation=new ExpenseAllocation(expenseGlideRecord, ruleGlideRecord);
allocation.createAllocation(costCenterGlideRecord, 2345.67);
```

