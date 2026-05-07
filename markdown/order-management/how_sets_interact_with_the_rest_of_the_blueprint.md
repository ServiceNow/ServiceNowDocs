---
title: How sets interact with the rest of a blueprint
description: The implications of sets when used in blueprints.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure sets, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# How sets interact with the rest of a blueprint

The implications of sets when used in blueprints.

Suppose you have a blueprint with the following fields:

-   field1
-   field2
-   setFieldA
-   setFieldB

The setFieldA and setFieldB fields are part of a set named sampleSet. The field1 and field2 fields are not part of a set, but they are in the same blueprint as sampleSet. For our case, assume that sampleSet has a size of 2. That structure would look something like this:

![Workflow](../images/cpq-sets-sample-structure.png)

Because a field can have a different value for each set index, a field in the set cannot influence a field outside the set \(such as field2\). However, fields outside the set \(such as field1\) can influence fields in the set. See the diagram:

![Work flow diagram](../images/cpq-sets-sample-structure-interaction.png)

## Example: Ambiguous conditions

If in sampleSet index 1, setFieldA=Video and in sampleSet index 2, setFieldA=Audio, we cannot have the following rule:

-   Condition: “if setFieldA==Video
-   Action: set field2 to mp4

For index1, the condition is true, and the rule fires. For index2, the condition is false, and the rule does not fire. Because field2 is outside the set, it is not clear whether the rule should fire.

However, you can write rules for fields that affect other fields in the same set. These rules are independently applied to each index. Fields in indexes cannot influence fields in other indexes.

## Example: A valid rule

The following rule is valid:

-   Condition: field1 == Mammals
-   Action: Include the following field options on setFieldA: \[“Lions”, “Tigers”, “Bears”\]

The field options Lions, Tigers, and Bears are present for each index in sampleSet.

## Example: Independent indexes

Suppose in sampleSet index 1, setFieldA=Video and in sampleSet index 2, setFieldA=Audio, and the following rule is set:

-   Condition: If setFieldA == Video
-   Action: setFieldB = true

For index1, the condtion is true, and the rule fires. For index2, the condition is false, and the rule does not fire. Therefore, setFieldB for index 1 is true, but the rule does not fire for the second index. Each index is independent of the other indexes.

![Workflow diagram](../images/cpq-sets-sample-structure-example-3.png)

A set that is isolated from the rest of the blueprint is not very useful, but there are ways that the set can affect the blueprint outside of the set. First, if a Product rule is created using fields in the set, each Index in the set uses the Product rule to affect the BOM when the conditions are met. This is beneficial because you can write a single rule that each Index of the set follows differently, depending on the field values in that index.

If we want to have set fields affect fields outside the set, we have to use the set aggregates. There are five set aggregates: Sum, Average, Min, Max and Count. Each created aggregate will have a field variable name \(with special formatting\). This is because the aggregate fields operate like any other field outside the set, and they can influence other fields.

![Workflow diagram](../images/cpq-sets-sample-structure-example-4.png)

**Related topics**  


[Creating set aggregates](creating_set_aggregates.md)

