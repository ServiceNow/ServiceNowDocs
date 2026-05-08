---
title: ClassificationSolutionStore - Global
description: Enables storing and retrieving solutions.Adds a new solution object to the store and returns a unique name. Removes a specified solution object from the store.Gets a solution object from the store.Gets the names of all solution definition records in the store.Replaces an existing object in the store with the object passed as a parameter. The object name provided must be empty or match.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ClassificationSolutionStore- Global

Enables storing and retrieving solutions.

The ClassificationSolutionStore API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ClassificationSolutionStore - add\(Object mlSolution\)

Adds a new solution object to the store and returns a unique name.

**Note:** Label values do not need to be unique. For example, if you run this method with the same label 10 times, this method adds 10 different uniquely-named objects to the store.

|Name|Type|Description|
|----|----|-----------|
|mlSolution|[ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)|[ClassificationSolution\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) object to add to the store.|

|Type|Description|
|----|-----------|
|String|System-generated solution name.|

The following example shows how to add a solution to the store. Use [ClassificationSolution - submitTrainingJob\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) to run the training job after adding it to the store.

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
```

## ClassificationSolutionStore - deleteObject\(String name\)

Removes a specified solution object from the store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the [ClassificationSolution\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) object to be deleted.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to delete a solution from the store.

```
sn_ml.ClassificationSolutionStore.deleteObject("ml_sn_global_global_solution");
```

## ClassificationSolutionStore - get\(String name\)

Gets a solution object from the store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of a solution in the store.|

|Type|Description|
|----|-----------|
|Object|[ClassificationSolutionVersion](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) object. Returns an error if the object does not exist.|

The following example shows how to get a solution object from the store using the get\(\) method and view its training status using the [ClassificationSolution - getActiveVersion\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) and [ClassificationSolutionVersion - getStatus\(\)](../../ClassificationSolutionVersion/concept/ClassificationSolutionVersionAPI.md#) methods.

```
// Get status
var mlSolution = sn_ml.ClassificationSolutionStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlSolution.getActiveVersion().getStatus(), null, 2)));
```

Output:

```
{
 "state":"solution_complete",
 "percentComplete":"100",
 "hasJobEnded":"true"
}
```

## ClassificationSolutionStore - getAllNames\(Object options\)

Gets the names of all solution definition records in the store.

<table id="id_bfn_kwh_wnb" class="parameters"><thead><tr><th>

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

Options for restricting results within the specified properties.```
{
  "label": "String",
  "domainName": "String",
  "scope": "String"
};
```

</td></tr><tr><td>

options.label

</td><td>

String

</td><td>

Optional. Label of your solution object.

</td></tr><tr><td>

options.domainName

</td><td>

String

</td><td>

Optional. Name of the domain for your solution object. Refer to Domain separation and Predictive Intelligence.

</td></tr><tr><td>

options.scope

</td><td>

String

</td><td>

Optional. Name of an application scope for your solution object.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array|List of strings representing solution object names in the store.|

In the following example, the getAllNames\(\) method returns a list of all names in the store.

```
gs.print(JSON.stringify(JSON.parse(sn_ml.ClassificationSolutionStore.getAllNames()), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_my_solution_definition_3",
  "ml_incident_assignment",
  "ml_x_snc_global_global_my_solution_definition",
  "ml_x_snc_global_global_my_solution_definition_2",
  "ml_sn_global_global_incident_service"
]
```

In the following example, the getAllNames\(\) method returns only names associated with values set in the **options** parameter.

```
var options = {
  'label' : 'my solution definition',
  'domainName' : 'global',
  'scope' : 'global'
};
var solNames = sn_ml.ClassificationSolutionStore.getAllNames(options);
gs.print(JSON.stringify(JSON.parse(solNames), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_my_solution_definition"
]
```

## ClassificationSolutionStore - update\(String name, Object mlSolution\)

Replaces an existing object in the store with the object passed as a parameter. The object name provided must be empty or match.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the solution to update.|
|mlSolution|[ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)|[ClassificationSolution\(\)](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#) object properties to update.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to update a solution object in the store.

```
var solutionUpdate = new sn_ml.ClassificationSolution({
  'label': 'my solution definition',
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames': ['short_description']
});

sn_ml.ClassificationSolutionStore.update('ml_sn_global_global_incident_service', solutionUpdate);
```

