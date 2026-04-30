---
title: Filter structure - iOS
description: The Filter structure provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.Creates a filter based on one or more filter criteria that are OR'd together.Creates a filter based on all specified conditions \(AND'd together\)Creates a filter using a specified encoded query.Creates a filter based on specific keywords and conditions that are AND'd together.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# Filter structure - iOS

The Filter structure provides the ability to configure filters that define the data to return in the return results of a REST endpoint query.

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## Filter - init\(criteria criteriaList: \[Criteria\], sortBy: \[Sort\]? = nil, queryCategory: String? = nil\)

Creates a filter based on one or more filter criteria that are OR'd together.

<table id="table_w5t_myg_kqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

criteria

</td><td>

Array

</td><td>

Top level criteria conditions to group with `OR` connectors.

</td></tr><tr><td>

sortBy

</td><td>

String

</td><td>

Optional. Sort order of the return results.Possible values:

-   asc: Ascending
-   desc: Desending

Default: asc

</td></tr><tr><td>

queryCategory

</td><td>

String

</td><td>

Optional. Name of the query category.Default: None

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows creating three separate criteria and when passed in, if any of those criteria are met, the record is passed back in the return results.

```
// All of criteria1 conditions must be met
let criteria1 = Criteria(conditions: …)

// OR all of criteria2 conditions must be met
let criteria2 = Criteria(conditions: …)

// OR all of criteria3 conditions must be met
let criteria3 = Criteria(conditions: …)

let filter = Filter(criterias: [criteria1, criteria2, criteria3])
```

## Filter - init\(conditions: \[QueryProviding\], sorts: \[Sort\]? = nil\)

Creates a filter based on all specified conditions \(AND'd together\)

<table id="table_w15_nch_kqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conditions

</td><td>

QueryProviding

</td><td>

Conditions to group with an `AND` connector.Possible values:

-   boolean
-   dateTime
-   email
-   integerChoice
-   numeric
-   reference
-   string
-   stringChoice

</td></tr><tr><td>

sorts

</td><td>

String

</td><td>

Optional. Sort order of the return results.Possible values:

-   asc: Ascending
-   desc: Desending

Default: asc

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
// Where the record is active
let condition1 = Condition.boolean(field: "active", .is(true))

// AND the date value of the SLA due field is on "today" or any date after today.
let condition2 = Condition.dateTime(field: "sla_due", .atOrAfter(0, .daysAgoStart))

let filter = Filter(conditions: [condition1, condition2])
```

## Filter - init\(query: String, queryCategory: String? = nil\)

Creates a filter using a specified encoded query.

|Name|Type|Description|
|----|----|-----------|
|query|String|[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)[Encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) to use to filter the records to return from the table.|
|queryCategory|String|Optional. Name of the query category to use for the query.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
let query = "active=true^short_descriptionLIKEbroken"
let filter = Filter(query: query)
```

## Filter - init\(keywords: String? = nil, conditions: \[Condition\], sortBy: \[Sort\]? = nil\)

Creates a filter based on specific keywords and conditions that are AND'd together.

<table id="table_ltk_k1h_kqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

keywords

</td><td>

String

</td><td>

Optional. Any specific word or phrase to search for.Default: nil - No specific word search.

</td></tr><tr><td>

conditions

</td><td>

String

</td><td>

Conditions to group with an `AND` connector.Possible values:

-   boolean
-   dateTime
-   email
-   integerChoice
-   numeric
-   reference
-   string
-   stringChoice

</td></tr><tr><td>

sortBy

</td><td>

String

</td><td>

Optional. Sort order of the return results.Possible values:

-   asc: Ascending
-   desc: Desending

Default: asc

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
// Keyword that must be found in the record
let searchTerm = "…"

// AND the specified condition must be met
let condition1 = Condition.email(field: "state", .changesFrom("4"))

let filter = Filter(keywords: searchTerm, condition: condition1)
```

