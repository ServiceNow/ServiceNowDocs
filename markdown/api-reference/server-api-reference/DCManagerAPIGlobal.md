---
title: DCManager - Global
description: The DCManager API enables you to group data by type.Assigns pre-defined or user-defined data classifications to existing dictionary entries.Removes all data classifications for the specified dictionary entries.Returns a list of all data classifications available in the current domain.Retrieves all data classifications for the specified dictionary entries.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DCManager- Global

The DCManager API enables you to group data by type.

Using this API you can:

-   Assign data classifications to existing dictionary entries.
-   Look up the data classifications for specific dictionary entries.
-   Remove all data classifications associated with specific dictionary entries.
-   Retrieve a list of all data classifications available in the current domain.

This API requires the Data Classification \[com.glide.data\_classification\] plugin.

For more information, see [Data Classification](https://www.servicenow.com/docs/access?context=data-classification&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DCManager - classify\(String dictEntries, String dataClasses\)

Assigns pre-defined or user-defined data classifications to existing dictionary entries.

Requires the admin or data\_classification\_admin role.

<table id="table_wkc_j5c_snb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictEntries

</td><td>

String

</td><td>

Sys\_ids of the records you want to classify. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\] table

</td></tr><tr><td>

dataClasses

</td><td>

String

</td><td>

Sys\_ids of the data classifications you want to assign. Entered as a comma-separated list enclosed in a string.

Table: Data Classification \[data\_classification\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Message describing the result of the operation.|

This example finds records containing social security numbers and classifies the records as confidential.

```
var dcm = new SNC.DCManager();
var confidentialClass = {};
var ssnFields = [];
var dataClasses = JSON.parse(dcm.getAllDataClasses());

// Get the Confidential data class record
dataClasses.forEach(function (dataClass) {
  if (dataClass.name == "Confidential")
    confidentialClass = dataClass;
});

// Find fields that seem to be strong social security numbers
var dictionaryGR = new GlideRecord("sys_dictionary");
dictionaryGR.addQuery("element", "ssn").addOrCondition("element", "social_security_number");
dictionaryGR.query();
while (dictionaryGR.next())
  ssnFields.push(dictionaryGR.getUniqueValue());

// Classify any found entries as Confidential
if (ssnFields.length > 0)
  dcm.classify(ssnFields.join(), confidentialClass.sys_id);

```

Output:

```
"Successfully stored the data classification configurations"
```

## DCManager - clearClassification\(String dictEntries\)

Removes all data classifications for the specified dictionary entries.

Requires the admin or data\_classification\_admin role.

<table id="table_jls_l5c_snb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictEntries

</td><td>

String

</td><td>

Sys\_ids of the records you want to remove classifications from. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Message describing the result of the operation.|

This example removes the data classification for a dictionary entry.

```
var dcm = new SNC.DCManager();
gs.info(dcm.clearClassification("445de0a6dba30300efc57416bf9619b0"));

```

Output:

```
"Classifications removed for the specified dictionary entries"
```

## DCManager - getAllDataClasses\(\)

Returns a list of all data classifications available in the current domain.

Requires the admin, data\_classification\_admin, or data\_classification\_auditor role.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ryt_m5c_snb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Array&gt;

</td><td>

Result of the request. Returns the sys\_id and name for each available data classification. If there are no data classifications, it returns an empty array.

 Data classifications can be organized into parent-child relationships. If there are parent data classifications, they are identified in the result.

 Data type: Array

 ```
[
  {
    "parent": {Object},
    "sys_id": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

&lt;Array&gt;.parent

</td><td>

Entry for a parent data classification.Data type: Object

 ```
"parent": {
  "sys_id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

&lt;Array&gt;.parent.sys\_id

</td><td>

Sys\_id of the parent data classification from the Data Classification \[data\_classification\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.parent.name

</td><td>

Name of the parent data classification.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.sys\_id

</td><td>

Sys\_id of the data classification from the Data Classification \[data\_classification\] table.Data type: String

</td></tr><tr><td>

&lt;Array&gt;.name

</td><td>

Name of the data classification.Data type: String

</td></tr></tbody>
</table>This example retrieves a list of all available data classifications.

```
var dcm = new SNC.DCManager();
gs.info(dcm.getAllDataClasses());

```

Output:

```
[
  {
    "parent": {
      "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
      "name": "Confidential"
    },
    "sys_id": "348107b951d71010f877f3f178e7dd0d",
    "name": "Personally identifiable information"
  },
  {
    "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
    "name": "Confidential"
  },
  {
    "sys_id": "59b7070b73fc1010ae8dd21efaf6a764",
    "name": "Restricted"
  },
  {
    "sys_id": "11d60fc773fc1010ae8dd21efaf6a744",
    "name": "Internal"
  },
  {
    "sys_id": "f5b4cf4773fc1010ae8dd21efaf6a766",
    "name": "Public"
  }
]
```

## DCManager - getClassification\(String dictEntries\)

Retrieves all data classifications for the specified dictionary entries.

<table id="table_mfh_k5c_snb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

dictEntries

</td><td>

String

</td><td>

Sys\_ids of the records you want to retrieve classifications for. Entered as a comma-separated list enclosed in a string.

Table: Dictionary \[sys\_dictionary\]

</td></tr></tbody>
</table><table id="table_nfh_k5c_snb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

JSON object containing each dictionary entry's sys\_id with an array of its associated data classes. If there are no associated data classifications, it returns a message describing the result of the operation.

 Data classifications can be organized into parent-child relationships. If there are parent data classifications, they are identified in the result.

 Data type: Object

 ```
{
  <sys_dictionary_sys_id>: [
    {
      "parent": {Object},
      "sys_id": "String",
      "name": "String"
    }
  ]
}

```

</td></tr><tr><td>

&lt;Object&gt;.parent

</td><td>

Entry for a parent data classification.Data type: Object

```
"parent": {
  "sys_id": "String",
  "name": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.parent.sys\_id

</td><td>

Sys\_id of the parent data classification from the Data Classification \[data\_classification\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.parent.name

</td><td>

Name of the parent data classification.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.sys\_id

</td><td>

Sys\_id of the data classification from the Data Classification \[data\_classification\] table.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.name

</td><td>

Name of the data classification.Data type: String

</td></tr></tbody>
</table>This example retrieves the data classifications for a dictionary entry.

```
var dcm = new SNC.DCManager();
gs.info(dcm.getClassification("445de0a6dba30300efc57416bf9619b0"));

```

Output:

```
{
  "445de0a6dba30300efc57416bf9619b0": [
    {
      "parent": {
        "sys_id": "a9670fc773fc1010ae8dd21efaf6a735",
        "name": "Confidential"
      },
      "sys_id": "348107b951d71010f877f3f178e7dd0d",
      "name": "Personally identifiable information"
    }
  ]
}
```

