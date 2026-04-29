---
title: PredictabilityEstimate - Global
description: The PredictabilityEstimate API is a scriptable object used in Predictive Intelligence stores. This object provides estimation of how predictable fields of a dataset can be, and which features can be useful for predicting those fields.Creates a predictability estimate.Cancels a job for a predictability estimate object that has been submitted for training.Gets the active PredictabilityEstimateVersion object.Gets all versions of a predictability estimate.Gets the latest version of a predictability estimate.Gets the name of the object to use for interaction with the store.Gets predictability estimate object properties.Gets a predictability estimate by provided version number.Activates a specified version of a predictability estimate in the store.Submits a training job.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PredictabilityEstimate- Global

The PredictabilityEstimate API is a scriptable object used in Predictive Intelligence stores. This object provides estimation of how predictable fields of a dataset can be, and which features can be useful for predicting those fields.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The predictability estimate setup-to-training flow is as follows:

1.  Create a dataset using the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) API.
2.  Use the [constructor](PredictabilityEstimateAPI.md#) to create a predictability estimate object.
3.  Add the predictability estimate object to the predictability estimate store using the [PredictabilityEstimateStore - add\(\)](../../PredictabilityEstimateStore/concept/PredictabilityEstimateStoreAPI.md#) method.
4.  Train the predictability estimate using the [submitTrainingJob\(\)](PredictabilityEstimateAPI.md#) method. This creates a version of the object that you can manage using the [PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) API.
5.  Get estimated predictive values using the [PredictabilityEstimateVersion – getResults\(\)](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) method.

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PredictabilityEstimate - PredictabilityEstimate\(Object config\)

Creates a predictability estimate.

To get new predictability estimates on the same dataset, use this constructor to create a new PredictabilityEstimate object with a unique name.

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

JavaScript object containing configuration properties of thepredictability estimate.```
{
  "dataset": {Object},
  "domainName": "String",
  "inputFieldNames": [Array],
  "label": "String",
  "minRowCount": "String",
  "predictedFieldName": "String",
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

Optional. Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). Default: Current domain, for example, `"global"`.

</td></tr><tr><td>

config.inputFieldNames

</td><td>

Array

</td><td>

List of candidate input fields as strings to be considered for estimation.

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

config.trainingFrequency

</td><td>

String

</td><td>

Optional. The frequency to retrain the model. Possible values:

-   every\_30\_days
-   every\_60\_days
-   every\_90\_days
-   every\_120\_days
-   every\_180\_days
-   run\_once

Default: run\_once

</td></tr></tbody>
</table>The following example shows how to create an estimation job and add it to the PredictabilityEstimate store.

```
var myIncidentData = new sn_ml.DatasetDefinition({
  'tableName' : 'incident',
  'encodedQuery' : 'activeANYTHING'
});

var myEstimate = new sn_ml.PredictabilityEstimate({
  'label': "predictability estimate",
  'dataset' : myIncidentData,
  'inputFieldNames':['short_description'], 
  'predictedFieldName': 'category'
});

var myEstimateName = sn_ml.PredictabilityEstimateStore.add(myEstimate);
```

## PredictabilityEstimate - cancelTrainingJob\(\)

Cancels a job for a predictability estimate object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var myEstimate = sn_ml.PredictabilityEstimateStore.get('ml_sn_global_global_predictability_estimate');

myEstimate.cancelTrainingJob();
```

## PredictabilityEstimate - getActiveVersion\(\)

Gets the active PredictabilityEstimateVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) object.|

The following example shows how to get an active PredictabilityEstimate version from the store and return its training status.

```
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_predictability_estimate');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getActiveVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "predictability_estimate_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## PredictabilityEstimate - getAllVersions\(\)

Gets all versions of a predictability estimate.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of a solution object. See also [PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) API.|

The following example shows how to get all PredictabilityEstimate version objects and call the getVersionNumber\(\) and getStatus\(\) estimate version methods on them.

```
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_predictability_estimate');

var mlEstimateVersions = mlEstimate.getAllVersions();

for (i = 0; i < mlEstimateVersions.length; i++) {
gs.print("Version " + mlEstimateVersions[i].getVersionNumber() + " Status: " + mlEstimateVersions[i].getStatus() +"\n");
};
```

Output:

```
Version 3 Status: {"state":"predictability_estimate_complete","percentComplete":"100","hasJobEnded":"true"}

Version 2 Status: {"state":"predictability_estimate_complete","percentComplete":"100","hasJobEnded":"true"}

Version 1 Status: {"state":"predictability_estimate_cancelled","percentComplete":"0","hasJobEnded":"true"}
```

## PredictabilityEstimate - getLatestVersion\(\)

Gets the latest version of a predictability estimate.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) object corresponding to the latest version of a [PredictabilityEstimate\(\)](PredictabilityEstimateAPI.md#).|

The following example shows how to get the latest version of a predictability estimate and return its training status.

```
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_predictability_estimate');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getLatestVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "predictability_estimate_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## PredictabilityEstimate - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the estimate object.|

The following example shows how to update PredictabilityEstimate dataset information and print the name of the object.

```
// Update estimate
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var myEstimate = new sn_ml.PredictabilityEstimate({
   'label': "my estimate",
   'dataset' : myIncidentData,
   'inputFieldNames':['short_description'],
   'predictedFieldName': 'category'
});

// update estimate
sn_ml.PredictabilityEstimateStore.update('ml_x_snc_global_global_my_definition_4', myEstimate);

// print estimate name
gs.print('Estimate Name: '+myEstimate.getName());
```

Output:

```
Estimate Name: ml_x_snc_global_global_my_definition_4
```

## PredictabilityEstimate - getProperties\(\)

Gets predictability estimate object properties.

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

Contents of the Dataset and [PredictabilityEstimate\(\)](PredictabilityEstimateAPI.md#) object details in the [PredictabilityEstimateStore](../../PredictabilityEstimateStore/concept/PredictabilityEstimateStoreAPI.md#).```
{
  "datasetProperties": {Object},
  "domainName": "String",
  "inputFieldNames": [Array],
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "scope": "String",
  "trainingFrequency": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties

</td><td>

Lists the properties of the [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object associated with the estimate.

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

&lt;Object&gt;.inputFieldNames

</td><td>

List of candidate input fields as strings to be considered for estimation.Data type: String.

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

</td></tr></tbody>
</table>The following example gets properties of a predictability estimate object in the store.

```
var mySolution = sn_ml.PredictabilityEstimateStore.get('ml_sn_global_global_predictability_estimate');

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
  "label": "my estimate definition",
  "name": "ml_x_snc_global_global_my_definition_26",
  "predictedFieldName": "category",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "trainingFrequency": "run_once"
}
```

## PredictabilityEstimate - getVersion\(String version\)

Gets a predictability estimate by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of a predictability estimate.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [PredictabilityEstimate\(\)](PredictabilityEstimateAPI.md#) object on which you can call [PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) API methods.|

The following example shows how to get the training status of a predictability estimate by version number.

```
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_x_snc_global_global_predictability_estimate');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getVersion('1').getStatus()), null, 2));
```

Output:

```
{
  "state": "predictability_estimate_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## PredictabilityEstimate - setActiveVersion\(String version\)

Activates a specified version of a predictability estimate in the store.

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

Name of the [PredictabilityEstimate\(\)](PredictabilityEstimateAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate a predictability estimate version in the store.

```
sn_ml.PredictabilityEstimate.setActiveVersion("ml_x_snc_global_global_my_estimate_definition");
```

## PredictabilityEstimate - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add a predictability estimate to the store using the [PredictabilityEstimateStore - add\(\)](../../PredictabilityEstimateStore/concept/PredictabilityEstimateStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[PredictabilityEstimateVersion](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) object corresponding to the [PredictabilityEstimate](PredictabilityEstimateAPI.md#) being trained.|

The following example shows how to create a dataset, apply it to a predictability estimate, add it to a store, and submit the training job.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create an estimate 
var myEstimate = new sn_ml.PredictabilityEstimate({

  'label': "my estimate definition",
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the estimate to the store to later be able to retrieve it.
var my_unique_name = sn_ml.PredictabilityEstimateStore.add(myEstimate);

// Train the estimate - this is a long running job 
var myEstimateVersion = myEstimate.submitTrainingJob();
```

