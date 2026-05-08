---
title: Predictive Intelligence API
description: The Predictive Intelligence API provides endpoints that predict a field value based on one or more input fields and a trained solution.Predicts an output field value using a specific solution.Returns predictions for multiple solutions.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Predictive Intelligence API

The Predictive Intelligence API provides endpoints that predict a field value based on one or more input fields and a trained solution.

You can only use this API when the Predictive Intelligence \(com.glide.platform\_ml\) plugin is activated.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Predictive Intelligence - GET /agent\_intelligence/solution/\{solution\_name\}/prediction

Predicts an output field value using a specific solution.

### URL format

Default URL: `/api/now/agent_intelligence/solution/{solution_name}/prediction`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

solution\_name

</td><td>

Name of solution to use for predictions. For example, `ml_incident_categorization`.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Solution definition input field key-value pair

</td><td>

Name-value pair of the solution input field. For example, enter the name: `short_description` and the value: `Unable to connect to VPN`. Data type: String

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

Name-value pairs that were specified as input to the call.Data type: Object

</td></tr><tr><td>

output

</td><td>

Predicted outcome values based on the specified solution.Data type: Object

 ```
"output": {
  "confidence": Number",
  "outcome": "String",
  "threshold": Number"
}
```

</td></tr><tr><td>

output.confidence

</td><td>

Estimated precision of the prediction as a percentage. For example, **53.84615375762915**.Data type: Number

</td></tr><tr><td>

output.outcome

</td><td>

Prediction output field value. For example, an incident categorization solution would return an incident category such as **inquiry**.Data type: String

</td></tr><tr><td>

output.threshold

</td><td>

Value of the configured threshold associated with the prediction. Data type: Number

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/now/predictive_intelligence/solution/ml_incident_categorization/prediction?short_description=unable%20to%20connect%20to%20VPN" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "input": {
      "short_description": "unable to connect to VPN",
      "api": "api"
    },
    "output": {
      "outcome": "inquiry",
      "confidence": 53.84615375762915,
      "threshold": 5
    }
  }
}
```

## Predictive Intelligence - GET /agent\_intelligence/solution/prediction

Returns predictions for multiple solutions.

**Note:** Outcome result objects are grouped by solution name and sys\_id in the format `result.<solutionname>.<sys_id>.[{ <result1> },{ <result2>}]`.

For customization information, see MLSolutionFactory scriptable objects.

### URL format

Versioned URL: `/now/{api_version}/agent_intelligence/solution/prediction`

Default URL: `/now/agent_intelligence/solution/prediction`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input\_filter

</td><td>

Required parameter if **input\_table** is used, don't use this parameter with **input\_maps** parameter. Filter to select records on which to run predictions. For example:```
sys_id 0ef47232db801300864adfea5e961912
```

Data type: String

</td></tr><tr><td>

input\_maps

</td><td>

Required unless using **input\_table** parameter. Array of input name-value pairs. For example: ```
[{"short_description":"my email is not working"}, {"short_description":"need help with password"}]
```

Data type: Array of Objects

</td></tr><tr><td>

input\_table

</td><td>

Required unless using **input\_maps** parameter. Table name on which you want to run predictions. For example:```
incident
```

Data type: String

</td></tr><tr><td>

options

</td><td>

JSON object with optional arguments. For example:```
{"top_n" : 5, "apply_threshold":false}
```

Valid options:

-   top\_n: Number. If provided, returns the top results, up to the specified number of predictions.
-   apply\_threshold: Boolean. Checks the threshold value for the solution and applies it to the result set. The threshold value is solution threshold for similarity or class-level threshold for classification. Default value is true.
-   custom\_results\_filter: String. Similarity solutions only. Specifies the allowed set from which results are returned using an encoded query.

Data type: Object

</td></tr><tr><td>

solution\_names

</td><td>

Required. Comma-separated list of solution names for which you want to run predictions. For example:```
ml_incident_categorization,ml_incident_assignment
```

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
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

confidence

</td><td>

Value of the confidence associated with the prediction. For example, 53.84. Data type: Number

</td></tr><tr><td>

predictedSysId

</td><td>

The sys\_id of the predicted value. Results can be from any table on which information is being predicted. Data type: String

</td></tr><tr><td>

predictedValue

</td><td>

Value representing the prediction result. Data type: String

</td></tr><tr><td>

threshold

</td><td>

Value of the configured threshold associated with the prediction. Data type: Number

</td></tr></tbody>
</table>### Sample cURL request

```
curl "http://instance.servicenow.com/api/now/agent_intelligence/solution/prediction?input_table=incident&input_filter=sys_id%3D0ef47232db801300864adfea5e961912&solution_names=ml_incident_categorization%2Cml_incident_assignment&options=%7B%22top_n%22%20%3A%202%2C%20%22apply_threshold%22%3Afalse%7D" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"
```

```
{
  "result": {
    "ml_incident_categorization": {
      "0ef47232db801300864adfea5e961912": [
        {
          "confidence": 29.12211732875455,
          "threshold": 15,
          "predictedValue": "Email",
          "predictedSysId": ""
        },
        {
          "confidence": 19.08583525847071,
          "threshold": 14,
          "predictedValue": "Platform Performance",
          "predictedSysId": ""
        }
      ]
    },
    "ml_incident_assignment": {
      "0ef47232db801300864adfea5e961912": [
        {
          "confidence": 5.782322543467415,
          "threshold": 5,
          "predictedValue": "IT Finance CAB",
          "predictedSysId": "5f63e48fc0a8010e00eeaad81cd4dd37"
        },
        {
          "confidence": 5.303589009246953,
          "threshold": -1,
          "predictedValue": "NY DB",
          "predictedSysId": "5f74727dc0a8010e01efe33a251993f9"
        }
      ]
    }
  }
}

```

