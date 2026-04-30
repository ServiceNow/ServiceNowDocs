---
title: Configure return results data
description: Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint, you can configure what data is passed back in the return results.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - Android, Developer guides, API implementation and reference]
---

# Configure return results data

Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint, you can configure what data is passed back in the return results.

You configure what data to pass back using the [FetchConfiguration](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/FetchConfiguration/concept/FetchConfigAndroidAPI.md#) API. This interface enables you to configure:

-   The specific records to return from a table.
-   The specific fields to return from the records.
-   The number of records to return.

**Note:** Generally you want to use the same FetchConfiguration for all of your CRUD operations for a certain model type as it determines which fields are returned. It should at least match the required properties on your model, or else JSON Decoding will fail.

## Configuring the specific records to return

The [Filter](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) object within a FetchConfiguration call enables you to define the filter and sort requirements for the records that are fetched from a ServiceNow instance and passed back in the return results from a REST endpoint. This filter is passed in the **sysparm\_query** parameter of the REST API endpoint. For additional information, see [Table API](../../../../inbound-rest/concept/c_TableAPI.md#).

You can initialize the Filter object in two different ways depending on the desired filtering capabilities:

1.  Filter by criteria. This filter enables you to filter based on one or more filter criteria that are OR'd together.

    For example, a manager has an employee Abel Tuter who is on PTO. They want to know if there are active incidents that are not assigned to anyone or assigned to Abel Tuter so they can assign/reassign them. They also want to see in that same list, all of the incidents that have high or overdue escalation so that they can also address those. The following shows how to create the necessary filters to obtain this data:

    ```
    val activeIncidents = BooleanSimpleCondition.conditionIs("active", true)
    val assignedToEmpty = StringSimpleCondition.isEmpty("assigned_to")
    val assignedToAbel = StringSimpleCondition.conditionIs("assigned_to", "Abel Tuter")
    
    val assignedToAbelOrEmpty =
      CompoundCondition(
      ConditionUtils.CompoundOperator.OR,
      listOf(assignedToEmpty, assignedToAbel))
    
    val needToReassign = Criteria().addConditions(listOf(activeIncidents,  
      assignedToAbelOrEmpty))
    
    val highEscelations = StringSimpleCondition.conditionIs("escalation", "2")
    val overdueEscelations = StringSimpleCondition.conditionIs("escalation", "3")
    
    val highOrOverdueEscelations =
      CompoundCondition(ConditionUtils.CompoundOperator.OR,
        listOf(highEscelations, overdueEscelations))
    
    val needToHandleEscalation =
      Criteria().addCondition(highOrOverdueEscelations)
    
    val myPrioritiesForTodayFilter = Filter(listOf(needToReassign,
      needToHandleEscalation))
    
    // Get record using filter
    val response = runCatching {
      getNowTableService()?.records(
        "sn_customerservice_case",
        FetchConfiguration(myPrioritiesForTodayFilter, 10)
      )?.execute()
    }
    ```

    To use this type of filtering, use the [Filter\(criteriaList: List&lt;Criteria&gt;, sortBy: List&lt;Sort&gt;? = null\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/Filter/concept/FilterAndroidAPI.md#) function.

2.  Filter by keywords and conditions. This filter enables you to filter records based on specific keywords and conditions that can be AND'd or OR'd together.

    For example:

    ```
    val keywords = "iOS 13 | iOS 14"
    val conditionA = BooleanSimpleCondition.conditionIs(testField, true)
    val conditionB = BooleanSimpleCondition.conditionIs(testField2, false)
    val sortA = Sort(testField, ConditionUtils.SortOperator.ORDER_ASC)
    val filter = Filter(conditions = listOf(conditionA, conditionB), keywords = keywords, sortBy = listOf(sortA))
    assertEquals(filter.query().second, "${conditionA.makeConditionQuery()}^${conditionB.makeConditionQuery()}^123TEXTQUERY321=$keywords^EQ^${sortA.makeSortQuery()}")
    ```

    To use this type of filtering, use the [Filter - Filter\(conditions: List&lt;Condition&gt;, keywords: String? = null, sortBy: List&lt;Sort&gt;? = null\)](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/Filter/concept/FilterAndroidAPI.md#) function.


## Configuring the specific fields to return

The [FieldReadConfiguration](../../../../../app-store/dev_portal/API_reference/MobileSDKAndroid/FieldReadConfiguration/concept/FieldReadConfigAndroidAPI.md#) object within the FetchConfiguration\(\) method call allows you to configure what fields to pass back in the return results. In addition, you can configure the format/content of the returned fields as:

-   display values
-   actual values
-   exclude reference links

