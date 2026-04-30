---
title: SimilaritySolution - Global
description: The SimilaritySolution API is a scriptable object used in Predictive Intelligence stores.Creates a similarity solution.Cancels a job for a solution object that has been submitted for training.Gets the active SimilaritySolutionVersion object.Gets all versions of a SimilaritySolution object.Gets the latest version of a solution.Gets the name of the object to use for interaction with the store.Gets solution object properties.Gets a solution by provided version number.Activates a specified version of a solution in the store.Submits a training job.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-02-03"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SimilaritySolution- Global

The SimilaritySolution API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The solution setup-to-training flow is as follows:

1.  Use the [constructor](SimilaritySolutionAPI.md#) to create a similarity solution object.
2.  Add the solution object to the similarity solution store using the [SimilaritySolutionStore - add\(\)](../../SimilaritySolutionStore/concept/SimilaritySolutionStoreAPI.md#) method.
3.  Train the solution using the [submitTrainingJob\(\)](SimilaritySolutionAPI.md#) method. This creates a version of the object that you can manage using the [SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) API.
4.  Get predictions using the [SimilaritySolutionVersion – predict\(\)](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) method.

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SimilaritySolution - SimilaritySolution\(Object config\)

Creates a similarity solution.

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
  "domainName": "String",
  "label": "String",
  "lookupDataset": {Object},
  "minRowCount": "String",
  "processingLanguage": "String",
  "stopwords": [Array],
  "testDataset": {Object},
  "trainingFrequency": "String",
  "updateFrequency": "String"
}
```

</td></tr><tr><td>

config.domainName

</td><td>

String

</td><td>

Optional. Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Default: Current domain, for example, `"global"`.

</td></tr><tr><td>

config.label

</td><td>

String

</td><td>

Identifies the prediction task.

</td></tr><tr><td>

config.lookupDataset

</td><td>

Object

</td><td>

Name of the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) to use as the lookup set.

</td></tr><tr><td>

config.minRowCount

</td><td>

String

</td><td>

Optional. Minimum number of records required in the dataset for training.Default: 10000

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Default: English Stopwords

</td></tr><tr><td>

config.testDataset

</td><td>

Object

</td><td>

Name of the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) to scan for similarities with **lookupDataset** results.

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

</td></tr><tr><td>

config.updateFrequency

</td><td>

 

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

</td></tr></tbody>
</table>The following example shows how to create an object and add it to the SimilaritySolution store.

```
var incidentData = new sn_ml.DatasetDefinition({
        'tableName' : 'incident',
        'fieldNames' : ['category', 'short_description']        
    });
    var kbData = new sn_ml.DatasetDefinition({
        'tableName' : 'kb_knowledge',
        'fieldNames' : ['short_description'],
        'encodedQuery' : 'active=true'
    });

    var mySolution = new sn_ml.SimilaritySolution({
        'label': "similarity solution",
        'lookupDataset' : kbData,
        'testDataset' : incidentData,              
    });
    
    // add solution
    var solutionName = sn_ml.SimilaritySolutionStore.add(mySolution);
```

## SimilaritySolution - cancelTrainingJob\(\)

Cancels a job for a solution object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var mySolution = sn_ml.SimilaritySolutionStore.get('ml_sn_global_global_similarity');

mySolution.cancelTrainingJob();
```

## SimilaritySolution - getActiveVersion\(\)

Gets the active SimilaritySolutionVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) object.|

The following example shows how to get an active SimilaritySolution version from the store and return its training status.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_global_similarity');

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

## SimilaritySolution - getAllVersions\(\)

Gets all versions of a SimilaritySolution object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of a solution object. See also [SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) API.|

The following example shows how to get all SimilaritySolution version objects and call the getVersionNumber\(\) and getStatus\(\) solution version methods on them.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_global_Similarity');

var mlSolutionVersions = mlSolution.getAllVersions();

for (i = 0; i < mlSolutionVersions.length; i++) {
gs.print("Version " + mlSolutionVersions[i].getVersionNumber() + " Status: " + mlSolutionVersions[i].getStatus() +"\n");

```

Output:

```
Version 3 Status: {"state":"solution_complete","percentComplete":"100","hasJobEnded":"true"}

Version 2 Status: {"state":"solution_complete","percentComplete":"100","hasJobEnded":"true"}

Version 1 Status: {"state":"solution_cancelled","percentComplete":"0","hasJobEnded":"true"}
```

## SimilaritySolution - getLatestVersion\(\)

Gets the latest version of a solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) object corresponding to the latest version of a [SimilaritySolution](SimilaritySolutionAPI.md#).|

The following example shows how to get the latest version of a solution and return its training status.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_global_Similarity');

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

## SimilaritySolution - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the solution object.|

The following example shows how to update SimilaritySolution dataset information and print the name of the object.

```
// Update solution
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields('Similarity'));

var mySimilarity = new sn_ml.SimilaritySolution({
   'label': "my Similarity solution",
   'dataset' : myIncidentData,
   'inputFieldNames': eligibleFields['eligibleInputFieldNames'],
   'predictedFieldName': 'category'
});

// update solution
sn_ml.SimilaritySolutionStore.update('ml_x_snc_global_global_my_solution_definition_4', mySimilarity);

// print solution name
gs.print('Solution Name: '+mySimilarity.getName());
```

Output:

```
Solution Name: ml_x_snc_global_global_my_solution_definition_4
```

## SimilaritySolution - getProperties\(\)

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

Contents of the Dataset and [SimilaritySolution\(\)](SimilaritySolutionAPI.md#) object details in the [SimilaritySolutionStore](../../SimilaritySolutionStore/concept/SimilaritySolutionStoreAPI.md#).```
{
  "domainName": "String",
  "label": "String",
  "lookupDatasetProperties": {Object},
  "name": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "testDatasetProperties": {Object},
  "trainingFrequency": "String",
  "updateFrequency": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: String.

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

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

System-assigned name. Data type: String.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: Array.

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

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Data type: String.

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

</td></tr></tbody>
</table>The following example gets properties of a solution object in the store.

```
var mySolution = sn_ml.SimilaritySolutionStore.get('ml_sn_global_global_similarity_solution');

gs.print(JSON.stringify(JSON.parse(mySolution.getProperties()), null, 2));
```

Output:

```
*** Script: {
  "domainName": "global",
  "label": "similarity",
  "lookupDatasetProperties": {
    "tableName": "incident",
    "fieldNames": [
      "short_description"
    ]
  },
  "name": "ml_x_snc_global_global_similarity",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "testDatasetProperties": {
    "tableName": "incident",
    "fieldNames": [
      "short_description"
    ]
  },
  "trainingFrequency": "every_30_days",
  "updateFrequency": "do_not_update"
}
```

## SimilaritySolution - getVersion\(String version\)

Gets a solution by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of a solution.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [SimilaritySolution\(\)](SimilaritySolutionAPI.md#) object on which you can call [SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) API methods.|

The following example shows how to get the training status of a solution by version number.

```
var mlSolution = sn_ml.SimilaritySolutionStore.get('ml_x_snc_global_global_similarity');

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

## SimilaritySolution - setActiveVersion\(String version\)

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

Name of the [SimilaritySolution\(\)](SimilaritySolutionAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate a solution version in the store.

```
sn_ml.SimilaritySolution.setActiveVersion("ml_x_snc_global_similarity_solution");
```

## SimilaritySolution - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add a solution to the store using the [SimilaritySolutionStore - add\(\)](../../SimilaritySolutionStore/concept/SimilaritySolutionStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[SimilaritySolutionVersion](../../SimilaritySolutionVersion/concept/SimilaritySolutionVersionAPI.md#) object corresponding to the [SimilaritySolution](SimilaritySolutionAPI.md#) being trained.|

```
// Create a dataset 
var incidentData = new sn_ml.DatasetDefinition({
    'tableName' : 'incident',
    'fieldNames' : ['category', 'short_description']
});

var kbData = new sn_ml.DatasetDefinition({
    'tableName' : 'kb_knowledge',
    'fieldNames' : ['short_description'],
    'encodedQuery' : 'active=true'
});

// Create a solution 
var mySolution = new sn_ml.SimilaritySolution({
    'label': "similarity solution",
    'lookupDataset' : kbData,
    'testDataset' : incidentData
});

// Add solution
var solutionName = sn_ml.SimilaritySolutionStore.add(mySolution);


// Train the solution - this is a long running job 
var mySimilarityVersion = mySolution.submitTrainingJob();
```

