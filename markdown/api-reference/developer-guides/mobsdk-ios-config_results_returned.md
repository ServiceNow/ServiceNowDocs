---
title: Configure return results data
description: Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint, you can configure what data is passed back in the return results.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Interact with table data in a ServiceNow instance, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Configure return results data

Within the Mobile SDK, when interacting with data from a ServiceNow instance through a REST endpoint, you can configure what data is passed back in the return results.

You configure what data to pass back using the [FetchConfiguration](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/FetchConfiguration/concept/FetchConfigiOSStructure.md#) structure. This structure enables you to configure:

-   The specific records to return from a table.
-   The specific fields to return from the records.
-   The number of records to return.

**Note:** Generally you want to use the same FetchConfiguration for all of your CRUD operations for a certain model type as it determines which fields are returned. It should at least match the required properties on your model, or else JSON Decoding will fail.

## Configuring the specific records to return

The [Filter](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) structure within a FetchConfiguration call enables you to filter and sort the records that are fetched from a ServiceNow instance and passed back in the return results from a REST endpoint. This filter is passed in the **sysparm\_query** parameter of the REST API endpoint. For additional information, see [Table API](../../../../inbound-rest/concept/c_TableAPI.md#).

You can initialize the Filter structure in four different ways depending on the desired filtering capabilities:

1.  Filter by [encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)[encoded query](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US). This type of filter enables you to pass an encoded query that is applied to the records within the specified table.

    For example, the following call only returns those records that are active and whose short description field contains the word "broken":

    ```
    Filter(query: "active=true^short_descriptionLIKEbroken"
    ```

    To use this type of filtering, initialize the Filter structure using the [Filter - init\(query: String, queryCategory: String? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) function.

2.  Filter by criteria. This filter enables you to filter based on one or more filter criteria that are OR'd together.

    For example, a manager has an employee Abel Tuter who is on PTO. They want to know if there are active incidents that are not assigned to anyone or assigned to Abel Tuter so they can assign/reassign them. They also want to see in that same list, all of the incidents that have high or overdue escalation so that they can also address those. The following shows how to create the necessary filters to obtain this data:

    ```
    let activeIncidents = Condition.boolean(field: "active", .is(true))
    
    let assignedToEmpty = Condition.string(field: "assigned_to", .isEmpty) 
    
    let assignedToAbel = Condition.string(field: "assigned_to", .is("Abel Tuter")) 
    
    let assignedToAbelOrEmpty = CompoundCondition.or([assignedToEmpty, assignedToAbel]) 
    
    let needToReassign = Criteria(conditions: [activeIncidents, assignedToAbelOrEmpty])
    
    let highEscelations = Condition.string(field: "escalation", .is("2"))
    
    let overdueEscelations = Condition.string(field: "escalation", .is("3"))
    
    let highORoverdueEscelations = CompoundCondition.or([highEscelations, overdueEscelations]) 
    
    let needToHandleEscalation = Criteria(condition: highOrOverdueEscelations) 
    
    let myPrioritiesForTodayFilter = Filter(criteria: [needToReassign, needToHandleEscalation])
    
    
    ```

    To use this type of filtering, initialize the Filter structure using the [Filter - init\(criteria criteriaList: \[Criteria\], sortBy: \[Sort\]? = nil, queryCategory: String? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) function.

3.  Filter by keywords and conditions. This filter enables you to filter records based on specific keywords and conditions that are AND'd together.

    For example, the following filters for all records that contain the keyword "iOS13 or iOS 14" and meet the specified condition sorted by testField.

    ```
    testKeywordsAndConditionsAndSort() {
      let keywords = "iOS 13 | iOS 14"
      let conditionA = Condition.boolean(field: testField, .is(true))
      let conditionB = Condition.boolean(field: testField2, .is(false))
      let sortA = Sort.asc(testField)
      let filter = Filter(keywords: keywords, conditions: [conditionA, conditionB], sortBy: [sortA])
      
      XCTAssertEqual(filter.query, "123TEXTQUERY321=\(keywords)^\(conditionA.query)^\(conditionB.query)^EQ^\(sortA.query)")
    }
    ```

    To use this type of filtering, initialize the Filter structure using the [Filter - init\(keywords: String? = nil, conditions: \[Condition\], sortBy: \[Sort\]? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) function.

4.  Filter by conditions. This filter enables you to filter records that meet all specified conditions \(AND'd together\).

    For example, the following filters for all records in which the Active field is "true" and the date value of the SLA due field is on "today" or any date after today.

    ```
    // Where the record is active
    let condition1 = Condition.boolean(field: "active", .is(true))
    
    // AND the date value of the SLA due field is on "today" or any date after today.
    let condition2 = Condition.dateTime(field: "sla_due", .atOrAfter(0, .daysAgoStart))
    
    let filter = Filter(conditions: [condition1, condition2])
    ```

    To use this type of filtering, initialize the Filter structure using the [Filter - init\(conditions: \[QueryProviding\], sorts: \[Sort\]? = nil\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/Filter/concept/FilteriOSStructure.md#) function.


## Configuring the specific fields to return

The [FieldReadConfiguration structure - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/FieldReadConfiguration/concept/FieldReadConfigurationiOSStruct.md#) within the FetchConfiguration method call allows you to configure what fields to pass back in the return results. In addition, you can configure the format/content of the returned fields as:

-   display values
-   actual values
-   exclude reference links

**Note:** Configuring the fields to match a Codable model may reduce the payload returned by the ServiceNow instance, improving network efficiency by reducing data transfer.

