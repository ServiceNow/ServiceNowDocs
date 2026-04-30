---
title: ClassificationSolutionVersion - Global
description: The ClassificationSolutionVersion API is a scriptable object used in Predictive Intelligence stores.Calculates solution precision and coverage.Gets estimated precision, estimated coverage, estimated recall values from the ML Solutions \[ml\_solution\] table and records from the Class Confidence \[ml\_class\] table.Gets solution object properties and version number.Gets training completion status.Gets all the training statistics for a given solution.Gets the version number of a solution object.Gets the input data for a prediction.Sets precision, coverage, or recall values at solution level or class level.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClassificationSolutionVersion- Global

The ClassificationSolutionVersion API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

This API is used for working with solution versions based on [ClassificationSolution API](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) objects in the [ClassificationSolution store](../../ClassificationSolutionStore/concept/ClassificationSolutionStoreAPI.md#).

The system creates a solution version each time you train a solution definition. Most versions are created during scheduled solution training.

Methods in this API are accessible using the following [ClassificationSolution - Global](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) methods:

-   [getActiveVersion\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)
-   [getAllVersions\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)
-   [getLatestVersion\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)
-   [getVersion\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClassificationSolutionVersion - getPredictionPerformance\(Object options\)

Calculates solution precision and coverage.

To use this method, you must first create settings using the setPredictionSettings\(\) method.

<table id="table_gby_x2w_plb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

Selects a metric to retrieve within a span of dates. For more information, see [Configuring target metrics](https://www.servicenow.com/docs/access?context=configuring-target-metrics-trained-classification-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).```
{
  "fromDate": "String",
  "metricName": "String",
  "toDate": "String"
}
```

</td></tr><tr><td>

options.fromDate

</td><td>

String

</td><td>

Optional. Start date from which to retrieve metrics in system date time format.

</td></tr><tr><td>

options.metricName

</td><td>

String

</td><td>

Name of the metric.Valid values:

-   **precision**
-   **coverage**

</td></tr><tr><td>

options.toDate

</td><td>

String

</td><td>

Optional. End date from which to retrieve metrics.Formnt: System date time format.

</td></tr></tbody>
</table><table id="table_hby_x2w_plb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Parseable JavaScript object containing the results for the input metric.```
{
  "metricName" : "String",
  "metricValue" : "String",
  "numberOfPredictionsConsidered" : "String"
}
```

</td></tr><tr><td>

Object.metricName

</td><td>

Name of metric selected as input.Data type: String

</td></tr><tr><td>

Object.metricValue

</td><td>

Value of the selected metric.Data type: String

</td></tr><tr><td>

Object.numberOfRecordsConsidered

</td><td>

Number of records in the Predictor Results \[ml\_predictor\_results\] table considered for calculations.Data type: String

</td></tr></tbody>
</table>The following example shows how to get a precision value from the active version of a solution.

```
// Get precision value
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getPredictionPerformance({"metricName": "precision"})), null, 2));
```

Output:

```
{
  "metricName": "precision",
  "metricValue": "70.10",
  "numberOfPredictionsConsidered": "10"
}
```

## ClassificationSolutionVersion - getPredictionSettings\(\)

Gets estimated precision, estimated coverage, estimated recall values from the ML Solutions \[ml\_solution\] table and records from the Class Confidence \[ml\_class\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wph_2dw_plb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Returns prediction settings for each class. Data includes precision, coverage, recall, and distribution values of all classes included in the trained model from the ML Solutions \[ml\_solution\] table. For details, see [Predictive model components](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).```
{
  "<class name>": {Object}
}
```

</td></tr><tr><td>

&lt;Object&gt;.&lt;class name&gt;

</td><td>

Training statistics data from the Class Confidence \[ml\_class\] table. For more information, see [Configuring target metrics](https://www.servicenow.com/docs/access?context=configuring-target-metrics-trained-classification-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).Data type: Object

```
{
  "precision": "String",
  "coverage": "String",
  "recall": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.&lt;class name&gt;.precision

</td><td>

Estimated solution precision metric for this class.Data type: String \(numerical value\)

</td></tr><tr><td>

&lt;Object&gt;.&lt;class name&gt;.coverage

</td><td>

Estimated solution coverage metric for this class.Data type: String \(numerical value\)

</td></tr><tr><td>

&lt;Object&gt;.&lt;class name&gt;.recall

</td><td>

Estimated solution recall metric for this class.Data type: String \(numerical value\)

</td></tr></tbody>
</table>The following example shows how to get prediction settings of an active solution version.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getPredictionSettings()), null, 2));
```

Output:

```
{
  "solutionSettings": {
    "precision": "61.69",
    "coverage": "66.75",
    "recall": "57.54"
  },
  "classSettings": {
    "Approvals": {
      "precision": "100",
      "coverage": "0",
      "recall": "0"
    },
    "Authentication": {
      "precision": "38.71",
      "coverage": "98.44",
      "recall": "56.25"
    },
    "Automation": {
      "precision": "100",
      "coverage": "0",
      "recall": "0"
    }, ...
```

## ClassificationSolutionVersion - getProperties\(\)

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

Contents of the Dataset and [ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) version details. Results vary by object property setup.```
{
  "algorithmConfig": {
    "algorithm": "String",
    "targetClassRecall": "String"
  },
  "datasetProperties": {Object},
  "domainName": "String",
  "encoder": {Object},
  "groupByFieldName": "String",   
  "inputFieldNames": [Array],
  "isActive": Boolean,
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "stopwords": [Array],
  "trainingFrequency": "String",
  "versionNumber": "Number"
}
```

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig

</td><td>

Method for encoding the solution. Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.algorithm

</td><td>

Name of the encoding algorithm for training this solution. Possible values:

-   **xgboost**: XGBoost encoding to optimize the training.
-   **logisticRegression**: Method using the logistic regression model for categorical targets such as nominal or ordinal.

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.targetClassRecall

</td><td>

Class recall parameter to steer a solution's training to bias a specific class. The recall value is a number between 0 and 100 representing a percentage.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties

</td><td>

Lists the properties of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object associated with the solution.

 Data type: Object

 ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames.fieldDetails

</td><td>

List of JavaScript objects that specify field properties. Data type: Array of Objects

```
[
  {
    "name": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames.fieldDetails.&lt;object&gt;.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails.&lt;object&gt;.type

</td><td>

Machine-learning field type. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails.encodedQuery

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Data type: String

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: String

</td></tr><tr><td>

&lt;Object&gt;.encoder

</td><td>

Encoder object assigned to this solution. See [Encoder - Encoder\(Object config\)](../../Encoder/concept/EncoderAPI.md#).Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.groupByFieldName

</td><td>

Field name by which the system groups records to build classification solutions. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.inputFieldNames

</td><td>

List of input field names as strings. The model uses these fields used to make predictions. Data type: String

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

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

System-assigned name. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.predictedFieldName

</td><td>

Identifies a field to be trained for predictability. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.processingLanguage

</td><td>

Processing language in two-letter ISO 639-1 language code format. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.scope

</td><td>

Object scope. Currently the only valid value is `global`.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.stopwords

</td><td>

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: Array

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

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.versionNumber

</td><td>

Version number of the ClassificationSolution object.Data type: String

</td></tr></tbody>
</table>The following example gets properties of the active object version in the store.

```
// Get properties
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getProperties()), null, 2));
```

Output:

```
*** Script: {
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

## ClassificationSolutionVersion - getStatus\(Boolean includeDetails\)

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

JavaScript object containing training status information for a [ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) object.```
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
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

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
var solutionName = 'ml_x_snc_global_global_classification_solution';
var mlSolution = sn_ml.ClassificationSolutionStore.get(solutionName);
var trainingStatus = mlSolution.getLatestVersion().getStatus();

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

## ClassificationSolutionVersion - getTrainingStatistics\(\)

Gets all the training statistics for a given solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_wph_2dw_plb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JavaScript object with statistics for each class included in training and values for each class that was excluded from training. For details, see [Predictive model components](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).```
{
  "includedClasses": {Object},
  "excludedClasses": {Object}
}
```

</td></tr><tr><td>

&lt;Object&gt;.includedClasses

</td><td>

Object containing precision, coverage, recall, and distribution values of each class in the trained model.Data type: Object

```

  "includedClasses": {
    "<class name>": {
      "distribution": "String",
      "statistics": [Array]
    },
```

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.distribution

</td><td>

Value of the outcome probability distribution for this class.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.statistics

</td><td>

List of objects providing training statistics data. For more information, see [Configuring target metrics](https://www.servicenow.com/docs/access?context=configuring-target-metrics-trained-classification-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).Data type: Array of Objects

```
[
  {
    "coverage": "String",
    "precision": "String",
    "recall": "String",
    "selected": "String"
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.statistics.coverage

</td><td>

Estimated solution coverage metric for this class.Data type: String \(numerical value\)

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.statistics.precision

</td><td>

Estimated solution precision metric for this class.Data type: String \(numerical value\)

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.statistics.recall

</td><td>

Estimated solution recall metric for this class.Data type: String \(numerical value\)

</td></tr><tr><td>

&lt;Object&gt;.includedClasses.&lt;class name&gt;.statistics.selected

</td><td>

Flag that indicates whether this class contains records included in solution training.Valid values:

-   true: This class contains records selected for training the solution.
-   false: This class is excluded from training.

Data type: String \(Boolean value\)

Default: false

</td></tr><tr><td>

&lt;Object&gt;.excludedClasses

</td><td>

Distribution and row count of all the classes excluded from training.Data type: Object

```

  "excludedClasses": {
    "<class name>": {
      "distribution": "0.11",
      "rowCount": "9"
    }
```

</td></tr><tr><td>

&lt;Object&gt;.excludedClasses.&lt;class name&gt;.distribution

</td><td>

Value of the outcome probability distribution for this class.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.excludedClasses.&lt;class name&gt;.rowCount

</td><td>

Number of rows excluded from training.Data type: String \(numerical value\)

</td></tr></tbody>
</table>The following example shows how to get training statistics from the active solution.

```
// Get training stats
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getTrainingStatistics()), null, 2));
```

Output:

```
{
  "includedClasses": {
    "Approvals": {
      "distribution": "0.43",
      "statistics": [
        {
          "precision": "100",
          "coverage": "0",
          "recall": "0",
          "selected": "true"
        }
      ]
    }, 
    "Authentication": {
      "distribution": "4.3",
      "statistics": [
        {
          "precision": "39.33",
          "coverage": "95.31",
          "recall": "54.69",
          "selected": "false"
        },
        {
          "precision": "100",
          "coverage": "0",
          "recall": "0",
          "selected": "false"
        },
     ...
    }
    ...
  "excludedClasses": {
    "ACE": {
      "distribution": "0.11",
      "rowCount": "9"
    },
    "AHA": {
      "distribution": "0.01",
      "rowCount": "1"
    }, 
    ...
}
```

## ClassificationSolutionVersion - getVersionNumber\(\)

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
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print("Version number: "+JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getVersionNumber()), null, 2));
```

Output:

```
Version number: 1
```

## ClassificationSolutionVersion - predict\(Object input, Object options\)

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
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

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

Output:

```
{
  "<sys_id/gr>": [
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
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

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

Output:

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

## ClassificationSolutionVersion - setPredictionSettings\(Object options\)

Sets precision, coverage, or recall values at solution level or class level.

<table id="table_b45_tdw_plb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

options

</td><td>

Object

</td><td>

Metric configuration values. For information about these features, see [Configuring target metrics](https://www.servicenow.com/docs/access?context=configuring-target-metrics-trained-classification-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).```
{  	 
   "metricName" : "String",
   "metricValue" : "String",
   "className" : "String"
}
```

</td></tr><tr><td>

options.metricName

</td><td>

String

</td><td>

Name of the metric to set.Valid values:

-   **coverage**
-   **precision**
-   **recall**

</td></tr><tr><td>

options.metricValue

</td><td>

String

</td><td>

Numeric value to assign to the metric.

</td></tr><tr><td>

options.className

</td><td>

String

</td><td>

Optional. Name of the class to restrict results to. Use the [getTrainingStatistics\(\)](ClassificationSolutionVersionAPI.md#) method to retrieve a complete list of classes for a solution.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to set a precision metric to 89.5 for a class named `Clone Issues`.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_classification');
var input = {"metricName" : "precision", "metricValue" : "89.5", "className" : "Clone Issues"};

mlSolution.getActiveVersion().setTrainingStatistics(input);
```

