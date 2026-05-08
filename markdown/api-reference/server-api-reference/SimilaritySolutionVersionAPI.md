---
title: SimilaritySolutionVersion - Global
description: The SimilaritySolutionVersion API is a scriptable object used in Predictive Intelligence stores.Gets solution object properties and version number.Gets training completion status.Gets the version number of a solution object.Gets the input data for a prediction.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SimilaritySolutionVersion- Global

The SimilaritySolutionVersion API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

This API is used is used for working with solution versions based on [SimilaritySolution API](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#) objects in the [SimilaritySolution store](../../SimilaritySolutionStore/concept/SimilaritySolutionStoreAPI.md#).

The system creates a solution version each time you train a solution definition. Most versions are created during scheduled solution training.

Methods in this API are accessible using the following SimilaritySolution methods:

-   [getActiveVersion\(\)](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#)
-   [getAllVersions\(\)](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#)
-   [getLatestVersion\(\)](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#)
-   [getVersion\(\)](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SimilaritySolutionVersion - getProperties\(\)

Gets solution object properties and version number.

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

Contents of the Dataset and [SimilaritySolution](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#) version details. Results vary by object property setup.```
{
  "domainName": "String",
  "isActive": "String",
  "label": "String",
  "lookupDatasetProperties": {Object},
  "name": "String",
  "predictedFieldName": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "testDatasetProperties": {Object},
  "trainingFrequency": "String",
  "updateFrequency": "String",
  "versionNumber": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See Domain separation and Predictive Intelligence. Data type: String.

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

&lt;Object&gt;.lookupDatasetProperties

</td><td>

Details of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object used as the lookup set. ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

 Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.lookupDatasetProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.lookupDatasetProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.lookupDatasetProperties.fieldNames.fieldDetails

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

&lt;Object&gt;.lookupDatasetProperties.fieldNames.fieldDetails.&lt;object&gt;.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.lookupDatasetProperties.fieldDetails.&lt;object&gt;.type

</td><td>

Machine-learning field type. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.lookupDatasetProperties.fieldDetails.encodedQuery

</td><td>

Encoded query string in standard Glide format. See Encoded query strings. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

System-assigned name. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.predictedFieldName

</td><td>

Identifies a field to be trained for predictability. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.processingLanguage

</td><td>

Processing language in two-letter ISO 639-1 language code format. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.scope

</td><td>

Object scope. Currently the only valid value is `global`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.stopwords

</td><td>

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see Create a custom stopwords list. Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties

</td><td>

Details of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object used to retrieve similarities between results searched in this model and results found in the **lookupDataset**. ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

 Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties.fieldNames.fieldDetails

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

&lt;Object&gt;.testDatasetProperties.fieldNames.fieldDetails.&lt;object&gt;.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties.fieldDetails.&lt;object&gt;.type

</td><td>

Machine-learning field type. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.testDatasetProperties.fieldDetails.encodedQuery

</td><td>

Encoded query string in standard Glide format. See Encoded query strings. Data type: String.

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

&lt;Object&gt;.updateFrequency

</td><td>

The frequency at which the model for the solution definition must be rebuilt. Possible values:

-   do\_not\_update
-   every\_1\_day
-   every\_1\_hour
-   every\_6\_hours
-   every\_12\_hours
-   every\_1\_minute
-   every\_15\_minutes
-   every\_30\_minutes

Default: do\_not\_update

 Datatype: String

</td></tr><tr><td>

&lt;Object&gt;.versionNumber

</td><td>

Version number of the SimilaritySolution object.Data type: String.

</td></tr></tbody>
</table>The following example gets properties of the active object version in the store.

```
// Get properties
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_similarity_solution');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getProperties()), null, 2));
```

Output:

```
*** Script: {
  "domainName": "global",
  "encoderProperties": {
    "datasetsProperties": [],
    "name": "wordCorpusA"
  },
  "isActive": "true",
  "label": "similarity",
  "lookupDatasetProperties": {
    "encodedQuery": "",
    "fieldNames": [
      "short_description"
    ],
    "tableName": "incident"
  },
  "name": "ml_x_snc_global_global_similarity",
  "processingLanguage": "en",
  "stopwords": [
    "Default English Stopwords"
  ],
  "testDatasetProperties": {
    "fieldNames": [
      "short_description"
    ],
    "tableName": "incident"
  },
  "versionNumber": "3"
}
```

## SimilaritySolutionVersion - getStatus\(Boolean includeDetails\)

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

JavaScript object containing training status information for a [SimilaritySolution](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#) object.```
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
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_similarity_solution');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getStatus(true), null, 2)));
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
var solutionName = 'ml_x_snc_global_global_similarity_solution';
var mlSolution = sn_ml.SimilaritySolutionStore.get(solutionName);
var trainingStatus = JSON.parse(mlSolution.getLatestVersion().getStatus());

gs.print(JSON.stringify(JSON.parse(trainingStatus), null, 2));
```

Output:

```
{
 "state":"solution_error",
 "percentComplete":"100",
 "hasJobEnded":"true"
}
```

## SimilaritySolutionVersion - getVersionNumber\(\)

Gets the version number of a solution object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Version number.|

The following example shows how to get a version number.

```
// Get version number
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_similarity_solution');

gs.print("Version number: "+JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getVersionNumber()), null, 2));
```

Output:

```
Version number: 1
```

## SimilaritySolutionVersion - predict\(Object input, Object options\)

Gets the input data for a prediction.

<table id="table_wwz_pbw_plb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

Object

</td><td>

[GlideRecord](../../GlideRecord/concept/c_GlideRecordAPI.md#) or array of JSON objects containing field names and values as key-value pairs.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional values for filtering prediction results.```
{
  "apply_threshold": Boolean,
  "top_n": Number
}
```

</td></tr><tr><td>

options.apply\_threshold

</td><td>

Boolean

</td><td>

Flag that indicates whether to check the threshold value for the solution and apply it to the result set.Valid values:

-   true: Return results in which confidence is greater than threshold.
-   false: Return all results.

Default: True

</td></tr><tr><td>

options.top\_n

</td><td>

Number

</td><td>

If provided, returns the top results, up to the specified number of predictions.

</td></tr></tbody>
</table><table id="table_xwz_pbw_plb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object containing the prediction results sorted by sys\_id or record\_number. ```
{
    <identifier>: [Array]
}
```

</td></tr><tr><td>

&lt;Object&gt;.&lt;identifier&gt;

</td><td>

List of objects with details for each prediction result.Data type: Array of Objects

```
<identifier>: [
  {
    "confidence": Number,
    "predictedSysId": "String",
    "predictedValue": "String", 
    "threshold": Number
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.&lt;identifier&gt;.&lt;object&gt;.confidence

</td><td>

Value of the confidence associated with the prediction. For example, 53.84. Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.&lt;identifier&gt;.&lt;object&gt;.predictedSysId

</td><td>

The sys\_id of the predicted value. Results can be from any table on which information is being predicted. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.&lt;identifier&gt;.&lt;object&gt;.predictedValue

</td><td>

Value representing the prediction result. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.&lt;identifier&gt;.&lt;object&gt;.threshold

</td><td>

Value of the configured threshold associated with the prediction. Data type: Number

</td></tr></tbody>
</table>The following example shows how to display prediction results for a predict\(\) method that takes a GlideRecord by sys\_id for input and includes optional parameters to restrict to top three results and exclude the threshold value.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_similarity_solution');

// single GlideRecord input
var input = new GlideRecord("incident");
input.get("<sys_id>");

// configure optional parameters
var options = {};
options.top_n = 3;
options.apply_threshold = false;

var results = mlSolution.getVersion(1).predict(input, options);
// pretty print JSON results
gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

```
{
        "<sys_id/now_GR>": [
    {
      "confidence": 62.10782320780268,
      "threshold": 20.36,
      "predictedValue": "Clone Issues",
      "predictedSysId": ""
    },
    {
      "confidence": 6.945237375770391,
      "threshold": 16.63,
      "predictedValue": "Instance Administration",
      "predictedSysId": ""
    },
    {
      "confidence": 5.321061076300759,
      "threshold": 23.7,
      "predictedValue": "Administration",
      "predictedSysId": ""
    }
  ]
}
```

The following example shows how to display prediction results for a predict\(\) method that takes an array of field names as key-value pairs for input and includes optional parameters to restrict to top three results and exclude the threshold value.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get("ml_x_snc_global_similarity_solution");
// key-value pairs input
var input = [{"short_description":"my email is not working"}, {short_description:"need help with password"}];
// configure optional parameters
var options = {};
options.top_n = 3;
options.apply_threshold = false;
var results = mlSolution.predict(input, options);
// pretty print JSON results
gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

```
{
  "1": [
    {
      "confidence": 37.5023032262591,
      "threshold": 10.72,
      "predictedValue": "Authentication",
      "predictedSysId": ""
    },
    {
      "confidence": 24.439964862166583,
      "threshold": 23.7,
      "predictedValue": "Administration",
      "predictedSysId": ""
    },
    {
      "confidence": 11.736320486031047,
      "threshold": 100,
      "predictedValue": "Security",
      "predictedSysId": ""
    }
  ],
  "2": [
    {
      "confidence": 99,
      "threshold": 17.77,
      "predictedValue": "Email",
      "predictedSysId": ""
    },
    {
      "confidence": 3.182137005157543,
      "threshold": 10.72,
      "predictedValue": "Authentication",
      "predictedSysId": ""
    },
    {
      "confidence": 2.8773826570713514,
      "threshold": -1,
      "predictedValue": "Email (I/f)",
      "predictedSysId": ""
    }
  ]
}
```

