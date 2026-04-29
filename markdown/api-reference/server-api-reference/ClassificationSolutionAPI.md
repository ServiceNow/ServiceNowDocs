---
title: ClassificationSolution - Global
description: The ClassificationSolution API is a scriptable object used in Predictive Intelligence stores.Creates a classification solution.Cancels a job for a solution object that has been submitted for training.Gets the active ClassificationSolutionVersion object.Gets all versions of a classification solution.Gets the latest version of a solution.Gets the name of the object to use for interaction with the store.Gets solution object properties.Gets a solution by provided version number.Activates a specified version of a solution in the store.Submits a training job.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClassificationSolution- Global

The ClassificationSolution API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The solution setup-to-training flow is as follows:

1.  Create a dataset using the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) API.
2.  Optional. Build an encoder using the [Encoder](../../Encoder/concept/EncoderAPI.md#) API.
3.  Use the [constructor](ClassificationSolutionAPI.md#) to create a classification solution object.
4.  Add the solution object to the classification solution store using the [ClassificationSolutionStore - add\(\)](../../ClassificationSolutionStore/concept/ClassificationSolutionStoreAPI.md#) method.
5.  Train the solution using the [submitTrainingJob\(\)](ClassificationSolutionAPI.md#) method. This creates a version of the object that you can manage using the [ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) API.
6.  Get predictions using the [ClassificationSolutionVersion – predict\(\)](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) method.

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClassificationSolution - ClassificationSolution\(Object config\)

Creates a classification solution.

<table id="table_gm2_yt5_flb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

config

</td><td>

Object

</td><td>

JavaScript object containing configuration properties of thesolution.```
{
  "algorithmConfig": {Object},
  "dataset": {Object},
  "domainName": "String",
  "encoder": {Object},
  "groupByFieldName": "String", 
  "inputFieldNames": [Array],
  "label": "String",
  "minRowCount": "String",
  "predictedFieldName": "String",
  "processingLanguage": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

</td></tr><tr><td>

config.algorithmConfig

</td><td>

Object

</td><td>

JavaScript object containing algorithm configuration properties. ```
'algorithmConfig' : {
  "algorithm": "String",
  "targetClassRecall": "String"
}
```

</td></tr><tr><td>

config.algorithmConfig.algorithm

</td><td>

String

</td><td>

Method for encoding your solution. Possible values:

-   **xgboost**: XGBoost encoding to optimize the training.
-   **logisticRegression**: Method using the logistic regression model for categorical targets such as nominal or ordinal.

</td></tr><tr><td>

config.algorithmConfig.targetClassRecall

</td><td>

String

</td><td>

Applies a class recall parameter to steer a solution's training to bias a specific class. Format is `"<ClassName:RecallValue>"` where the recall value is a number between 0 and 100 representing a percentage. For example, to set and apply this solution parameter to 90% accuracy for all records you train in the Email class, the value is set to `"Email:90"`.

</td></tr><tr><td>

config.dataset

</td><td>

Object

</td><td>

[DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) name.

</td></tr><tr><td>

config.domainName

</td><td>

String

</td><td>

Optional. Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Default: Current domain, for example, `"global"`.

</td></tr><tr><td>

config.encoder

</td><td>

Object

</td><td>

Optional. Trained encoder object to assign to this solution. See [Encoder - Encoder\(Object config\)](../../Encoder/concept/EncoderAPI.md#).

</td></tr><tr><td>

config.explainability

</td><td>

Boolean

</td><td>

Flag that indicates whether to provide model explainability. Use model explainability to identify the importance of each input field to your model's predictions.Valid values:

-   true: The Classification model includes explainability details. Information can be viewed on the **Feature Importance** tab of the model's solution form.
-   false: The Classification model does not include explainability details.

Default: false

See also: [Model Explainability](https://www.servicenow.com/docs/access?context=predictive-intel-explainability&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)

</td></tr><tr><td>

config.groupByFieldName

</td><td>

String

</td><td>

Optional. Field name by which the system groups records to build classification solutions. For usage information, see [Using group by for classification](https://www.servicenow.com/docs/access?context=using-group-by-for-classification&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

config.inputFieldNames

</td><td>

Array

</td><td>

List of input field names as strings. The model uses these fields used to make predictions.

</td></tr><tr><td>

config.label

</td><td>

String

</td><td>

Identifies the prediction task.

</td></tr><tr><td>

config.minRowCount

</td><td>

String

</td><td>

Optional. Minimum number of records required in the dataset for training.Default: 10000

</td></tr><tr><td>

config.predictedFieldName

</td><td>

String

</td><td>

Identifies a field to be trained for predictability.

</td></tr><tr><td>

config.processingLanguage

</td><td>

String

</td><td>

Optional. Processing language in two-letter ISO 639-1 language code format. Default: "en"

</td></tr><tr><td>

config.stopwords

</td><td>

Array

</td><td>

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Default: English Stopwords

</td></tr><tr><td>

config.trainingFrequency

</td><td>

String

</td><td>

The frequency to retrain the model. Possible values:

-   every\_30\_days
-   every\_60\_days
-   every\_90\_days
-   every\_120\_days
-   every\_180\_days
-   run\_once

Default: run\_once

</td></tr></tbody>
</table>The following example shows how to create an object and add it to the ClassificationSolution store.

```
var myData = new sn_ml.DatasetDefinition(
  { 
     'tableName' : 'incident', 
     'fieldNames' : ['category', 'short_description', 'priority'],
     'fieldDetails' : [
       {
         'name' : 'category',
         'type' : 'nominal'
       },
       {
         'name' : 'short_description',
         'type' : 'text'
       }], 
     'encodedQuery' : 'activeANYTHING'
  });

var mySolution = new sn_ml.ClassificationSolution({
  'label': "my solution definition",
  'dataset' : myData,
  'predictedFieldName' : 'category',
  'inputFieldNames': ['short_description']
});

var myClassificationName = sn_ml.ClassificationSolutionStore.add(mySolution);
```

## ClassificationSolution - cancelTrainingJob\(\)

Cancels a job for a solution object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var mySolution = sn_ml.ClassificationSolutionStore.get('ml_sn_global_global_classification');

mySolution.cancelTrainingJob();
```

## ClassificationSolution - getActiveVersion\(\)

Gets the active ClassificationSolutionVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) object.|

The following example shows how to get an active ClassificationSolution version from the store and return its training status.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_classification');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "solution_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## ClassificationSolution - getAllVersions\(\)

Gets all versions of a classification solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of a solution object. See also [ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) API.|

The following example shows how to get all ClassificationSolution version objects and call the getVersionNumber\(\) and getStatus\(\) solution version methods on them.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_classification');

var mlSolutionVersions = mlSolution.getAllVersions();

for (i = 0; i < mlSolutionVersions.length; i++) {
gs.print("Version " + mlSolutionVersions[i].getVersionNumber() + " Status: " + mlSolutionVersions[i].getStatus() +"\n");
};
```

Output:

```
Version 3 Status: {"state":"solution_complete","percentComplete":"100","hasJobEnded":"true"}

Version 2 Status: {"state":"solution_complete","percentComplete":"100","hasJobEnded":"true"}

Version 1 Status: {"state":"solution_cancelled","percentComplete":"0","hasJobEnded":"true"}
```

## ClassificationSolution - getLatestVersion\(\)

Gets the latest version of a solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) object corresponding to the latest version of a [ClassificationSolution\(\)](ClassificationSolutionAPI.md#).|

The following example shows how to get the latest version of a solution and return its training status.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_classification');

gs.print(JSON.stringify(JSON.parse(mlSolution.getLatestVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "solution_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## ClassificationSolution - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the solution object.|

The following example shows how to update ClassificationSolution dataset information and print the name of the object.

```
// Update solution
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields('classification'));

var myClassification = new sn_ml.ClassificationSolution({
   'label': "my classification solution",
   'dataset' : myIncidentData,
   'inputFieldNames': eligibleFields['eligibleInputFieldNames'],
   'predictedFieldName': 'category'
});

// update solution
sn_ml.ClassificationSolutionStore.update('ml_x_snc_global_global_my_solution_definition_4', myClassification);

// print solution name
gs.print('Solution Name: '+myClassification.getName());
```

Output:

```
Solution Name: ml_x_snc_global_global_my_solution_definition_4
```

## ClassificationSolution - getProperties\(\)

Gets solution object properties.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qps_43z_llb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Contents of the Dataset and [ClassificationSolution\(\)](ClassificationSolutionAPI.md#) object details in the [ClassificationSolutionStore](../../ClassificationSolutionStore/concept/ClassificationSolutionStoreAPI.md#).```
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
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig

</td><td>

Method for encoding the solution. Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.algorithm

</td><td>

Name of the encoding algorithm for training this solution. Possible values:

-   **xgboost**: XGBoost encoding to optimize the training.
-   **logisticRegression**: Method using the logistic regression model for categorical targets such as nominal or ordinal.

 Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.targetClassRecall

</td><td>

Class recall parameter to steer a solution's training to bias a specific class. The recall value is a number between 0 and 100 representing a percentage.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties

</td><td>

Lists the properties of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object associated with the solution.

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

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.encoder

</td><td>

Encoder object assigned to this solution. See [Encoder - Encoder\(Object config\)](../../Encoder/concept/EncoderAPI.md#).Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.groupByFieldName

</td><td>

Field name by which the system groups records to build classification solutions. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.inputFieldNames

</td><td>

List of input field names as strings. The model uses these fields used to make predictions. Data type: String.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Data type: Array.

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

</td></tr></tbody>
</table>The following example gets properties of a solution object in the store.

```
var mySolution = sn_ml.ClassificationSolutionStore.get('ml_sn_global_global_classification_solution');

gs.print(JSON.stringify(JSON.parse(mySolution.getProperties()), null, 2));
```

Output:

```
*** Script: {
  "datasetProperties": {
    "tableName": "incident",
    "fieldNames": [
      "category",
      "short_description",
      "priority",
      "assignment_group.name"
    ],
    "fieldDetails": [
      {
        "name": "category",
        "type": "nominal"
      },
      {
        "name": "short_description",
        "type": "text"
      }
    ]
  },
  "domainName": "global",
  "inputFieldNames": [
    "short_description"
  ],
  "label": "my solution definition",
  "name": "ml_x_snc_global_global_my_solution_definition_26",
  "predictedFieldName": "category",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "trainingFrequency": "run_once"
}
```

## ClassificationSolution - getVersion\(String version\)

Gets a solution by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of a solution.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [ClassificationSolution\(\)](ClassificationSolutionAPI.md#) object on which you can call [ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) API methods.|

The following example shows how to get the training status of a solution by version number.

```
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_x_snc_global_global_classification');

gs.print(JSON.stringify(JSON.parse(mlSolution.getVersion('1').getStatus()), null, 2));
```

Output:

```
{
  "state": "solution_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## ClassificationSolution - setActiveVersion\(String version\)

Activates a specified version of a solution in the store.

<table id="table_pps_43z_llb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

version

</td><td>

String

</td><td>

Name of the [ClassificationSolution\(\)](ClassificationSolutionAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate a solution version in the store.

```
sn_ml.ClassificationSolution.setActiveVersion("ml_incident_categorization");
```

## ClassificationSolution - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add a solution to the store using the [ClassificationSolutionStore - add\(\)](../../ClassificationSolutionStore/concept/ClassificationSolutionStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) object corresponding to the [ClassificationSolution](ClassificationSolutionAPI.md#) being trained.|

The following example shows how to create a dataset, apply it to a solution, add the solution to a store, and submit the training job.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create a solution 
var mySolution = new sn_ml.ClassificationSolution({

  'label': "my solution definition",
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the solution to the store to later be able to retrieve it.
var my_unique_name = sn_ml.ClassificationSolutionStore.add(mySolution);

// Train the solution - this is a long running job 
var myClassifierVersion = mySolution.submitTrainingJob();
```

