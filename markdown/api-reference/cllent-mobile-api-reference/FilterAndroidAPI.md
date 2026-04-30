---
title: Filter API - Android
description: The Filter class provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.Creates a filter based on specific keywords and conditions that can be OR'd or AND'd together.Creates a filter based on one or more filter criteria that are OR'd together.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# Filter API - Android

The Filter class provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.

|Name|Type|Description|
|----|----|-----------|
|queryItems|Map&lt;String, String&gt;|Collection of query items representing the filter.|

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## Filter - Filter\(conditions: List&lt;Condition&gt;, keywords: String? = null, sortBy: List&lt;Sort&gt;? = null\)

Creates a filter based on specific keywords and conditions that can be OR'd or AND'd together.

<table id="table_yzp_jz2_4qb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conditions

</td><td>

List&lt;Condition&gt;

</td><td>

Simple or compound conditions to add to the query.Possible conditions:

-   BooleanSimpleCondition: Conditions available for boolean record fields.
-   DateSimpleTimeCondition: Conditions available for date-time record fields.
-   EmailSimpleCondition: Conditions available for email fields.
-   IntegerChoiceSimpleCondition: Conditions available for integer choice fields.
-   NumericSimpleCondition: Conditions available for various numeric fields.
-   ReferenceSimpleCondition: Condition operators available for reference record fields.
-   StringChoiceSimpleCondition: Condition operators available for choice record fields containing strings.
-   StringSimpleCondition: Condition operators available for string record fields.
-   CompoundCondition: Allows you to group SimpleConditions into a compound condition using ConditionUtils.CompoundOperator connectors.

</td></tr><tr><td>

keywords

</td><td>

String

</td><td>

Optional. Any specific word or phrase to search for.Default: nil - No specific word search.

</td></tr><tr><td>

sortBy

</td><td>

List&lt;Sort&gt;

</td><td>

Optional. List of record field names and the associated sort order constant to sort the returned records by. For example: `val sortBy = listOf("zipcode", ORDER_DESC)`If you include multiple sort fields, each subsequent field is a further sort of the prior field\(s\).

Valid sort values:

-   ORDER\_ASC: Sort ascending
-   ORDER\_DESC: Sort descending

Default: ORDER\_ASC

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Where the record is active 

val condition1 = BooleanSimpleCondition.conditionIs("active", true) 

// AND the date value of the SLA due field is on "today" or any date after today. 

val condition2 = DateSimpleTimeCondition.atOrAfter("sla_due", 0, ConditionUtils.DateTimeValueOperator.daysAgoStart) 

val filter = Filter(conditions = listOf(condition1, condition2))  
```

## Filter - Filter\(criteriaList: List&lt;Criteria&gt;, sortBy: List&lt;Sort&gt;? = null\)

Creates a filter based on one or more filter criteria that are OR'd together.

<table id="table_ebq_fbz_nqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

criteriaList

</td><td>

List&lt;Criteria&gt;

</td><td>

Top level criteria conditions to group with `OR` connectors.

</td></tr><tr><td>

sortBy

</td><td>

List&lt;Sort&gt;

</td><td>

Optional. List of record field names and the associated sort order constant to sort the returned records by. For example: `val sortBy = listOf("zipcode", ORDER_DESC)`If you include multiple sort fields, each subsequent field is a further sort of the prior field\(s\).

Valid sort values:

-   ORDER\_ASC: Sort ascending
-   ORDER\_DESC: Sort descending

Default: ORDER\_ASC

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
val activeIncidents = BooleanSimpleCondition.conditionIs("active", true)
val assignedToEmpty = StringSimpleCondition.isEmpty("assigned_to")
val assignedToAbel = StringSimpleCondition.conditionIs("assigned_to", "Abel Tuter")
val assignedToAbelOrEmpty = CompoundCondition(ConditionUtils.CompoundOperator.OR, listOf(assignedToEmpty, assignedToAbel))
val needToReassign = Criteria().addConditions(listOf(activeIncidents, assignedToAbelOrEmpty))
val highEscelations = StringSimpleCondition.conditionIs("escalation", "2")
val overdueEscelations = StringSimpleCondition.conditionIs("escalation", "3")
val highOrOverdueEscelations = CompoundCondition(ConditionUtils.CompoundOperator.OR, listOf(highEscelations, overdueEscelations))
val needToHandleEscalation = Criteria().addCondition(highOrOverdueEscelations)
val myPrioritiesForTodayFilter = Filter(listOf(needToReassign, needToHandleEscalation))
```

