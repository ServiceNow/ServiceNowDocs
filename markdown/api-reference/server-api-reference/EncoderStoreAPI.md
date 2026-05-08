---
title: EncoderStore - Global
description: The EncoderStore API provides methods to store and retrieve encoders.Adds a new encoder object to the store and returns a unique name.Removes a specified encoder object from the store.Gets an encoder object from a store.Gets the names of all encoder definition records in the store.Updates an encoder object in a store.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# EncoderStore- Global

The EncoderStore API provides methods to store and retrieve encoders.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## EncoderStore - add\(Object mlEncoder\)

Adds a new encoder object to the store and returns a unique name.

**Note:** Label values do not need to be unique. For example, if you run this method with the same label 10 times, this method adds 10 different uniquely-named objects to the store.

|Name|Type|Description|
|----|----|-----------|
|mlEncoder|[Encoder](../../Encoder/concept/EncoderAPI.md#)|[Encoder\(\)](../../Encoder/concept/EncoderAPI.md#) object to add to the store.|

|Type|Description|
|----|-----------|
|String|System-generated solution name.|

The following example shows how to add an encoder to the store. Use [Encoder - submitTrainingJob\(\)](../../Encoder/concept/EncoderAPI.md#) to run the training job after adding it to the store.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create a solution 
var myEncoder = new sn_ml.Encoder({

  'label': "my encoder definition",
  'datasets' : [myData],
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the encoder to the store to later be able to retrieve it.
var my_unique_name = sn_ml.EncoderStore.add(myEncoder);
```

## EncoderStore - deleteObject\(String name\)

Removes a specified encoder object from the store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the [Encoder\(\)](../../Encoder/concept/EncoderAPI.md#) object to be deleted.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to delete an encoder from the store.

```
sn_ml.EncoderStore.deleteObject("ml_sn_global_global_encoder");
```

## EncoderStore - get\(String name\)

Gets an encoder object from a store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of an encoder in a store.|

|Type|Description|
|----|-----------|
|Object|[Encoder](../../Encoder/concept/EncoderAPI.md#) object. Returns an error if the object does not exist.|

The following example shows how to get an encoder object from the store using the get\(\) method and view its training status using the [Encoder - getActiveVersion\(\)](../../Encoder/concept/EncoderAPI.md#) and [EncoderVersion - getStatus\(\)](../../EncoderVersion/concept/EncoderVersionAPI.md#) methods.

```
// Get status
var myEncoder = sn_ml.EncoderStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(myEncoder.getActiveVersion().getStatus(), null, 2)));
```

Output:

```
{
 "state":"solution_complete",
 "percentComplete":"100",
 "hasJobEnded":"true"
}
```

## EncoderStore - getAllNames\(Object options\)

Gets the names of all encoder definition records in the store.

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
|Array|List of strings representing encoder object names in the store.|

In the following example, the getAllNames\(\) method returns a list of all names in the store.

```
gs.print(JSON.stringify(JSON.parse(sn_ml.EncoderStore.getAllNames()), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_classification_word_corpus",
  "ml_x_snc_global_global_predictability_estimate",
  "GloVe",
  "ml_x_snc_global_global_encoder",
  "ml_x_snc_global_global_predictability_estimate_1"
]
```

In the following example, the getAllNames\(\) method returns only names associated with values set in the **options** parameter.

```
var options = {
  'label' : 'my encoder definition',
  'domainName' : 'global',
  'scope' : 'global'
};
var solNames = sn_ml.EncoderStore.getAllNames(options);
gs.print(JSON.stringify(JSON.parse(solNames), null, 2));
```

Output:

```
[
  "ml_x_snc_global_global_my_encoder_definition"
]
```

## EncoderStore - update\(String name, Object mlEncoder\)

Updates an encoder object in a store.

|Name|Type|Description|
|----|----|-----------|
|name|String|Name of the encoder to update.|
|mlEncoder|[Encoder](../../Encoder/concept/EncoderAPI.md#)|[Encoder\(\)](../../Encoder/concept/EncoderAPI.md#) object properties to update.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to update an encoder object in the store.

```
var encoderUpdate = new sn_ml.Encoder({
  'label': 'my encoder definition',
  'dataset' : myData,
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames': ['short_description']
});

sn_ml.EncoderStore.update('ml_sn_global_global_incident_service', encoderUpdate);
```

