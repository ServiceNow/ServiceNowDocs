---
title: DatasetDefinition - Global
description: The DatasetDefinition API provides methods to identify a set of records including a table name, columns, and row selection criteria to use as input for ML training algorithms. Datasets don't contain the actual data.Creates an instance of the DatasetDefinition class, enabling you to define a dataset by table name, fields, and query.Returns a list of fields that are eligible as either input fields \(features\) or predicted fields regarding a solution of a given capability, for example, a classification solution. Eligibility is determined based on the fields having the appropriate glide data types.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DatasetDefinition- Global

The DatasetDefinition API provides methods to identify a set of records including a table name, columns, and row selection criteria to use as input for ML training algorithms. Datasets don't contain the actual data.

This API requires the Predictive Intelligence plugin \(com.glide.platform\_ml\) and is provided within the `sn_ml` namespace. For information, see [Predictive Intelligence](https://www.servicenow.com/docs/access?context=predictive-intelligence&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Use the dataset to estimate mutual information [PredictabilityEstimate](../../PredictabilityEstimate/concept/PredictabilityEstimateAPI.md#) or train data specified by an [Encoder](../../Encoder/concept/EncoderAPI.md#). You can also use the dataset to train data specified by one of the following solution types:

-   [ClassificationSolution](../../ClassificationSolution/concept/ClassificationSolutionAPI.md#)
-   [ClusteringSolution](../../ClusteringSolution/concept/ClusteringSolutionAPI.md#)
-   [RegressionSolution](../../RegressionSolution/concept/RegressionSolutionAPI.md#)
-   [SimilaritySolution](../../SimilaritySolution/concept/SimilaritySolutionAPI.md#)

For usage guidelines, refer to [Using ML APIs](https://www.servicenow.com/docs/access?context=using-ml-apis&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DatasetDefinition - DatasetDefinition\(Object\)

Creates an instance of the DatasetDefinition class, enabling you to define a dataset by table name, fields, and query.

Create your dataset definition by passing a table and a list of fields. You can also pass a query to restrict datasets to include rows with specific characteristics.

Once created, a DatasetDefinition object cannot be modified.

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

JavaScript object containing the dataset definition properties.```
{
  "encodedQuery": "String",
  "fieldDetails": [Array],
  "fieldNames": [Array],
  "tableName": "String"
}
```

</td></tr><tr><td>

config.tableName

</td><td>

String

</td><td>

Name of the table for the dataset. For example, `"tableName" : "Incident"`.

</td></tr><tr><td>

config.fieldNames

</td><td>

Array

</td><td>

Optional. List of field names from the specified table as strings. For example, `"fieldNames" : ["short_description", "priority"]`. Default: All fields

</td></tr><tr><td>

config.fieldDetails

</td><td>

Array

</td><td>

Optional. List of JavaScript objects that specify field properties. Use this property to force machine learning algorithms to interpret fields as being a specific type. You do not need to get field details for every field listed in the **fieldNames** property. All details must correspond with a field listed in the **fieldNames** array.

 ```
[
  {
    "name": "String",
    "type": "String"
  }
]
```

</td></tr><tr><td>

config.fieldDetails.name

</td><td>

String

</td><td>

Name of the field defining the type of information to restrict this dataset to. If used, this field name must match the corresponding name listed in the **fieldNames** property.

</td></tr><tr><td>

config.fieldDetails.type

</td><td>

String

</td><td>

Machine-learning field type. Specifying the data type forces the ML trainer to interpret a field as having that type. If no data type is specified, the system determines the type.Supported types:

-   **nominal**: ML interprets this field as containing classes or categories.
-   **numeric**: ML interprets this field as containing numbers.
-   **text**: ML interprets this field as containing text.

 These types identify data types from a machine learning perspective. The ML type might differ from the type listed in the source table. A field can be a string type, but its purpose can be to encode a nominal value. For example, t-shirt sizes such as "XL", "L", or "M" are string types in the table, but each value represents a categorgy of a nominal attribute from an ML perspective.

</td></tr><tr><td>

config.encodedQuery

</td><td>

String

</td><td>

Optional. Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US). You can construct the query to be absolute or relative. For example, your query can return rows for the previous 3 months \(relative\), or for the May through July period \(absolute\). Whether using an absolute or relative pattern, the data a definition identifies can change if the rows in the underlying table change.

</td></tr></tbody>
</table>The following example shows how to create a dataset definition.

```
var myData = new sn_ml.DatasetDefinition(
  { 
     'tableName' : 'incident', 
     'fieldNames' : ['category', 'short_description', 'priority', 'assignment_group.name'],
     'fieldDetails' : [
       {
         'name' : 'category',
         'type' : 'nominal'
       },
       {
         'name' : 'short_description',
         'type' : 'text'
       }], 
     'encodedQuery' : 'sys_created_onONLast%202%20quarters@javascript:gs.beginningOfLast2Quarters()@javascript:gs.endOfLast2Quarters()^state=3'
  });
```

## DatasetDefinition - getEligibleFields\(String capability\)

Returns a list of fields that are eligible as either input fields \(features\) or predicted fields regarding a solution of a given capability, for example, a classification solution. Eligibility is determined based on the fields having the appropriate glide data types.

<table id="table_j34_5w4_flb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

capability

</td><td>

String

</td><td>

Capability for which to retrieve fields eligible for training. This method currently only supports classification solutions, any other value for the capability throws a "capability not supported" exception.Valid values: `"classification"`

</td></tr></tbody>
</table><table id="table_k34_5w4_flb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object containing eligible input field names and eligible output field names.```
{	 
  "eligibleInputFieldNames" : [Array],
  "eligibleOutputFieldNames" : [Array] 
}
```

</td></tr><tr><td>

&lt;Object&gt;.eligibleInputFieldNames

</td><td>

List of strings indicating input fields eligible for training. Data type: Array

</td></tr><tr><td>

&lt;Object&gt;.eligibleOutputFieldNames

</td><td>

List of strings indicating output fields eligible for training. Data type: Array

</td></tr></tbody>
</table>The following example shows how to display eligible fields for a classification solution.

```
var myIncidentData = new sn_ml.DatasetDefinition({
  'tableName' : 'incident',
  'encodedQuery' : 'activeANYTHING'
});

var eligibleFields = JSON.parse(myIncidentData.getEligibleFields('classification'));

gs.print(JSON.stringify(eligibleFields, null, 2));
```

Output:

```
{
  "eligibleInputFieldNames": [
    "resolved_by",
    "short_description",
    "description",
    "notify"
  ],
  "eligibleOutputFieldNames": [
    "parent",
    "caused_by",
    "location",
    "category"
  ]
}
```

