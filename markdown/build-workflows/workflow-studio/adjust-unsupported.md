---
title: Modify Decision Tables in the Classic UI
description: Workflow Studio supports decision tables that were created in the classic environment. However, some data types and conditions from the classic environment aren’t fully supported in Workflow Studio. For unsupported field types and decisions with complex conditional logic, use the decision rule view to modify these condition expressions.
locale: en-US
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using decision tables, Decision tables, Workflow Studio, Build workflows]
---

# Modify Decision Tables in the Classic UI

Workflow Studio supports decision tables that were created in the classic environment. However, some data types and conditions from the classic environment aren’t fully supported in Workflow Studio. For unsupported field types and decisions with complex conditional logic, use the decision rule view to modify these condition expressions.

The first time you open a decision table that was created in the classic environment, Workflow Studio automatically creates condition columns for all unique fields evaluated in the condition criteria.

-   If the table contains table-compatible decision rules, one condition per cell is displayed.
-   If a decision rule contains unsupported field types or complex logic, all the conditions in the condition columns are merged into a single condition expression. This expression is a hyperlink to Condition Builder that you can use to modify the conditions for the decision rule. For more information, see Condition builder.
-   If you remove the aspects of the condition expression that define the decision as complex, the decision is displayed in the supported format.

The following sections provide summaries of complex types of conditional logic.

## Decisions with complex logic

Some decision rules may not be supported in Workflow Studio. These decisions are:

-   Decisions with an OR condition in the condition expression
-   Decisions with multiple criteria evaluating the same non-reference input
-   Decisions with multiple criteria evaluating the same reference field or record
-   Decisions that evaluate unsupported input data types
-   Decisions that evaluate inactive inputs

## Decision tables with unsupported input data types

If an input has an unsupported data type, you can change only the input label and the **Mandatory** toggle switch. The input data type is read-only, and you cannot add new condition columns.

## Decision tables with unsupported conditions

If a condition column has an unsupported data type, you can still change the label and description. The input and default operator are read-only.

-   In an unsupported condition column, cells without values are inactive. Users must use decision rule view to enter a value.
-   When a value is entered for an unsupported condition column, the resulting decision row will be an unsupported decision.

**Parent Topic:**[Using decision tables](using-decision-builder.md)

