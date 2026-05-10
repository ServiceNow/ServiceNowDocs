---
title: PredictabilityEstimateStore - Global
description: Enables storing and retrieving predictability estimates.Adds a new predictability estimate object to the store and returns a unique name.Removes a specified predictability estimate object from the store.Gets a predictability estimate object from a store.Gets the names of all predictability estimate definition records in the store.Updates a predictability estimate object in a store.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# PredictabilityEstimateStore- Global

Enables storing and retrieving predictability estimates.

The PredictabilityEstimateStore API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## PredictabilityEstimateStore - add\(Object mlEstimate\)

Adds a new predictability estimate object to the store and returns a unique name.

**Note:** Label values do not need to be unique. For example, if you run this method with the same label 10 times, this method adds 10 different uniquely-named objects to the store.

|Name|Type|Description|
|----|----|-----------|
|mlEstimate|[PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)|[PredictabilityEstimate\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) object to add to the store.|

|Type|Description|
|----|-----------|
|String|System-generated predictability estimate name.|

The following example shows how to add a predictability estimate to the store. Use [PredictabilityEstimate - submitTrainingJob\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) to run the training job after adding it to the store.

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
```

## PredictabilityEstimateStore - deleteObject\(String name\)

Removes a specified predictability estimate object from the store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the [PredictabilityEstimate\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) object to be deleted.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to delete a predictability estimate from the store.

```
sn_ml.PredictabilityEstimateStore.deleteObject("ml_sn_global_global_estimate");
```

## PredictabilityEstimateStore - get\(String name\)

Gets a predictability estimate object from a store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of a predictability estimate in a store.|

|Type|Description|
|----|-----------|
|Object|[PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) object. Returns an error if the object does not exist.|

The following example shows how to get a predictability estimate object from the store using the get\(\) method and view its training status using the [PredictabilityEstimate - getActiveVersion\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) and [PredictabilityEstimateVersion - getStatus\(\)](../../PredictabilityEstimateVersion/concept/PredictabilityEstimateVersionAPI.md#) methods.

```
// Get status
var mlEstimate = sn_ml.PredictabilityEstimateStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlEstimate.getActiveVersion().getStatus(), null, 2)));
```

Output:

```
{
 "state":"solution_complete",
 "percentComplete":"100",
 "hasJobEnded":"true"
}
```

## PredictabilityEstimateStore - getAllNames\(Object options\)

Gets the names of all predictability estimate definition records in the store.

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

Optional. Name of the domain for your solution object. Refer to [Domain separation and Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/domain-separation-predictive-intelligence.md).

</td></tr><tr><td>

options.scope

</td><td>

String

</td><td>

Optional. Name of an [application scope](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationScope.md) for your solution object.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array|List of strings representing predictability estimate object names in the store.|

In the following example, the getAllNames\(\) method returns a list of all names in the store.

```
gs.print(JSON.stringify(JSON.parse(sn_ml.PredictabilityEstimateStore.getAllNames()), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_predictability_estimate_1",
  "ml_x_snc_global_global_predictability_estimate",
  "ml_x_snc_global_global_predictability_estimate_2",
  "ml_x_snc_global_global_my_estimate_definition"
]
```

In the following example, the getAllNames\(\) method returns only names associated with values set in the **options** parameter.

```
var options = {
  'label' : 'my estimate definition',
  'domainName' : 'global',
  'scope' : 'global'
};
var solNames = sn_ml.PredictabilityEstimateStore.getAllNames(options);
gs.print(JSON.stringify(JSON.parse(solNames), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_my_estimate_definition"
]
```

## PredictabilityEstimateStore - update\(String name, Object mlEstimate\)

Updates a predictability estimate object in a store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the predictability estimate to update.|
|mlEstimate|[PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#)|[PredictabilityEstimate\(\)](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) object properties to update.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to update a predictability estimate object in the store.

```
var estimateUpdate = new sn_ml.PredictabilityEstimate({
  'label': 'my estimate definition',
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames': ['short_description']
});

sn_ml.PredictabilityEstimateStore.update('ml_sn_global_global_incident_service', estimateUpdate);
```

