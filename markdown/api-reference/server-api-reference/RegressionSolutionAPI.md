---
title: RegressionSolution - Global
description: The RegressionSolution API is a scriptable object used in Predictive Intelligence stores.Creates a regression solution.Cancels a job for a solution object that has been submitted for training.Gets the active RegressionSolutionVersion object.Gets all versions of a RegressionSolution object.Gets the latest version of a solution.Gets the name of the object to use for interaction with the store.Gets solution object properties.Gets a solution by provided version number.Activates a specified version of a solution in the store.Submits a training job.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# RegressionSolution- Global

The RegressionSolution API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The solution setup-to-training flow is as follows:

1.  Create a dataset using the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) API.
2.  Optional. Build an encoder using the [Encoder](../../Encoder/concept/EncoderAPI.md#) API.
3.  Use the [constructor](RegressionSolutionAPI.md#) to create a regression solution object.
4.  Add the solution object to the regression solution store using the [RegressionSolutionStore - add\(\)](../../RegressionSolutionStore/concept/RegressionSolutionStoreAPI.md#) method.
5.  Train the solution using the [submitTrainingJob\(\)](RegressionSolutionAPI.md#) method. This creates a version of the object that you can manage using the [RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) API.
6.  Get predictions using the [RegressionSolutionVersion – predict\(\)](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) method.

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see Query ACLs.

For usage guidelines, refer to Using ML APIs.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## RegressionSolution - RegressionSolution\(Object config\)

Creates a regression solution.

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
  "inputFieldNames": [Array],
  "label": "String",
  "minRowCount": "String",
  "predictedFieldName": "String",
  "predictedInterval": [Array],
  "processingLanguage": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

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

Optional. Domain name associated with this dataset. See Domain separation and Predictive Intelligence. Default: Current domain, for example, `"global"`.

</td></tr><tr><td>

config.encoder

</td><td>

Object

</td><td>

Optional. Trained encoder object to assign to this solution. See [Encoder - Encoder\(Object config\)](../../Encoder/concept/EncoderAPI.md#).

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

Mandatory unless setting **predictedInterval**. Identifies a field to be trained for predictability.

</td></tr><tr><td>

config.predictedInterval

</td><td>

Array

</td><td>

Mandatory unless setting **predictedFieldName**. Sets a range of fields to train your solution for confidence. Supports providing 2 non-numeric date fields. For example, `'predictedInterval': ['sys_updated_on', 'sys_created_on']`.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see Create a custom stopwords list. Default: English Stopwords

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
</table>The following example shows how to create an object and add it to the RegressionSolution store.

```
var myNewData = new sn_ml.DatasetDefinition(
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

var mySimSolution = new sn_ml.SimilaritySolution({
  'label': "my solution definition",
  'dataset' : myNewData,
  'predictedFieldName' : 'category',
  'inputFieldNames': ['short_description']
});

var mySimilarityName = sn_ml.SimilaritySolutionStore.add(mySimSolution);
```

The following example shows how to create an object to train using the **predictedInterval** property.

```
var myIncidentData = new sn_ml.DatasetDefinition({
'tableName' : 'incident',
'fieldNames' : ['short_description', 'sys_updated_on','sys_created_on'],
'encodedQuery' : 'activeANYTHING'
});
 
var mySolution = new sn_ml.RegressionSolution({
'label': 'reg assinGroup',
'dataset' : myIncidentData,
'predictedInterval': ['sys_updated_on', 'sys_created_on'],
'inputFieldNames': ['short_description']
});
 
var my_unique_name = sn_ml.RegressionSolutionStore.add(mySolution)
```

## RegressionSolution - cancelTrainingJob\(\)

Cancels a job for a solution object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var mySolution = sn_ml.RegressionSolutionStore.get('ml_sn_global_global_regression');

mySolution.cancelTrainingJob();
```

## RegressionSolution - getActiveVersion\(\)

Gets the active RegressionSolutionVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) object.|

The following example shows how to get an active RegressionSolution version from the store and return its training status.

```
var mlSolution = sn_ml.RegressionSolutionStore.get('ml_x_snc_global_global_regression');

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

## RegressionSolution - getAllVersions\(\)

Gets all versions of a RegressionSolution object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of a solution object. See also [RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) API.|

The following example shows how to get all RegressionSolution version objects and call the getVersionNumber\(\) and getStatus\(\) solution version methods on them.

```
var mlSolution = sn_ml.RegressionSolutionStore.get('ml_x_snc_global_global_regression');

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

## RegressionSolution - getLatestVersion\(\)

Gets the latest version of a solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) object corresponding to the latest version of a [RegressionSolution\(\)](RegressionSolutionAPI.md#).|

The following example shows how to get the latest version of a solution and return its training status.

```
var mlSolution = sn_ml.RegressionSolutionStore.get('ml_x_snc_global_global_regression');

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

## RegressionSolution - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the solution object.|

The following example shows how to update RegressionSolution dataset information and print the name of the object.

```
// Update solution
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields('regression'));

var myRegression = new sn_ml.RegressionSolution({
   'label': "my regression solution",
   'dataset' : myIncidentData,
   'inputFieldNames': eligibleFields['eligibleInputFieldNames'],
   'predictedFieldName': 'category'
});

// update solution
sn_ml.RegressionSolutionStore.update('ml_x_snc_global_global_my_solution_definition_4', myRegression);

// print solution name
gs.print('Solution Name: '+myRegression.getName());
```

Output:

```
Solution Name: ml_x_snc_global_global_my_solution_definition_4
```

## RegressionSolution - getProperties\(\)

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

Contents of the Dataset and [RegressionSolution\(\)](RegressionSolutionAPI.md#) object details in the [RegressionSolutionStore](../../RegressionSolutionStore/concept/RegressionSolutionStoreAPI.md#).```
{
  "datasetProperties": {Object},
  "domainName": "String",
  "encoder": {Object},
  "inputFieldNames": [Array],
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "predictedInterval": [Array],
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

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

Encoded query string in standard Glide format. See Encoded query strings. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See Domain separation and Predictive Intelligence. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.encoder

</td><td>

Encoder object assigned to this solution. See [Encoder - Encoder\(Object config\)](../../Encoder/concept/EncoderAPI.md#).Data type: Object.

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

&lt;Object&gt;.predictedInterval

</td><td>

Range of values specifying the prediction confidence level.Data type: Array

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
var mySolution = sn_ml.RegressionSolutionStore.get('ml_sn_global_global_regression_solution');

gs.print(JSON.stringify(JSON.parse(mySolution.getProperties()), null, 2));
```

Output:

```
*** Script: {
  "datasetProperties": {
    "tableName": "cloudinfratext",
    "fieldNames": [
      "short_description",
      "sourcedc",
      "targetdc",
      "dbsize",
      "duration"
    ]
  },
  "domainName": "global",
  "encoderProperties": {
    "datasetsProperties": [],
    "name": "wc_regression"
  },
  "inputFieldNames": [
    "short_description",
    "sourcedc",
    "targetdc",
    "dbsize"
  ],
  "label": "Regression Test for DB Restore",
  "name": "ml_x_snc_global_global_regression",
  "predictedFieldName": "duration",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "trainingFrequency": "every_30_days"
}
```

## RegressionSolution - getVersion\(String version\)

Gets a solution by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of a solution.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [RegressionSolution\(\)](RegressionSolutionAPI.md#) object on which you can call [RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) API methods.|

The following example shows how to get the training status of a solution by version number.

```
var mlSolution = sn_ml.RegressionSolutionStore.get('ml_x_snc_global_global_regression');

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

## RegressionSolution - setActiveVersion\(String version\)

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

Name of the [RegressionSolution\(\)](RegressionSolutionAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate a solution version in the store.

```
sn_ml.RegressionSolution.setActiveVersion("ml_incident_categorization");
```

## RegressionSolution - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add a solution to the store using the [RegressionSolutionStore - add\(\)](../../RegressionSolutionStore/concept/RegressionSolutionStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[RegressionSolutionVersion](../../RegressionSolutionVersion/concept/RegressionSolutionVersionAPI.md#) object corresponding to the [RegressionSolution](RegressionSolutionAPI.md#) being trained.|

The following example shows how to create a dataset, apply it to a solution, add the solution to a store, and submit the training job.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create a solution 
var mySolution = new sn_ml.RegressionSolution({

  'label': "my solution definition",
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the solution to the store to later be able to retrieve it.
var my_unique_name = sn_ml.RegressionSolutionStore.add(mySolution);

// Train the solution - this is a long running job 
var myRegressionVersion = mySolution.submitTrainingJob();
```

