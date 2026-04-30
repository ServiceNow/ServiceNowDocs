---
title: Work Order Management API
description: The Work Order Management API provides endpoints to create, update, and retrieve work orders.Retrieves a specified work order from the Work Order \[wm\_order\] table.Retrieves a list of all work orders from the Work Order \[wm\_order\] table.Updates a work order and associated tasks.Cancels a specified work order and all associated tasks.Creates a work order and associated tasks.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 52
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Work Order Management API

The Work Order Management API provides endpoints to create, update, and retrieve work orders.

This API is included in the Telecommunication Open APIs application, which is available on the ServiceNow Store.

This API is provided within the `sn_tmf_api` namespace.

The calling user must have the sn\_tmf\_api.work\_order\_integrator role.

The Work Order Management API is a ServiceNow implementation of the TM Forum Work Order Management API REST specification. This implementation is based on the [TMF697 Work Order Management API v5.0](https://www.tmforum.org/oda/open-apis/directory/work-order-management-api-TMF697/v5.0.0).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Work Order Management - GET /sn\_tmf\_api/work\_order\_management\_api/workorder/\{id\}

Retrieves a specified work order from the Work Order \[wm\_order\] table.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/work_order_management_api/workorder/{id}`

Default URL: `/api/sn_tmf_api/work_order_management_api/workorder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or **externalIdentifier** of the work order.Table: Work Order \[wm\_order\]

Field: Sys\_id or correlation\_id

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid values:

-   @type
-   category
-   completionDate
-   description
-   expectedCompletionDate
-   href
-   id
-   initiatedFrom
-   priority
-   requestedCompletionDate
-   requestedStartDate
-   shortDescription
-   startDate
-   state
-   workOrderNumber

Default: Returns all fields.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table id="table_cdw_gk3_bgc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

category

</td><td>

Category for the work order that can be used by an order management system, such as `enterprise` or `residential`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "author": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

Author of the note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the note was added to the work order.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedProductOrder

</td><td>

List of product orders for the work order.Data type: Array

```
"relatedProductOrder": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

relatedProductOrder.@type

</td><td>

This value is always `ProductOrderRef`.Data type: String

</td></tr><tr><td>

relatedProductOrder.id

</td><td>

Sys\_id of the product order.Table: Product Order \[sn\_ind\_tmt\_orm\_product\_order\]

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "description": "String",
      "id": "String",
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "relatedWork": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedWork

</td><td>

List of related work order tasks. Data type: Array

```
"relatedWork": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedWork.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedWork.id

</td><td>

Sys\_id of the related task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr><tr><td>

workOrderRelationship

</td><td>

List of task relationships to the work order.Data type: Array

```
"workOrderRelationship": [
   {
      "@type": "String",
      "id": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

workOrderRelationship.@type

</td><td>

This value is always `OrderRelationship`.Data type: String

</td></tr><tr><td>

workOrderRelationship.id

</td><td>

Sys\_id of the task relationship.Table: Task Relationship \[task\_rel\_task\]

Data type: String

</td></tr><tr><td>

workOrderRelationship.relationshipType

</td><td>

Task relationship type.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieves the specified work order.

```
curl "https://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/workorder/27e756a1df113100dca6a5f59bf263da" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
   "@type": "WorkOrder",
   "href": "api/sn_tmf_api/workordermanagement/workorder/6d22c6f0ff0de650f8dfffffffffff98",
   "workOrderNumber": "WO0008004",
   "id": "6d22c6f0ff0de650f8dfffffffffff98",
   "category": "test",
   "shortDescription": "Test-Test",
   "description": "Test",
   "startDate": "",
   "requestedCompletionDate": "2025-04-19 07:17:04",
   "requestedStartDate": "",
   "state": "Awaiting Qualification",
   "priority": "4 - Low",
   "initiatedFrom": "",
   "completionDate": "",
   "expectedCompletionDate": "",
   "place": {
      "@type": "GeographicSite",
      "id": "920cf6ac73d423002728660c4cf6a799",
      "relatedParty": [
         {
            "@type": "RelatedPartyRef",
            "id": "320ee92637232000158bbfc8bcbe5d40",
            "name": "East Qualifiers",
            "role": "QualificationGroup"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "5408091a3b100300e81d47b334efc452",
         "name": "Ashley Parker",
         "role": "Contact"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "",
         "name": "",
         "role": "Account"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "",
         "name": "",
         "role": "Consumer"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "820351a1c0a8018b67c73d51c074097c",
         "name": "Acer",
         "role": "Company"
      }
   ],
   "appointment": {},
   "relatedProductOrder": [
      {
         "@type": "ProductOrderRef",
         "id": "19f5456dff092a50f8dfffffffffff01"
      },
      {
         "@type": "ProductOrderRef",
         "id": "7116456dff092a50f8dfffffffffff6e"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifierRef",
         "id": "r6879"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "id": "2fa566fdff456a50f8dfffffffffffc6",
         "shortDescription": "abc",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "2fa566fdff456a50f8dfffffffffffc6",
            "workType": "",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "25ab8dcd0a0a0bb300bd8a8899934d72"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "bb420af0ff0de650f8dfffffffffff4a"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "c301e379ff096a50f8dfffffffffff43"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      },
      {
         "@type": "WorkOrderItem",
         "id": "bb420af0ff0de650f8dfffffffffff4a",
         "shortDescription": "Test",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "bb420af0ff0de650f8dfffffffffff4a",
            "workType": "38f719ec3b8a10103f09080044efc4cd",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "920cf6ac73d423002728660c4cf6a799"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "2fa566fdff456a50f8dfffffffffffc6"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "c301e379ff096a50f8dfffffffffff43"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      },
      {
         "@type": "WorkOrderItem",
         "id": "c301e379ff096a50f8dfffffffffff43",
         "shortDescription": "hi",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "c301e379ff096a50f8dfffffffffff43",
            "workType": "",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "6808184aeb211100420124e05206fe12"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "2fa566fdff456a50f8dfffffffffffc6"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "bb420af0ff0de650f8dfffffffffff4a"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      }
   ],
   "workOrderRelationship": [
      {
         "@type": "OrderRelationship",
         "id": "02016b46ffcd6a50f8dfffffffffff31",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "0e016b46ffcd6a50f8dfffffffffff30",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "66da174eff8d6a50f8dfffffffffffda",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "aada174eff8d6a50f8dfffffffffffd9",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "bd20e706ffcd6a50f8dfffffffffffc6",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "c2016b46ffcd6a50f8dfffffffffff31",
         "relationshipType": "Contains::Task of"
      }
   ],
   "note": [
      {
         "@type": "Note",
         "author": "System Administrator",
         "date": "2025-04-23",
         "text": "This is a note."
      }
   ]
}
```

## Work Order Management - GET /sn\_tmf\_api/work\_order\_management\_api/workordermanagement

Retrieves a list of all work orders from the Work Order \[wm\_order\] table.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/work_order_management_api/workordermanagement`

Default URL: `/api/sn_tmf_api/work_order_management_api/workordermanagement`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid values:

-   @type
-   category
-   completionDate
-   description
-   expectedCompletionDate
-   href
-   id
-   initiatedFrom
-   priority
-   requestedCompletionDate
-   requestedStartDate
-   shortDescription
-   startDate
-   state
-   workOrderNumber

Default: Returns all fields.

Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_ids to use to filter work orders. Only work orders matching the specified sys\_ids are returned in the response.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Default: 20

Data type: Number

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Default: 0

Data type: Number

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

<table id="table_lpj_dh1_vxb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr><td>

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|206|Partial content. The request was successfully processed and returned a partial range of content specified by a paginated call.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

category

</td><td>

Category for the work order that can be used by an order management system, such as `enterprise` or `residential`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "author": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.author

</td><td>

Author of the note.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the note was added to the work order.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

relatedProductOrder

</td><td>

List of product orders for the work order.Data type: Array

```
"relatedProductOrder": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

relatedProductOrder.@type

</td><td>

This value is always `ProductOrderRef`.Data type: String

</td></tr><tr><td>

relatedProductOrder.id

</td><td>

Sys\_id of the product order.Table: Product Order \[sn\_ind\_tmt\_orm\_product\_order\]

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "description": "String",
      "id": "String",
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "relatedWork": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedWork

</td><td>

List of related work order tasks. Data type: Array

```
"relatedWork": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedWork.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedWork.id

</td><td>

Sys\_id of the related task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr><tr><td>

workOrderRelationship

</td><td>

List of task relationships to the work order.Data type: Array

```
"workOrderRelationship": [
   {
      "@type": "String",
      "id": "String",
      "relationshipType": "String"
   }
]
```

</td></tr><tr><td>

workOrderRelationship.@type

</td><td>

This value is always `OrderRelationship`.Data type: String

</td></tr><tr><td>

workOrderRelationship.id

</td><td>

Sys\_id of the task relationship.Table: Task Relationship \[task\_rel\_task\]

Data type: String

</td></tr><tr><td>

workOrderRelationship.relationshipType

</td><td>

Task relationship type.Data type: String

</td></tr></tbody>
</table>### cURL request

Retrieves the first page of work orders.

```
curl "https://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/workordermanagement" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
[{
   "@type": "WorkOrder",
   "href": "api/sn_tmf_api/workordermanagement/workorder/6d22c6f0ff0de650f8dfffffffffff98",
   "workOrderNumber": "WO0008004",
   "id": "6d22c6f0ff0de650f8dfffffffffff98",
   "category": "test",
   "shortDescription": "Test-Test",
   "description": "Test",
   "startDate": "",
   "requestedCompletionDate": "2025-04-19 07:17:04",
   "requestedStartDate": "",
   "state": "Awaiting Qualification",
   "priority": "4 - Low",
   "initiatedFrom": "",
   "completionDate": "",
   "expectedCompletionDate": "",
   "place": {
      "@type": "GeographicSite",
      "id": "920cf6ac73d423002728660c4cf6a799",
      "relatedParty": [
         {
            "@type": "RelatedPartyRef",
            "id": "320ee92637232000158bbfc8bcbe5d40",
            "name": "East Qualifiers",
            "role": "QualificationGroup"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "5408091a3b100300e81d47b334efc452",
         "name": "Ashley Parker",
         "role": "Contact"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "",
         "name": "",
         "role": "Account"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "",
         "name": "",
         "role": "Consumer"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "820351a1c0a8018b67c73d51c074097c",
         "name": "Acer",
         "role": "Company"
      }
   ],
   "appointment": {},
   "relatedProductOrder": [
      {
         "@type": "ProductOrderRef",
         "id": "19f5456dff092a50f8dfffffffffff01"
      },
      {
         "@type": "ProductOrderRef",
         "id": "7116456dff092a50f8dfffffffffff6e"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifierRef",
         "id": "r6879"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "id": "2fa566fdff456a50f8dfffffffffffc6",
         "shortDescription": "abc",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "2fa566fdff456a50f8dfffffffffffc6",
            "workType": "",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "25ab8dcd0a0a0bb300bd8a8899934d72"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "bb420af0ff0de650f8dfffffffffff4a"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "c301e379ff096a50f8dfffffffffff43"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      },
      {
         "@type": "WorkOrderItem",
         "id": "bb420af0ff0de650f8dfffffffffff4a",
         "shortDescription": "Test",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "bb420af0ff0de650f8dfffffffffff4a",
            "workType": "38f719ec3b8a10103f09080044efc4cd",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "920cf6ac73d423002728660c4cf6a799"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "2fa566fdff456a50f8dfffffffffffc6"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "c301e379ff096a50f8dfffffffffff43"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      },
      {
         "@type": "WorkOrderItem",
         "id": "c301e379ff096a50f8dfffffffffff43",
         "shortDescription": "hi",
         "description": "",
         "state": "Draft",
         "work": {
            "@type": "WorkRefOrValue",
            "id": "c301e379ff096a50f8dfffffffffff43",
            "workType": "",
            "scheduledStartDate": "",
            "expectedCompletionDate": "",
            "workPriority": "4 - Low",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "6808184aeb211100420124e05206fe12"
                  }
               }
            ],
            "relatedWork": [
               {
                  "@type": "WorkRefOrValue",
                  "id": "2fa566fdff456a50f8dfffffffffffc6"
               },
               {
                  "@type": "WorkRefOrValue",
                  "id": "bb420af0ff0de650f8dfffffffffff4a"
               }
            ],
            "relatedParty": [],
            "workforceEmployeeAssignment": []
         }
      }
   ],
   "workOrderRelationship": [
      {
         "@type": "OrderRelationship",
         "id": "02016b46ffcd6a50f8dfffffffffff31",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "0e016b46ffcd6a50f8dfffffffffff30",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "66da174eff8d6a50f8dfffffffffffda",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "aada174eff8d6a50f8dfffffffffffd9",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "bd20e706ffcd6a50f8dfffffffffffc6",
         "relationshipType": "Contains::Task of"
      },
      {
         "@type": "OrderRelationship",
         "id": "c2016b46ffcd6a50f8dfffffffffff31",
         "relationshipType": "Contains::Task of"
      }
   ],
   "note": [
      {
         "@type": "Note",
         "author": "System Administrator",
         "date": "2025-04-23",
         "text": "This is a note."
      }
   ]
}]
```

## Work Order Management - PATCH /sn\_tmf\_api/work\_order\_management\_api/workOrder/\{id\}

Updates a work order and associated tasks.

The work order record is updated in the Work Order \[wm\_order\] table. Task records are updated in the Work Order Task \[wm\_task\] table.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/work_order_management_api/workOrder/{id}`

Default URL: `/api/sn_tmf_api/work_order_management_api/workOrder/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Sys\_id of the template to use for the work order.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "action": "String",
      "completionDate": "String",
      "description": "String",
      "id": "String",
      "note": {Object},
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.action

</td><td>

Action to perform on the product for the task. Possible values:

-   add
-   delete
-   modify
-   noChange

Data type: String

</td></tr><tr><td>

workOrderItem.completionDate

</td><td>

Date and time the task was completed.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.note

</td><td>

List of notes about the task.Data type: Array

```
"note": [
   {
      "@type": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

workOrderItem.note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Sys\_id of the template to use for the work order.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "action": "String",
      "completionDate": "String",
      "description": "String",
      "id": "String",
      "note": {Object},
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.action

</td><td>

Action to perform on the product for the task. Possible values:

-   add
-   delete
-   modify
-   noChange

Data type: String

</td></tr><tr><td>

workOrderItem.completionDate

</td><td>

Date and time the task was completed.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.note

</td><td>

List of notes about the task.Data type: Array

```
"note": [
   {
      "@type": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

workOrderItem.note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr></tbody>
</table>### cURL request

Updates the specified work order.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/workOrder/2d3f32f0df113100dca6a5f59bf263a9" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "@type": "WorkOrder",
   "description": "Fixed Fibre Broadband Installation",
   "shortDescription": "Fixed Fibre",
   "priority": "1 - Critical",
   "place": {
      "@type": "GeographicSite",
      "id": "f48b22530a0a0ba70001913a1c181eeb",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "781da52637232000158bbfc8bcbe5db8",
            "name": "Jane Smith",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "86a08090ffcd62105e0dffffffffff8b",
         "name": "Workforce Engineering Group",
         "role": "Consumer"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "id": "3df59e8cff5d26105e0dffffffffff0e",
         "action": "add",
         "description": "FTTH Installation",
         "shortDescription": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "state": "Accepted",
         "work": {
            "@type": "WorkRefOrValue",
            "scheduledStartDate": "2024-04-22T14:23:06.528Z",
            "workType": "38f719ec3b8a10103f09080044efc4cd",
            "description": "Cabinet Configuration",
            "name": "FTTH Installation",
            "workPriority": "high",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "b04b813bffc126105e0dffffffffff0d"
                  }
               }
            ],
            "note": {
               "@type": "Note",
               "text": "Demand Point Type: SDU"
            }
         }
      }
   ],
   "note": {
      "@type": "Note",
      "text": "This is important"
   }
}" \
--user 'username':'password'
```

Response body.

```
{
   "@type": "WorkOrder",
   "description": "Fixed Fibre Broadband Installation",
   "shortDescription": "Fixed Fibre",
   "priority": "1 - Critical",
   "place": {
      "@type": "GeographicSite",
      "id": "f48b22530a0a0ba70001913a1c181eeb",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "781da52637232000158bbfc8bcbe5db8",
            "name": "Jane Smith",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "86a08090ffcd62105e0dffffffffff8b",
         "name": "Workforce Engineering Group",
         "role": "Consumer"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "id": "3df59e8cff5d26105e0dffffffffff0e",
         "action": "add",
         "description": "FTTH Installation",
         "shortDescription": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "state": "Accepted",
         "work": {
            "@type": "WorkRefOrValue",
            "scheduledStartDate": "2024-04-22T14:23:06.528Z",
            "workType": "38f719ec3b8a10103f09080044efc4cd",
            "description": "Cabinet Configuration",
            "name": "FTTH Installation",
            "workPriority": "high",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "b04b813bffc126105e0dffffffffff0d"
                  }
               }
            ],
            "note": {
               "@type": "Note",
               "text": "Demand Point Type: SDU"
            }
         }
      }
   ],
   "note": {
      "@type": "Note",
      "text": "This is important"
   },
   "id": "2d3f32f0df113100dca6a5f59bf263a9",
   "href": "/api/sn_tmf_api/work_order_management_api/workOrder/2d3f32f0df113100dca6a5f59bf263a9"
}
```

## Work Order Management - POST /sn\_tmf\_api/work\_order\_management\_api/cancelWorkOrder

Cancels a specified work order and all associated tasks.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/work_order_management_api/cancelWorkOrder`

Default URL: `/api/sn_tmf_api/work_order_management_api/cancelWorkOrder`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `CancelWorkOrder`.Data type: String

</td></tr><tr><td>

cancellationReason

</td><td>

Reason for canceling the work order.Data type: String

</td></tr><tr><td>

workOrder

</td><td>

Details about the work order.Data type: Object

```
"workOrder": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrder.@type

</td><td>

This value is always `WorkOrderRef`.Data type: String

</td></tr><tr><td>

workOrder.id

</td><td>

Required. Sys\_id of the work order to cancel.Table: Work Order \[wm\_order\]

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `CancelWorkOrder`.Data type: String

</td></tr><tr><td>

cancellationReason

</td><td>

Reason for canceling the work order.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the cancellation request. If the work order was successfully canceled, this value is `Cancelled`.Data type: String

</td></tr><tr><td>

workOrder

</td><td>

Details about the work order.Data type: Object

```
"workOrder": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrder.@type

</td><td>

This value is always `WorkOrderRef`.Data type: String

</td></tr><tr><td>

workOrder.id

</td><td>

Sys\_id of the canceled work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr></tbody>
</table>### cURL request

Cancels the specified work order.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/cancelWorkOrder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "@type": "CancelWorkOrder",
   "cancellationReason": "Workforce unavailability",
   "workOrder": {
      "@type": "WorkOrderRef",
      "id": "f8ec1c38-4e4d-4378-a693-f95680e51e25"
   }
}" \
--user 'username':'password'
```

Response body.

```
{
  "@type": "CancelWorkOrder",
  "cancellationReason": "Workforce unavailability",
  "state": "Cancelled",
  "workOrder": {
    "@type": "WorkOrderRef",
    "id": "f8ec1c38-4e4d-4378-a693-f95680e51e25"
  }
}
```

## Work Order Management - POST /sn\_tmf\_api/work\_order\_management\_api/workOrder

Creates a work order and associated tasks.

A record for the work order is created in the Work Order \[wm\_order\] table. A record for each task is created in the Work Order Task \[wm\_task\] table.

### URL format

Versioned URL: `/api/sn_tmf_api/{api_version}/work_order_management_api/workOrder`

Default URL: `/api/sn_tmf_api/work_order_management_api/workOrder`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

category

</td><td>

Category for the work order that can be used by an order management system, such as `enterprise` or `residential`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the note was added to the work order.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Sys\_id of the template to use for the work order.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "action": "String",
      "completionDate": "String",
      "description": "String",
      "id": "String",
      "note": {Object},
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.action

</td><td>

Action to perform on the product for the task. Possible values:

-   add
-   delete
-   modify
-   noChange

Data type: String

</td></tr><tr><td>

workOrderItem.completionDate

</td><td>

Date and time the task was completed.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.note

</td><td>

List of notes about the task.Data type: Array

```
"note": [
   {
      "@type": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

workOrderItem.note.date

</td><td>

Date the note was added to the task.Data type: String

</td></tr><tr><td>

workOrderItem.note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Created. The work order was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@type

</td><td>

This value is always `WorkOrder`.Data type: String

</td></tr><tr><td>

category

</td><td>

Category for the work order that can be used by an order management system, such as `enterprise` or `residential`.Data type: String

</td></tr><tr><td>

completionDate

</td><td>

Date and time the work order was completed.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the work order.Data type: String

</td></tr><tr><td>

expectedCompletionDate

</td><td>

Expected completion date and time designated by the provider.Data type: String

</td></tr><tr><td>

externalIdentifier

</td><td>

List of external references such as vendor or correlation ID.Data type: Array

```
"externalIdentifier": [
   {
      "@type": "String",
      "id": "String"
   }
]
```

</td></tr><tr><td>

externalIdentifier.@type

</td><td>

This value is always `ExternalIdentifierRef`.Data type: String

</td></tr><tr><td>

externalIdentifier.id

</td><td>

External reference such as vendor or correlation ID.Data type: String

</td></tr><tr><td>

href

</td><td>

Relative link to the work order record.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id of the work order.Table: Work Order \[wm\_order\]

Data type: String

</td></tr><tr><td>

initiatedFrom

</td><td>

Reference id indicating where the work order was initiated. For example, a task sys\_id from the Work Order Task \[wm\_task\] table.Data type: String

</td></tr><tr><td>

note

</td><td>

List of notes about the order.Data type: Array

```
"note": [
   {
      "@type": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

note.date

</td><td>

Date the note was added to the work order.Data type: String

</td></tr><tr><td>

note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

place

</td><td>

The geographic location associated with the work order.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String",
   "relatedParty": [Array]
}
```

</td></tr><tr><td>

place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

place.relatedParty

</td><td>

List of support groups for the location.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

place.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

place.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

place.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

place.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority ranking for the work order.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

relatedParty

</td><td>

List of associated contacts for the work order.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

relatedParty.id

</td><td>

Sys\_id of the related party.Table: Account \[customer\_account\], Company \[core\_company\], or User \[sys\_user\]

Data type: String

</td></tr><tr><td>

relatedParty.name

</td><td>

Name of the related party.Data type: String

</td></tr><tr><td>

relatedParty.role

</td><td>

Role of the related party.Possible values:

-   Account
-   Company
-   Consumer
-   Contact

Data type: String

</td></tr><tr><td>

requestedCompletionDate

</td><td>

Requested completion date and time.Data type: String

</td></tr><tr><td>

requestedStartDate

</td><td>

Order fulfillment start date designated by the requester. Used in cases where the requester can't allow the provider to begin fulfillment before a specified date.Data type: String

</td></tr><tr><td>

shortDescription

</td><td>

Brief summary of the work order.Data type: String

</td></tr><tr><td>

startDate

</td><td>

Date and time when the order started.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the work order. Possible values:

-   Draft
-   Awaiting qualification
-   Qualified
-   Assigned
-   Work in progress
-   Complete

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Sys\_id of the template to use for the work order.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

workOrderItem

</td><td>

List of tasks under the work order.Data type: Array

```
"workOrderItem": [
   {
      "@type": "String",
      "action": "String",
      "completionDate": "String",
      "description": "String",
      "id": "String",
      "note": {Object},
      "shortDescription": "String",
      "state": "String",
      "work": {Object}
   }
]
```

</td></tr><tr><td>

workOrderItem.@type

</td><td>

This value is always `WorkOrderItem`.Data type: String

</td></tr><tr><td>

workOrderItem.action

</td><td>

Action to perform on the product for the task. Possible values:

-   add
-   delete
-   modify
-   noChange

Data type: String

</td></tr><tr><td>

workOrderItem.completionDate

</td><td>

Date and time the task was completed.Data type: String

</td></tr><tr><td>

workOrderItem.description

</td><td>

Description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.id

</td><td>

Sys\_id of the task.Table: Work Order Task \[wm\_task\]

Data type: String

</td></tr><tr><td>

workOrderItem.note

</td><td>

List of notes about the task.Data type: Array

```
"note": [
   {
      "@type": "String",
      "date": "String",
      "text": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.note.@type

</td><td>

This value is always `Note`.Data type: String

</td></tr><tr><td>

workOrderItem.note.date

</td><td>

Date the note was added to the task.Data type: String

</td></tr><tr><td>

workOrderItem.note.text

</td><td>

The note text.Data type: String

</td></tr><tr><td>

workOrderItem.shortDescription

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

workOrderItem.state

</td><td>

State of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work

</td><td>

Description of the work required for the task.Data type: Object

```
"work": {
   "@type": "String",
   "expectedCompletionDate": "String",
   "id": "String",
   "place": [Array],
   "relatedParty": [Array],
   "scheduledStartDate": "String",
   "workforceEmployeeAssignment": [Array],
   "workPriority": "String",
   "workType": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.@type

</td><td>

This value is always `WorkRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.expectedCompletionDate

</td><td>

Expected completion date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.id

</td><td>

Sys\_id of the work type for the task.Table: Work Type \[wm\_work\_type\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place

</td><td>

List of geographic locations associated with the task.```
"place": [
   {
      "@type": "String",
      "place": {Object},
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.place.@type

</td><td>

This value is always `RelatedPlaceRefOrValue`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place

</td><td>

Details about the location.Data type: Object

```
"place": {
   "@type": "String",
   "id": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.place.place.@type

</td><td>

This value is always `GeographicSite`.Data type: String

</td></tr><tr><td>

workOrderItem.work.place.place.id

</td><td>

Sys\_id of the location.Table: Location \[cmn\_location\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.place.role

</td><td>

Role of this location in the context of the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty

</td><td>

List of support groups for the task.Data type: Array

```
"relatedParty": [
   {
      "@type": "String",
      "id": "String",
      "name": "String",
      "role": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.relatedParty.@type

</td><td>

This value is always `RelatedPartyRef`.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.id

</td><td>

Sys\_id of the support group.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.name

</td><td>

Name of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.relatedParty.role

</td><td>

Role of the support group.Data type: String

</td></tr><tr><td>

workOrderItem.work.scheduledStartDate

</td><td>

Scheduled start date for the task.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment

</td><td>

Assignment details for the task.Data type: Array

```
"workforceEmployeeAssignment": [
   {
      "@type":"String",
      "id": "String",
      "workforceEmployee": {Object}      
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.@type

</td><td>

This value is always `WorkforceEmployeeAssignment`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.id

</td><td>

Sys\_id of the group assigned to the task.Table: Group \[sys\_user\_group\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee

</td><td>

Details about the employee assigned to the task.Data type: Object

```
"workforceEmployee": {
   "@type": "String",
   "contactMedium": [Array],
   "id": "String",
   "name": "String"
}
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.@type

</td><td>

This value is always `Individual`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium

</td><td>

List of the employee's phone numbers.Data type: Array

```
"contactMedium": [
   {
      "@type": "String",
      "phoneNumber": "String"
   }
]
```

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.@type

</td><td>

This value is always `PhoneContactMedium`.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.contactMedium.phoneNumber

</td><td>

Phone number for the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.id

</td><td>

Sys\_id of the employee.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

workOrderItem.work.workforceEmployeeAssignment.workforceEmployee.name

</td><td>

Name of the employee.Data type: String

</td></tr><tr><td>

workOrderItem.work.workPriority

</td><td>

Priority ranking for the task.Possible values:

-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

Data type: String

</td></tr><tr><td>

workOrderItem.work.workType

</td><td>

The work type for the task.Table: Work Type \[wm\_work\_type\]

Field: Name

Data type: String

</td></tr><tr><td>

workOrderNumber

</td><td>

Unique identifier for the work order, such as WO0008004.Table: Work Order \[wm\_order\]

Field: Number

Data type: String

</td></tr></tbody>
</table>### cURL request

Creates a work order and task using a template.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/workOrder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "id": "323",
   "@type": "WorkOrder",
   "category": "service",
   "shortDescription": "Fixed Fibre Broadband Installation sb",
   "description": "Fixed Fibre description",
   "startDate": "2025-07-22T14:23:06.528Z",
   "requestedCompletionDate": "2024-06-22T14:23:06.528Z",
   "requestedStartDate": "2024-06-22T14:23:06.528Z",
   "priority": "2 - High",
   "expectedCompletionDate": "2025-07-28T14:23:06.528Z",
   "initiatedFrom": "d090df34df113100dca6a5f59bf26335",
   "templateId": "191ba0e0df113100dca6a5f59bf26336",
   "place": {
      "@type": "GeographicSite",
      "id": "423e85f037d0200044e0bfc8bcbe5d12",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "539546b237232000158bfc8bcbe5d7",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "d79249762fc1a610b79db3bf42faf3d2",
         "name": "Workforce Engineering Group",
         "role": "Company"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "b88d14843bc02300bfe04d72f3efc4cd",
         "name": "Workforce Engineering Group",
         "role": "Contact"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifier",
         "id": "1223412"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "action": "add",
         "id": "12232332",
         "description": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "work": {
            "@type": "WorkRefOrValue",
            "workType": "999469283bca10103f09080044efc4cf",
            "orderDate": "2024-04-22 14:23:06.528",
            "scheduledStartDate": "2025-06-25 14:23:06.528",
            "expectedCompletionDate": "2025-08-22 14:23:06.528",
            "workPriority": "2 - High",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "16ff753837d0200044e0bfc8bcbe5d5f"
                  }
               }
            ],
            "relatedParty": [
               {
                  "@type": "RelatedPartyRef",
                  "id": "4c0482b237232000158bbfc8bcbe5d09",
                  "name": "Louisiana Dispatchers",
                  "role": "DispatchGroup"
               }
            ],
            "workforceEmployeeAssignment": [
               {
                  "@type": "WorkforceEmployeeAssignment",
                  "id": "7172ea0037332000158bbfc8bcbe5db6",
                  "workforceEmployee": {
                     "@type": "Individual",
                     "name": "Athelstan Amos",
                     "id": "46c1293aa9fe1981000dc753e75ebeee"
                  }
               }
            ]
         },
         "note": {
            "@type": "Note",
            "id": "afa9-3d90aaa8da0f",
            "text": "This is a work order task note."
         }
      }
   ],
   "note": {
      "@type": "Note",
      "id": "afa9-3d90aaa8da0f",
      "text": "This is a work order note."
   }
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "ca6d72d1ffa96210b79dffffffffffa1",
   "@type": "WorkOrder",
   "category": "service",
   "shortDescription": "Fixed Fibre Broadband Installation sb",
   "description": "Fixed Fibre description",
   "startDate": "2025-07-22T14:23:06.528Z",
   "requestedCompletionDate": "2024-06-22T14:23:06.528Z",
   "requestedStartDate": "2024-06-22T14:23:06.528Z",
   "priority": "2 - High",
   "expectedCompletionDate": "2025-07-28T14:23:06.528Z",
   "initiatedFrom": "d090df34df113100dca6a5f59bf26335",
   "templateId": "191ba0e0df113100dca6a5f59bf26336",
   "place": {
      "@type": "GeographicSite",
      "id": "423e85f037d0200044e0bfc8bcbe5d12",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "539546b237232000158bfc8bcbe5d7",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "d79249762fc1a610b79db3bf42faf3d2",
         "name": "Workforce Engineering Group",
         "role": "Company"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "b88d14843bc02300bfe04d72f3efc4cd",
         "name": "Workforce Engineering Group",
         "role": "Contact"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifier",
         "id": "1223412"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "action": "add",
         "id": "12232332",
         "description": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "work": {
            "@type": "WorkRefOrValue",
            "workType": "999469283bca10103f09080044efc4cf",
            "orderDate": "2024-04-22 14:23:06.528",
            "scheduledStartDate": "2025-06-25 14:23:06.528",
            "expectedCompletionDate": "2025-08-22 14:23:06.528",
            "workPriority": "2 - High",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "16ff753837d0200044e0bfc8bcbe5d5f"
                  }
               }
            ],
            "relatedParty": [
               {
                  "@type": "RelatedPartyRef",
                  "id": "4c0482b237232000158bbfc8bcbe5d09",
                  "name": "Louisiana Dispatchers",
                  "role": "DispatchGroup"
               }
            ],
            "workforceEmployeeAssignment": [
               {
                  "@type": "WorkforceEmployeeAssignment",
                  "id": "7172ea0037332000158bbfc8bcbe5db6",
                  "workforceEmployee": {
                     "@type": "Individual",
                     "name": "Athelstan Amos",
                     "id": "46c1293aa9fe1981000dc753e75ebeee"
                  }
               }
            ]
         },
         "note": {
            "@type": "Note",
            "id": "afa9-3d90aaa8da0f",
            "text": "This is a work order task note."
         }
      }
   ],
   "note": {
      "@type": "Note",
      "id": "afa9-3d90aaa8da0f",
      "text": "This is a work order note."
   },
   "href": "api/sn_tmf_api/work_order_management_api/workOrder/ca6d72d1ffa96210b79dffffffffffa1"
}
```

### cURL request

Creates a work order and task without using a template.

```
curl "http://instance.servicenow.com/api/sn_tmf_api/work_order_management_api/workOrder" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "id": "323",
   "@type": "WorkOrder",
   "category": "service",
   "shortDescription": "Fixed Fibre Broadband Installation sb",
   "description": "Fixed Fibre description",
   "startDate": "2025-07-22T14:23:06.528Z",
   "requestedCompletionDate": "2024-06-22T14:23:06.528Z",
   "requestedStartDate": "2024-06-22T14:23:06.528Z",
   "priority": "2 - High",
   "expectedCompletionDate": "2025-07-28T14:23:06.528Z",
   "initiatedFrom": "d090df34df113100dca6a5f59bf26335",
   "place": {
      "@type": "GeographicSite",
      "id": "423e85f037d0200044e0bfc8bcbe5d12",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "539546b237232000158bfc8bcbe5d7",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "d79249762fc1a610b79db3bf42faf3d2",
         "name": "Workforce Engineering Group",
         "role": "Company"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "b88d14843bc02300bfe04d72f3efc4cd",
         "name": "Workforce Engineering Group",
         "role": "Contact"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifier",
         "id": "1223412"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "action": "add",
         "id": "12232332",
         "description": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "work": {
            "@type": "WorkRefOrValue",
            "workType": "999469283bca10103f09080044efc4cf",
            "orderDate": "2024-04-22 14:23:06.528",
            "scheduledStartDate": "2025-06-25 14:23:06.528",
            "expectedCompletionDate": "2025-08-22 14:23:06.528",
            "workPriority": "2 - High",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "16ff753837d0200044e0bfc8bcbe5d5f"
                  }
               }
            ],
            "relatedParty": [
               {
                  "@type": "RelatedPartyRef",
                  "id": "4c0482b237232000158bbfc8bcbe5d09",
                  "name": "Louisiana Dispatchers",
                  "role": "DispatchGroup"
               }
            ],
            "workforceEmployeeAssignment": [
               {
                  "@type": "WorkforceEmployeeAssignment",
                  "id": "7172ea0037332000158bbfc8bcbe5db6",
                  "workforceEmployee": {
                     "@type": "Individual",
                     "name": "Athelstan Amos",
                     "id": "46c1293aa9fe1981000dc753e75ebeee"
                  }
               }
            ]
         },
         "note": {
            "@type": "Note",
            "id": "afa9-3d90aaa8da0f",
            "text": "This is a work order task note."
         }
      }
   ],
   "note": {
      "@type": "Note",
      "id": "afa9-3d90aaa8da0f",
      "text": "This is a work order note."
   }
}" \
--user 'username':'password'
```

Response body.

```
{
   "id": "24fc3259ffa96210b79dffffffffff56",
   "@type": "WorkOrder",
   "category": "service",
   "shortDescription": "Fixed Fibre Broadband Installation sb",
   "description": "Fixed Fibre description",
   "startDate": "2025-07-22T14:23:06.528Z",
   "requestedCompletionDate": "2024-06-22T14:23:06.528Z",
   "requestedStartDate": "2024-06-22T14:23:06.528Z",
   "priority": "2 - High",
   "expectedCompletionDate": "2025-07-28T14:23:06.528Z",
   "initiatedFrom": "d090df34df113100dca6a5f59bf26335",
   "place": {
      "@type": "GeographicSite",
      "id": "423e85f037d0200044e0bfc8bcbe5d12",
      "relatedParty": [
         {
            "role": "QualificationGroup",
            "id": "539546b237232000158bfc8bcbe5d7",
            "@type": "PartyRef",
            "@referredType": "Individual"
         }
      ]
   },
   "relatedParty": [
      {
         "@type": "RelatedPartyRef",
         "id": "d79249762fc1a610b79db3bf42faf3d2",
         "name": "Workforce Engineering Group",
         "role": "Company"
      },
      {
         "@type": "RelatedPartyRef",
         "id": "b88d14843bc02300bfe04d72f3efc4cd",
         "name": "Workforce Engineering Group",
         "role": "Contact"
      }
   ],
   "externalIdentifier": [
      {
         "@type": "ExternalIdentifier",
         "id": "1223412"
      }
   ],
   "workOrderItem": [
      {
         "@type": "WorkOrderItem",
         "action": "add",
         "id": "12232332",
         "description": "FTTH Installation",
         "completionDate": "2024-04-22T14:23:06.528Z",
         "work": {
            "@type": "WorkRefOrValue",
            "workType": "999469283bca10103f09080044efc4cf",
            "orderDate": "2024-04-22 14:23:06.528",
            "scheduledStartDate": "2025-06-25 14:23:06.528",
            "expectedCompletionDate": "2025-08-22 14:23:06.528",
            "workPriority": "2 - High",
            "place": [
               {
                  "@type": "RelatedPlaceRefOrValue",
                  "role": "string",
                  "place": {
                     "@type": "GeographicSite",
                     "id": "16ff753837d0200044e0bfc8bcbe5d5f"
                  }
               }
            ],
            "relatedParty": [
               {
                  "@type": "RelatedPartyRef",
                  "id": "4c0482b237232000158bbfc8bcbe5d09",
                  "name": "Louisiana Dispatchers",
                  "role": "DispatchGroup"
               }
            ],
            "workforceEmployeeAssignment": [
               {
                  "@type": "WorkforceEmployeeAssignment",
                  "id": "7172ea0037332000158bbfc8bcbe5db6",
                  "workforceEmployee": {
                     "@type": "Individual",
                     "name": "Athelstan Amos",
                     "id": "46c1293aa9fe1981000dc753e75ebeee"
                  }
               }
            ]
         },
         "note": {
            "@type": "Note",
            "id": "afa9-3d90aaa8da0f",
            "text": "This is a work order task note."
         }
      }
   ],
   "note": {
      "@type": "Note",
      "id": "afa9-3d90aaa8da0f",
      "text": "This is a work order note."
   },
   "href": "api/sn_tmf_api/work_order_management_api/workOrder/24fc3259ffa96210b79dffffffffff56"
}
```

