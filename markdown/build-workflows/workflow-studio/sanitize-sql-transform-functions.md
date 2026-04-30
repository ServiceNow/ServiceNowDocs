---
title: Sanitize SQL transform functions
description: Use sanitize SQL transform functions to escape special characters and prevent injection in String data pills to be used for SQL statements.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Transform functions, Flows, subflows, and actions reference, Reference, Workflow Studio, Build workflows]
---

# Sanitize SQL transform functions

Use sanitize SQL transform functions to escape special characters and prevent injection in String data pills to be used for SQL statements.

Sanitize SQL transform functions require a String input data pill. Make sure to use the correct input [data pill type](action-inputs-outputs.md) when applying sanitize SQL transform functions. If a sanitize SQL transform function is applied to an improper data type, the data is not transformed at runtime and the input value is returned instead. For more information on confirming your flow runtime values, see [Test a flow](../task/flow-test.md).

**Note:** When a data pill is dropped into the **SQL Statement** input for a [JDBC step](jdbc-step.md), the sanitize SQL transform function category automatically appears.

## Sanitize SQL Identifier

Returns a String with escaped special characters/injected values for SQL identifiers \(such as table, view, and column names\). Wraps the input String in database-specific quotes.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|**Database** - The database-specific context in which characters are escaped. Choices include MySQL, Oracle, PostgreSQL, and Microsoft SQL Server.|String - String with SQL identifiers that are properly escaped based on the selected database|

-   Input: `simple_column`
-   Database: `MySQL`
-   Output: ``simple_column``

**Note:**

-   If your input String contains a period character, **Sanitize SQL Identifier** returns an error. To join SQL identifiers using a period, use two data pills concatenated with a period and apply **Sanitize SQL Identifier** to both pills.
-   Don't enclose the input data pill in quotes. The system automatically wraps the input value with the type of quotes or backticks that apply to your database type.

## Sanitize SQL Value

Returns a String with escaped special characters or injected values for SQL values. Wraps the input String in database-specific quotes.

|Input data pill|Parameters|Output data pill|
|---------------|----------|----------------|
|String|**Database** - The database-specific context in which characters are escaped. Choices include MySQL, Oracle, PostgreSQL, and Microsoft SQL Server.|String - String with SQL values that are properly escaped based on the selected database|

-   Input: `'1'='1`
-   Database: `SQLServer`
-   Output: `''1''=''1'`

**Note:** Don't enclose the input data pill in quotes. The system automatically wraps the input value with the type of quotes or backticks that apply to your database type.

**Parent Topic:**[Transform functions](../concept/transform-functions.md)

