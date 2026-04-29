---
title: Service Test Management Open API
description: The Service Test Management Open API provides endpoints to create and retrieve service test definitions and service tests.Retrieves a list of all service tests.Retrieves a service test entity based on the given ID of a service test.Retrieves a list of all service test definitions.Retrieves a service test definition entity.Updates a service test entity.Allows partial updates of a service test definition entity.Creates a service test.Creates a new service test definition.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 91
keywords: [Service Test Management Open API, Customer Service Problem Management]
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Service Test Management Open API

The Service Test Management Open API provides endpoints to create and retrieve service test definitions and service tests.

Use this API to manage service problem management information between external systems and the ServiceNow AI Platform. The Service Test Management Open API is a ServiceNow implementation of the TM Forum Service Problem Management API REST specification. This implementation is based on the [TMF653 Service Test Management API User Guide v4.1.0](https://www.tmforum.org/resources/specification/tmf653-service-test-management-api-user-guide-v4-1-0/), July 2021.

This REST API is designed to manage and execute service tests within a telecommunications environment. It allows users to define, trigger, and monitor service tests, ensuring that services meet quality and performance standards. The API provides capabilities for test management, including creating and updating test definitions, executing tests, retrieving test results, and managing test schedules.

The Service Test Management Open API requires the Customer Service Problem Management \(com.sn\_sprb\_mgmt\) application, which is available on the ServiceNow Store. For more information, see [Customer Service Problem Management](https://www.servicenow.com/docs/access?context=cspm-landing-page&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).

This API runs in the `sn_sprb_mgmt` namespace. The calling user must have the sn\_sprb\_mgmt.test\_integrator role.

The Service Test Management Open API creates or updates data in the following tables:

-   Test Run \[sn\_st\_mgmt\_test\]
-   Service Test definition \[sn\_st\_mgmt\_test\_definition\]
-   Test Definition Characteristic \[sn\_st\_mgmt\_test\_definition\_characteristic\]
-   Test Characteristic \[sn\_st\_mgmt\_test\_characteristic\]
-   Specification to Test Definition Relationship \[sn\_st\_mgmt\_test\_definition\_m2m\]
-   Test Definition Relationship \[sn\_st\_mgmt\_test\_definition\_rel\]
-   Test Measure \[sn\_st\_mgmt\_test\_measure\]
-   Measure Consequence \[sn\_st\_mgmt\_measure\_consequence\]
-   Test Measure Definition \[sn\_st\_mgmt\_test\_measure\_definition\]
-   Applied Consequence \[sn\_st\_mgmt\_applied\_consequence\]
-   Threshold Rule \[sn\_st\_mgmt\_threshold\_rule\]
-   Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Service Test Management Open API – GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTest

Retrieves a list of all service tests.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTest`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter isn't used, all fields are returned. Located in the Service Test \[sn\_st\_mgmt\_test\] table.Valid fields:

-   characteristic
-   description
-   endDateTime
-   id
-   mode
-   relatedService
-   startDateTime
-   state
-   testMeasure
-   testSpecification
-   validFor

Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

Maximum value: 100

Default: 20

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this parameter to paginate results in small and manageable chunks. The first record is indexed at 0.Data type: Number

Default: 0

</td></tr><tr><td>

state

</td><td>

Filter test definitions by the test's current state. Only test definitions in the specified state are returned in the response.Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Specifies the range of content returned in a paginated call.For example, if `offset=2` and `limit=3`, the value of the Content-Range header is items `3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports application/json.

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
|206|Partial resource returned in response \(with pagination\).|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

<table id="table_ash_mhx_vbc" class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test. For more information about test definition characteristics, see Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics. If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr><td>

endDateTime

</td><td>

End date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

href

</td><td>

Hyperlink reference to the service test.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

mode

</td><td>

Mode that the service test is running in.Valid values:

-   ONDEMAND: Triggers the service test manually.
-   PROACTIVE: Triggers the service test automatically.

Data type: String

Default: ONDEMAND

</td></tr><tr><td>

name

</td><td>

Required. Name of the service test.Data type: String

</td></tr><tr><td>

relatedService

</td><td>

Required. Test definition associated with the service test.Data type: Object

```
"relatedService": {
 "href": "String",
 "id": "String",
 "name": "String"
}
```

</td></tr><tr><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: In the sys\_id or external\_id field of the product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

relatedService.name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

state

</td><td>

State the service test is in. Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr><tr><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasure": [
 {
 "accuracy": "String",
 "captureDateTime": "String",
 "captureMethod": "String",
 "id": "String",
 "metricDescription": "String",
 "metricName": "String",
 "ruleViolation": [Array],
 "unitOfMeasure": "String",
 "value": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the Test Measures.Data type: String

Table: In the sys\_id or external\_id fields of the Test Measures table \[sn\_st\_mgmt\_test\_measure\] table.

</td></tr><tr><td>

testMeasure.Measure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasure.metricName

</td><td>

Name of the test measure metric.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation

</td><td>

An object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"ruleViolation"[
  {
    appliedConsequence: [Array],
    conformanceTargetUpper: Number,
    conformanceComparatorUpper: "String",
    description: "String",
    id: "String",
    name: "String",
    numberOfAllowedCrossing: Number,
    thresholdRuleSeverity: "String",
    tolerancePeriod: "String"
  }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Number of periods before applying the consequence.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.repeatAction

</td><td>

Flag that indicates whether to repeat the consequence when a second violation occurs.Valid values:

-   true: Repeat the action.
-   false: Don't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorExact

</td><td>

Flag that indicates whether a value is identical.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorLower

</td><td>

Operator for checking if a value falls below the threshold.Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorUpper

</td><td>

Operator for checking if a value is above the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr><td>

testMeasure.ruleViolation.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Specified time interval during which crossing occurrences are enabled without triggering any immediate consequences or actions.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasure.unitOfMeasure

</td><td>

Unit of measurement for the conformance target values of the test measure.Data type: String

</td></tr><tr><td>

testMeasure.value

</td><td>

Value of the test measure.Data type: Object

```
"value": {
 "id": "String",
 "name": "String",
 "valueType": "String",
 "value": "String
}
```

</td></tr><tr><td>

testMeasure.value.id

</td><td>

ID of the test measure value.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the test measure value.Data type: String

</td></tr><tr><td>

testMeasure.value.value

</td><td>

Value of the test measure.Data type: String

</td></tr><tr><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr><td>

testSpecification

</td><td>

Required. Test definition associated with this test. Data type: Object

```
"testSpecification": {
 "href": "String",
 "id": "String"
}
```

</td></tr><tr><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: In the sys\_id or external\_id field of the Service Test Definition \[sn\_st\_mgmt\_test\_definition\] table.

</td></tr><tr><td>

validFor

</td><td>

Date range the service test is valid for.Data type: Object

```
"validFor": {
 "endDateTime ": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

Validity end date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Validity start date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example retrieves information about the two service tests in the instance.

```
curl --location --request GET “https://instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTest” \
--user 'username’: ‘password'
```

Response body.

```
[
  {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/09d1f42e3be28210d140068aa4e45ae2",
    "id": "09d1f42e3be28210d140068aa4e45ae2",
    "description": "Service test",
    "endDateTime": "2025-01-31 15:05:43",
    "mode": "proactive",
    "name": "Speed Test TR0001002",
    "startDateTime": "2024-06-05 09:07:10",
    "validFor": {
      "startDateTime": "",
      "endDateTime": ""
    },
    "relatedService": {
      "id": "fa6d13f45b5620102dff5e92dc81c77f",
      "name": "Internet_VPLS_PI0000011"
    },
    "testSpecification": {
      "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/7d3854864316c6500e51203d5fb8f2d8",
      "id": "7d3854864316c6500e51203d5fb8f2d8"
    },
    "characteristic": [],
    "testMeasure": [
      {
        "id": "61d1382e3be28210d140068aa4e45a2e",
        "accuracy": "0.0001",
        "captureDateTime": "",
        "captureMethod": "automatic",
        "metricDescription": "",
        "metricName": "Flow speed",
        "unitOfMeasure": "A second",
        "value": "3000",
        "ruleViolation": [
          {
            "id": "61d1382e3be28210d140068aa4e45a2f",
            "description": "This speed is greater than the target",
            "name": "tooMuchTraffic",
            "numberOfAllowedCrossing": "0",
            "thresholdRuleSeverity": "high",
            "tolerancePeriod": "",
            "conformanceTargetLower": "2500",
            "conformanceComparatorLower": "greater than",
            "appliedConsequence": [
              {
                "id": "65d1382e3be28210d140068aa4e45a31",
                "appliedAction": "sendWarning",
                "description": "send a warning to the system",
                "name": "sendWarning",
                "repeatAction": "0"
              }
            ]
          }
        ]
      }
    ]
  },
  {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/18682a2a3b2682107222bf9985e45a55",
    "id": "18682a2a3b2682107222bf9985e45a55",
    "description": "Service test",
    "endDateTime": "2025-01-31 15:05:43",
    "mode": "proactive",
    "name": "Speed Test TR0001012",
    "startDateTime": "2024-06-05 17:45:07",
    "validFor": {
      "startDateTime": "",
      "endDateTime": ""
    },
    "relatedService": {
      "id": "fa6d13f45b5620102dff5e92dc81c77f",
      "name": "Internet_VPLS_PI0000011"
    },
    "testSpecification": {
      "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/7d3854864316c6500e51203d5fb8f2d8",
      "id": "7d3854864316c6500e51203d5fb8f2d8"
    },
    "characteristic": [
      {
        "id": "5c682a2a3b2682107222bf9985e45a5a",
        "name": "url",
        "valueType": "single_line_text",
        "value": "http://abc.com"
      }
    ],
    "testMeasure": [
      {
        "id": "7c686a2a3b2682107222bf9985e45a4d",
        "accuracy": "0.0001",
        "captureDateTime": "",
        "captureMethod": "automatic",
        "metricDescription": "",
        "metricName": "Flow speed",
        "unitOfMeasure": "A second",
        "value": "3000",
        "ruleViolation": [
          {
            "id": "38686a2a3b2682107222bf9985e45a4e",
            "description": "This speed is greater than the target",
            "name": "tooMuchTraffic",
            "numberOfAllowedCrossing": "0",
            "thresholdRuleSeverity": "high",
            "tolerancePeriod": "",
            "conformanceTargetLower": "2500",
            "conformanceComparatorLower": "greater than",
            "appliedConsequence": [
              {
                "id": "34686a2a3b2682107222bf9985e45a50",
                "appliedAction": "sendWarning",
                "description": "send a warning to the system",
                "name": "sendWarning",
                "repeatAction": "0"
              }
            ]
          }
        ]
      }
    ]
  }
]
```

## Service Test Management Open API – GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTest/\{id\}

Retrieves a service test entity based on the given ID of a service test.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test to retrieve.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter isn't used, all fields are returned. Located in the Service Test \[sn\_st\_mgmt\_test\] table.Valid fields:

-   characteristic
-   description
-   endDateTime
-   id
-   mode
-   relatedService
-   startDateTime
-   state
-   testMeasure
-   testSpecification
-   validFor

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table class="rest-api-response-body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test.Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics.If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr><td>

endDateTime

</td><td>

End date and time of the service test.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

href

</td><td>

Hyperlink reference to the service test.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

mode

</td><td>

Mode that the service test is running in.Valid values:

-   ONDEMAND: Triggers the service test manually.
-   PROACTIVE: Triggers the service test automatically.

Data type: String

Default: ONDEMAND

</td></tr><tr><td>

name

</td><td>

Name of the service test.Data type: String

</td></tr><tr><td>

relatedService

</td><td>

Test definition associated with this test.Data type: Object

```
"relatedService": {
 "href": "String",
 "id": "String",
 "name": "String"
}
```

</td></tr><tr><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: In the sys\_id or external\_id field of the Product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

relatedService.name

</td><td>

Name of the product inventory item.Data type: String

</td></tr><tr><td>

startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

state

</td><td>

State of the service test.Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr><tr><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasureDefinition": [
 {
  "accuracy": "String",
  "captureDateTime": "String",
  "captureMethod": "String",
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "ruleViolation": [Array]
  "unitOfMeasure": "String",
  "value": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the test measure.Data type: String

Table: Test Measures \[sn\_st\_mgmt\_test\_measure\]

</td></tr><tr><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasure.metricName

</td><td>

Name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation

</td><td>

Object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"RuleViolation": [
{
  "appliedConsequence": [Array],
  "conformanceComparatorExact": Boolean,
  "conformanceComparatorLower": "String",
  "conformanceComparatorUpper": "String",
  "conformanceTargetExact": "String",
  "conformanceTargetLower": "String",
  "conformanceTargetUpper": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "numberOfAllowedCrossing": Number,
  "thresholdRuleSeverity": "String",
  "tolerancePeriod": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is violated.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction.repeatAction

</td><td>

Flag that indicates whether to repeat the applied action or not.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value of **conformanceTargetExact**.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorLower

</td><td>

An operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorUpper

</td><td>

An operator that checks if a value exceeds the threshold.Valid values:

-   is
-   lesser than

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule violation.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr><td>

testMeasure.ruleViolation.name

</td><td>

Name of the threshold rule violation.Date type: String

</td></tr><tr><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum: 40

</td></tr><tr><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   low
-   medium

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Duration or time interval in which allowed crossings can occur before a consequence is initiated.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Amount of the period in number.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasure.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasure.value

</td><td>

Value of metric in the test.Data type: Object

```
"value": {
  "id": "String",
  "name": "String",
  "valueType": "String",
  "value": "String"
}
```

</td></tr><tr><td>

testMeasure.value.id

</td><td>

ID of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.value

</td><td>

Value of metric in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr><td>

testSpecification

</td><td>

Test definition associated for this test. Data type: Object

```
"testSpecification": {
 "href": "String",
 "id": "String"
}
```

</td></tr><tr><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

validFor

</td><td>

Date range that the service test is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example retrieves details about the service test entity associated with the given ID, 44b7a8ea3b6a42107222bf9985e45a45.

```
curl --location --request GET “https://instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/44b7a8ea3b6a42107222bf9985e45a45 \
--user 'username’: ‘password'
```

Response body.

```
{
  "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/44b7a8ea3b6a42107222bf9985e45a45",
  "id": "44b7a8ea3b6a42107222bf9985e45a45",
  "description": "Service test",
  "endDateTime": "2025-01-31 15:05:43",
  "mode": "proactive",
  "name": "Speed Test TR0001001",
  "startDateTime": "2024-06-05 08:22:52",
  "validFor": {
    "startDateTime": "",
    "endDateTime": ""
  },
  "relatedService": {
    "id": "fa6d13f45b5620102dff5e92dc81c77f",
    "name": "Internet_VPLS_PI0000011"
  },
  "testSpecification": {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/7d3854864316c6500e51203d5fb8f2d8",
    "id": "7d3854864316c6500e51203d5fb8f2d8"
  },
  "characteristic": [
        { 
        "id": "5c682a2a3b2682107222bf9985e45a5a", 
        "name": "url", 
        "valueType": "single_line_text", 
        "value": "test" 
         }
],
  "testMeasure": [
    {
      "id": "62ade42a3ba28210d140068aa4e45a71",
      "accuracy": "0.0001",
      "captureDateTime": "",
      "captureMethod": "automatic",
      "metricDescription": "",
      "metricName": "Downstream Speed",
      "unitOfMeasure": "",
      "value": "16",
      "ruleViolation": [
        {
          "id": "b9bee4ae3ba28210d140068aa4e45a3a",
          "description": "This speed is less than the target upper",
          "name": "tooMuchTraffic",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "75",
          "conformanceComparatorUpper": "less than",
          "appliedConsequence": [
            {
              "id": "489074aa3be28210d140068aa4e45a42",
              "appliedAction": "generateReport",
              "description": "",
              "name": "generateReport",
              "repeatAction": "0"
            },
            {
              "id": "785f2ce23be28210d140068aa4e45a75",
              "appliedAction": "sendWarning",
              "description": "",
              "name": "sendWarning",
              "repeatAction": "0"
            }
          ]
        }
      ]
    }
  ]
}
```

## Service Test Management Open API - GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification

Retrieves a list of all service test definitions.

### URL format

Default URL: `GET /api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter isn't used, all fields are returned. Located in the Service Test Definition \[sn\_st\_mgmt\_test\_definition\] table.Valid values:

-   description
-   id
-   name
-   relatedServiceSpecification
-   serviceTestSpecRelationship
-   specCharacteristic
-   testMeasureDefinition
-   validFor

Data type: String

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval.Data type: Number

Maximum value: 100

Default: 20

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this parameter to paginate results in small and manageable chunks. The first record is indexed at 0.Data type: Number

Default: 0

</td></tr><tr><td>

state

</td><td>

Filter test definitions by the test's current state. Only test definitions in the specified state are returned in the response.Valid values:

-   archived
-   draft
-   published
-   retired

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Range

</td><td>

Specifies the range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the Content-Range header is items `3-5`.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the response body. Only supports application/json.

</td></tr><tr><td>

Link

</td><td>

Contains the following links to navigate through query results:-   first
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
|206|Partial resource returned in response \(with pagination\).|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="table_yvz_1lx_4bc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the service test definition.Data type: String

</td></tr><tr><td>

relatedServiceSpecification

</td><td>

Required. Service specifications of the test definition.Data type: Array of Objects

```
"relatedServiceSpecification": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of Objects

```
"serviceTestSpecRelationship": [
 {
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Accepted values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Characteristics of the test definition.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range that the characteristic is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. For more information, see [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.captureFrequency

</td><td>

The frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Doesn't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasureDefinition.capturePeriod

</td><td>

Period or duration of the metric capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the test measure definitions.Data type: String

Table: Test Measure definition table \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines conditions to achieve before applying consequences when a threshold is crossed \(or not crossed\)​ in the test measure definition. For more information, [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of Objects

```
{
  "thresholdRule": {
    "consequence": [Array],
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": {Object}
  }
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value set for **testMeasureDefinition.thresholdRule.conformanceTargetExact**. If set to true, **testMeasureDefinition.thresholdRule.conformanceTargetExact** is required.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed. See [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more information.Data type: Array of objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied consequence.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: In the sys\_id or external\_id field of the Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\] table.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity level of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasureDefinition.validFor

</td><td>

Date range that the test measure definition is valid for.Data type: String

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor

</td><td>

Date range that the test definition is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

Date and time of the test definition on which the state of it is retired. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Date and time of the test definition on which the state of it is published. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

This example retrieves details about all test service test definitions in the instance. In this case, two definitions are returned.

```
curl --location --request GET 
“https://instance.servicenow.com//api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification” \
--user 'username’: ‘password'

```

Response body.

```
[
  {
    "description": "Operation, Administration and Maintenance",
    "id": "76a3b160432a02104fefe4511fb8f2ad",
    "name": "OAM Test",
    "validFor": {
      "startDateTime": "",
      "endDateTime": ""
    },
    "testMeasureDefinition": [
      {
        "id": "77b9b964432a02104fefe4511fb8f26e",
        "captureFrequency": "once",
        "captureMethod": "automatic",
        "metricDescription": "This is the Rx signal level",
        "metricName": "Rx Optical Signal Level",
        "name": "Rx Optical Signal Level",
        "unitOfMeasure": "a minute",
        "valueType": "",
        "capturePeriod": "",
        "validFor": {
          "startDateTime": "",
          "endDateTime": ""
        },
        "thresholdRule": [
          {
            "id": "d3e97d64432a02104fefe4511fb8f281",
            "description": "",
            "name": "gponOntAniOpInfoRxOpticalSignalLevel",
            "numberOfAllowedCrossing": "",
            "thresholdRuleSeverity": "",
            "tolerancePeriod": "",
            "conformanceTargetUpper": "0",
            "conformanceComparatorUpper": "less than",
            "conformanceTargetLower": "-50",
            "conformanceComparatorLower": "greater than",
            "consequence": []
          }
        ]
      },
      {
        "id": "878afd64432a02104fefe4511fb8f28d",
        "captureFrequency": "once",
        "captureMethod": "automatic",
        "metricDescription": "This is the Tx signal level",
        "metricName": "TX Optical Signal Level",
        "name": "TX Optical Signal Level",
        "unitOfMeasure": "a minute",
        "valueType": "",
        "capturePeriod": "",
        "validFor": {
          "startDateTime": "",
          "endDateTime": ""
        },
        "thresholdRule": [
          {
            "id": "b3dab5a4432a02104fefe4511fb8f2d3",
            "description": "",
            "name": "gponOntAniOpInfoTxOpticalSignalLevel",
            "numberOfAllowedCrossing": "",
            "thresholdRuleSeverity": "",
            "tolerancePeriod": "",
            "conformanceTargetUpper": "65",
            "conformanceComparatorUpper": "less than",
            "conformanceTargetLower": "-65",
            "conformanceComparatorLower": "greater than",
            "consequence": []
          }
        ]
      }
    ],
    "specCharacteristic": [
      {
        "name": "AccessRequired",
        "description": "AccessRequired",
        "valueType": "yes_no",
        "validFor": {
          "startDatetime": "2024-05-30 09:09:57"
        },
        "characteristicValueSpecification": [
          {
            "value": "Yes",
            "validFor": {
              "startDateTime": "",
              "endDateTime": ""
            }
          },
          {
            "value": "No",
            "validFor": {
              "startDateTime": "",
              "endDateTime": ""
            }
          }
        ]
      }
    ],
    "serviceTestSpecRelationship": [],
    "relatedServiceSpecification": [
      {
        "id": "f559b564432a02104fefe4511fb8f2e0",
        "name": "OAM"
      }
    ]
  },
  {
    "description": "Upstream and Downstream speed ",
    "id": "89d2b920432a02104fefe4511fb8f22e",
    "name": "Speed Test",
    "validFor": {
      "startDateTime": "2024-05-31",
      "endDateTime": "2024-06-27"
    },
    "testMeasureDefinition": [
      {
        "id": "1a04f560432a02104fefe4511fb8f2ad",
        "captureFrequency": "once",
        "captureMethod": "automatic",
        "metricDescription": "This is the downstream speed in a service",
        "metricName": "Downstream Speed",
        "name": "Downstream Speed",
        "unitOfMeasure": "a second",
        "valueType": "",
        "capturePeriod": "30 Minutes",
        "validFor": {
          "startDateTime": "2024-05-30 08:49:26",
          "endDateTime": "2024-05-31 08:49:29"
        },
        "thresholdRule": [
          {
            "id": "a754f960432a02104fefe4511fb8f2d0",
            "description": "This speed is greater than the target upper",
            "name": "InternetSpeedValue",
            "numberOfAllowedCrossing": "0",
            "thresholdRuleSeverity": "high",
            "tolerancePeriod": "15 Minutes",
            "conformanceTargetLower": "75",
            "conformanceComparatorLower": "greater than",
            "consequence": [
              {
                "id": "15a4bd60432a02104fefe4511fb8f2b8",
                "prescribeAction": "null",
                "description": "generate a waring report",
                "name": "degradedQualityOfService",
                "repeatAction": "0",
                "validFor": {
                  "startDateTime": "2024-05-30 08:51:29",
                  "endDateTime": "2024-08-06 08:51:31"
                }
              },
              {
                "id": "e6847d60432a02104fefe4511fb8f2c3",
                "prescribeAction": "null",
                "description": "send a warning to the system",
                "name": "packetdrop",
                "repeatAction": "0",
                "validFor": {
                  "startDateTime": "2024-05-30 08:50:53",
                  "endDateTime": "2024-08-06 08:50:55"
                }
              }
            ]
          },
          {
            "id": "cb55b5a0432a02104fefe4511fb8f201",
            "description": "",
            "name": "InternetSpeedValue",
            "numberOfAllowedCrossing": "0",
            "thresholdRuleSeverity": "medium",
            "tolerancePeriod": "",
            "conformanceTargetUpper": "120",
            "conformanceComparatorUpper": "less than",
            "consequence": []
          }
        ]
      },
      {
        "id": "8f987524432a02104fefe4511fb8f2f0",
        "captureFrequency": "once",
        "captureMethod": "automatic",
        "metricDescription": "This is the upstream speed in the service",
        "metricName": "Upstream Speed",
        "name": "Upstream Speed",
        "unitOfMeasure": "a second",
        "valueType": "",
        "capturePeriod": "",
        "validFor": {
          "startDateTime": "",
          "endDateTime": ""
        },
        "thresholdRule": []
      }
    ],
    "specCharacteristic": [
      {
        "name": "restart",
        "description": "restart",
        "valueType": "yes_no",
        "validFor": {
          "startDatetime": "2024-05-30 08:45:49"
        },
        "characteristicValueSpecification": [
          {
            "value": "No",
            "validFor": {
              "startDateTime": "",
              "endDateTime": ""
            }
          },
          {
            "value": "Yes",
            "validFor": {
              "startDateTime": "",
              "endDateTime": ""
            }
          }
        ]
      }
    ],
    "serviceTestSpecRelationship": [
      {
        "id": "76a3b160432a02104fefe4511fb8f2ad",
        "name": "OAM Test",
        "relationshipType": ""
      }
    ],
    "relatedServiceSpecification": [
      {
        "id": "aeddcd1fb7d69910ff00f203ae11a990",
        "name": "Home Internet"
      }
    ]
  }
]
```

## Service Test Management Open API - GET /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification/\{id\}

Retrieves a service test definition entity.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition to retrieve.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored. If this parameter isn't used, all fields are returned. Located in the Service Test Definition \[sn\_st\_mgmt\_test\_definition\] table.Valid values:

-   description
-   id
-   name
-   relatedServiceSpecification
-   serviceTestSpecRelationship
-   specCharacteristic
-   testMeasureDefinition
-   validFor

Data type: String

</td></tr><tr><td>

state

</td><td>

Filter test definitions by the test's current state. Only test definitions in the specified state are returned in the response.Valid values:

-   archived
-   draft
-   published
-   retired

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the request body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the service test definition.Data type: String

</td></tr><tr><td>

relatedServiceSpecification

</td><td>

Required. Service specifications of the test definition.Data type: Array of Objects

```
"relatedServiceSpecification": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of Objects

```
"serviceTestSpecRelationship": [
 {
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Accepted values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Characteristics of the test definition.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range that the characteristic is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. For more information, see [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.captureFrequency

</td><td>

The frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Doesn't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasureDefinition.capturePeriod

</td><td>

Period or duration of the metric capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the test measure definitions.Data type: String

Table: Test Measure definition table \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines conditions to achieve before applying consequences when a threshold is crossed \(or not crossed\)​ in the test measure definition. For more information, [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of Objects

```
{
  "thresholdRule": {
    "consequence": [Array],
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": {Object}
  }
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value set for **testMeasureDefinition.thresholdRule.conformanceTargetExact**. If set to true, **testMeasureDefinition.thresholdRule.conformanceTargetExact** is required.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed. See [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more information.Data type: Array of objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied consequence.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: In the sys\_id or external\_id field of the Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\] table.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity level of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasureDefinition.validFor

</td><td>

Date range that the test measure definition is valid for.Data type: String

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor

</td><td>

Date range that the test definition is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

Date and time of the test definition on which the state of it is retired. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Date and time of the test definition on which the state of it is published. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

This example retrieves details of a service test definition with a given ID.

```
curl --location --request GET "https:/instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/89d2b920432a02104fefe4511fb8f22e" \
--user 'username’: ‘password'
```

Response body.

```
{
  "description": "Upstream and Downstream speed ",
  "id": "89d2b920432a02104fefe4511fb8f22e",
  "name": "Speed Test",
  "validFor": {
    "startDateTime": "2024-05-31",
    "endDateTime": "2024-06-27"
  },
  "testMeasureDefinition": [
    {
      "id": "1a04f560432a02104fefe4511fb8f2ad",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the downstream speed in a service",
      "metricName": "Downstream Speed",
      "name": "Downstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "30 Minutes",
      "validFor": {
        "startDateTime": "2024-05-30 08:49:26",
        "endDateTime": "2024-05-31 08:49:29"
      },
      "thresholdRule": [
        {
          "id": "a754f960432a02104fefe4511fb8f2d0",
          "description": "This speed is greater than the target upper",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "15 Minutes",
          "conformanceTargetLower": "75",
          "conformanceComparatorLower": "greater than",
          "consequence": [
            {
              "id": "15a4bd60432a02104fefe4511fb8f2b8",
              "prescribeAction": "null",
              "description": "generate a waring report",
              "name": "degradedQualityOfService",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:51:29",
                "endDateTime": "2024-08-06 08:51:31"
              }
            },
            {
              "id": "e6847d60432a02104fefe4511fb8f2c3",
              "prescribeAction": "null",
              "description": "send a warning to the system",
              "name": "packetdrop",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:50:53",
                "endDateTime": "2024-08-06 08:50:55"
              }
            }
          ]
        },
        {
          "id": "cb55b5a0432a02104fefe4511fb8f201",
          "description": "",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "medium",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "120",
          "conformanceComparatorUpper": "less than",
          "consequence": []
        }
      ]
    }
  ],
  "specCharacteristic": [
    {
      "name": "restart",
      "description": "restart",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2024-05-30 08:45:49"
      },
      "characteristicValueSpecification": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": "",
            "endDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": "",
            "endDateTime": ""
          }
        }
      ]
    }
  ],
  "serviceTestSpecRelationship": [
    {
      "id": "76a3b160432a02104fefe4511fb8f2ad",
      "name": "OAM Test",
      "relationshipType": ""
    }
  ],
  "relatedServiceSpecification": [
    {
      "id": "aeddcd1fb7d69910ff00f203ae11a990",
      "name": "Home Internet"
    }
  ]
}
```

## Service Test Management Open API - PATCH /sn\_sprb\_mgmt/servicetestmanagement/serviceTest/\{id\}

Updates a service test entity.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test to retrieve.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test. For more information about test definition characteristics, see Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics. If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr><td>

endDateTime

</td><td>

End date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

mode

</td><td>

Mode that the service test is running in.Valid values:

-   ONDEMAND: Triggers the service test manually.
-   PROACTIVE: Triggers the service test automatically.

Data type: String

Default: ONDEMAND

</td></tr><tr><td>

name

</td><td>

Required. Name of the service test.Data type: String

</td></tr><tr><td>

relatedService

</td><td>

Required. Test definition associated with the service test.Data type: Object

```
"relatedService": {
 "href": "String",
 "id": "String",
 "name": "String"
}
```

</td></tr><tr><td>

relatedService.href

</td><td>

Hyperlink reference to the related service.Data type: String

</td></tr><tr><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: In the sys\_id or external\_id field of the product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr><td>

startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

state

</td><td>

State the service test is in. Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr><tr><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasure": [
 {
 "accuracy": "String",
 "captureDateTime": "String",
 "captureMethod": "String",
 "id": "String",
 "metricDescription": "String",
 "metricName": "String",
 "ruleViolation": [Array],
 "unitOfMeasure": "String",
 "value": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the Test Measures.Data type: String

Table: In the sys\_id or external\_id fields of the Test Measures table \[sn\_st\_mgmt\_test\_measure\] table.

</td></tr><tr><td>

testMeasure.Measure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasure.metricName

</td><td>

Name of the test measure metric.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation

</td><td>

An object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"ruleViolation"[
  {
    appliedConsequence: [Array],
    conformanceTargetUpper: Number,
    conformanceComparatorUpper: "String",
    description: "String",
    id: "String",
    name: "String",
    numberOfAllowedCrossing: Number,
    thresholdRuleSeverity: "String",
    tolerancePeriod: "String"
  }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Number of periods before applying the consequence.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.repeatAction

</td><td>

Flag that indicates whether to repeat the consequence when a second violation occurs.Valid values:

-   true: Repeat the action.
-   false: Don't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorExact

</td><td>

Flag that indicates whether a value is identical.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorLower

</td><td>

Operator for checking if a value falls below the threshold.Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComporatorUpper

</td><td>

Operator for checking if a value is above the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr><td>

testMeasure.ruleViolation.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Specified time interval during which crossing occurrences are enabled without triggering any immediate consequences or actions.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasure.unitOfMeasure

</td><td>

Unit of measurement for the conformance target values of the test measure.Data type: String

</td></tr><tr><td>

testMeasure.value

</td><td>

Value of the test measure.Data type: Object

```
"value": {
 "id": "String",
 "name": "String",
 "valueType": "String",
 "value": "String
}
```

</td></tr><tr><td>

testMeasure.value.id

</td><td>

ID of the test measure value.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the test measure value.Data type: String

</td></tr><tr><td>

testMeasure.value.value

</td><td>

Value of the test measure.Data type: String

</td></tr><tr><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr><td>

testSpecification

</td><td>

Required. Test definition associated with this test. Data type: Object

```
"testSpecification": {
 "href": "String",
 "id": "String"
}
```

</td></tr><tr><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: In the sys\_id or external\_id field of the Service Test Definition \[sn\_st\_mgmt\_test\_definition\] table.

</td></tr><tr><td>

validFor

</td><td>

Date range the service test is valid for.Data type: Object

```
"validFor": {
 "endDateTime ": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

Validity end date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Validity start date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test.Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics. If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

name

</td><td>

Name of the service test.Data type: String

</td></tr><tr><td>

relatedService

</td><td>

Test definition associated for this test.Data type: Object

```
"relatedService": {
  "href": "string",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: Product Inventory \[sn\_prd\_invt\_product\_inventory\]

</td></tr><tr><td>

relatedService.name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasureDefinition": [
 {
  "accuracy": "String",
  "captureDateTime": "String",
  "captureMethod": "String",
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "ruleViolation": [Array]
  "unitOfMeasure": "String",
  "value": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the test measure.Data type: String

Table: Test Measures \[sn\_st\_mgmt\_test\_measure\]

</td></tr><tr><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasure.metricName

</td><td>

Name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation

</td><td>

Object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"RuleViolation": [
{
  "appliedConsequence": [Array],
  "conformanceComparatorExact": Boolean,
  "conformanceComparatorLower": "String",
  "conformanceComparatorUpper": "String",
  "conformanceTargetExact": "String",
  "conformanceTargetLower": "String",
  "conformanceTargetUpper": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "numberOfAllowedCrossing": Number,
  "thresholdRuleSeverity": "String",
  "tolerancePeriod": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is violated.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction.repeatAction

</td><td>

Flag that indicates whether to repeat the applied action or not.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value of **conformanceTargetExact**.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorLower

</td><td>

An operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorUpper

</td><td>

An operator that checks if a value exceeds the threshold.Valid values:

-   is
-   lesser than

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule violation.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum: 40

</td></tr><tr><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   low
-   medium

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Duration or time interval in which allowed crossings can occur before a consequence is initiated.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Amount of the period in number.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasure.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasure.value

</td><td>

Value of metric in the test.Data type: Object

```
"value": {
  "id": "String",
  "name": "String",
  "valueType": "String",
  "value": "String"
}
```

</td></tr><tr><td>

testMeasure.value.id

</td><td>

ID of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.value

</td><td>

Value of metric in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr><td>

testSpecification

</td><td>

Test definition associated for this test. Data type: Object

```
"testSpecification": {
  "href": "String",
  "id": "String"
}
```

</td></tr><tr><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

validFor

</td><td>

Date range that the service test is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example updates the given service test entity according to details provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTest/2b406ec043b202104fefe4511fb8f211" \ 
--request PATCH \
--header "Accept:application/json" \
--user 'username':'password'
--data {
  "description": "Service test description",
  "endDateTime": "2025-01-31 15:05:43",
  "mode": "proactive",
  "name": "Speed Test TR0001002",
  "startDateTime": "2024-06-05 09:07:10",
  "validFor": {
    "startDateTime": "",
    "endDateTime": ""
  },
  "relatedService": {
    "id": "fa6d13f45b5620102dff5e92dc81c77f",
    "name": "Internet_VPLS_PI0000011"
  },
  "testSpecification": {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/76a3b160432a02104fefe4511fb8f2ad",
    "id": "76a3b160432a02104fefe4511fb8f2ad"
  },
  "characteristic": [
    {
      "id": "e7ef960443f202104fefe4511fb8f224",
      "name": "AccessRequired",
      "valueType": "yes_no",
      "value": "No"
    }
  ],
  "testMeasure": [
    {
      "id": "61d1382e3be28210d140068aa4e45a2e",
      "accuracy": "0.0001",
      "captureDateTime": "",
      "captureMethod": "automatic",
      "metricDescription": "",
      "metricName": "Flow speed",
      "unitOfMeasure": "A second",
      "value": "3000",
      "ruleViolation": [
        {
          "id": "61d1382e3be28210d140068aa4e45a2f",
          "description": "This speed is greater than the target",
          "name": "tooMuchTraffic",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "",
          "conformanceTargetLower": "2500",
          "conformanceComparatorLower": "greater than",
          "appliedConsequence": [
            {
              "id": "65d1382e3be28210d140068aa4e45a31",
              "appliedAction": "sendWarning",
              "description": "send a warning to the system",
              "name": "sendWarning",
              "repeatAction": "0"
            }
          ]
        }
      ]
    }
  ]
}
```

The response shows a successful update by returning the modified information in the given test service.

```
{
  "description": "Service test description",
  "endDateTime": "2025-01-31 15:05:43",
  "mode": "proactive",
  "name": "Speed Test TR0001002",
  "startDateTime": "2024-06-05 09:07:10",
  "validFor": {
    "startDateTime": "",
    "endDateTime": ""
  },
  "relatedService": {
    "id": "fa6d13f45b5620102dff5e92dc81c77f",
    "name": "Internet_VPLS_PI0000011"
  },
  "testSpecification": {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/76a3b160432a02104fefe4511fb8f2ad",
    "id": "76a3b160432a02104fefe4511fb8f2ad"
  },
  "characteristic": [
    {
      "id": "e7ef960443f202104fefe4511fb8f224",
      "name": "AccessRequired",
      "valueType": "yes_no",
      "value": "yes"
    }
  ],
  "testMeasure": [
    {
      "id": "61d1382e3be28210d140068aa4e45a2e",
      "accuracy": "0.0001",
      "captureDateTime": "",
      "captureMethod": "automatic",
      "metricDescription": "",
      "metricName": "Flow speed",
      "unitOfMeasure": "A second",
      "value": "3000",
      "ruleViolation": [
        {
          "id": "61d1382e3be28210d140068aa4e45a2f",
          "description": "This speed is greater than the target",
          "name": "tooMuchTraffic",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "",
          "conformanceTargetLower": "2500",
          "conformanceComparatorLower": "greater than",
          "appliedConsequence": [
            {
              "id": "65d1382e3be28210d140068aa4e45a31",
              "appliedAction": "sendWarning",
              "description": "send a warning to the system",
              "name": "sendWarning",
              "repeatAction": "0"
            }
          ]
        }
      ]
    }
  ]
}
```

## Service Test Management Open API - PATCH /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification/\{id\}

Allows partial updates of a service test definition entity.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition to retrieve.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the service test definition.Data type: String

</td></tr><tr><td>

relatedServiceSpecification

</td><td>

Required. Service specifications of the test definition.Data type: Array of Objects

```
"relatedServiceSpecification": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of Objects

```
"serviceTestSpecRelationship": [
 {
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Accepted values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Characteristics of the test definition.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range that the characteristic is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. For more information, see [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.captureFrequency

</td><td>

The frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Doesn't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasureDefinition.capturePeriod

</td><td>

Period or duration of the metric capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the test measure definitions.Data type: String

Table: Test Measure definition table \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines conditions to achieve before applying consequences when a threshold is crossed \(or not crossed\)​ in the test measure definition. For more information, [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of Objects

```
{
  "thresholdRule": {
    "consequence": [Array],
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": {Object}
  }
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value set for **testMeasureDefinition.thresholdRule.conformanceTargetExact**. If set to true, **testMeasureDefinition.thresholdRule.conformanceTargetExact** is required.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed. See [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more information.Data type: Array of objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied consequence.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: In the sys\_id or external\_id field of the Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\] table.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity level of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasureDefinition.validFor

</td><td>

Date range that the test measure definition is valid for.Data type: String

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-JSON-only-entry-RESTAPI">

Data format of the request body. Only supports **application/json**.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|404|Not found. The requested item wasn't found.|

### Response body parameters \(JSON or XML\)

<table id="table_i1m_wz4_qbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

name

</td><td>

Name of the service test definition.Data type: String

</td></tr><tr><td>

relatedServiceSpecification

</td><td>

Service specifications for the test definitions.Data type: Array of Objects

```
"relatedServiceSpecification": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of Objects

```
"serviceTestSpecRelationship": [
 {
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Accepted values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Test definition characteristics.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
 {
  "value": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. See [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more infomation.Data type: Array of Objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.captureFrequency

</td><td>

Frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasureDefinition.capturePeriod

</td><td>

Duration or period of the capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Accepted values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the Test Measure definitions.Data type: String

Table: Test Measure definition \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines the condition \(raise or clear\) to achieve to apply consequences when a threshold is crossed or ceased to be crossed​ for a particular test measure definition.Data type: Array of Objects

```
{
  "thresholdRule": {
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": Object
  }
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value of **conformanceTargetExact**.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   lesser than
-   is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed.Data type: Array of Objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied action or not.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\]

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   low
-   medium

Data type: String

</td></tr><tr><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasureDefinition.validFor

</td><td>

Date range the test measure definition is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example partially updates the given service test definition ID according to modifications provided in the request body.

```
curl "http://instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/89d2b920432a02104fefe4511fb8f22e " 
--request PATCH
--header "Accept:application/json" 
--user 'username':'password'
--data {
  "description": "Upstream and Downstream speed ",
  "name": "This is my new Speed Test",
  "testMeasureDefinition": [
    {
      "id": "1a04f560432a02104fefe4511fb8f2ad",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the downstream speed in a service",
      "metricName": "Downstream Speed",
      "name": "Downstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "30 Minutes",
      "validFor": {
        "startDateTime": "2024-05-30 08:49:26",
        "endDateTime": "2024-05-31 08:49:29"
      },
      "thresholdRule": [
        {
          "id": "a754f960432a02104fefe4511fb8f2d0",
          "description": "This speed is greater than the target upper",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "15 Minutes",
          "conformanceTargetLower": "75",
          "conformanceComparatorLower": "greater than",
          "consequence": [
            {
              "id": "15a4bd60432a02104fefe4511fb8f2b8",
              "prescribeAction": "null",
              "description": "generate a waring report",
              "name": "degradedQualityOfService",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:51:29",
                "endDateTime": "2024-08-06 08:51:31"
              }
            },
            {
              "id": "e6847d60432a02104fefe4511fb8f2c3",
              "prescribeAction": "null",
              "description": "send a warning to the system",
              "name": "packetdrop",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:50:53",
                "endDateTime": "2024-08-06 08:50:55"
              }
            }
          ]
        },
        {
          "id": "cb55b5a0432a02104fefe4511fb8f201",
          "description": "",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "medium",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "120",
          "conformanceComparatorUpper": "less than",
          "consequence": []
        }
      ]
    },
    {
      "id": "8f987524432a02104fefe4511fb8f2f0",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the upstream speed in the service",
      "metricName": "Upstream Speed",
      "name": "Upstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "",
      "validFor": {
        "startDateTime": "",
        "endDateTime": ""
      },
      "thresholdRule": []
    }
  ],
  "specCharacteristic": [
    {
      "name": "restart",
      "description": "restart",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2024-05-30 08:45:49"
      }
    }
  ],
  "serviceTestSpecRelationship": [
    {
      "id": "76a3b160432a02104fefe4511fb8f2ad",
      "name": "OAM Test",
      "relationshipType": ""
    }
  ],
  "relatedServiceSpecification": [
    {
      "id": "aeddcd1fb7d69910ff00f203ae11a990",
      "name": "Home Internet"
    }
  ]
}
```

The response body returns the updated portion of the service test specification:

```
{
  "description": "Upstream and Downstream speed ",
  "name": "This is my new Speed Test",
  "testMeasureDefinition": [
    {
      "id": "1a04f560432a02104fefe4511fb8f2ad",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the downstream speed in a service",
      "metricName": "Downstream Speed",
      "name": "Downstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "30 Minutes",
      "validFor": {
        "startDateTime": "2024-05-30 08:49:26",
        "endDateTime": "2024-05-31 08:49:29"
      },
      "thresholdRule": [
        {
          "id": "a754f960432a02104fefe4511fb8f2d0",
          "description": "This speed is greater than the target upper",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "15 Minutes",
          "conformanceTargetLower": "75",
          "conformanceComparatorLower": "greater than",
          "consequence": [
            {
              "id": "15a4bd60432a02104fefe4511fb8f2b8",
              "prescribeAction": "null",
              "description": "generate a waring report",
              "name": "degradedQualityOfService",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:51:29",
                "endDateTime": "2024-08-06 08:51:31"
              }
            },
            {
              "id": "e6847d60432a02104fefe4511fb8f2c3",
              "prescribeAction": "null",
              "description": "send a warning to the system",
              "name": "packetdrop",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:50:53",
                "endDateTime": "2024-08-06 08:50:55"
              }
            }
          ]
        },
        {
          "id": "cb55b5a0432a02104fefe4511fb8f201",
          "description": "",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "medium",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "120",
          "conformanceComparatorUpper": "less than",
          "consequence": []
        }
      ]
    },
    {
      "id": "8f987524432a02104fefe4511fb8f2f0",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the upstream speed in the service",
      "metricName": "Upstream Speed",
      "name": "Upstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "",
      "validFor": {
        "startDateTime": "",
        "endDateTime": ""
      },
      "thresholdRule": []
    }
  ],
  "specCharacteristic": [
    {
      "name": "restart",
      "description": "restart",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2024-05-30 08:45:49"
      }
    }
  ],
  "serviceTestSpecRelationship": [
    {
      "id": "76a3b160432a02104fefe4511fb8f2ad",
      "name": "OAM Test",
      "relationshipType": ""
    }
  ],
  "relatedServiceSpecification": [
    {
      "id": "aeddcd1fb7d69910ff00f203ae11a990",
      "name": "Home Internet"
    }
  ]
}
```

## Service Test Management Open API - POST /sn\_sprb\_mgmt/servicetestmanagement/serviceTest

Creates a service test.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTest`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="id_q31_zd1_qbc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="serviceTest-request-characteristic"><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test. For more information about test definition characteristics, see Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr id="serviceTest-request-characteristic.id"><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics. If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr id="serviceTest-request-characteristic.name"><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr id="serviceTest-request-characteristic.value"><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr id="serviceTest-request-characteristic.valueType"><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr id="serviceTest-request-description"><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr id="serviceTest-request-endDateTime"><td>

endDateTime

</td><td>

End date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="serviceTest-request-id"><td>

id

</td><td>

Sys\_id or external\_id of the service test. This ID creates a service test and is used as the external\_id.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr id="serviceTest-request-mode"><td>

mode

</td><td>

Mode that the service test is running in.Valid values:

-   ONDEMAND: Triggers the service test manually.
-   PROACTIVE: Triggers the service test automatically.

Data type: String

Default: ONDEMAND

</td></tr><tr id="serviceTest-request-name"><td>

name

</td><td>

Required. Name of the service test.Data type: String

</td></tr><tr id="serviceTest-request-relatedService"><td>

relatedService

</td><td>

Required. Test definition associated with the service test.Data type: Object

```
"relatedService": {
 "href": "String",
 "id": "String",
 "name": "String"
}
```

</td></tr><tr id="serviceTest-request-relatedService.href"><td>

relatedService.href

</td><td>

Hyperlink reference to the related service.Data type: String

</td></tr><tr id="serviceTest-request-relatedService.id"><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: In the sys\_id or external\_id field of the product Inventory \[sn\_prd\_invt\_product\_inventory\] table.

</td></tr><tr id="serviceTest-request-relatedService.name"><td>

relatedService.name

</td><td>

Name of the product inventory item.Data type: String

</td></tr><tr id="serviceTest-request-startDateTime"><td>

startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="serviceTest-request-state"><td>

state

</td><td>

State the service test is in. Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure"><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasure": [
 {
 "accuracy": "String",
 "captureDateTime": "String",
 "captureMethod": "String",
 "id": "String",
 "metricDescription": "String",
 "metricName": "String",
 "ruleViolation": [Array],
 "unitOfMeasure": "String",
 "value": {Object}
 }
]
```

</td></tr><tr id="serviceTest-request-testMeasure.accuracy"><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr id="serviceTest-request-testMeasure.captureDateTime"><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="serviceTest-request-testMeasure.id"><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the Test Measures.Data type: String

Table: In the sys\_id or external\_id fields of the Test Measures table \[sn\_st\_mgmt\_test\_measure\] table.

</td></tr><tr id="serviceTest-request-testMeasure.captureMethod"><td>

testMeasure.Measure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.metricDescription"><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.metricName"><td>

testMeasure.metricName

</td><td>

Name of the test measure metric.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation"><td>

testMeasure.ruleViolation

</td><td>

An object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"ruleViolation"[
  {
    appliedConsequence: [Array],
    conformanceTargetUpper: Number,
    conformanceComparatorUpper: "String",
    description: "String",
    id: "String",
    name: "String",
    numberOfAllowedCrossing: Number,
    thresholdRuleSeverity: "String",
    tolerancePeriod: "String"
  }
]
```

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence"><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence.appliedAction"><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence.description"><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence.id"><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence.name"><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.appliedConsequence.repeatAction"><td>

testMeasure.ruleViolation.appliedConsequence.repeatAction

</td><td>

Flag that indicates whether to repeat the consequence when a second violation occurs.Valid values:

-   true: Repeat the action.
-   false: Don't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceComporatorExact"><td>

testMeasure.ruleViolation.conformanceComporatorExact

</td><td>

Flag that indicates whether a value is identical.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceComporatorLower"><td>

testMeasure.ruleViolation.conformanceComporatorLower

</td><td>

Operator for checking if a value falls below the threshold.Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceComporatorUpper"><td>

testMeasure.ruleViolation.conformanceComporatorUpper

</td><td>

Operator for checking if a value is above the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceTargetExact"><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceTargetLower"><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.conformanceTargetUpper"><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.description"><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr id="serviceTest-request-test.Measure.ruleViolation.id"><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.name"><td>

testMeasure.ruleViolation.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.numberOfAllowedCrossing"><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr id="serviceTest-request-estMeasure.ruleViolation.thresholdRuleSeverity"><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.tolerancePeriod"><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Specified time interval during which crossing occurrences are enabled without triggering any immediate consequences or actions.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.amount"><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Number of periods before applying the consequence.Data type: Number

</td></tr><tr id="serviceTest-request-testMeasure.ruleViolation.tolerancePeriod.units"><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.unitOfMeasure"><td>

testMeasure.unitOfMeasure

</td><td>

Unit of measurement for the conformance target values of the test measure.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.value"><td>

testMeasure.value

</td><td>

Value of the test measure.Data type: Object

```
"value": {
 "id": "String",
 "name": "String",
 "valueType": "String",
 "value": "String
}
```

</td></tr><tr id="serviceTest-request-testMeasure.value.id"><td>

testMeasure.value.id

</td><td>

ID of the test measure value.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.value.name"><td>

testMeasure.value.name

</td><td>

Name of the test measure value.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.value.value"><td>

testMeasure.value.value

</td><td>

Value of the test measure.Data type: String

</td></tr><tr id="serviceTest-request-testMeasure.value.valueType"><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr id="serviceTest-request-testSpecification"><td>

testSpecification

</td><td>

Required. Test definition associated with this test. Data type: Object

```
"testSpecification": {
 "href": "String",
 "id": "String"
}
```

</td></tr><tr id="serviceTest-request-testSpecification.href"><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr id="serviceTest-request-testSpecification.id"><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: In the sys\_id or external\_id field of the Service Test Definition \[sn\_st\_mgmt\_test\_definition\] table.

</td></tr><tr id="serviceTest-request-validFor"><td>

validFor

</td><td>

Date range the service test is valid for.Data type: Object

```
"validFor": {
 "endDateTime ": "String",
 "startDateTime": "String"
}
```

</td></tr><tr id="serviceTest-request-validFor.endDateTime"><td>

validFor.endDateTime

</td><td>

Validity end date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="serviceTest-request-validFor.startDateTime"><td>

validFor.startDateTime

</td><td>

Validity start date of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

<table id="table_qzk_r2p_qbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

characteristic

</td><td>

List that describes the characteristics of the associated service test.Data type: Array of Objects

```
"characteristic": [
 {
  "id": "String",
  "name": "String",
  "value": "String",
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

characteristic.id

</td><td>

Sys\_id or external\_id of characteristics. If external\_id is present for that record, the response returns the external\_id otherwise it returns the sys\_id.Data type: String

Table: Characteristics \[sn\_prd\_pm\_characteristic\]

</td></tr><tr><td>

characteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

characteristic.value

</td><td>

Characteristic options associated with the service test. Characteristics vary based on the customer instance.Data type: String

</td></tr><tr><td>

characteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the service test.Data type: String

</td></tr><tr><td>

endDateTime

</td><td>

End date and time of the service test.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

mode

</td><td>

Mode that the service test is running in.Valid values:

-   ONDEMAND: Triggers the service test manually.
-   PROACTIVE: Triggers the service test automatically.

Data type: String

Default: ONDEMAND

</td></tr><tr><td>

name

</td><td>

Name of the service test.Data type: String

</td></tr><tr><td>

relatedService

</td><td>

Test definition associated for this test.Data type: Object

```
"relatedService": {
  "href": "string",
  "id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

relatedService.id

</td><td>

Sys\_id or external\_id of the product inventory.Data type: String

Table: Product Inventory \[sn\_prd\_invt\_product\_inventory\]

</td></tr><tr><td>

relatedService.name

</td><td>

Name of the product inventory.Data type: String

</td></tr><tr><td>

startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

state

</td><td>

State of the service test.Valid values:

-   acknowledged
-   canceled
-   completed
-   failed
-   inProgress
-   pending
-   rejected

Data type: String

</td></tr><tr><td>

testMeasure

</td><td>

Measure of a specific aspect of a product, service, or resource test, such as lost packets or connectivity status.Data type: Array of Objects

```
"testMeasureDefinition": [
 {
  "accuracy": "String",
  "captureDateTime": "String",
  "captureMethod": "String",
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "ruleViolation": [Array]
  "unitOfMeasure": "String",
  "value": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.accuracy

</td><td>

Float decimal value representing the test measure accuracy captured for the associated metrics.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasure.captureDateTime

</td><td>

The date and time that the metric was captured.Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasure.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasure.id

</td><td>

Sys\_id or external\_id of the test measure.Data type: String

Table: Test Measures \[sn\_st\_mgmt\_test\_measure\]

</td></tr><tr><td>

testMeasure.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasure.metricName

</td><td>

Name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation

</td><td>

Object for defining a rule in the threshold rule definition, along with consequences if the rule is violated.Data type: Array of Objects

```
"RuleViolation": [
{
  "appliedConsequence": [Array],
  "conformanceComparatorExact": Boolean,
  "conformanceComparatorLower": "String",
  "conformanceComparatorUpper": "String",
  "conformanceTargetExact": "String",
  "conformanceTargetLower": "String",
  "conformanceTargetUpper": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "numberOfAllowedCrossing": Number,
  "thresholdRuleSeverity": "String",
  "tolerancePeriod": {Object}
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is violated.Data type: Array of Objects

```
"appliedConsequence": [
 {
  "appliedAction": "String",
  "description": "String",
  "id": "String",
  "name": "String",
  "repeatAction": Boolean
 }
]
```

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction

</td><td>

Action to take when a threshold rule is violated. For example, sending a warning or generating a report. Applied actions can vary between instances.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.appliedAction.repeatAction

</td><td>

Flag that indicates whether to repeat the applied action or not.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.description

</td><td>

Description of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.id

</td><td>

Sys\_id or external\_id of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.appliedConsequence.name

</td><td>

Name of the applied consequence.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value of **conformanceTargetExact**.Valid values:

-   true: The value is identical.
-   false: The value isn't identical.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorLower

</td><td>

An operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   is

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceComparatorUpper

</td><td>

An operator that checks if a value exceeds the threshold.Valid values:

-   is
-   lesser than

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results. Determines if the threshold is crossed or no longer crossed.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.description

</td><td>

Description of the threshold rule violation.Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.id

</td><td>

Sys\_id or external\_id of the threshold rule violation.Data type: String

Table: Threshold Rule Violation \[sn\_st\_mgmt\_threshold\_rule\_violation\]

</td></tr><tr><td>

testMeasure.ruleViolation.name

</td><td>

Name of the threshold rule violation.Date type: String

</td></tr><tr><td>

testMeasure.ruleViolation.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum: 40

</td></tr><tr><td>

testMeasure.ruleViolation.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   low
-   medium

Data type: String

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod

</td><td>

Duration or time interval in which allowed crossings can occur before a consequence is initiated.Date type: Object

```
"tolerancePeriod": {
 "amount": Number,
 "units": "String"
}
```

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.amount

</td><td>

Amount of the period in number.Data type: Number

</td></tr><tr><td>

testMeasure.ruleViolation.tolerancePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasure.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasure.value

</td><td>

Value of metric in the test.Data type: Object

```
"value": {
  "id": "String",
  "name": "String",
  "valueType": "String",
  "value": "String"
}
```

</td></tr><tr><td>

testMeasure.value.id

</td><td>

ID of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.name

</td><td>

Name of the metric value in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.value

</td><td>

Value of metric in the test.Data type: String

</td></tr><tr><td>

testMeasure.value.valueType

</td><td>

Type of test measure value such as numeric, text, and so forth.Data type: String

</td></tr><tr><td>

testSpecification

</td><td>

Test definition associated for this test. Data type: Object

```
"testSpecification": {
  "href": "String",
  "id": "String"
}
```

</td></tr><tr><td>

testSpecification.href

</td><td>

Hyperlink reference to the service test definition.Data type: String

</td></tr><tr><td>

testSpecification.id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

validFor

</td><td>

Date range that the service test is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and timestamp of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example creates a new service test according to specific details provided in the request body.

```
curl "https:/instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTest" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data {
  "description": "Service test",
  "endDateTime": "2025-01-31 15:05:43",
  "mode": "proactive",
  "name": "Speed Test TR0001002",
  "startDateTime": "2024-06-05 09:07:10",
  "validFor": {
    "startDateTime": "",
    "endDateTime": ""
  },
  "relatedService": {
    "id": "fa6d13f45b5620102dff5e92dc81c77f",
    "name": "Internet_VPLS_PI0000011"
  },
  "testSpecification": {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/76a3b160432a02104fefe4511fb8f2ad",
    "id": "76a3b160432a02104fefe4511fb8f2ad"
  },
  "characteristic": [
    {
      "id": "e7ef960443f202104fefe4511fb8f224",
      "name": "AccessRequired",
      "valueType": "yes_no",
      "value": "Yes"
    }
  ],
  "testMeasure": [
    {
      "id": "61d1382e3be28210d140068aa4e45a2e",
      "accuracy": "0.0001",
      "captureDateTime": "",
      "captureMethod": "automatic",
      "metricDescription": "",
      "metricName": "Flow speed",
      "unitOfMeasure": "A second",
      "value": "3000",
      "ruleViolation": [
        {
          "id": "61d1382e3be28210d140068aa4e45a2f",
          "description": "This speed is greater than the target",
          "name": "tooMuchTraffic",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "",
          "conformanceTargetLower": "2500",
          "conformanceComparatorLower": "greater than",
          "appliedConsequence": [
            {
              "id": "65d1382e3be28210d140068aa4e45a31",
              "appliedAction": "sendWarning",
              "description": "send a warning to the system",
              "name": "sendWarning",
              "repeatAction": "0"
            }
          ]
        }
      ]
    }
  ]
}
```

The response returns confirmation details about the new test service and assigns it a unique ID, 2b406ec043b202104fefe4511fb8f211:

```
{
  "description": "Service test",
  "endDateTime": "2025-01-31 15:05:43",
  "mode": "proactive",
  "name": "Speed Test TR0001002",
  "startDateTime": "2024-06-05 09:07:10",
  "validFor": {
    "startDateTime": "",
    "endDateTime": ""
  },
  "relatedService": {
    "id": "fa6d13f45b5620102dff5e92dc81c77f",
    "name": "Internet_VPLS_PI0000011"
  },
  "testSpecification": {
    "href": "/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification/76a3b160432a02104fefe4511fb8f2ad",
    "id": "76a3b160432a02104fefe4511fb8f2ad"
  },
  "characteristic": [
    {
      "id": "e7ef960443f202104fefe4511fb8f224",
      "name": "AccessRequired",
      "valueType": "yes_no",
      "value": "Yes"
    }
  ],
  "testMeasure": [
    {
      "id": "61d1382e3be28210d140068aa4e45a2e",
      "accuracy": "0.0001",
      "captureDateTime": "",
      "captureMethod": "automatic",
      "metricDescription": "",
      "metricName": "Flow speed",
      "unitOfMeasure": "A second",
      "value": "3000",
      "ruleViolation": [
        {
          "id": "61d1382e3be28210d140068aa4e45a2f",
          "description": "This speed is greater than the target",
          "name": "tooMuchTraffic",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "",
          "conformanceTargetLower": "2500",
          "conformanceComparatorLower": "greater than",
          "appliedConsequence": [
            {
              "id": "65d1382e3be28210d140068aa4e45a31",
              "appliedAction": "sendWarning",
              "description": "send a warning to the system",
              "name": "sendWarning",
              "repeatAction": "0"
            }
          ]
        }
      ]
    }
  ],
  "id": "2b406ec043b202104fefe4511fb8f211"
}
```

## Service Test Management Open API - POST /sn\_sprb\_mgmt/servicetestmanagement/serviceTestSpecification

Creates a new service test definition.

### URL format

Default URL: `/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="id_thr_xwn_qbc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="testSpec-request-description-param"><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr id="testSpec-request-id-param"><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr id="testSpec-request-name-param"><td>

name

</td><td>

Required. Name of the service test definition.Data type: String

</td></tr><tr id="testSpec-request-relatedServiceSpecification-param"><td>

relatedServiceSpecification

</td><td>

Required. Service specifications of the test definition.Data type: Array of Objects

```
"relatedServiceSpecification": [
  {
    "id": "String",
    "name": "String"
  }
]
```

</td></tr><tr id="testSpec-request-relatedServiceSpecification.id-param"><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr id="testSpec-request-relatedServiceSpecification.name-param"><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of objects

```
"serviceTestSpecRelationship": [
{
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: In the sys\_id or external\_id field of the Test Definition \[sn\_st\_mgmt\_test\_definition\] table.

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Valid values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr id="testSpec-request-specCharacteristics-param"><td>

specCharacteristic

</td><td>

Characteristics of the test definition.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr id="testSpec-request-specCharacteristics.characteristicValueSpecification-param"><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
  {
    "value": "String"
  }
]
```

</td></tr><tr id="testSpec-request-specCharacteristic.characteristicValueSpecification.value-param"><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr id="testSpec-request-specCharacteristic.characteristicValueSpecification.descr-param"><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr id="testSpec-request-specCharacteristic.characteristicValueSpecification.name-param"><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr id="testSpec-request-specCharacteristic.validFor-param"><td>

specCharacteristic.validFor

</td><td>

Date range that the characteristic is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr id="testSpec-request-specCharacteristic.validFor.endDateTime-param"><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr id="testSpec-request-specCharacteristic.validFor.startDateTime-param"><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

Data type: String

</td></tr><tr id="testSpec-request-specCharacteristic.valueType-param"><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition-param"><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. For more information, see [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.captureFrequency-param"><td>

testMeasureDefinition.captureFrequency

</td><td>

The frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.captureMethod-param"><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Doesn't capture the metric.

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.capturePeriod-param"><td>

testMeasureDefinition.capturePeriod

</td><td>

Period or duration of the metric capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.capturePeriod.amount-param"><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr id="testSpec-request-testMeasureDefinition.capturePeriod.units-param"><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Valid values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.id-param"><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the test measure definitions.Data type: String

Table: Test Measure definition table \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr id="testSpec-request-testMeasureDefinition.metricDescription-param"><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.metricName-param"><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.name-param"><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule-param"><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines conditions to achieve before applying consequences when a threshold is crossed \(or not crossed\)​ in the test measure definition. For more information, [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US).Data type: Array of Objects

```
{
  "thresholdRule": {
    "consequence": [Array],
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": {Object}
  }
}
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.ComporatorExact-param"><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value set for **testMeasureDefinition.thresholdRule.conformanceTargetExact**. If set to true, **testMeasureDefinition.thresholdRule.conformanceTargetExact** is required.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.ComporatorLower-param"><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   greater than or is

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.ComporatorUpper-param"><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   less than
-   less than or is

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.TargetExact-param"><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.TargetLower-param"><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.TargetUpper-param"><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence-param"><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed. See [Define threshold rules for a test measure definition](https://www.servicenow.com/docs/access?context=define-threshold-rules&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more information.Data type: Array of objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.description-param"><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.id-param"><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.name-param"><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.prescribeAction-param"><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.repeatAction-param"><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied consequence.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.validFor-param"><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime-param"><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime-param"><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.description-param"><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.id-param"><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: In the sys\_id or external\_id field of the Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\] table.

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.name-param"><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.numberOfAllowedCrossing-param"><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr id="testSpec-request-testMeasureDefinition.thresholdRule.thresholdRuleSeverity-param"><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity level of the threshold rule.Valid values:

-   high
-   medium
-   low

Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.unitOfMeasure-param"><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr id="testSpec-request-testMeasureDefinition.validFor-param"><td>

testMeasureDefinition.validFor

</td><td>

Date range that the test measure definition is valid for.Data type: String

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr id="testSpec-request-testMeasureDefinition.validFor.endDateTime-param"><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="testSpec-request-testMeasureDefinition.validFor.startDateTime-param"><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="testSpec-request-validFor-param"><td>

validFor

</td><td>

Date range that the test definition is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr id="testSpec-request-validFor.endDateTime-param"><td>

validFor.endDateTime

</td><td>

Date and time of the test definition on which the state of it is retired. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr id="testSpec-request-validFor.startDateTime-param"><td>

validFor.startDateTime

</td><td>

Date and time of the test definition on which the state of it is published. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports application/json.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON or XML\)

<table id="table_qqg_3s4_qbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the service test definition.Data type: String

</td></tr><tr><td>

id

</td><td>

Sys\_id or external\_id of the service test definition.Data type: String

Table: Service Test \[sn\_st\_mgmt\_test\]

</td></tr><tr><td>

name

</td><td>

Name of the service test definition.Data type: String

</td></tr><tr><td>

relatedServiceSpecification

</td><td>

Service specifications for the test definitions.Data type: Array of Objects

```
"relatedServiceSpecification": [
 {
  "id": "String",
  "name": "String"
 }
]
```

</td></tr><tr><td>

relatedServiceSpecification.id

</td><td>

Sys\_id or external\_id of the service specification.Data type: String

Table: In the sys\_id or external\_id field of the Specification \[sn\_prd\_pm\_specification\] table.

</td></tr><tr><td>

relatedServiceSpecification.name

</td><td>

Name of the service specification.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship

</td><td>

Related service test definition.Data type: Array of Objects

```
"serviceTestSpecRelationship": [
 {
  "id": "String",
  "name": "String",
  "relationshipType": "String"
 }
]
```

</td></tr><tr><td>

serviceTestSpecRelationship.id

</td><td>

Sys\_id or external\_id of the related service test definition.Data type: String

Table: Test Definition \[sn\_st\_mgmt\_test\_definition\]

</td></tr><tr><td>

serviceTestSpecRelationship.name

</td><td>

Name of the related test definition.Data type: String

</td></tr><tr><td>

serviceTestSpecRelationship.relationshipType

</td><td>

Type of relationship.Accepted values:

-   dependency
-   exclusivity
-   substitution

Data type: String

</td></tr><tr><td>

specCharacteristic

</td><td>

Test definition characteristics.Data type: Array of Objects

```
"specCharacteristic": [
 {
  "characteristicValueSpecification": [Array],
  "description": "String",
  "name": "String",
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification

</td><td>

Possible values of the characteristic.Data type: Array of Objects

```
"characteristicValueSpecification": [
 {
  "value": "String"
 }
]
```

</td></tr><tr><td>

specCharacteristic.characteristicValueSpecification.value

</td><td>

Value of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.description

</td><td>

Description of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.name

</td><td>

Name of the characteristic.Data type: String

</td></tr><tr><td>

specCharacteristic.validFor

</td><td>

Date range the characteristic is valid for.Data type: Object

```
"validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
}
```

</td></tr><tr><td>

specCharacteristic.validFor.endDateTime

</td><td>

End date of the characteristic. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

specCharacteristic.validFor.startDateTime

</td><td>

Start date of the characteristic. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

specCharacteristic.valueType

</td><td>

Type of characteristic value.-   choice
-   date
-   date/time
-   duration
-   email
-   label
-   single line test
-   yes/no

Data type: String

</td></tr><tr><td>

testMeasureDefinition

</td><td>

Test measure definitions for this service test definition. See [Define test measure definitions for a service test](https://www.servicenow.com/docs/access?context=define-test-measure-spm&version=australia&pubname=australia-telecom-media-technology&ft:locale=en-US) for more infomation.Data type: Array of Objects

```
"testMeasureDefinition": [
 {
  "captureFrequency": "String",
  "captureMethod": "String",
  "capturePeriod": {Object},
  "id": "String",
  "metricDescription": "String",
  "metricName": "String",
  "name": "String",
  "unitOfMeasure": "String",
  "thresholdRule": [Array],
  "validFor": {Object},
  "valueType": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.captureFrequency

</td><td>

Frequency at which to capture the metric. Valid values:

-   daily
-   monthly
-   none
-   once
-   weekly

Data type: String

</td></tr><tr><td>

testMeasureDefinition.captureMethod

</td><td>

Method used to capture the metric.Valid values:

-   automatic: Automatically capture the metric.
-   manual: Manually capture the metric.
-   none: Don't capture the metric.

Data type: String

</td></tr><tr><td>

testMeasureDefinition.capturePeriod

</td><td>

Duration or period of the capture.Data type: Object

```
"capturePeriod": {
  "amount": Number,
  "units": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.amount

</td><td>

Number of capture periods.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.capturePeriod.units

</td><td>

Units of the period.Accepted values:

-   days
-   hours
-   minutes
-   seconds

Data type: String

</td></tr><tr><td>

testMeasureDefinition.id

</td><td>

Sys\_id or external\_id of the Test Measure definitions.Data type: String

Table: Test Measure definition \[sn\_st\_mgmt\_test\_measure\_definition\]

</td></tr><tr><td>

testMeasureDefinition.metricDescription

</td><td>

Brief description of the metric.Data type: String

</td></tr><tr><td>

testMeasureDefinition.metricName

</td><td>

User-defined name of a metric in the test measure.Data type: String

</td></tr><tr><td>

testMeasureDefinition.name

</td><td>

Name of the test measure definition.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule

</td><td>

Rule that defines the condition \(raise or clear\) to achieve to apply consequences when a threshold is crossed or ceased to be crossed​ for a particular test measure definition.Data type: Array of Objects

```
{
  "thresholdRule": {
    "conformanceComparatorExact": Boolean,
    "conformanceComparatorLower": "String",
    "conformanceComparatorUpper": "String",
    "conformanceTargetExact": "String",
    "conformanceTargetLower": "String",
    "conformanceTargetUpper": "String",
    "consequence": [Array],
    "description": "String",
    "id": "String",
    "name": "String",
    "numberOfAllowedCrossing": Number,
    "thresholdRuleSeverity": "String",
    "tolerancePeriod": Object
  }
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorExact

</td><td>

Flag that indicates whether a value is identical to the value of **conformanceTargetExact**.Valid values:

-   true: The value is identical to the value of **conformanceTargetExact**.
-   false: The value isn't identical **conformanceTargetExact**.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorLower

</td><td>

Operator that checks if a value falls below the threshold. Valid values:

-   greater than
-   is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceComparatorUpper

</td><td>

Operator that checks if a value exceeds the threshold.Valid values:

-   lesser than
-   is

Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetExact

</td><td>

Required if **conformanceComparatorExact** is set to true. If the **conformanceComparatorExact** value is set to true, its value matches the value defined in **conformanceTargetExact**.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetLower

</td><td>

Lower threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.conformanceTargetUpper

</td><td>

Upper threshold value for comparing the test measure results.Data type: Number

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence

</td><td>

Action \(prescribed action or notification\) to take when a threshold rule is crossed.Data type: Array of Objects

```
"consequence": [
 {
  "description": "String",
  "id": "String",
  "name": "String",
  "prescribeAction": "String",
  "repeatAction": Boolean,
  "validFor": {
  "endDateTime": "String",
  "startDateTime": "String"
 }
]
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.description

</td><td>

Description of the consequence. Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.id

</td><td>

Sys\_id or external\_id of the measure consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.name

</td><td>

Name of the consequence.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.prescribeAction

</td><td>

User-defined action to take for threshold violations. Actions vary between instances.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.repeatAction

</td><td>

Flag that indicates whether to repeat the applied action or not.Valid values:

-   true: Repeats the action.
-   false: Doesn't repeat the action.

Data type: Boolean

Default: false

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor

</td><td>

Date range that the consequence is valid for.Data type: Object

```
"validFor": {
 "startDateTime": "String",
 "endDateTime ": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.endDateTime

</td><td>

Validity end date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.consequence.validFor.startDateTime

</td><td>

Validity start date of the consequence. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.description

</td><td>

Description of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.id

</td><td>

Sys\_id or external\_id of the threshold rules.Data type: String

Table: Threshold Rules \[sn\_st\_mgmt\_threshold\_rule\]

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.name

</td><td>

Name of the threshold rule.Data type: String

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.numberOfAllowedCrossing

</td><td>

Maximum crossings allowed within the tolerance period before consequences are applied.Data type: Number

Maximum value: 40

</td></tr><tr><td>

testMeasureDefinition.thresholdRule.thresholdRuleSeverity

</td><td>

Severity of the threshold rule.Valid values:

-   high
-   low
-   medium

Data type: String

</td></tr><tr><td>

testMeasureDefinition.unitOfMeasure

</td><td>

Measurable value of time used to calculate the performance of a service in days, minutes, and seconds.Data type: String

</td></tr><tr><td>

testMeasureDefinition.validFor

</td><td>

Date range the test measure definition is valid for.Data type: Object

```
"validFor": {
 "endDateTime": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

testMeasureDefinition.validFor.endDateTime

</td><td>

Validity end date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

testMeasureDefinition.validFor.startDateTime

</td><td>

Validity start date of the test measure definition. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor

</td><td>

Date range the service test is valid for.Data type: Object

```
"validFor": {
 "endDateTime ": "String",
 "startDateTime": "String"
}
```

</td></tr><tr><td>

validFor.endDateTime

</td><td>

End date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr><tr><td>

validFor.startDateTime

</td><td>

Start date and time of the service test. Data type: String

Format: YYYY-MM-DD 00:00:00. For example, `2025-01-31 09:35:43`.

</td></tr></tbody>
</table>### cURL request

The following example creates a new service test definition.

```
curl "https:/instance.servicenow.com/api/sn_sprb_mgmt/servicetestmanagement/serviceTestSpecification" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--user 'username':'password'
-- data {
  "description": "Upstream and Downstream speed ",
  "name": "Speed Test",
  "validFor": {
    "startDateTime": "2024-05-31",
    "endDateTime": "2024-06-27"
  },
  "testMeasureDefinition": [
    {
      "id": "1a04f560432a02104fefe4511fb8f2ad",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the downstream speed in a service",
      "metricName": "Downstream Speed",
      "name": "Downstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "30 Minutes",
      "validFor": {
        "startDateTime": "2024-05-30 08:49:26",
        "endDateTime": "2024-05-31 08:49:29"
      },
      "thresholdRule": [
        {
          "id": "a754f960432a02104fefe4511fb8f2d0",
          "description": "This speed is greater than the target upper",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "15 Minutes",
          "conformanceTargetLower": "75",
          "conformanceComparatorLower": "greater than",
          "consequence": [
            {
              "id": "15a4bd60432a02104fefe4511fb8f2b8",
              "prescribeAction": "null",
              "description": "generate a waring report",
              "name": "degradedQualityOfService",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:51:29",
                "endDateTime": "2024-08-06 08:51:31"
              }
            },
            {
              "id": "e6847d60432a02104fefe4511fb8f2c3",
              "prescribeAction": "null",
              "description": "send a warning to the system",
              "name": "packetdrop",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:50:53",
                "endDateTime": "2024-08-06 08:50:55"
              }
            }
          ]
        },
        {
          "id": "cb55b5a0432a02104fefe4511fb8f201",
          "description": "",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "medium",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "120",
          "conformanceComparatorUpper": "less than",
          "consequence": []
        }
      ]
    },
    {
      "id": "8f987524432a02104fefe4511fb8f2f0",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the upstream speed in the service",
      "metricName": "Upstream Speed",
      "name": "Upstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "",
      "validFor": {
        "startDateTime": "",
        "endDateTime": ""
      },
      "thresholdRule": []
    }
  ],
  "specCharacteristic": [
    {
      "name": "restart",
      "description": "restart",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2024-05-30 08:45:49"
      },
      "characteristicValueSpecification": [
        {
          "value": "No",
        },
        {
          "value": "Yes",
        }
      ]
    }
  ],
  "serviceTestSpecRelationship": [
    {
      "id": "76a3b160432a02104fefe4511fb8f2ad",
      "name": "OAM Test",
      "relationshipType": ""
    }
  ],
  "relatedServiceSpecification": [
    {
      "id": "aeddcd1fb7d69910ff00f203ae11a990",
      "name": "Home Internet"
    }
  ]
}
```

Response body.

```
{
  "description": "Upstream and Downstream speed ",  
  "name": "Speed Test",
  "validFor": {
    "startDateTime": "2024-05-31",
    "endDateTime": "2024-06-27"
  },
  "testMeasureDefinition": [
    {
      "id": "1a04f560432a02104fefe4511fb8f2ad",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the downstream speed in a service",
      "metricName": "Downstream Speed",
      "name": "Downstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "30 Minutes",
      "validFor": {
        "startDateTime": "2024-05-30 08:49:26",
        "endDateTime": "2024-05-31 08:49:29"
      },
      "thresholdRule": [
        {
          "id": "a754f960432a02104fefe4511fb8f2d0",
          "description": "This speed is greater than the target upper",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "high",
          "tolerancePeriod": "15 Minutes",
          "conformanceTargetLower": "75",
          "conformanceComparatorLower": "greater than",
          "consequence": [
            {
              "id": "15a4bd60432a02104fefe4511fb8f2b8",
              "prescribeAction": "null",
              "description": "generate a waring report",
              "name": "degradedQualityOfService",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:51:29",
                "endDateTime": "2024-08-06 08:51:31"
              }
            },
            {
              "id": "e6847d60432a02104fefe4511fb8f2c3",
              "prescribeAction": "null",
              "description": "send a warning to the system",
              "name": "packetdrop",
              "repeatAction": "0",
              "validFor": {
                "startDateTime": "2024-05-30 08:50:53",
                "endDateTime": "2024-08-06 08:50:55"
              }
            }
          ]
        },
        {
          "id": "cb55b5a0432a02104fefe4511fb8f201",
          "description": "",
          "name": "InternetSpeedValue",
          "numberOfAllowedCrossing": "0",
          "thresholdRuleSeverity": "medium",
          "tolerancePeriod": "",
          "conformanceTargetUpper": "120",
          "conformanceComparatorUpper": "less than",
          "consequence": []
        }
      ]
    },
    {
      "id": "8f987524432a02104fefe4511fb8f2f0",
      "captureFrequency": "once",
      "captureMethod": "automatic",
      "metricDescription": "This is the upstream speed in the service",
      "metricName": "Upstream Speed",
      "name": "Upstream Speed",
      "unitOfMeasure": "a second",
      "valueType": "",
      "capturePeriod": "",
      "validFor": {
        "startDateTime": "",
        "endDateTime": ""
      },
      "thresholdRule": []
    }
  ],
  "specCharacteristic": [
    {
      "name": "restart",
      "description": "restart",
      "valueType": "yes_no",
      "validFor": {
        "startDatetime": "2024-05-30 08:45:49"
      },
      "characteristicValueSpecification": [
        {
          "value": "No",
          "validFor": {
            "startDateTime": "",
            "endDateTime": ""
          }
        },
        {
          "value": "Yes",
          "validFor": {
            "startDateTime": "",
            "endDateTime": ""
          }
        }
      ]
    }
  ],
  "serviceTestSpecRelationship": [
    {
      "id": "76a3b160432a02104fefe4511fb8f2ad",
      "name": "OAM Test",
      "relationshipType": ""
    }
  ],
  "relatedServiceSpecification": [
    {
      "id": "aeddcd1fb7d69910ff00f203ae11a990",
      "name": "Home Internet"
    }
  ]
  "id": "89d2b920432a02104fefe4511fb8f22e"
}

```

