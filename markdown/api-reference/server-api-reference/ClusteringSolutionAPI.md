---
title: ClusteringSolution - Global
description: The ClusteringSolution API is a scriptable object used in Predictive Intelligence stores.Creates a cluster solution.Cancels a job for a solution object that has been submitted for training.Gets the active ClusteringSolutionVersion object.Gets all versions of a clustering solution.Gets the latest version of a solution.Gets the name of the object to use for interaction with the store.Gets solution object properties.Gets a solution by provided version number.Activates a specified version of a solution in the store.Submits a training job.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClusteringSolution- Global

The ClusteringSolution API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The solution setup-to-training flow is as follows:

1.  Create a dataset using the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) API.
2.  Use the [constructor](ClusteringSolutionAPI.md#) to create a clustering solution object.
3.  Add the solution object to the clustering solution store using the [ClusteringSolutionStore - add\(\)](../../ClusteringSolutionStore/concept/ClusteringSolutionStoreAPI.md#) method.
4.  Train the solution using the [submitTrainingJob\(\)](ClusteringSolutionAPI.md#) method. This creates a version of the object that you can manage using the [ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) API.

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClusteringSolution - ClusteringSolution\(Object config\)

Creates a cluster solution.

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
  "clusterConcept": "String",
  "clusterConceptFieldNames": [Array],
  "dataset": {Object},
  "domainName": "String",
  "groupByFieldName": "String",
  "groupUnclusteredRecords": Boolean,
  "inputFieldNames": [Array],
  "label": "String",
  "maxTimeWindowForUpdate" : Number,
  "minRecordsPerCluster" : Number,
  "minRowCount": "String",
  "processingLanguage": "String",
  "stopwords": [Array],
  "trainingFrequency": "String",
  "updateFrequency": "String"
}
```

</td></tr><tr><td>

config.algorithmConfig

</td><td>

Object

</td><td>

Required. JavaScript object containing algorithm configuration properties. Property settings vary by the value set in the **algorithm** property.```
'algorithmConfig': {
  "algorithm": "String",  
  // See algorithmConfig.algorithm setting description for property settings based on algorithm
}
```

</td></tr><tr><td>

config.algorithmConfig.algorithm

</td><td>

String

</td><td>

Method for encoding your solution. Valid values:

-   **dbscan** – Density-Based Spatial Clustering of Applications with Noise \(DBSCAN\) clustering algorithm. Properties used with this algorithm:
    -   **distanceMetric**
    -   **epsilon**
    -   **minimumNeighbours**
-   **hdbscan** – Hierarchical Density Based Spatial Clustering of Applications with Noise \(HDBSCAN\) clustering algorithm. Properties used with this algorithm:
    -   **minimumSamples**
-   **kmeans** – K-means clustering algorithm. Default. The **targetCoverage** property is used with this algorithm.

 Some users prefer DBSCAN because it doesn't require you to specify the number of clusters in the data before clustering.

 Properties for **dbscan**:

```
'algorithmConfig': {
  "algorithm": "dbscan",
  "distanceMetric": "String",
  "epsilon": Number,
  "minimumNeighbours": Number
}
```

 Properties for **hdbscan**:

```
'algorithmConfig': {
  "algorithm": "hdbscan",
  "minimumSamples": Number
}
```

 Properties for **kmeans**:

```
'algorithmConfig': {
  "algorithm": "kmeans",
  "targetCoverage": Number
}
```

</td></tr><tr><td>

config.algorithmConfig.distanceMetric

</td><td>

String

</td><td>

DBSCAN algorithm only. Distance metric to scan for similar data objects. Valid values: **levenshteinDistance**

</td></tr><tr><td>

config.algorithmConfig.epsilon

</td><td>

Number

</td><td>

DBSCAN algorithm only. Decimal value between 0 and 1 representing the size of the neighborhood search radius.

</td></tr><tr><td>

config.algorithmConfig.minimumNeighbours

</td><td>

Number

</td><td>

DBSCAN algorithm only. Minimum number of neighbors required in a point to be a part of a cluster. For **levenshteinDistance** the value must be 1 so that no points are excluded from the dataset.

</td></tr><tr><td>

config.algorithmConfig.minimumSamples

</td><td>

Number

</td><td>

Minimum number of data samples in a neighborhood required to determine if a point is a core point.Default: None

</td></tr><tr><td>

config.algorithmConfig.targetCoverage

</td><td>

Number

</td><td>

K-means algorithm only. Percentile field to filter out records that are less similar to each other.

</td></tr><tr><td>

config.clusterConcept

</td><td>

String

</td><td>

Optional. Concept type. A concept is a set of words listed in descending order of frequency. To generate a TFIDF-based cluster concept, set the value to `tfidf`. Concept types are listed in the Clustering Definitions \[ml\_capability\_definition\_clustering\] table. Default: Frequency-based cluster concept

</td></tr><tr><td>

config.clusterConceptFieldNames

</td><td>

Array

</td><td>

Optional. List of cluster concept field names. These values are external columns for creating a cluster concept and not used for cluster solution training. If external columns are provided, those columns are only used for the cluster concept and not for clustering solution training. Cluster concept fields are listed in the Clustering Definitions \[ml\_capability\_definition\_clustering\] table.Default: Input text columns generate the cluster concept

</td></tr><tr><td>

config.dataset

</td><td>

Object

</td><td>

[DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object name.

</td></tr><tr><td>

config.domainName

</td><td>

String

</td><td>

Optional. Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Default: Current domain, for example, `"global"`.

</td></tr><tr><td>

config.groupByFieldName

</td><td>

String

</td><td>

Optional. Field name by which the system groups records into one or more clusters. In the following setup example, the system groups each type into an individual cluster, rendering 10 clusters.

-   **groupByFieldName** value is `'category'`
-   [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) **tableName** value is `'incident'`
-   Incident \[incident\] table has 10 category types

</td></tr><tr><td>

config.groupUnclusteredRecords

</td><td>

Boolean

</td><td>

Flag that indicates whether to group unclustered records in results.

 Valid values:

-   true: Group unclustered records separately in results.
-   false: Do not group unclustered records in results. Unclustered values \(-1\) display with the rest of the results.

 Default: false

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

config.maxTimeWindowForUpdate

</td><td>

Number

</td><td>

Optional. Number of minutes preceding the model update point to look for records. For example, if the value is 15, the system only looks for records created in the preceding 15 minutes. By default, the system scans all records.

</td></tr><tr><td>

config.minRecordsPerCluster

</td><td>

Number

</td><td>

Optional. Minimum number of records to allow in any cluster. The value must be greater than or equal to 2.Default: 2

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

Processing language in two-letter ISO 639-1 language code format.

</td></tr><tr><td>

config.stopwords

</td><td>

Array

</td><td>

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Default: English Stopwords

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
</table>The following example shows how to create an object and add it to the ClusteringSolution store. The example also shows how to submit the object for training.

```
try{
    var myData = new sn_ml.DatasetDefinition({
        'tableName' : 'incident',
        'fieldNames' : ['category', 'short_description', 'state', 'description'],
        'encodedQuery' : 'activeANYTHING'
    });
      
    var mySolution = new sn_ml.ClusteringSolution({
        'label': "clustering solution",
        'dataset' : myData,
        'inputFieldNames':['short_description'],                
        'groupByFieldName' : 'category',        
        'algorithmConfig' : {
            'algorithm' : 'kmeans',
            'targetCoverage' : '90'
        }
    });
    
    // add solution
    var solutionName = sn_ml.ClusteringSolutionStore.add(mySolution);
    var solutionVersion = mySolution.submitTrainingJob();    
    var trainingStatus = solutionVersion.getStatus();
    gs.print(JSON.stringify(JSON.parse(trainingStatus), null, 2));
​
} catch(ex){
    gs.print('Exception caught: '+ ex.getMessage());
}
```

Output:

```
{
  "state": "waiting_for_training",
  "percentComplete": "0",
  "hasJobEnded": "false"
}
```

The following example shows how to include the 'description' field as a cluster concept field.

```
var myIncidentData = new sn_ml.DatasetDefinition({
    'tableName' : 'incident',
    'fieldNames' : ['category', 'short_description', 'description'],
});

var mySolution = new sn_ml.ClusteringSolution({
	'label': 'clustering_test',
	'dataset': myIncidentData,
	'inputFieldNames': ['short_description'],
	'clusterConceptFieldNames': ['description']
});

var solutionNameFromStore = sn_ml.ClusteringSolutionStore.add(mySolution);
var myClassifier = mySolution.submitTrainingJob(); 
```

## ClusteringSolution - cancelTrainingJob\(\)

Cancels a job for a solution object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var mySolution = sn_ml.ClusteringSolutionStore.get('ml_sn_global_global_clustering');

mySolution.cancelTrainingJob();
```

## ClusteringSolution - getActiveVersion\(\)

Gets the active ClusteringSolutionVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) object.|

The following example shows how to get an active ClusteringSolution version from the store and return its training status.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering');

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

## ClusteringSolution - getAllVersions\(\)

Gets all versions of a clustering solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of a solution object. See also [ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) API.|

The following example shows how to get all ClusteringSolution version objects and call the getVersionNumber\(\) and getStatus\(\) solution version methods on them.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering');

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

## ClusteringSolution - getLatestVersion\(\)

Gets the latest version of a solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) object corresponding to the latest version of a [ClusteringSolution\(\)](ClusteringSolutionAPI.md#).|

The following example shows how to get the latest version of a solution and return its training status.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering');

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

## ClusteringSolution - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the solution object.|

The following example shows how to update ClusteringSolution dataset information and print the name of the object.

```
// Update solution
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields('clustering'));

var myCluster = new sn_ml.ClusteringSolution({
   'label': "my clustering solution",
   'dataset' : myIncidentData,
   'inputFieldNames': eligibleFields['eligibleInputFieldNames'],
   'predictedFieldName': 'category'
});

// update solution
sn_ml.ClusteringSolutionStore.update('ml_x_snc_global_global_clustering_solution', myCluster);

// print solution name
gs.print('Solution Name: '+myCluster.getName());
```

Output:

```
Solution Name: ml_x_snc_global_global_clustering_solution
```

## ClusteringSolution - getProperties\(\)

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

Contents of the Dataset and [ClusteringSolution\(\)](ClusteringSolutionAPI.md#) object details in the [ClusteringSolutionStore](../../ClusteringSolutionStore/concept/ClusteringSolutionStoreAPI.md#).```
{
  "algorithmConfig": {Object},
  "datasetProperties": {Object},
  "domainName": "String",
  "groupByFieldName": "String",
  "inputFieldNames": [Array],
  "label": "String",
  "minRecordsPerCluster" : Number,
  "name": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String",
  "updateFrequency": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig

</td><td>

JavaScript object containing algorithm configuration properties. Property results vary by the value set in the **algorithm** property.```
'algorithmConfig' : {
  "algorithm": "String",  
  // See algorithmConfig.algorithm setting description for property settings based on algorithm
}
```

 Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.algorithm

</td><td>

Method for encoding your solution. Properties for **dbscan**:

```
'algorithmConfig': {
  "algorithm": "dbscan",
  "distanceMetric": "String",
  "epsilon": Number,
  "minimumNeighbours": Number
}
```

 Properties for **kmeans**:

```
'algorithmConfig': {
  "algorithm": "kmeans",
  "targetCoverage": Number
}
```

 Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.distanceMetric

</td><td>

DBSCAN algorithm only. Distance metric to scan for similar data objects. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.epsilon

</td><td>

DBSCAN algorithm only. Decimal value between 0 and 1 representing the size of the neighborhood search radius. Data type: Number.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.minimumNeighbours

</td><td>

DBSCAN algorithm only. Minimum number of neighbors required in a point to be a part of a cluster. For **levenshteinDistance** the value must be 1 so that no points are excluded from the dataset. Data type: Number.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.targetCoverage

</td><td>

K-means algorithm only. Percentile field to filter out records that are less similar to each other. Data type: Number.

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

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.groupByFieldName

</td><td>

Field name by which the system groups records into one or more clusters. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.groupByFieldName

</td><td>

Field name by which the system groups records into one or more clusters. Data type: String

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

&lt;Object&gt;.minRecordsPerCluster

</td><td>

Minimum number of records to allow in any cluster. Data type: Number.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: Array.

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
var myCluster = new sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

gs.print(JSON.stringify(JSON.parse(myCluster.getProperties()), null, 2));
```

Output:

```
*** Script: {
  "algorithmConfig": {
    "algorithm": "kmeans",
    "targetCoverage": "90"
  },
  "datasetProperties": {
    "tableName": "incident",
    "fieldNames": [
      "category",
      "short_description",
      "state",
      "description"
    ],
    "encodedQuery": "activeANYTHING"
  },
  "domainName": "global",
  "groupByFieldName": "category",
  "inputFieldNames": [
    "short_description"
  ],
  "label": "clustering solution",
  "minRecordsPerCluster": 2,
  "name": "ml_x_snc_global_global_clustering_solution",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "trainingFrequency": "run_once",
  "updateFrequency": "do_not_update"
}}
```

## ClusteringSolution - getVersion\(String version\)

Gets a solution by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of a solution.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [ClusteringSolution\(\)](ClusteringSolutionAPI.md#) object on which you can call [ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) API methods.|

The following example shows how to get the training status of a solution by version number.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering');

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

## ClusteringSolution - setActiveVersion\(String version\)

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

Name of the [ClusteringSolution\(\)](ClusteringSolutionAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate a solution version in the store.

```
sn_ml.ClusteringSolution.setActiveVersion("ml_incident_categorization");
```

## ClusteringSolution - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add a solution to the store using the [ClusteringSolutionStore - add\(\)](../../ClusteringSolutionStore/concept/ClusteringSolutionStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[ClusteringSolutionVersion](../../ClusteringSolutionVersion/concept/ClusteringSolutionVersionAPI.md#) object corresponding to the [ClusteringSolution](ClusteringSolutionAPI.md#) being trained.|

The following example shows how to create a dataset, apply it to a solution, add the solution to a store, and submit the training job.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create a solution 
var mySolution = new sn_ml.ClusteringSolution({

  'label': "my solution definition",
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the solution to the store to later be able to retrieve it.
var my_unique_name = sn_ml.ClusteringSolutionStore.add(mySolution);

// Train the solution - this is a long running job 
var myClusterVersion = mySolution.submitTrainingJob();
```

