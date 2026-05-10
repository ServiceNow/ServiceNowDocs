---
title: EncoderVersion - Global
description: The EncoderVersion API provides a scriptable object used in Predictive Intelligence stores.Gets encoder object properties and version number.Returns vectors for each input sentence.Returns words similar to each input word in the descending rank order of similarity.Gets training completion status.Gets the version number of a solution object.Returns vectors for each input word.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# EncoderVersion- Global

The EncoderVersion API provides a scriptable object used in Predictive Intelligence stores.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace.

This API is used for working with encoder versions based on [Encoder API](../../Encoder/concept/EncoderAPI.md#) objects in the [Encoder store](../../EncoderStore/concept/EncoderStoreAPI.md#).

The system activates the most recent version of the encoder when it completes training, and only allows one version to be active at a time. However, you can activate any previously trained version you want to use to make predictions.

Methods in this API are accessible using the following Encoder methods:

-   [getActiveVersion\(\)](../../Encoder/concept/EncoderAPI.md#)
-   [getAllVersions\(\)](../../Encoder/concept/EncoderAPI.md#)
-   [getLatestVersion\(\)](../../Encoder/concept/EncoderAPI.md#)
-   [getVersion\(\)](../../Encoder/concept/EncoderAPI.md#)

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## EncoderVersion - getProperties\(\)

Gets encoder object properties and version number.

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

Contents of the Dataset and [Encoder](../../Encoder/concept/EncoderAPI.md#) details. Results vary by object property setup.```
{
  "algorithmConfig" : {Object},
  "datasetsProperties": [Array],
  "domainName": "String",
  "isActive": "String",
  "label": "String",
  "name": "String",
  "predictedFieldName": "String",
  "processingLanguage": "String",
  "scope": "String",
  "stopwords": [Array],
  "trainingFrequency": "String",
  "versionNumber": "Number"
}
```

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

&lt;Object&gt;.algorithmConfig.algorithm

</td><td>

Name of the algorithm for training this encoder. Possible values:

-   **paravec**: Paragraph vector word embedding.
-   **tf-idf**: Term Frequency–Inverse Document Frequency \(TF-IDF\)-based text.

 Data type: String.

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

Encoded query string in standard Glide format. See [Encoded query strings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_EncodedQueryStrings.md). Data type: String.

</td></tr><tr><td>

&lt;Object&gt;.domainName

</td><td>

Domain name associated with this dataset. See [Domain separation and Predictive Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/domain-separation-predictive-intelligence.md). Data type: String.

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

Optional. Preset list of strings that the system automatically generates based on the **language** property setting. For details, see [Create a custom stopwords list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence/create-custom-stopwords-list.md). Data type: Array.

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

&lt;Object&gt;.versionNumber

</td><td>

Version number of the Encoder object.Data type: String.

</td></tr></tbody>
</table>The following example gets properties of the active object version in the store.

```
// Get properties
var mlEncoder = sn_ml.EncoderStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlEncoder.getActiveVersion().getProperties()), null, 2));
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
  "isActive": "true",
  "label": "my encoder definition",
  "name": "ml_x_snc_global_global_my_encoder_definition",
  "processingLanguage": "en",
  "stopwords": [
    "Default English Stopwords"
  ],
  "versionNumber": "1"
}
```

## EncoderVersion - getSentenceVectors\(Array input\)

Returns vectors for each input sentence.

|Name|Type|Description|
|----|----|-----------|
|input|Array|Array of strings as sentences from which to receive vectors.|

|Type|Description|
|----|-----------|
|String|Array of sentence vectors.|

The following example shows how to return a vector for a single sentence.

```
var myEncoderName = 'GloVe';

var myEncoder = sn_ml.EncoderStore.get(myEncoderName);

var input = ["I like to code."];

var vectors = myEncoder.getActiveVersion().getSentenceVectors(input);

gs.print(vectors);

```

Output:

```
*** Script: [-0.16243751347064972,0.30614474415779114,0.08489049971103668,
-0.48100000619888306,-0.170997753739357,0.08779674768447876,-0.07848624140024185,-0.15123701095581055,
-0.07843250036239624,-1.9505999088287354,0.3007825016975403,-0.07804800570011139,-0.04779449850320816,
0.04803549498319626,0.09848674386739731,0.2427891194820404,-0.41138750314712524,0.10880374908447266,
 … ,
0.21227750182151794,0.18478751182556152,-0.3113832473754883,-0.16560424864292145,0.09052124619483948]
```

## EncoderVersion - getSimilarWords\(Array input, Object options\)

Returns words similar to each input word in the descending rank order of similarity.

<table id="table_mxj_kdb_rlb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

input

</td><td>

Array

</td><td>

Array of words for which to find similar words.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Map to refine results. ```
{ "topN":"String" }
```

</td></tr><tr><td>

options.topN

</td><td>

String

</td><td>

If provided, returns the top results up to the specified number of words. For example, use `"10"` to return the top 10 most similar words.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Array|List of elements containing the similar words for the input word in the corresponding position. These similar words are represented by an of array of pairs in the format `[word, similarity score]`.|

The following example shows how to get similar words using the `GloVe` encoder.

```
var myEncoderName = 'GloVe';
var myEncoder = sn_ml.EncoderStore.get(myEncoderName);
var input =  ["apple"];
var options = {"topN":"5"};
gs.print(myEncoder.getActiveVersion().getSimilarWords(input, options));	
```

Output:

```
*** Script: [[["iphone",0.5987],["macintosh",0.5836],["ipod",0.5761],["microsoft",0.5664],["ipad",0.5628]]]
```

## EncoderVersion - getStatus\(Boolean includeDetails\)

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

JavaScript object containing training status information for an [Encoder](../../Encoder/concept/EncoderAPI.md#) object.```
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
var mlEncoder = sn_ml.EncoderStore.get('ml_incident_categorization');

gs.print(JSON.stringify(JSON.parse(mlEncoder.getActiveVersion().getStatus(true), null, 2)));
```

Output:

```
{
 "state":"solution_complete",
 "percentComplete":"100",
 "hasJobEnded":"true",
 "details":{"stepLabel":"Encoder Complete"} // This information is only returned if getStatus(true);
}
```

The following example shows an unsuccessful result with training complete.

```
// Get status
var encoderName = 'ml_x_snc_global_global_encoder';
var mlEncoder = sn_ml.EncoderStore.get(encoderName);
var trainingStatus = mlEncoder.getLatestVersion().getStatus();

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

## EncoderVersion - getVersionNumber\(\)

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
var mlEncoder = sn_ml.EncoderStore.get('ml_incident_categorization');

gs.print("Version number: "+JSON.stringify(JSON.parse(mlEncoder.getActiveVersion().getVersionNumber()), null, 2));
```

Output:

```
Version number: 1
```

## EncoderVersion - getWordVectors\(Array input\)

Returns vectors for each input word.

|Name|Type|Description|
|----|----|-----------|
|input|Array|List of strings as words from which to receive vectors.|

|Type|Description|
|----|-----------|
|Array|List of vectors for each word provided.|

The following example shows how to get a vector from the word `hello`.

```
var myEncoderName = 'GloVe';
var myEncoder = sn_ml.EncoderStore.get(myEncoderName);
var input =  ["hello"];

gs.print(myEncoder.getActiveVersion().getWordVectors(input));
```

Output:

```
*** Script: [[-0.337119996547699,-0.2169100046157837,-0.006636499892920256,
-0.41624999046325684,-1.2554999589920044,-0.0284659992903471,-0.7219499945640564,
-0.5288699865341187,0.0072085000574588776,0.3199700117111206,0.02942500077188015,
-0.013236000202596188,0.4351100027561188,0.2571600079536438,0.3899500072002411,
 … ,
0.3384299874305725,0.4055800139904022,0.18073000013828278,0.6424999833106995]]
```

