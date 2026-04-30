---
title: CriteriaEvaluator - Global
description: The CriteriaEvaluator script include provides methods to implement a general-purpose criteria evaluator.Adds the criteria to be evaluated.Evaluates the criteria.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# CriteriaEvaluator- Global

The CriteriaEvaluator script include provides methods to implement a general-purpose criteria evaluator.

The general use pattern is to construct the class, add as many criteria as needed, then evaluate.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## CriteriaEvaluator - addCriterion\(String lhComparand, String operator, String rhComparand\)

Adds the criteria to be evaluated.

|Name|Type|Description|
|----|----|-----------|
|lhComparand|String|The left hand comparand. Must be a named value in the left hand values input into evaluate\(\).|
|operator|String|The operator. Must be one of: equals, starts with, contains, does not contain, ends with, or regex matches.|
|rhComparand|String|The right hand comparand. Can be evaluated either as one of the right hand values input to evaluate\(\) or as a literal string.|

|Type|Description|
|----|-----------|
|void| |

## CriteriaEvaluator - evaluate\(Object lhValues, String rhValues, Boolean any\)

Evaluates the criteria.

|Name|Type|Description|
|----|----|-----------|
|lhValues|Object|A hashmap of name-value pairs to evaluate the left hand comparands of the criteria.|
|rhValues|String|Optional right hand values to use instead of the literal value in evaluating the right hand comparands.|
|any|Boolean|If true, any criterion matching suffices for a true result. If false, all criteria must match for a true result.|

|Type|Description|
|----|-----------|
|Boolean|True if the supplied values satisfy the criteria, false otherwise.|

