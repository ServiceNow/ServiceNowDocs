---
title: GlideDBFunctionCaseBuilder - Global
description: The GlideDBCaseStatementBuilder API allows you to build SQL CASE statements and return values based on a series of conditions.Instantiates a GlideDBFunctionCaseBuilder object.Concludes the list of conditions and builds the final CASE statement.Optional. Following at least one pair of calls to when and then, the otherwise\(\) call allows you to specify a value to output if none of the when expressions are satisfied.Following any when\(\) method, then\(\) allows you to specify a value to output if the when\(\) expression is satisfied.The most versatile of the supported 'when' expressions, the when\(\) method allows you to supply any boolean-valued Glide function as the condition to satisfy.Begins a comparison case condition.Similar to whenCompare\(\), whenEqual\(\) is a convenient method for checking equality. It is equivalent to whenCompare\(leftExpression, ‘=’, rightExpression\).
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideDBFunctionCaseBuilder- Global

The GlideDBCaseStatementBuilder API allows you to build SQL CASE statements and return values based on a series of conditions.

You can use this API as part of the definition of the [GlideElement - Global](../../GlideElement_global/concept/c_GlideElementAPI.md#) API or when querying a table. To build a `CASE` statement, start by instantiating the GlideDBFunctionCaseBuilder object using its constructor, GlideDBFunctionCaseBuilder\(\). Then, define one or more cases using a series of when\(\) and then\(\) calls followed by a single, optional otherwise\(\) call. Lastly, call the build\(\) method to finalize the builder and produce the completed database function case statement. This statement can then be used directly or as part of other Glide function definitions.

Required roles: Admin, function\_field\_admin.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GlideDBFunctionCaseBuilder - GlideDBFunctionCaseBuilder\(\)

Instantiates a GlideDBFunctionCaseBuilder object.

|Name|Type|Description|
|----|----|-----------|
|None| ||

This example instantiates a GlideDBFunctionCaseBuilder object.

```
var caseBuilder = new GlideDBFunctionCaseBuilder();

```

## GlideDBFunctionCaseBuilder - build\(\)

Concludes the list of conditions and builds the final CASE statement.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|string|The completed case statement.|

The following example shows how to define and build a simple case statement. Depending on the numerical value of the impact field, it will output one of four different strings.

```
const caseStatement = new GlideDBFunctionCaseBuilder()
    .whenCompare("impact", "'='", "'1'").then("'CRITICAL'")
    .whenCompare("impact", "'='", "'2'").then("'URGENT'")
    .whenCompare("impact", "'='", "'3'").then("'IMPORTANT'")
    .otherwise("'NOT IMPORTANT'")
    .build();

const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement);
gr_incident.setLimit(10);
gr_incident.query();
while(gr_incident.next())  {
    gs.info("impact: {0}  case: {1}",
            [gr_incident.impact, gr_incident.getValue(caseStatement)]);
}
```

Output:

```
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 3  case: IMPORTANT
```

## GlideDBFunctionCaseBuilder - otherwise\(String exp\)

Optional. Following at least one pair of calls to when and then, the otherwise\(\) call allows you to specify a value to output if none of the when expressions are satisfied.

|Name|Type|Description|
|----|----|-----------|
|exp|String|Value to output. Can be a constant, a reference to a field, or another Glide function.|

|Type|Description|
|----|-----------|
|GlideDBFunctionCaseBuilder|The fluent builder object to continue building the statement.|

The following example shows how to define and build a simple case statement.

```
const caseStatement = new GlideDBCaseFunctionBuilder()
    .whenEqual("impact", "'1'").then("'CRITICAL'") 
    .whenEqual("impact", "'2'").then("category")
    .whenEqual("impact", "'3'").then("length(short_description)")
    .otherwise("'NOT IMPORTANT'")
    .build();

const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement);
gr_incident.setLimit(10);
gr_incident.query();
while(gr_incident.next())  {
      gs.info("impact: {0}  case: {1}",
              [gr_incident.impact, gr_incident.getValue(caseStatement)]);
}
```

Output:

```
*** Script: impact: 2  case: inquiry
*** Script: impact: 2  case: Hardware
*** Script: impact: 1  case:  CRITICAL
*** Script: impact: 2  case: database
*** Script: impact: 2  case: inquiry
*** Script: impact: 3  case: 28
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 3  case: 17
*** Script: impact: 3  case: 29
```

## GlideDBFunctionCaseBuilder - then\(String exp\)

Following any when\(\) method, then\(\) allows you to specify a value to output if the when\(\) expression is satisfied.

|Name|Type|Description|
|----|----|-----------|
|exp|String|Value to output. Can be a constant, reference to a field, or another Glide function.|

|Type|Description|
|----|-----------|
|GlideDBFunctionCaseBuilder|The fluent builder object to continue building the statement.|

The following example shows how to define and build a simple case statement. In this case, the then\(\) expressions show how you can output not only strings, but also the results of other glide functions such as the `length(short_description)`.

```
const caseStatement = new GlideDBCaseFunctionBuilder()
    .whenEqual("impact", "'1'").then("'CRITICAL'") 
    .whenEqual("impact", "'2'").then("category")
    .whenEqual("impact", "'3'").then("length(short_description)")
    .otherwise("'NOT IMPORTANT'")
    .build();

const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement);
gr_incident.setLimit(10);
gr_incident.query();
while(gr_incident.next())  {
      gs.info("impact: {0}  case: {1}",
              [gr_incident.impact, gr_incident.getValue(caseStatement)]);
}
```

Output:

```
*** Script: impact: 2  case: inquiry
*** Script: impact: 2  case: Hardware
*** Script: impact: 1  case:  CRITICAL
*** Script: impact: 2  case: database
*** Script: impact: 2  case: inquiry
*** Script: impact: 3  case: 28
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 3  case: 17
*** Script: impact: 3  case: 29
```

## GlideDBFunctionCaseBuilder - when\(String func\)

The most versatile of the supported 'when' expressions, the when\(\) method allows you to supply any boolean-valued Glide function as the condition to satisfy.

<table id="table_dmg_sy2_xwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

func

</td><td>

String

</td><td>

A Glide function that results in a boolean-valued result when evaluated. Possible values: -   glidefunction:compare
-   glidefunction:and
-   glidefunction:or

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|glideDBFunctionCaseBuilder|The object to continue building the statement.|

The following example shows how to define and build a simple case statement. In this case, the when\(\) method is used to specify more complex comparison expressions. If the expression evaluates to true, the corresponding string is returned.

```
const caseStatement = new GlideDBFunctionCaseBuilder() 
    // if impact == 1 AND category == 'Software' then output "CRITICAL SOFTWARE" 
    .when("and(compare(impact, '=', '1'), compare(category, '=',  
'Software')") 
        .then("'CRITICAL SOFTWARE'") 
    // if impact == 1 then output "CRITICAL OTHER" 
    .when("compare(impact, '=', '1')") 
        .then("'CRITICAL OTHER'") 
    // if impact == 2 OR category == 'Software' then output "URGENT" 
    .when("or(compare(impact, '=', '2'), compare(category, '=', 'Software')") 
        .then("'URGENT'") 
    // If none of the above expressions are true, output "NOT IMPORTANT" 
    .otherwise("'NOT IMPORTANT'") 
    .build(); 
 
const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement); 
gr_incident.setLimit(20); 
gr_incident.query(); 
while(gr_incident.next())  { 
      gs.info("impact: {0}  category: {1}  case: {2}", 
            [gr_incident.impact, gr_incident.category, gr_incident.getValue(caseStatement)]); 
}
```

Output:

```
impact: 2  category: inquiry  case: URGENT
impact: 2  category: Hardware  case: URGENT
impact: 1  category: inquiry  case:  CRITICAL OTHER
impact: 2  category: database  case: URGENT
impact: 2  category: inquiry  case: URGENT
impact: 3  category: software  case: URGENT
impact: 1  category: inquiry  case: CRITICAL OTHER
impact: 1  category: inquiry  case: CRITICAL OTHER
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 3  category: hardware  case: NOT IMPORTANT
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 3  category: hardware  case: NOT IMPORTANT
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 1  category: inquiry  case: CRITICAL OTHER
impact: 1  category: software  case: CRITICAL SOFTWARE
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 3  category: inquiry  case: NOT IMPORTANT
impact: 2  category: software  case: URGENT
impact: 1  category: software  case: CRITICAL SOFTWARE
```

## GlideDBFunctionCaseBuilder - whenCompare\(String exp1, String op, String exp2\)

Begins a comparison case condition.

<table id="table_jj1_2q2_xwb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

exp1

</td><td>

String

</td><td>

Left comparison expression. Can be a constant, reference to a field, or another Glide function.

</td></tr><tr><td>

op

</td><td>

String

</td><td>

Comparison operator, surrounded with quotes. Valid values:

-   "'='"
-   "'&lt;'"
-   "'&gt;'"
-   "'&lt;='"
-   "'&gt;='"

</td></tr><tr><td>

exp2

</td><td>

String

</td><td>

Right comparison expression. Can be a constant, reference to a field, or another Glide function.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|GlideDBFunctionCaseBuilder|The function builder object to continue building the statement.|

The following example shows how to define and build a simple case statement. In this case, the whenCompare\(\) method is used to compare the value of the impact field to a number and output a specified string if they match.

```
const caseStatement = new GlideDBFunctionCaseBuilder()
    .whenCompare("impact", "'='", "'1'").then("'CRITICAL'")
    .whenCompare("impact", "'='", "'2'").then("URGENT")
    .whenCompare("impact", "'='", "'3'").then("IMPORTANT")
    .otherwise("'NOT IMPORTANT'")
    .build();

const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement);
gr_incident.setLimit(10);
gr_incident.query();
while(gr_incident.next()) {
    gs.info("impact: {0} case: {1}",
            [gr_incident.impact, gr_incident.getValue(caseStatement)]);
}
```

Output:

```
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 3  case: IMPORTANT

```

## GlideDBFunctionCaseBuilder - whenEqual\(String exp1, String exp2\)

Similar to whenCompare\(\), whenEqual\(\) is a convenient method for checking equality. It is equivalent to whenCompare\(leftExpression, ‘=’, rightExpression\).

|Name|Type|Description|
|----|----|-----------|
|exp1|String|Left comparison expression. Can be a constant, a reference to a field, or another Glide function.|
|exp2|String|Right comparison expression. Can be a constant, a reference to a field, or another Glide function.|

|Type|Description|
|----|-----------|
|GlideDBFunctionCaseBuilder|The function builder object to continue building the statement.|

The following example shows how to define and build a simple case statement. In this case, the whenEqual\(\) method is used to compare the value of the impact field to a number and output a specified string if they match.

```
const caseStatement = new GlideDBFunctionCaseBuilder()
    .whenEqual("impact", "'1'").then("'CRITICAL'")
    .whenEqual("impact", "'2'").then("'URGENT'")
    .whenEqual("impact", "'3'").then("'IMPORTANT'")
    .otherwise("'NOT IMPORTANT'")
    .build();

const gr_incident = new GlideRecord("incident");
gr_incident.addFunction(caseStatement);
gr_incident.setLimit(10);
gr_incident.query();
while(gr_incident.next())  {
    gs.info("impact: {0}  case: {1}",
            [gr_incident.impact, gr_incident.getValue(caseStatement)]);
}
```

Output:

```
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 2  case: URGENT
*** Script: impact: 2  case: URGENT
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 1  case: CRITICAL
*** Script: impact: 3  case: IMPORTANT
*** Script: impact: 3  case: IMPORTANT
```

