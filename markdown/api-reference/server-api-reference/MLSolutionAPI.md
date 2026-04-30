---
title: MLSolution - Global
description: The MLSolution API provides methods for handling Predictive Intelligence predictions and retrieving solution objects for all capabilities: similarity, classification, and clustering\).Gets the prediction result for a classification solution and applies it to the input GlideRecord if the confidence value is higher than the threshold.Gets the capability information of a trained solution.Gets assignments for a clustering solution.Gets the cluster information for a clustering solution.Gets information for a specified clustering solution.Gets the version of the active solution.Determines if a solution is active.Gets the prediction results from the prediction server given a GlideRecord or an array of key-value pairs.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MLSolution- Global

The MLSolution API provides methods for handling Predictive Intelligence predictions and retrieving solution objects for all capabilities: similarity, classification, and clustering\).

This API provides methods commonly used among all solution capabilities and methods unique to classification and clustering solutions.

-   Common methods used for all solution objects:
    -   getCapability\(\)
    -   getVersion\(\)
    -   isActive\(\)
    -   predict\(\)
-   Methods only used for classification and regression solutions:
    -   applyPrediction\(\)
-   Methods only used for clustering solutions:
    -   getClusterAssignments\(\)
    -   getClusterForRecord\(\)
    -   getClusterInfo\(\)

The MLSolution API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

The methods in this object are instantiated using [MLSolutionFactory](../../MLSolutionFactory/concept/MLSolutionFactoryAPI.md#).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

**Related topics**  


[MLSolutionUtil](../../MLSolutionUtil/concept/MLSolutionUtilAPI.md#)

[REST API: Get predictions for multiple solutions](../../../../../integrate/inbound-rest/concept/agent-intelligence-api.md#)

## MLSolution - applyPrediction\(GlideRecord now\_GR\)

Gets the prediction result for a classification solution and applies it to the input GlideRecord if the confidence value is higher than the threshold.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|GlideRecord object containing values on which to run a prediction and apply the results.|

<table id="table_iqw_pbm_yfb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the prediction was applied:

 -   true: Prediction applied
-   false: Prediction rejected

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization");

var inputGR = new GlideRecord("incident");
inputGR.get("0ef47232db801300864adfea5e961912");

mlSolution.applyPrediction(inputGR);
```

## MLSolution - getCapability\(\)

Gets the capability information of a trained solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_fm3_pfx_ggb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Type of trained solution.Possible values:

-   Similarity
-   Classification
-   Clustering

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_x_global_clustering");

// configure optional parameters
var options = {};
options.group_by = 'network';
options.cluster_id = 1;
options.top_n_per_cluster = 3;

if (mlSolution.getCapability() == 'clustering') {
	var results = mlSolution.getClusterAssignments(options);
	// pretty print JSON results
	gs.print(JSON.stringify(JSON.parse(results), null, 2));
}
```

## MLSolution - getClusterAssignments\(Object options\)

Gets assignments for a clustering solution.

<table id="table_t1q_hxt_rhb" class="parameters"><thead><tr><th>

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

Optional. Values to use to narrow down the returned results by group and level within a clustering solution. Default: Return cluster memberships for all clusters.

</td></tr><tr><td>

options.group\_by

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment\_group.This field provides the same grouping as options provided in the **Use Group By** check box in the **Clustering Definition** form. The information provided varies based on the table selected in the **Table** field. For more information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.cluster\_id

</td><td>

String

</td><td>

Optional. Cluster ID of a trained solution in the Cluster Summary \[ml\_cluster\_summary\] table.

</td></tr><tr><td>

options.top\_n\_per\_cluster

</td><td>

Number

</td><td>

Number of top results to receive for each cluster.

</td></tr></tbody>
</table><table id="table_u1q_hxt_rhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON array containing cluster information in increasing order by cluster\_id:-   cluster\_id: String. Unique cluster number within a solution of clusters.
-   rec\_display\_id: String. Record type and number.
-   rec\_sys\_id: String. Record sys\_id.
-   group\_by: If grouped, name of the segmentation field associated with this cluster.

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_x_global_clustering");

// configure optional parameters
var options = {};
options.group_by = 'network';
options.cluster_id = '1';
// returns top 3 results per cluster
options.top_n_per_cluster = 3;

var results = mlSolution.getClusterAssignments(options);


```

Output:

```
[{"cluster_id":"1","rec_display_id":"Incident: INC0014483","rec_sys_id":"04e33e7adb401300864adfea5e961900","group_by":"network"},
 {"cluster_id":"1","rec_display_id":"Incident: INC0011133","rec_sys_id":"5bd23af2db401300864adfea5e96194d","group_by":"network"}]
```

## MLSolution - getClusterForRecord\(GlideRecord now\_GR\)

Gets the cluster information for a clustering solution.

|Name|Type|Description|
|----|----|-----------|
|now\_GR|GlideRecord|Name of the input GlideRecord.|

|Type|Description|
|----|-----------|
|String|The cluster\_id from the Cluster Summary \[ml\_cluster\_summary\] table if the record belongs to a cluster. Empty string returns if the record does not belong to a cluster.|

```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("solution_name");
var now_GR = new GlideRecord('incident');
if (mlSolution.getCapability() == 'clustering') {
var clusterId = mlSolution.getClusterForRecord(now_GR);
}
```

## MLSolution - getClusterInfo\(Object options\)

Gets information for a specified clustering solution.

<table id="table_ak2_xcn_rhb" class="parameters"><thead><tr><th>

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

Optional. Narrows down the returned results by group and level within a clustering solution. Default: Return cluster memberships for all clusters.

</td></tr><tr><td>

options.group\_by

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment\_group.This field provides the same grouping as options provided in the **Use Group By** check box in the **Clustering Definition** form. The information provided varies based on the table selected in the **Table** field. For more information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.cluster\_id

</td><td>

String

</td><td>

Optional. Cluster ID of a trained solution in the Cluster Summary \[ml\_cluster\_summary\] table.

</td></tr></tbody>
</table><table id="table_bk2_xcn_rhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON array containing cluster information in increasing order by cluster\_id:-   cluster\_id: String. Unique cluster number within a solution of clusters.
-   cluster\_quality: String. Number from 0 to 100. Higher numbers indicate higher cluster density.
-   cluster\_size: String. Number of records in a cluster.
-   group\_by: If grouped, name of the segmentation field associated with this cluster.
-   cluster\_concept: String. Set of words that describe the cluster in descending order of frequency.

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_x_global_clustering");

// configure optional parameters
var options = {};
options.group_by = 'network';
options.cluster_id = 1;

var results = mlSolution.getClusterInfo(options);
```

Output:

```
[ {"cluster_id":"1","cluster_quality":"56.6","cluster_size":"46","group_by":"SLA","cluster_concept":"issue occur capacity ..."},
  {"cluster_id":"2","cluster_quality":"55.47","cluster_size":"75","group_by":"SLA","cluster_concept":"clone instance request ..."},
... ]
```

## MLSolution - getVersion\(\)

Gets the version of the active solution.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Version of the active solution.|

```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("solution_name");

var solutionVersion = mlSolution.getVersion();
```

## MLSolution - isActive\(\)

Determines if a solution is active.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_yzj_lgx_ggb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the solution is active.-   true: Solution active
-   false: Solution inactive

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("solution_name");

var isActive = mlSolution.isActive();
```

## MLSolution - predict\(Object input, Object options\)

Gets the prediction results from the prediction server given a GlideRecord or an array of key-value pairs.

You can use this method to call prediction with multiple input records because GlideRecord is an iterator.

<table id="table_vv5_yfx_ggb" class="parameters"><thead><tr><th>

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

Optional. JSON key-value pair with the following properties:-   top\_n: Number. If provided, returns the top results, up to the specified number of predictions.
-   apply\_threshold: Boolean. Checks the threshold value for the solution and applies it to the result set. The threshold value is solution threshold for similarity or class-level threshold for classification. Default value is true.
-   custom\_results\_filter: String. Similarity solutions only. Specifies the allowed set from which results are returned using an encoded query.

</td></tr></tbody>
</table><table id="table_khq_hgx_ggb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

JSON object containing the prediction results sorted by sys\_id or record\_number. -   predictedValue: String. Value representing the prediction result.
-   predictedSysId: String. The sys\_id of the predicted value. Results can be from any table on which information is being predicted.
-   confidence: Number. Value of the confidence associated with the prediction. For example, 53.84.
-   threshold: Number. Value of the configured threshold associated with the prediction.

</td></tr></tbody>
</table>```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization");

// single GlideRecord input
var input = new GlideRecord("incident");
input.get("0ef47232db801300864adfea5e961912");

// configure optional parameters
var options = {};
options.top_n = 3;
options.apply_threshold = false;

var results = mlSolution.predict(input, options);
// pretty print JSON results
gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization");

// multiple GlideRecord input
var input = new GlideRecord("incident");
input.addQuery("sys_created_onONLast week@javascript:gs.beginningOfLastWeek()@javascript:gs.endOfLastWeek()");
input.query();

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
    input_gr_sys_id1: [
                {
                    predictedValue : xxx,
                    predictedSysId : xx0,
                    confidence : xxx,
                    threshold : xxx

                }, 
                {
                    predictedValue : yyy,
                    predictedSysId : xx1,
                    confidence : xxx,
                    threshold : xxx
                }
        ],
    input_gr_sys_id2 : [
                {
                    predictedValue : xxx,
                    predictedSysId : xx0,
                    confidence : xxx,
                    threshold : xxx

                }, 
            ...
        ]
}
```

```
var mlSolution = sn_ml.MLSolutionFactory.getSolution("ml_incident_categorization");

// key-value pairs input
var input = [{"short_description":"my email is not working"}, 
			{short_description:"need help with password"}];

// configure optional parameters
var options = {};
options.top_n = 3;
options.apply_threshold = false;

var results = mlSolution.predict(input, options);
// pretty print JSON results
gs.print(JSON.stringify(JSON.parse(results), null, 2));
```

