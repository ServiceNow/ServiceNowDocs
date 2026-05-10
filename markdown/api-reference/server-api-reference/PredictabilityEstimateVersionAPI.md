---
title: PredictabilityEstimateVersion - Global
description: The PredictabilityEstimateVersion API is a scriptable object used in Predictive Intelligence stores.Gets predictability estimate object properties and version number.Returns JSON results containing suggested input fields for an output field.Gets training completion status.Gets the version number of a predictability estimate object.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PredictabilityEstimateVersion- Global

The PredictabilityEstimateVersion API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

Use this API when working with predictability estimate versions based on [PredictabilityEstimate API](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) objects in the [PredictabilityEstimate store](../../PredictabilityEstimateStore/concept/PredictabilityEstimateStoreAPI.md#).

The system activates the most recent version of the predictability estimate when it completes training, and only allows one version to be active at a time. However, you can activate any previously trained version you want to use to make predictions.

Methods in this API are accessible using the following PredictabiltyEstimate methods:

-   [getActiveVersion\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)
-   [getAllVersions\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)
-   [getLatestVersion\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)
-   [getVersion\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PredictabilityEstimateVersion - getProperties\(\)

Gets predictability estimate object properties and version number.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_e2m_zwz_4lb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Contents of the Dataset and [PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) version details. Results vary by object property setup.```
{
  "datasetProperties": {Object},
  "domainName": "String", 
  "inputFieldNames": [Array],
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "scope": "String",
  "trainingFrequency": "String",
  "versionNumber": "Number"
}
```

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties

</td><td>

Lists the properties of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object associated with the predictability estimate.

 ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

 Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames.fieldDetails

</td><td>

List of JavaScript objects that specify field properties. ```
[
  {
    "name": "String",
    "type": "String"
  }
]
```

 Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames.fieldDetails.&lt;object&gt;.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails.&lt;object&gt;.type

</td><td>

Machine-learning field type. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails.encodedQuery

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/domain-separation-predictive-intelligence.md). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.inputFieldNames

</td><td>

List of candidate input fields as strings to be considered for estimation.Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.isActive

</td><td>

Flag that indicates whether this version is active.Valid values:

-   true: Version is active.
-   false: Version is not active.

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.label

</td><td>

Identifies the prediction task. ```
{
  "label": "my first prediction"
}
```

 Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

System-assigned name. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.predictedFieldName

</td><td>

Identifies a field to be trained for predictability. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.scope

</td><td>

Object scope. Currently the only valid value is `global`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.trainingFrequency

</td><td>

The frequency to retrain the model. Possible values:

-   every\_30\_days
-   every\_60\_days
-   every\_90\_days
-   every\_120\_days
-   every\_180\_days
-   run\_once

Default: run\_once

 Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.versionNumber

</td><td>

Version number of the PredictabilityEstimate object.Data type: String.

</td></tr></tbody>
</table>The following example gets properties of the active object version in the store.

```
// Get properties
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getActiveVersion().getProperties()), null, 2));
```

Output:

```
"datasetProperties": {
    "encodedQuery": "activeANYTHING^EQ",
    "fieldNames": [
      "short_description",
      "category"
    ],
    "tableName": "incident"
  },
  "domainName": "global",
  "inputFieldNames": [
    "short_description"
  ],
  "isActive": "true",
  "label": "Incident Categorization_Trainer",
  "name": "ml_incident_categorization",
  "predictedFieldName": "category",
  "processingLanguage": "en",
  "stopwords": [
    "Default English Stopwords"
  ],
  "versionNumber": "1"
}
```

## PredictabilityEstimateVersion - getResults\(\)

Returns JSON results containing suggested input fields for an output field.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ztt_1xz_qlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object results containing suggested input field options for an output field.

</td></tr><tr><td>

&lt;Object&gt;.&lt;output field name&gt;

</td><td>

Output field name, e.g., `category`, containing suggested input fields.```
{
  "<output field name>": {
    "nominalInputFields": [Array],
    "textInputFields": [Array]
  }
}
```

 Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.&lt;output field name&gt;.nominalInputFields

</td><td>

Nominal input field details.```
"nominalInputFields": [
      {
        "fieldName": "String",
        "modelImprovement": "String"     
      }
    ]
```

 Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.&lt;output field name&gt;.nominalInputFields.fieldName

</td><td>

Nominal input field name.Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.&lt;output field name&gt;.nominalInputFields.modelImprovement

</td><td>

Score as a relative indication of how likely this field is to improve results.Data type: Number as a string.

</td></tr><tr><td>

&lt;Object&gt;.textInputFields

</td><td>

Text input field details.```

    "textInputFields": [
      {
        "fieldName": "String",
        "density": "String"
      }
    ]
```

 Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.textInputFields.fieldName

</td><td>

Text input field name.Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.textInputFields.density

</td><td>

Value between 0 and 1.0 that represents frequency that the field is not empty. A value of 1.0 means that the field is not empty in all rows, and a value of 0 indicates that the field is empty in all rows.Data type: Number as a string.

</td></tr></tbody>
</table>The following example shows how to get results for a selected version of a predictability estimate in the store.

```
// Get results
var estimateName = "ml_x_snc_global_global_predictability_estimate;"
var mlEstimate = sn_ml.PredictabilityEstimateStore.get(estimateName);

var results = mlEstimate.getActiveVersion().getResults();

gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

Output:

```
{
  "category": {
    "nominalInputFields": [
      {
        "fieldName": "number",
        "modelImprovement": "0.167052396325189"
      },
      {
        "fieldName": "task_effective_number",
        "modelImprovement": "0.167052396325189"
      }
    ],
    "textInputFields": [
      {
        "fieldName": "short_description",
        "density": "1.0"
      }
    ]
  }
}
```

## PredictabilityEstimateVersion - getStatus\(Boolean includeDetails\)

Gets training completion status.

<table id="table_xfh_vbw_plb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

includeDetails

</td><td>

Boolean

</td><td>

Flag that indicates whether to return status **details**.Valid values:

-   true: Return additional details.
-   false: Don't return additional details.

Default: False

</td></tr></tbody>
</table><table id="table_yfh_vbw_plb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JavaScript object containing training status information for a [PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) object.```
{
  "state": "String",
  "percentComplete": "Number as a String",
  "hasJobEnded": "Boolean value as a String",
  "details": {Object}
}
```

</td></tr><tr><td>

&lt;Object&gt;.state

</td><td>

Training completion state. If the training job reaches a terminal state, the job does not leave that state. If the state is terminal, the **hasJobEnded** property is set to `true`.Possible values:

-   `fetching_files_for_training`
-   `preparing_data`
-   `retry`
-   `solution_cancelled` \(terminal\)
-   `solution_complete`\(terminal\)
-   `solution_error` \(terminal\)
-   `solution_incomplete`
-   `training_request_received`
-   `training_request_timed_out` \(terminal\)
-   `training_solution`
-   `uploading_solution`
-   `waiting_for_training`

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.hasJobEnded

</td><td>

Flag that indicates whether training is complete.Valid values:

-   true: Training is complete.
-   false: Training is incomplete.

Data type: Boolean value as a String

</td></tr><tr><td>

&lt;Object&gt;.percentComplete

</td><td>

Training percent complete. If the completion percentage is less than 100, the job might be in a terminal state. For example, if training times out.Data type: Number as a String

Range: 0 thru 100

</td></tr><tr><td>

&lt;Object&gt;.details

</td><td>

Object containing a list of additional training details.Data type: Object

</td></tr></tbody>
</table>The following example shows a successful result with training complete.

```
// Get status
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getActiveVersion().getStatus(true), null, 2)));
```

Output:

```
{
 "state":"solution_complete",
 "percentComplete":"100",
 "hasJobEnded":"true",
 "details":{"stepLabel":"Solution Complete"} // This information is only returned if getStatus(true);
}
```

The following example shows an unsuccessful result with training complete.

```
// Get status
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_my_estimate_definition');
var trainingStatus = mlEstimate.getLatestVersion().getStatus();

gs.print(JSON.stringify(JSON.parse(trainingStatus), null, 2));
```

Output:

```
{
  "state": "solution_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## PredictabilityEstimateVersion - getVersionNumber\(\)

Gets the version number of a predictability estimate object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Version number.|

The following example shows how to get a version number.

```
// Get version number
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_predictability_estimate');

gs.print("Version number: "+JSON.stringify(JSON.parse(mlEstimate.getActiveVersion().getVersionNumber()), null, 2));
```

Output:

```
Version number: 1
```

