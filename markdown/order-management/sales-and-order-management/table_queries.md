---
title: Minimizing table queries
description: Learn how to minimize queries to maximize performance.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Minimizing table queries

Learn how to minimize queries to maximize performance.

The more queries you have, the more they impact performance. This article discusses two ways to minimize queries to help keep performance as fast as possible.

## Implementing rules

When you create a configuration, consider how you might implement it to minimize queries.

For example, suppose you have a table of the length, width and height of various components. Once you select a part number, you want to query those values to calculate the volume. The best way to query that information depends on the use case and where the values are needed downstream of the query.

If the configuration only uses the total volume, the best approach is to put the query in the advanced determination rule for the volume, similar to this simplified code:

-   Query L,W and H from table
-   Var vol = L\*W\*H
-   Return vol

Total queries: 1.

However, if you are writing a volume rule and you know you will need to use the length, width and height values elsewhere, the above code is not appropriate. Instead, you should write your determination rule as follows:

-   Var vol=L\*W\*H
-   Return vol

You should have the queries in the determination rules. Determination rules can only define one field at a time, so this would need three determination rules—one rule each for length, width and height—and three queries. Doing this prevents running a fourth query \(one in each length, width and height rule, and one in the volume determination rule\).

Another way to reduce queries is to be aware of the fields associated with a rule. Suppose you have a query in a rule that references a lot of fields. The rule runs every time one of the fields associated with that rule changes. Therefore, the query runs every time.

Let’s say you need to calculate the volume and then multiply that volume by density \(which could change based on material the user selects\) to get the total weight. The user does not need to use volume anywhere else downstream. Here is a sample script:

-   Query L,W,H from table
-   Var vol= L\*W\*H
-   Var mass = vol \* cfg.density
-   Return mass

The problem is that every time the density changes, the rule runs and then the query runs. But the values of L, W and H do not change. Therefore, the processor has to go to the table, find the values for L, W and H, and redefine the variable `vol` to the same value it was before. A better approach is to calculate volume as a separate field with a separate rule. Then, write the mass rule as follows:

```
var mass = cfg.volume * cfg.density;
return mass;
```

Mass still recalculates every time, but it is intended to. No processing time is wasted doing unnecessary querying and redefining values.

## Querying a list

As seen above with L,W and H, you can pull multiple columns from a table in a single query. At other times, you might want to query the table on multiple values. For example, suppose you have a multiselect picklist \(field name `selectedColors`\) of different colors. You also have a “hues” table that has a red, blue and green column to tell you the ratios.

If you wanted to query the table for all the selected options of the multiselect picklist, there are two options.

```
for (color of cfg.selectedColors){
        var tableResults=lookup(“Select blue, red, green from hues where value := value”, {“value”: color});
        //more code
```

This `for` loop means that the number of queries is based on the number of selected options for the `selectedColors` field. Alternatively, the following code queries the table once.

```
var tableResults=lookup(“select blue, red, green from hues where value in (:list)”, {“list”: cfg.selectedColors});
```

This method is better.

For more information on what is supported in a query, see [The lookup function: commands and syntax](cpq-the-lookup-function-commands-and-syntax.md).

