---
title: MLSolutionResult - Global \(deprecated\)
description: The MLSolutionResult API provides methods for managing cluster information and members of a clustering solution. You can embed the results in business logic.Instantiates a new MLSolutionResult object.Returns the solution object.Returns all members of a clustering solution.Returns all outcome information for a clustering solution.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# MLSolutionResult- Global \(deprecated\)

The MLSolutionResult API provides methods for managing cluster information and members of a clustering solution. You can embed the results in business logic.

**Note:** This API has been deprecated and is intended to be removed in a future release. Refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for the most recent guidelines.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## MLSolutionResult - MLSolutionResult\(\)

Instantiates a new MLSolutionResult object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

## MLSolutionResult - findActiveSolution\(String solutionName\)

Returns the solution object.

This method only returns the solutions if the ml\_solution definition and solution are active \(that is, trained\). For information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

|Name|Type|Description|
|----|----|-----------|
|solutionName|String|Name of the clustering ml\_solution record.|

|Type|Description|
|----|-----------|
|Object|Clustering solution object for the specified `solutionName` if the ml\_solution definition and solution is active, null otherwise.|

```
var solutionName = 'ml_incident_assignment';
  var MLS = new MLSolutionResult();
  var solution = MLS.findActiveSolution(solutionName);
  gs.print(solution);
        
```

## MLSolutionResult - getClusterAssignments\(String solutionName, Object options\)

Returns all members of a clustering solution.

<table id="table_t1q_hxt_rhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

solutionName

</td><td>

String

</td><td>

Name of active cluster solution.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. Narrows down the returned results by group and level within a clustering solution. Default: Return cluster memberships for all clusters.

</td></tr><tr><td>

options.segmentation\_field

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment group.This field provides the same grouping as options provided via **Use Group By** check box in **Clustering Solution Definitions** table. Information provided varies by table selected in the **Table** field. For information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.cluster\_id

</td><td>

String

</td><td>

Optional. The sys\_id from the ml\_cluster\_summary table.

</td></tr><tr><td>

options.rec\_sys\_id

</td><td>

String

</td><td>

Optional. The sys\_id from the table record the cluster solution is based on.

</td></tr></tbody>
</table><table id="table_u1q_hxt_rhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array of outcome objects including:-   segmentation – Field name by which to group data
-   cluster\_num – Unique cluster number within a solution of clusters \(that is, label\)
-   rec\_sys\_id – The sys\_id from the table record that the cluster solution is based on
-   rec\_display\_id – Name of the record associated with the record sys\_id.

</td></tr></tbody>
</table>The following example shows how to return all cluster members for a solution without setting values for the options object.

```
var solutionName = "<Name_of_Active_Cluster_Solution>";
var solutionResult = new MLSolutionResult();
var outcome_array = solutionResult.getClusterAssignments(solutionName);
for (var i = 0; i < outcome_array.length; i++) {
   gs.print(outcome_array [i].segmentation + ' ' + outcome_array [i].cluster_num + ' ' + outcome_array [i].rec_sys_id + ' ' + outcome_array [i].rec_display_id);
}
```

The following example shows how to return all cluster members for one record using options.rec\_sys\_id.

```
var now_GR = new GlideRecord('incident');
now_GR.get('sys_id');

var solutionName = "solution_example";
var solutionResult = new MLSolutionResult();
var options = { "rec_sys_id": now_GR.getUniqueValue() };
var outcome_array = solutionResult.getClusterAssignments(solutionName, options);
for (var i = 0; i < outcome_array.length; i++) {
   gs.print(outcome_array [i].segmentation + ' ' + outcome_array [i].cluster_num + ' ' + outcome_array [i].rec_sys_id + ' ' + outcome_array [i].rec_display_id);
}
```

## MLSolutionResult - getClusterInfo\(String solutionName, Object options\)

Returns all outcome information for a clustering solution.

<table id="table_ak2_xcn_rhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

solutionName

</td><td>

String

</td><td>

Name of active cluster solution.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional. Narrows down the returned results by group and level within a clustering solution. Default: Return cluster memberships for all clusters.

</td></tr><tr><td>

options.segmentation\_field

</td><td>

String

</td><td>

Optional. Identifies the segmentation field for which to retrieve cluster memberships, for example, assignment group.This field provides the same grouping as options provided via **Use Group By** check box in **Clustering Solution Definitions** table. Information provided varies by table selected in the **Table** field. For information, see [Create and train a clustering solution](https://www.servicenow.com/docs/access?context=create-clustering-solution&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

options.cluster\_id

</td><td>

String

</td><td>

Optional. The sys\_id from the ml\_cluster\_summary table.

</td></tr></tbody>
</table><table id="table_bk2_xcn_rhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

Array of outcome objects including:-   segmentation – Field name by which to group data
-   cluster\_num – Unique cluster number within a solution of clusters \(that is, label\)
-   total\_members – Number of records in cluster \(that is, size\)
-   cluster\_quality – Cluster quality percentile value

</td></tr></tbody>
</table>```
var solutionName = "solution_example";
var solutionResult = new MLSolutionResult();
var outcome_array = solutionResult.getClusterInfo(solutionName);
for (var i = 0; i < outcome_array.length; i++) {
gs.print(outcome_array[i].segmentation + ' ' + outcome_array[i].cluster_num + ' ' + outcome_array[i].total_members + ' ' + outcome_array[i].cluster_quality);
}
```

