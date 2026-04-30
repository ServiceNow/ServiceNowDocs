---
title: Encoder - Global
description: The Encoder API provides a scriptable object used in Predictive Intelligence stores. This object converts input data into vectors of numbers, based on encoder-specific goals and configurations. Encoders can be used independently to run encodings or can be configured as part of solutions to encode text columns.Creates an encoder.Cancels a job for a encoder object that has been submitted for training.Gets the active EncoderVersion object.Gets all versions of an encoder.Gets the latest version of an encoder.Gets the name of the object to use for interaction with the store.Gets solution object properties.Gets an encoder by provided version number.Activates a specified version of an encoder in the store.Submits a training job.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Encoder- Global

The Encoder API provides a scriptable object used in Predictive Intelligence stores. This object converts input data into vectors of numbers, based on encoder-specific goals and configurations. Encoders can be used independently to run encodings or can be configured as part of solutions to encode text columns.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

Encoders are text processing objects that are either pre-trained or trained based on the language datasets you provide. You can train encoders that determine how the system interprets and processes text fields. For ML solutions that include text, you can train an encoder to specify how to process text and use the trained encoder in a solution.

Encoders have configuration and versions, and can be trained independently with their own retraining frequency. API-defined encoders are different from UI-defined encoders, because the retraining of UI-defined encoders is controlled by the solutions using them.

The encoder setup-to-training flow is as follows:

1.  Create one or more datasets using the [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) API.
2.  Use the [constructor](EncoderAPI.md#) to create an encoder object.
3.  Add the encoder object to the encoder store using the [EncoderStore - add\(\)](../../EncoderStore/concept/EncoderStoreAPI.md#) method.
4.  Train the encoder using the [submitTrainingJob\(\)](EncoderAPI.md#) method. This creates a version of the object that you can manage using the [EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) API.

Once you have trained an encoder, you can use it in a solution object:

-   [ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)
-   [ClusteringSolution](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#) \(required unless using the Levenshtein distance algorithm\)
-   [RegressionSolution](../../RegressionSolution/concept/RegressionSolutionAPI.md#)
-   [SimilaritySolution](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#) \(required\)

**Note:** This API runs with full privileges before the Vancouver Patch 7 Hotfix 2b and Washington DC Patch 7 releases. With later releases, grant access using ACLs. For more information see [Query ACLs](https://www.servicenow.com/docs/access?context=query-acl-rule&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Encoder - Encoder\(Object config\)

Creates an encoder.

To get an encoder for one or more datasets, use this constructor to create a new encoder object with a unique name.

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

JavaScript object containing configuration properties of theencoder.```
{
  "algorithmConfig": {Object},
  "datasets": [Array],
  "domainName": "String",
  "label": "String",
  "minRowCount": "String",
  "processingLanguage": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

</td></tr><tr><td>

config.algorithmConfig

</td><td>

Object

</td><td>

Optional. JavaScript object containing algorithm configuration properties. ```
'algorithmConfig' : {
  "algorithm": "String"
}
```

</td></tr><tr><td>

config.algorithmConfig.algorithm

</td><td>

String

</td><td>

Name of the algorithm for training this encoder. Possible values:

-   **paravec**: Paragraph vector word embedding.
-   **tf-idf**: Term Frequency–Inverse Document Frequency \(TF-IDF\)-based text.

</td></tr><tr><td>

config.datasets

</td><td>

Array

</td><td>

List of [DatasetDefinition](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) object names.

</td></tr><tr><td>

config.domainName

</td><td>

String

</td><td>

Optional. Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Default: Current domain, for example, `"global"`.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Default: English Stopwords

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
</table>The following example shows how to create an encoder job and add it to the encoder store.

```
var myPrbData = new sn_ml.DatasetDefinition({
    'tableName' : 'problem',
    'fieldNames' : ['short_description'],
    'encodedQuery' : 'activeANYTHING'
});

var myIncidentData = new sn_ml.DatasetDefinition({
    'tableName' : 'incident',
    'fieldNames' : ['short_description', 'description'],
    'encodedQuery' : 'activeANYTHING'
});

var myEncoder = new sn_ml.Encoder({
    'label': "encoder",
    'datasets' : [myPrbData, myIncidentData],
    'algorithmConfig' : {
        'algorithm' : 'tf-idf'
    }
});
var myEncoderName = sn_ml.EncoderStore.add(myEncoder);
```

## Encoder - cancelTrainingJob\(\)

Cancels a job for a encoder object that has been submitted for training.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following example shows how to cancel an existing training job.

```
var myEncoder = sn_ml.EncoderStore.get('ml_sn_global_global_encoder');

myEncoder.cancelTrainingJob();
```

## Encoder - getActiveVersion\(\)

Gets the active EncoderVersion object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Active [EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) object.|

The following example shows how to get an active Encoder version from the store and return its training status.

```
var mlEncoder = sn_ml.EncoderStore.get('ml_x_snc_global_global_encoder');

gs.print(JSON.stringify(JSON.parse(mlEncoder.getActiveVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "encoder_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## Encoder - getAllVersions\(\)

Gets all versions of an encoder.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Existing versions of an encoder object. See also [EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) API.|

The following example shows how to get all Encoder version objects and call the getVersionNumber\(\) and getStatus\(\) encoder version methods on them.

```
var mlEncoder = sn_ml.EncoderStore.get('ml_x_snc_global_global_encoder');

var mlEncoderVersions = mlEncoder.getAllVersions();

for (i = 0; i < mlEncoderVersions.length; i++) {
gs.print("Version " + mlEncoderVersions[i].getVersionNumber() + " Status: " + mlEncoderVersions[i].getStatus() +"\n");
};
```

Output:

```
Version 3 Status: {"state":"encoder_complete","percentComplete":"100","hasJobEnded":"true"}

Version 2 Status: {"state":"encoder_complete","percentComplete":"100","hasJobEnded":"true"}

Version 1 Status: {"state":"encoder_cancelled","percentComplete":"0","hasJobEnded":"true"}
```

## Encoder - getLatestVersion\(\)

Gets the latest version of an encoder.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) object corresponding to the latest version of an [Encoder\(\)](EncoderAPI.md#).|

The following example shows how to get the latest version of an encoder and return its training status.

```
var mlEncoder = sn_ml.EncoderStore.get('ml_x_snc_global_global_encoder');

gs.print(JSON.stringify(JSON.parse(mlEncoder.getLatestVersion().getStatus()), null, 2));
```

Output:

```
{
  "state": "encoder_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## Encoder - getName\(\)

Gets the name of the object to use for interaction with the store.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the encoder object.|

The following example shows how to update Encoder dataset information and print the name of the object.

```
// Update encoder
var myIncidentData = new sn_ml.DatasetDefinition({
   'tableName' : 'incident',
   'fieldNames' : ['category', 'short_description', 'priority'],
   'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields(encoder));

var myEncoder = new sn_ml.Encoder({
   'label': "my encoder",
   'datasets' : [myIncidentData],
   'inputFieldNames': eligibleFields['eligibleInputFieldNames'],
   'predictedFieldName': 'category'
});

// update encoder
sn_ml.EncoderStore.update('ml_x_snc_global_global_my_definition_4', myEncoder);

// print encoder name
gs.print('Encoder Name: '+myEncoder.getName());
```

Output:

```
Encoder Name: ml_x_snc_global_global_my_definition_4
```

## Encoder - getProperties\(\)

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

Contents of the Dataset and [Encoder\(\)](EncoderAPI.md#) object details in the [EncoderStore](../../EncoderStore/concept/EncoderStoreAPI.md#).```
{
  "algorithmConfig" : {Object},
  "datasetsProperties": [Array],
  "domainName": "String",
  "label": "String",
  "name": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig.algorithm

</td><td>

Name of the algorithm for training this encoder. Possible values:

-   **paravec**: Paragraph vector word embedding.
-   **tf-idf**: Term Frequency–Inverse Document Frequency \(TF-IDF\)-based text.

 Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.algorithmConfig

</td><td>

Optional. JavaScript object containing algorithm configuration properties. ```
'algorithmConfig' : {
  "algorithm": "String"
}
```

 Data type: Object.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties

</td><td>

List of [DatasetDefinition\(\)](../../DatasetDefinition/concept/DatasetDefinitionAPI.md#) properties associated with the encoder.

 ```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

 Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties.tableName

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties.fieldNames

</td><td>

List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Data type: Array.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties.fieldNames.fieldDetails

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

&lt;Object&gt;.datasetsProperties.fieldNames.fieldDetails.&lt;object&gt;.name

</td><td>

Name of the field defining the type of information to restrict this dataset to. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties.fieldDetails.&lt;object&gt;.type

</td><td>

Machine-learning field type. Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.datasetsProperties.fieldDetails.encodedQuery

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://www.servicenow.com/docs/access?context=domain-separation-predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Data type: String.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://www.servicenow.com/docs/access?context=create-custom-stopwords-list&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US). Data type: Array.

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
</table>The following example gets properties of an encoder object in the store.

```
var myEncoder = sn_ml.EncoderStore.get('ml_sn_global_global_encoder');

gs.print(JSON.stringify(JSON.parse(myEncoder.getProperties()), null, 2));
```

Output:

```
*** Script: {
  "datasetsProperties": [
    {
      "tableName": "incident",
      "fieldNames": [
        "assignment_group",
        "short_description",
        "description"
      ],
      "encodedQuery": "activeANYTHING"
    }
  ],
  "domainName": "global",
  "label": "my encoder definition",
  "name": "ml_x_snc_global_global_my_encoder_definition",
  "processingLanguage": "en",
  "scope": "global",
  "stopwords": [
    "Default English Stopwords"
  ],
  "trainingFrequency": "run_once"
}
```

## Encoder - getVersion\(String version\)

Gets an encoder by provided version number.

|Name|Type|Description|
|----|----|-----------|
|version|String|Existing version number of an encoder.|

|Type|Description|
|----|-----------|
|Object|Specified version of the [Encoder\(\)](EncoderAPI.md#) object on which you can call [EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) API methods.|

The following example shows how to get the training status of an encoder by version number.

```
var mlEncoder = sn_ml.EncoderStore.get('ml_x_snc_global_global_encoder');

gs.print(JSON.stringify(JSON.parse(mlEncoder.getVersion('1').getStatus()), null, 2));
```

Output:

```
{
  "state": "encoder_complete",
  "percentComplete": "100",
  "hasJobEnded": "true"
}
```

## Encoder - setActiveVersion\(String version\)

Activates a specified version of an encoder in the store.

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

Name of the [Encoder\(\)](EncoderAPI.md#) object version to activate.Activating this version deactivates any other version.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to activate an encoder version in the store.

```
sn_ml.Encoder.setActiveVersion("ml_incident_categorization");
```

## Encoder - submitTrainingJob\(\)

Submits a training job.

**Note:** Before running this method, you must first add an encoder to the store using the [EncoderStore - add\(\)](../../EncoderStore/concept/EncoderStoreAPI.md#) method.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|[EncoderVersion](../../EncoderVersion/concept/EncoderVersionAPI.md#) object corresponding to the [Encoder](EncoderAPI.md#) being trained.|

The following example shows how to create a dataset, apply it to an encoder, add it to a store, and submit the training job.

```
// Create a dataset 
var myData = new sn_ml.DatasetDefinition({

  'tableName' : 'incident',
  'fieldNames' : ['assignment_group', 'short_description', 'description'],
  'encodedQuery' : 'activeANYTHING'

});

// Create an encoder 
var myEncoder = new sn_ml.Encoder({

  'label': "my encoder definition",
  'datasets' : [myData],
  'predictedFieldName' : 'assignment_group',
  'inputFieldNames':['short_description']

});

// Add the encoder to the store to later be able to retrieve it.
var my_unique_name = sn_ml.EncoderStore.add(myEncoder);

// Train the encoder - this is a long running job 
var myEncoderVersion = myEncoder.submitTrainingJob();
```

