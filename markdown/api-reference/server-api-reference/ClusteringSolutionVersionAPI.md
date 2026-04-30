---
title: ClusteringSolutionVersion - Global
description: The ClusteringSolutionVersion API is a scriptable object used in Predictive Intelligence stores.Cancels an update job on a trainer.Deletes cluster assignments from rows by position in table sequence or GlideDateTime.Gets assignments for a clustering solution.Gets information for a specified clustering solution in the store. The purity measurement provides insights as a percentage for the clustering fields on which the purity is based.Gets solution object properties and version number.Gets training completion status.Gets the top purity results for a clustering solution. The purity measurement provides insights as a percentage for the clustering fields on which the purity is based.Gets the status of the most recent clustering solution update job.Gets the version number of a solution object.Submits clustering update jobs with options to narrow results to a specific table and filter for matching records.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 15
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClusteringSolutionVersion- Global

The ClusteringSolutionVersion API is a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

It is used for working with solution versions based on [ClusteringSolution API](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#) objects in the [ClusteringSolution store](../../ClusteringSolutionStore/concept/ClusteringSolutionStoreAPI.md#).

The system creates a solution version each time you train a solution definition. Most versions are created during scheduled solution training.

Methods in this API are accessible using the following ClusteringSolution methods:

-   [getActiveVersion\(\)](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#)
-   [getAllVersions\(\)](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#)
-   [getLatestVersion\(\)](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#)
-   [getVersion\(\)](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClusteringSolutionVersion - cancelUpdateJob\(\)

Cancels an update job on a trainer.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an active training job that has been submitted using the [submitTrainingJob\(\)](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#) method.

```
var myCluster = new sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");
var mlSolutionVersion = myCluster.getActiveVersion();

mlSolutionVersion.cancelUpdateJob();
```

## ClusteringSolutionVersion - deleteClusterAssignments\(Object options\)

Deletes cluster assignments from rows by position in table sequence or GlideDateTime.

<table id="table_cwv_r3b_rlb" class="parameters"><thead><tr><th>

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

Object defining one option for deleting cluster assignments.**Note:** Only one delete option is valid.

</td></tr><tr><td>

options.updatedUntil

</td><td>

String

</td><td>

Deletes rows for clusters with `updated_since` values occurring before this value. Format must be provided as [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#).```
{ "updatedUntil" : "String" }
```

</td></tr><tr><td>

options.sequenceUntil

</td><td>

String

</td><td>

Deletes rows for clusters with `insert_sequence` values occurring before this value in the ML Cluster Detail \[ml\_cluster\_detail\] table. The sequence position starting point value is 1. ```
{ "sequenceUntil" : Number }
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Number|Number of rows deleted from the ML Cluster Detail \[ml\_cluster\_detail\] table.|

The following example shows how to delete rows for clusters with `updated_since` time preceding `'2020-06-28 02:50:53'`.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

var mlSolutionVersion = mlSolution.getActiveVersion();

var options = {};
options.updatedUntil = '2020-06-28 02:50:53';

var results = mlSolutionVersion.deleteClusterAssignments(options);

gs.print("Number of deleted rows: "+results);
```

Output:

```
Number of deleted rows: 6417
```

The following example shows how to delete rows for clusters with `updated_since` that are sequentially positioned prior to `1000`.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

var mlSolutionVersion = mlSolution.getActiveVersion();

var options = {};
options.sequenceUntil = 1000;

var results = mlSolutionVersion.deleteClusterAssignments(options);

gs.print("Number of deleted rows: "+results);
```

Output:

```
Number of deleted rows: 999
```

## ClusteringSolutionVersion - getClusterAssignments\(Object options\)

Gets assignments for a clustering solution.

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

Values to use to narrow down the returned results by group, level, system update times, and table row number within a clustering solution. Minimum of one argument must be specified.```
{
     "cluster_id": "String",
     "group_by": "String",
     "limit": Number,
     "sequenceSince": Number,
     "sequenceUntil": Number,
     "topNPerCluster": Number,
     "updatedSince": "String",
     "updatedUntil": "String"
}
```

</td></tr><tr><td>

options.cluster\_id

</td><td>

String

</td><td>

Optional. Cluster ID of a trained solution in the Cluster Summary \[ml\_cluster\_summary\] table.

</td></tr><tr><td>

options.group\_by

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment\_group.This field provides the same grouping as options provided in the **Use Group By** check box in the **Clustering Definition** form. The information provided varies based on the table selected in the **Table** field. For more information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.limit

</td><td>

Number

</td><td>

Optional. Maximum number of cluster assignments to retrieve.

</td></tr><tr><td>

options.sequenceSince

</td><td>

Number

</td><td>

Starting position in a table sequence. Returns information for clusters with insert\_sequence enabled and positioned after this value in the ML Cluster Detail \[ml\_cluster\_detail\] table. The sequence position starting point value is 1.

</td></tr><tr><td>

options.sequenceUntil

</td><td>

Number

</td><td>

Returns assignments for clusters with `insert_sequence` values occurring before this value in the ML Cluster Detail \[ml\_cluster\_detail\] table. The sequence position starting point value is 1.

</td></tr><tr><td>

options.topNPerCluster

</td><td>

Number

</td><td>

Number of top results to receive for each cluster.

</td></tr><tr><td>

options.updatedSince

</td><td>

String

</td><td>

Optional. Date and time. Returns information for clusters with `sys_updated_on` after the value provided in [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#).

</td></tr><tr><td>

options.updatedUntil

</td><td>

String

</td><td>

Optional. Date and time. Returns information for clusters with `sys_updated_on` before the value provided in [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#).

</td></tr></tbody>
</table><table id="table_u1q_hxt_rhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of objects containing cluster information in increasing order by cluster\_id.```
[
    {
       "cluster_id": "String",
       "group_by": "String",
       "rec_display_id": "String",
       "rec_sys_id": "String"
     }
]
```

</td></tr><tr><td>

&lt;object&gt;.cluster\_id

</td><td>

Unique cluster number within a solution of clusters.

</td></tr><tr><td>

&lt;object&gt;.group\_by

</td><td>

If grouped, name of the segmentation field associated with this cluster.

</td></tr><tr><td>

&lt;object&gt;.rec\_display\_id

</td><td>

Record type and number.

</td></tr><tr><td>

&lt;object&gt;.rec\_sys\_id

</td><td>

Record sys\_id.

</td></tr></tbody>
</table>The following example shows how to use the **options** object to filter clustering results.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get("solution_name");

var mlSolutionVersion = mlSolution.getActiveVersion();

var options = {};
options.clusterId = 56;
options.topNPerCluster = 10;
options.updatedUntil = '2020-01-17 23:16:14'; 
options.updatedSince = '2020-01-17 23:16:13'; 
options.sequenceUntil = 1000; 
options.sequenceSince = 1100; 
options.limit = 100;

var results = mlSolutionVersion.getClusterAssignments(options)

gs.print(results);
```

Output:

```
[{"cluster_id":"1","rec_display_id":"Incident": "INC0014483","rec_sys_id":"04e33e7adb401300864adfea5e961900","group_by":"network"},
 {"cluster_id":"1","rec_display_id":"Incident": "INC0011133","rec_sys_id":"5bd23af2db401300864adfea5e96194d","group_by":"network"}]
```

## ClusteringSolutionVersion - getClusterInfo\(Object options\)

Gets information for a specified clustering solution in the store. The purity measurement provides insights as a percentage for the clustering fields on which the purity is based.

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

Optional. Object containing properties that enable filtering results within a clustering solution.```
{
  "clusterId": "String",     
  "groupBy": "String",
  "limit": "String",
  "recSysId": "String",
  "sequenceSince": Number,
  "sequenceUntil": Number,
  "updatedSince": "String",
  "updatedUntil": "String"
}
```

 Default: Return cluster memberships for all clusters.

</td></tr><tr><td>

options.clusterId

</td><td>

String

</td><td>

Optional. Cluster ID of a trained solution in the Cluster Summary \[ml\_cluster\_summary\] table.

</td></tr><tr><td>

options.groupBy

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment\_group.This field provides the same grouping as options provided in the **Use Group By** check box in the **Clustering Definition** form. The information provided varies based on the table selected in the **Table** field. For more information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.limit

</td><td>

Number

</td><td>

Optional. Maximum number of cluster assignments to retrieve.

</td></tr><tr><td>

options.recSysId

</td><td>

String

</td><td>

Optional. Sys\_id of a record by which to find cluster information.

</td></tr><tr><td>

options.sequenceSince

</td><td>

Number

</td><td>

Starting position in a table sequence. Returns information for clusters with insert\_sequence enabled and positioned after this value in the ML Cluster Detail \[ml\_cluster\_detail\] table. The sequence position starting point value is 1.

</td></tr><tr><td>

options.sequenceUntil

</td><td>

Number

</td><td>

Optional. Ending position in a table sequence. Returns assignments for clusters with `insert_sequence` values occurring before this value in the ML Cluster Detail \[ml\_cluster\_detail\] table. The sequence position starting point value is 1.

</td></tr><tr><td>

options.updatedSince

</td><td>

String

</td><td>

Optional. Date and time. Returns information for clusters with `sys_updated_on` after the value provided in [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#) format.

</td></tr><tr><td>

options.updatedUntil

</td><td>

String

</td><td>

Optional. Date and time. Returns information for clusters with `sys_updated_on` before the value provided in [GlideDateTime](../../GlideDateTime/concept/c_GlideDateTimeAPI.md#).

</td></tr></tbody>
</table><table id="table_xk3_v3b_rlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of objects containing cluster information.```
[
  {   
    "cluster_concept": "String",
    "cluster_id": "String",
    "cluster_quality": "String",
    "cluster_size": "String",
    "group_by": "String",
    "insert_sequence": "String",
    "purity": "String",
    "sys_updated_on": "String"
  }
]
```

</td></tr><tr><td>

&lt;object&gt;.cluster\_concept

</td><td>

Set of words that describe the cluster in descending order of frequency. Data type: String

</td></tr><tr><td>

&lt;object&gt;.cluster\_id

</td><td>

Unique cluster number within a solution of clusters.

</td></tr><tr><td>

&lt;object&gt;.cluster\_quality

</td><td>

Number from 0 to 100. Higher numbers indicate higher cluster density. Data type: String

</td></tr><tr><td>

&lt;object&gt;.cluster\_size

</td><td>

Number of records in a cluster. Data type: String

</td></tr><tr><td>

&lt;object&gt;.group\_by

</td><td>

If grouped, name of the segmentation field associated with this cluster. Data type: String

</td></tr><tr><td>

&lt;object&gt;.insert\_sequence

</td><td>

Sequential position number of the cluster in the Cluster Summary \[ml\_cluster\_summary\] table.Data type: String

</td></tr><tr><td>

&lt;object&gt;.purity

</td><td>

Percentage value representing the purity of cluster quality.

</td></tr><tr><td>

&lt;object&gt;.sys\_updated\_on

</td><td>

System [GlideDateTime](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) value representing the date and time at which this cluster was last updated.Data type: String

</td></tr></tbody>
</table>The following example shows how to set the options object parameter and print the filtered cluster results.

```
var mlSolution = sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

var mlSolutionVersion = mlSolution.getActiveVersion();

var options = {};
options.updatedSince = '2020-05-28 02:09:53'; 
options.updatedUntil = '2020-05-28 03:15:00';
options.sequenceSince = 1;
options.limit = 10;

var results = mlSolutionVersion.getClusterInfo(options);

gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

Output:

```
[
  {
    "cluster_id": "1",
    "cluster_quality": "100",
    "cluster_size": "17",
    "purity": "",
    "insert_sequence": "8",
    "group_by": "VPN   Customer",
    "sys_updated_on": "2020-05-28 02:09:53",
    "cluster_concept": "vpn instance connection ldap user log unable usability tunnel"
  },
  {
    "cluster_id": "1",
    "cluster_quality": "100",
    "cluster_size": "10",
    "purity": "",
    "insert_sequence": "24",
    "group_by": "Live Feed",
    "sys_updated_on": "2020-05-28 02:09:53",
    "cluster_concept": "feed live user note work disable group default usability sort"
  },
  {
    "cluster_id": "1",
    "cluster_quality": "100",
    "cluster_size": "18",
    "purity": "",
    "insert_sequence": "40",
    "group_by": "Integrations",
    "sys_updated_on": "2020-05-28 02:09:53",
    "cluster_concept": "integrate usability certificate error"
  },
...
]
```

## ClusteringSolutionVersion - getProperties\(\)

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

Contents of the Dataset and [ClusteringSolution](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#) version details. Results vary by object property setup.```
{
  "algorithmConfig": {Object},
  "datasetProperties": {Object},
  "domainName": "String",
  "groupByFieldName": "String", 
  "inputFieldNames": [Array],
  "isActive": Boolean,
  "label": "String",
  "minRecordsPerCluster": Number,
  "name": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String",
  "updateFrequency": "String",
  "versionNumber": Number
}
```

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig

</td><td>

JavaScript object containing algorithm configuration properties. Property results vary by the value set in the **algorithm** property.Data type: Object

```
'algorithmConfig' : {
  "algorithm": "String",  
  // See algorithmConfig.algorithm setting description for property settings based on algorithm
}
```

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

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.distanceMetric

</td><td>

DBSCAN algorithm only. Distance metric to scan for similar data objects. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.epsilon

</td><td>

DBSCAN algorithm only. Decimal value between 0 and 1 representing the size of the neighborhood search radius. Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.minimumNeighbours

</td><td>

DBSCAN algorithm only. Minimum number of neighbors required in a point to be a part of a cluster. For **levenshteinDistance** the value must be 1 so that no points are excluded from the dataset. Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.targetCoverage

</td><td>

K-means algorithm only. Percentile field to filter out records that are less similar to each other. Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties

</td><td>

Lists the properties of the [DatatsetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object associated with the solution.

 ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

 Data type: Object

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.encodedQuery

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails

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

&lt;Object&gt;.datasetProperties.fieldDetails.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldDetails.type

</td><td>

Machine-learning field type. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.datasetProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). Data type: String

</td></tr><tr><td>

Object.groupByFieldName

</td><td>

Field name by which the system groups records into one or more clusters. Data type: String

</td></tr><tr><td>

Object.inputFieldNames

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

&lt;Object&gt;.minRecordsPerCluster

</td><td>

Minimum number of records to allow in any cluster. Data type: Number

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

System-assigned name. Data type: String

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

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.versionNumber

</td><td>

Version number of the ClusteringSolution object.

</td></tr></tbody>
</table>The following example gets properties of the active object version in the store.

```
// Get properties
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering_solution');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getProperties()), null, 2));
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
  "isActive": "true",
  "label": "clustering solution",
  "minRecordsPerCluster": 2,
  "name": "ml_x_snc_global_global_clustering_solution",
  "processingLanguage": "en",
  "stopwords": [
    "Default English Stopwords"
  ],
  "updateFrequency": "do_not_update",
  "versionNumber": "1"
}
```

## ClusteringSolutionVersion - getStatus\(Boolean includeDetails\)

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

JavaScript object containing training status information for a [ClusteringSolution](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#) object.```
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
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_cluster_solution');

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
var solutionName = 'ml_x_snc_global_global_cluster_solution';
var mlSolution = sn_ml.ClusteringSolutionStore.get(solutionName);
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

## ClusteringSolutionVersion - getTopNPurityInfo\(Object options\)

Gets the top purity results for a clustering solution. The purity measurement provides insights as a percentage for the clustering fields on which the purity is based.

<table id="table_q13_tk3_wnb" class="parameters"><thead><tr><th>

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

Options that determine the number and format of the top cluster purity results.```
{
  "clusterIds": [Array],
  "groupBy": [Array],
  "purityFields": [Array],
  "topN": Number,
  "topNFields": Number
}
```

</td></tr><tr><td>

options.clusterIds

</td><td>

Array

</td><td>

Optional. List of cluster IDs provided as strings. A cluster ID is provided in the Cluster Summary \[ml\_cluster\_summary\] table. If provided, this method returns purity cluster information for each specified cluster. Default: This method returns purity information for all clusters.

</td></tr><tr><td>

options.groupBy

</td><td>

Array

</td><td>

Optional. List of group\_by field strings from your table to help the system identify the class which is most frequent in the cluster. If provided, returns purity information for cluster solutions using group\_by fields. The Cluster Summary \[ml\_cluster\_summary\] table lists clusters and any associated Group by values.This field only applies to clusters that use group by in the clustering definition. Eligible fields are listed in the **Table** field. For details on the group by feature, refer to [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.purityFields

</td><td>

Array

</td><td>

Optional. List of purity field strings. If provided, this method only returns information for these purity fields. You can view purity values for a cluster in the Cluster Summary \[ml\_cluster\_summary\] table lists.**Note:** If both **purity\_fields** and **top\_n\_fields** are provided, this method returns **top\_n\_fields** first, then selects fields from **purity\_fields**.

 Default: Return purity information for all purity fields saved for the cluster.

</td></tr><tr><td>

options.topN

</td><td>

Number

</td><td>

Optional. Restricts the number of predictions to return to the highest values for each purity field.Maximum value: 10

 Default: Return all purity information for each purity field.

</td></tr><tr><td>

options.topNFields

</td><td>

Number

</td><td>

Optional. Restricts the number of purity fields returned to fields with the highest purity for each cluster.Maximum value: 10

 Default: Return all fields in the cluster.

</td></tr></tbody>
</table><table id="table_r13_tk3_wnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

JSON-formatted string containing a list of clusters with purity fields and details.**Note:** Results vary based on settings made in the **options** input parameter.

 The following information illustrates how cluster purity results are sorted and categorized. Refer to the example for actual output.

 ```
{
  "<clusterID>":[
    // List sorted by purity per field
    { "<fieldName>":[
      // List sorted by purity per field value
      {"<field_val1_1>":"<purity>"},
        // Additional field values
    ]},
    // Additional fields
  ],	  
  // Additional clusters
}
```

</td></tr><tr><td>

String.&lt;clusterID&gt;

</td><td>

List of clusters arranged in descending order by purity value per cluster.Data type: Array

</td></tr><tr><td>

String.&lt;clusterID&gt;.&lt;field&gt;

</td><td>

List of objects representing purity fields arranged in descending order by purity value per field. The **options.top\_n\_fields** input object parameter property determines the number of fields returned.```
"<field>":[{"<field_val>":"<purity>"}]}
```

 Data type: Array

</td></tr><tr><td>

String.&lt;clusterID&gt;.&lt;field&gt;.&lt;values&gt;

</td><td>

List of objects containing field value and purity. For example, `{"priority":[{"5":"100"}]}` is a priority field with a score of 5 and a purity value of 100 percent. Results list in descending order by purity percentage. The **options.top\_n** input object parameter property determines the number of results returned.Data type: Array

</td></tr></tbody>
</table>The following example shows how to get the top two purity results for the category field in specific cluster solutions.

```
var solution = new GlideRecord('ml_solution');
solution.addQuery('sys_id', '<clustering_solution_sys_id>');
solution.addQuery('active', 'true');
solution.query();

while (solution.next()) {

  var options = {};
  options.clusterIds = ['1', '3', '5'];
  options.purityFields = ['category'];
  options.topN = '2';
  options.topNFields = '2';

  var clustering = new sn_ml.ClusteringSolutionVersion(solution);
  var results = clustering.getTopNPurityInfo(options);

  gs.info(results);
}
```

Output displays purity insights based on the settings provided in the options parameter.

```
{"1":[{"category":[{"network":"99.96"},{"inquiry":"0.04"}]}],"3":[{"category":[{"Systems Engineering":"100"}]}],
"5":[{"category":[{"Security":"100"}]}]}
```

## ClusteringSolutionVersion - getUpdateStatus\(\)

Gets the status of the most recent clustering solution update job.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_lx2_w3b_rlb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

State of the clustering solution update.States:

-   Configuration or network error
-   Error while updating solution
-   Fetching files for updating
-   Preparing data
-   Unauthorized
-   Update complete
-   Updating is cancelled
-   Updating request received
-   Updating request timed out
-   Updating solution
-   Uploading
-   Waiting

</td></tr></tbody>
</table>The following example shows how to get the update status of a clustering solution.

```
var myCluster = new sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

gs.print(JSON.stringify(myCluster.getActiveVersion().getUpdateStatus()));
```

Output:

```
"Update Complete"
```

## ClusteringSolutionVersion - getVersionNumber\(\)

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
var mlSolution = sn_ml.ClusteringSolutionStore.get('ml_x_snc_global_global_clustering_solution');

gs.print("Version number: "+JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getVersionNumber()), null, 2));
```

Output:

```
Version number: 1
```

## ClusteringSolutionVersion - submitUpdateJob\(Object options\)

Submits clustering update jobs with options to narrow results to a specific table and filter for matching records.

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

JavaScript object containing options on which to base a clustering solution update.```
{
        "filter" : "String",
        "table" : "String"
    }
```

</td></tr><tr><td>

options.filter

</td><td>

String

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US). Enables running an update job based on the filter provided.

</td></tr><tr><td>

options.table

</td><td>

String

</td><td>

Name of the table on which to run an update job.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to submit an update job.

```
var myCluster = new sn_ml.ClusteringSolutionStore.get("ml_x_snc_global_global_clustering_solution");

var options = {"filter" : "precision", "table" : "incident"};

myCluster.getActiveVersion().submitUpdateJob(options);
```

