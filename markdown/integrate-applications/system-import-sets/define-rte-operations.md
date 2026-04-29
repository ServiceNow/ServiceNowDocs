---
title: Define Robust Transform Engine operations
description: Define the operations the Robust Transform Engine \(RTE\) should perform.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create Extract Transform Load \(ETL\) definitions, Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# Define Robust Transform Engine operations

Define the operations the Robust Transform Engine \(RTE\) should perform.

## Before you begin

Role required: import\_transformer

## About this task

You should always perform operations on only one entry. Select all source and target fields from the same entity.

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **ETL Definitions**.

2.  Select an ETL definition.

3.  On the ETL Entities tab, select an ETL entity.

4.  On the RTE Entity Operations tab, click **New**.

5.  Select the kind of operation you want to create.

6.  Complete the form.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the operation.|
    |Source Field|Input ETL field for the operation if the operation takes a single input.|
    |Target Field|Output ETL field for the operation if the operation takes a single output.|
    |Source Fields|Input ETL fields for the operation if the operation takes multiple inputs.|
    |Target Fields|Output ETL fields for the operation if the operation takes multiple outputs.|
    |Operation Group|Optional name to group related operations.|
    |Overwrite Existing Value|If true, overwrites an existing non-empty value in the target fields.|
    |Optional Joining String|Optional string to join values on.|
    |Decimal Places|Optional number of decimal places to force output value to.|
    |Remainder Target Field|Optional second target field to write the trimmed remainder of the source string after the first numeric value is removed.|
    |Glide Matching Fields|Comma-delimited list of column names to use for lookup in the target table.|
    |Target Table|Table to perform a lookup on.|
    |Glide Target Fields|Comma-delimited list of columns to return from the target table.|
    |Match Regular Expression|Matching regular expression for replace operations.|
    |Replacement Regular Expression|Replacement string.|
    |Use Unique Input Sets|If true, the operation processes only the unique set of inputs to the operation. Otherwise, the operation processes every record individually.|
    |Literal Set Value|String value to set to target.|
    |Splitting String|String to split the input value on.|
    |Date Format|Date/time format expressed in simple Java format.|
    |Order|Order in which the operation runs on the entity.|
    |Script|Script that runs as part of the operation.|
    |Is Conditional|Specifies whether to apply the operation if the specified conditions are met.|
    |Conditional Fields|Fields to use in the condition.|
    |Conditional Script|Condition specified as a string. For an example of a conditional script, see [Temporary entity model](../concept/temp-entity-model.md).|
    |Application|Application scope for this record.|
    |Operation Type|Operation type for this operation.|
    |Entity|Entity this operation applies to.|
    |Definition|Selected ETL entity definition that this entity and operation belong to.|

7.  Click **Submit**.


