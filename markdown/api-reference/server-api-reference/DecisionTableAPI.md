---
title: DecisionTableAPI - Scoped, Global
description: The DecisionTableAPI class enables you to access Decision Tables data in scoped and global server-side scripts.Instantiates a DecisionTableAPI object.Creates multiple records in the Choices \[sys\_choice\] table that are linked to answer elements.Creates multiple records in the Result \[sys\_decision\_multi\_result\_element\] table that are related to the specified decision table.Creates multiple records in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table that are related to the specified decision table.Creates a decision table record in the Decision Tables \[sys\_decision\] table.Creates multiple records in the Choices \[sys\_choice\] table that are linked to decision inputs.Creates multiple records in the Decision Inputs \[sys\_decision\_input\] table that are related to the specified decision table.Creates multiple records in the Decisions \[sys\_decision\_question\] table that are related to the specified decision table.Deletes a record in the Result \[sys\_decision\_multi\_result\_element\] table.Deletes a record in the Choices \[sys\_choice\] table.Deletes a record in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.Deletes a record in the Decision Tables \[sys\_decision\] table.Deletes a record in the Decision Inputs \[sys\_decision\_input\] table.Deletes a record in the Decisions \[sys\_decision\_question\] table.Returns all decision tables from the Decision Tables \[sys\_decision\] table.Returns the answers associated with the specified decision table. An answer is a record on any table associated with a Decision \[sys\_decision\_question\] record.Evaluates a decision table based on the provided inputs and returns an answer. If no inputs are provided, returns the first default answer found.Evaluates a decision table based on the provided inputs and returns all correctly evaluated answers. If no inputs are provided, returns all default answers.Returns a single decision table from the Decision Tables \[sys\_decision\] table.Returns the decision inputs from the Decision Inputs \[sys\_decision\_input\] table associated with the passed in decision table.Returns the decisions from the Decision \[sys\_decision\_question\] table associated with the passed in decision table.Updates a record in the Result \[sys\_decision\_multi\_result\_element\] table.Updates a record in the Choices \[sys\_choice\] table.Updates a record in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.Updates a record in the Decision Tables \[sys\_decision\] table.Updates a record in the Decision Inputs \[sys\_decision\_input\] table.Updates a record in the Decisions \[sys\_decision\_question\] table.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 49
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# DecisionTableAPI - Scoped, Global

The DecisionTableAPI class enables you to access Decision Tables data in scoped and global server-side scripts.

To access DecisionTableAPI methods, use the `sn_dt` namespace. You must have the decision\_table\_crud\_api role to use this API. To learn more about Decision Tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Date/Time inputs

When using date/time inputs in a decision table, values passed to DecisionTableAPI must be provided in the ServiceNow dateTime format:

```
yyyy-MM-dd HH:mm:ss

```

Date/time values are processed without applying time zone conversion. All comparisons are performed using the internal UTC representation of the dateTime value.

As a result:

-   Decision table inputs don't support time zone offsets.
-   The system doesn't apply user and system timezones during evaluation.
-   `between` conditions compare the literal dateTime values exactly as provided.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## DecisionTableAPI - DecisionTableAPI\(\)

Instantiates a DecisionTableAPI object.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var dt = new sn_dt.DecisionTableAPI();
```

## DecisionTableAPI - createAnswerElementChoices\(String decisionID, Array questions\)

Creates multiple records in the Choices \[sys\_choice\] table that are linked to answer elements.

<table id="table_u5r_1zg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

choices

</td><td>

Array

</td><td>

Array of objects used to create records in the Choices \[sys\_choice\] table. Each object creates one choice record.```
[
  {
    "answerElementID": "String",
    "label": "String",
    "order": Number,
    "value": "String"
  }
]
```

</td></tr><tr><td>

choices.answerElementID

</td><td>

String

</td><td>

Sys\_id of the answer element to associate with the choice.Table: Result \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

choices.label

</td><td>

String

</td><td>

Label of the choice.

</td></tr><tr><td>

choices.order

</td><td>

Number

</td><td>

Optional. Order of the choice.

</td></tr><tr><td>

choices.value

</td><td>

String

</td><td>

Value of the choice.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each choice.Data type: Array

 ```
"results": [
   {
      "errors": [Array],
      "record": GlideRecord,
      "status": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the choice.Data type: Array

 ```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the choice created in the Choices \[sys\_choice\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the choice record was successfully created.Possible values:

-   Failure
-   Success

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two choices for an answer element.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var answerElementID = '99d197c83d0b9910f8776a598af912df';
var choices = [
   {
      label: 'Hyderabad',
      value: 'hyd',
      answerElementId: answerElementID,
      order: 20
   },
   { 
      label: 'Mumbai', 
      value: 'mum',
      answerElementId: answerElementID,
      order: 40
   }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createAnswerElementChoices(decisionID, choices);
gs.info('Status - ' + response.status);
gs.info('First choice sys id - ' + response.results[0].record.getValue('sys_id'));
gs.info('Second choice sys id - ' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First choice sys id - 6bc0d3c03d0b9910f8776a598af912c6
Second choice sys id - 6fc0d3c03d0b9910f8776a598af912c9
```

## DecisionTableAPI - createAnswerElements\(String decisionID, Array answerElements\)

Creates multiple records in the Result \[sys\_decision\_multi\_result\_element\] table that are related to the specified decision table.

<table id="table_adc_lyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

answerElements

</td><td>

Array

</td><td>

Array of objects used to create records in the Result Elements \[sys\_decision\_multi\_result\_element\] table. Each object creates one answer element record.```
[
   {
      label: "String",
      maxsize: Number,
      order: Number,
      reference: "String",
      type: "String"
   }
]
```

</td></tr><tr><td>

answerElements.label

</td><td>

String

</td><td>

Label of the answer element record.

</td></tr><tr><td>

answerElements.maxsize

</td><td>

Number

</td><td>

Optional. Maximum number of characters allowed in the answer element field.Use this property only if **answerElements.type** is `String`.

 Default value: 250

</td></tr><tr><td>

answerElements.order

</td><td>

Number

</td><td>

Optional. Order of the answer element.

</td></tr><tr><td>

answerElements.reference

</td><td>

String

</td><td>

Required if the value of **answerElements.type** is `Reference`. Name of the reference table used by the answer element.

</td></tr><tr><td>

answerElements.type

</td><td>

String

</td><td>

Answer element input type.Valid values:

-   Boolean
-   Choice
-   Currency
-   Decimal
-   Due\_date
-   [Glide\_date](../../glideDateScoped/concept/c_GlideDateScopedAPI.md#)
-   [Glide\_date\_time](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#)
-   [Glide\_duration](../../glideDurationScoped/concept/c_GlideDurationScopedAPI.md#)
-   Integer
-   Longint
-   Reference
-   String

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each answer element.Data type: Array

 ```
"results": [
   {
      "errors": [Array],
      "record": GlideRecord,
      "status": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the answer element.Data type: Array

 ```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the answer element created in the Result Elements \[sys\_decision\_multi\_result\_element\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the answer element record was successfully created.Possible values:

-   Failure
-   Success

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two answer elements for a decision table.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var answerElements = [
   {
      label: 'City name',
      name: 'city',
      type: 'choice',
      comments: 'City name',
   },
   { 
      label: 'Assigned To', 
      name: 'assigned_to',
      type: 'reference',
      reference: 'sys_user'
   }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createAnswerElements(decisionID, answerElements);
gs.info('Status - ' + response.status);
gs.info('First answer element sys id - ' + response.results[0].record.getValue('sys_id'));
gs.info('Second answer element sys id - ' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First answer element sys id - 41c707803d0b9910f8776a598af91201
Second answer element sys id - 51c707803d0b9910f8776a598af91217
```

## DecisionTableAPI - createConditions\(String decisionID, Array conditions\)

Creates multiple records in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table that are related to the specified decision table.

<table id="table_cqq_fyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

conditions

</td><td>

Array

</td><td>

Array of objects used to create records in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table. Each object creates one decision condition record.```
[
  { 
    "decisionInput": "String",        
    "defaultOperator": "String",
    "label": "String"
  }
]
```

</td></tr><tr><td>

conditions.decisionInput

</td><td>

String

</td><td>

Sys\_id of the decision input to associate with the condition. Table: Decision Inputs \[sys\_decision\_input\]

</td></tr><tr><td>

conditions.defaultOperator

</td><td>

String

</td><td>

Optional. Default operator for the condition. For a list of valid operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

conditions.label

</td><td>

String

</td><td>

Label of the decision condition record.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each decision condition.Data type: Array of Objects

```
"results": [
  {
    "errors": [Array],
    "record": GlideRecord,
    "status": "String"
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the decision condition.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the decision condition created in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the decision condition record was successfully created.Possible values:

-   Failure
-   Success

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two decision conditions for a decision table.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var conditions = [
    {
        label: 'Total count',
        decisionInput: '22bde5003dc39910f8776a598af91292',        
        defaultOperator: '!='
    },
    {
        label: 'Is Incident Active',
        decisionInput: '6abde5003dc39910f8776a598af9127e',
        default_operator: 'ISEMPTY',        
        order: 10,
        field: 'u_incident.active'
    }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createConditions(decisionID, conditions);
gs.info('Status - ' + response.status);
gs.info('First condition sys id - ' + response.results[0].record.getValue('sys_id'));
gs.info('Second condition sys id - ' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First condition sys id - c1530f4c3dc79910f8776a598af912ef
Second condition sys id - c9530f4c3dc79910f8776a598af912f1
```

## DecisionTableAPI - createDecisionTable\(Object decisionTable\)

Creates a decision table record in the Decision Tables \[sys\_decision\] table.

<table id="table_os1_bgn_lvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionTable

</td><td>

Object

</td><td>

Key-value pairs of the field names and values to use to create a decision table record.```
{
  "accessibleFrom": "String",
  "name": "String",
  "scope": "String
}
```

</td></tr><tr><td>

decisionTable.accessibleFrom

</td><td>

String

</td><td>

Optional. Scopes that have access to the decision table record.Valid values:

-   package\_private
-   public

</td></tr><tr><td>

decisionTable.name

</td><td>

String

</td><td>

Name of the decision table.

</td></tr><tr><td>

decisionTable.scope

</td><td>

String

</td><td>

Scope of the decision table record.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the decision table created in the Decision Tables \[sys\_decision\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates an Emergency Change Policy decision table.

```
var decisionTable = {
    name: 'Emergency Change Policy',  
    scope: 'global',
    accessibleFrom: 'public'
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createDecisionTable(decisionTable);
gs.info('Status -' + response.status);
gs.info('Decision Table sys id - ' + response.record.getValue('sys_id'));
```

Output:

```
Status - Success
Decision Table sys id - 665569083d839910f8776a598af91223
```

## DecisionTableAPI - createInputChoices\(String decisionID, Array choices\)

Creates multiple records in the Choices \[sys\_choice\] table that are linked to decision inputs.

<table id="table_u5r_1zg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

choices

</td><td>

Array

</td><td>

Array of objects used to create records in the Choices \[sys\_choice\] table. Each object creates one choice record.```
[
  {
    "inputID": "String",
    "label": "String",
    "order": Number,
    "value": "String"
  }
]
```

</td></tr><tr><td>

choices.inputID

</td><td>

String

</td><td>

Sys\_id of the decision input to associate with the choice.Table: Decision Inputs \[sys\_decision\_input\]

</td></tr><tr><td>

choices.label

</td><td>

String

</td><td>

Label of the choice.

</td></tr><tr><td>

choices.order

</td><td>

Number

</td><td>

Optional. Order of the choice.

</td></tr><tr><td>

choices.value

</td><td>

String

</td><td>

Value of the choice.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each choice.Data type: Array of Objects

```
"results": [
   {
      "errors": [Array],
      "record": GlideRecord,
      "status": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the choice.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the choice created in the Choices \[sys\_choice\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the choice record was successfully created.Possible values:

-   Failure
-   Success

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two choices for a decision input.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var inputID = '4d1f8f083d0b9910f8776a598af91274';
var choices = [
   {
      label: 'Hyderabad',
      value: 'hyd',
      inputId: inputID,
      order: 20
   },
   { 
      label: 'Mumbai', 
      value: 'mum',
      inputId: inputID,
      order: 40
   }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createInputChoices(decisionID, choices);
gs.info(JSON.stringify(response));
gs.info('Status - ' + response.status);
gs.info('First choice sys id - ' + response.results[0].record.getValue('sys_id'));
gs.info('Second choice sys id - ' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First choice sys id - 6bc0d3c03d0b9910f8776a598af912c6
Second choice sys id - 6fc0d3c03d0b9910f8776a598af912c9
```

## DecisionTableAPI - createInputs\(String decisionID, Array inputs\)

Creates multiple records in the Decision Inputs \[sys\_decision\_input\] table that are related to the specified decision table.

<table id="table_rrm_zxg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

inputs

</td><td>

Array

</td><td>

Array of objects used to create records in the Decision Input \[sys\_decision\_input\] table. Each object creates one decision input record.```
[
   {
      label: "String",
      maxsize: Number,
      order: Number,
      reference: "String",
      type: "String"
   }
]
```

</td></tr><tr><td>

inputs.label

</td><td>

String

</td><td>

Label of the decision input record.

</td></tr><tr><td>

inputs.maxsize

</td><td>

Number

</td><td>

Optional. Maximum number of characters allowed in the input field.Use this property only if **inputs.type** is `String`.

 Default value: 250

</td></tr><tr><td>

inputs.order

</td><td>

Number

</td><td>

Optional. Order of the input.

</td></tr><tr><td>

inputs.reference

</td><td>

String

</td><td>

Required if the value of **inputs.type** is `Reference`. Name of the reference table used by the decision input.

</td></tr><tr><td>

inputs.type

</td><td>

String

</td><td>

Decision input type.Valid values:

-   String
-   Integer
-   True/False
-   Choice
-   Reference
-   Date
-   Date/Time

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each decision input.Data type: Array

 ```
"results": [
   {
      "errors": [Array],
      "record": GlideRecord,
      "status": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the decision input.Data type: Array

 ```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the decision input created in the Decision Inputs \[sys\_decision\_input\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the decision input record was successfully created.Possible values:

-   Failure
-   Success

 Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two inputs for a decision table.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var inputs = [
   {
      label: 'Incident',
      type: 'reference',
      reference: 'incident',
      ref_qual: 'active=true^EQ' 
   },
   {
      label: 'Total count',
      type: 'integer'
   }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createInputs(decisionID,inputs);
gs.info('Status - ' + response.status);
gs.info('First input id –' + response.results[0].record.getValue('sys_id'));
gs.info('Second input id –' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First input id - 5dbfa58c3d839910f8776a598af91219
Second input id - 95bfe1803dc39910f8776a598af912fa
```

## DecisionTableAPI - createQuestions\(String decisionID, Array questions\)

Creates multiple records in the Decisions \[sys\_decision\_question\] table that are related to the specified decision table.

<table id="table_ucd_qyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

questions

</td><td>

Array

</td><td>

Array of objects used to create records in the Decisions \[sys\_decision\_question\] table. Each object creates one question record.```
[
  {
    "active": Boolean,
    "answer": [Array],
    "condition": "String",
    "defaultAnswer": Boolean,
    "order": Number
  }
]
```

</td></tr><tr><td>

questions.active

</td><td>

Boolean

</td><td>

Flag that indicates whether the question record is active.Valid values:

-   true: The question record is active.
-   false: The question record isn't active.

</td></tr><tr><td>

questions.answer

</td><td>

Array

</td><td>

List of possible answers to the question.For a single result table, the array can only have one object. For a multi-result table, the array can have multiple objects.

```
[
  {
    "name": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

questions.answer.name

</td><td>

String

</td><td>

Name of the answer element. Table: Result \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

questions.answer.value

</td><td>

String

</td><td>

Value of the answer element.Table: Result \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

questions.condition

</td><td>

String

</td><td>

Conditions required to reach this question.The fields available for the conditions are the decision inputs that are associated with the decision table.

For more information about creating conditions, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

questions.defaultAnswer

</td><td>

Boolean

</td><td>

Flag that indicates whether this question is the default question for the decision table.Valid values:

-   true: The question is the default question.
-   false: The question isn't the default question.

</td></tr><tr><td>

questions.order

</td><td>

Number

</td><td>

Order of the question.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Object with information about the status of the API request.```
{
  "errors": [Array],
  "results": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results

</td><td>

Array with information about the status of each question.Data type: Array of Objects

```
"results": [
   {
      "errors": [Array],
      "record": GlideRecord,
      "status": "String"
   }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors

</td><td>

Error information for the question.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.results.errors.message

</td><td>

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.errors.type

</td><td>

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.results.record

</td><td>

GlideRecord reference to the question created in the Decisions \[sys\_decision\_question\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.results.status

</td><td>

Status that indicates whether the question record was successfully created.Possible values:

-   Failure
-   Success

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example creates two questions for a decision table.

```
var decisionID = 'a45be18c3d839910f8776a598af91269';
var questions = [
   {
      condition: 'u_item=Phone^u_price=500^EQ',
      answer:[
         {
            name: 'u_seller',
            value: '02826bf03710200044e0bfc8bcbe5d64'
         },
         {
            name: 'u_discount',
            value: '5'
         }
      ],
      active: true,
      defaultAnswer: true,
      order: 300
   },
   {
      condition: 'u_item=Laptop^u_price>800^EQ',
      answer:[ 
         {
            name: 'u_discount',
            value: '20'
         }
      ],
      active: true,
      defaultAnswer: false,
      order: 150
   }
];

var dt = new sn_dt.DecisionTableAPI();
var response = dt.createQuestions(decisionID, questions);
gs.info(JSON.stringify(response));
gs.info('Status - ' + response.status);
gs.info('First decision sys id - ' + response.results[0].record.getValue('sys_id'));
gs.info('Second decision sys id - ' + response.results[1].record.getValue('sys_id'));
```

Output:

```
Status - Success
First decision sys id - 21c8d3003d4b9910f8776a598af91213
Second decision sys id - e9c8d3003d4b9910f8776a598af91218
```

## DecisionTableAPI - deleteAnswerElement\(String answerElementID\)

Deletes a record in the Result \[sys\_decision\_multi\_result\_element\] table.

<table id="table_bkq_4yg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

answerElementID

</td><td>

String

</td><td>

Sys\_id of the answer element record.Table: Result Elements \[sys\_decision\_multi\_result\_element\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes an answer element.

```
var answerElementID = '51c707803d0b9910f8776a598af91217';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteAnswerElement(answerElementID);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - deleteChoice\(String choiceID\)

Deletes a record in the Choices \[sys\_choice\] table.

<table id="table_yzy_szg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

choiceID

</td><td>

String

</td><td>

Sys\_id of the choice record. Table: Choices \[sys\_choice\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes a choice.

```
var choiceID = '4532db883d0b9910f8776a598af912e7';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteChoice(choiceID);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - deleteCondition\(String conditionID\)

Deletes a record in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.

<table id="table_apn_3yg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conditionID

</td><td>

String

</td><td>

Sys\_id of the decision condition record. Table: Decision Conditions \[sn\_decision\_table\_decision\_condition\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes a decision condition.

```
var conditionID = 'c9530f4c3dc79910f8776a598af912f1';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteCondition(conditionID);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - deleteDecisionTable\(String decisionID\)

Deletes a record in the Decision Tables \[sys\_decision\] table.

<table id="table_y3r_xxg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes a decision table.

```
var decisionID = 'a1f6e14c3d039910f8776a598af9129d';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteDecisionTable(decisionID);
gs.info('Status -' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - deleteInput\(String inputID\)

Deletes a record in the Decision Inputs \[sys\_decision\_input\] table.

<table id="table_lql_pdd_rvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputID

</td><td>

String

</td><td>

Sys\_id of the decision input record.Table: Decision Inputs \[sys\_decision\_input\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes a decision input.

```
var inputID = 'a1f6e14c3d039910f8776a598af9129d';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteInput(inputID);
gs.info('Status -' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - deleteQuestion\(String questionID\)

Deletes a record in the Decisions \[sys\_decision\_question\] table.

<table id="table_wbw_vyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

questionID

</td><td>

String

</td><td>

Sys\_id of the question record.Table: Decisions \[sys\_decision\_question\]

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example deletes a question.

```
var questionId = '700602fe81d21110f87735acbca2c610';

var dt = new sn_dt.DecisionTableAPI();
var response = dt.deleteQuestion(questionId);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - getAll\(\)

Returns all decision tables from the Decision Tables \[sys\_decision\] table.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_y44_ktc_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

All decision tables and their fields from the Decision Tables \[sys\_decision\] table. Each decision table contains these key-value pairs: -   distinctAnswers: Array. Answer records associated with the decision table. Each record contains these key-value pairs.
    -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
        -   answerElementName: String. Name of the answer element.
        -   label: String. Answer record label.
        -   table: String. Table of the answer element if the answer element is a Reference type.
        -   type: String. Type of the answer element.
        -   valid: Boolean. True if the record exists in the system; otherwise false.
        -   value: String. Value of the answer element.
    -   label: String. Answer record label.
    -   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
    -   valid: Boolean. True if the record exists in the system; otherwise false.
    -   value: String. Sys\_id of the answer record.
    -   table: String. Table containing the answer record.
-   referenceQualifier: String. Used for internal purposes.
-   inputs: Array. Decision inputs from the Decision Inputs \[sys\_decision\_input\] table associated with the decision table. Each record contains these key-value pairs.
    -   searchField: String. Used for internal purposes.
    -   defaultValue: String. Default value for the input.
    -   show\_ref\_finder: Boolean. Used for internal purposes.
    -   use\_dependent: Boolean. Used for internal purposes.
    -   type: String. Input data type.
    -   mandatory: Boolean. True if the input is mandatory; otherwise false.
    -   extended: Boolean. True if the input extends another field; otherwise false.
    -   local: Boolean. Used for internal purposes.
    -   sys\_class\_name: String. Used for internal purposes.
    -   reference: String. Reference table used if the input type is reference.
    -   dependent\_on: String. Field that document ID and choice inputs depend on.
    -   data\_structure: String. Used for internal purposes.
    -   readonly: Boolean. True if the input is read-only; otherwise false.
    -   id: String. Sys\_id of the input from the Decision Inputs \[sys\_decision\_input\] table.
    -   type\_label: String. Input data type label.
    -   table: String. Reference field table if the input type is reference.
    -   order: Number. Order in which the system evaluates inputs.
    -   ref\_qual: String. Condition applied to the reference table.
    -   reference\_display: String. Used for internal purposes.
    -   choiceOption: String. Method for users to see a list of suggested values.
    -   label: String. Label of the input record.
    -   hint: String. Hint text used to help users understand the input required.
    -   name: String. Internal name of the input record.
    -   attributes: Array. Field attributes that apply to the input record.
    -   maxsize: Number. Maximum number of characters allowed in the field.
    -   columnName: String. Name of the input.
-   answerElements: Array. Answer elements from the Answer elements \[sys\_decision\_multi\_result\_element\] table associated with the decision table. Each record contains these key-value pairs.
    -   searchField: String. Used for internal purposes.
    -   defaultValue: String. Default value for the answer element.
    -   show\_ref\_finder: Boolean. Used for internal purposes.
    -   use\_dependent: Boolean. Used for internal purposes.
    -   type: String. Answer element data type.
    -   mandatory: Boolean. True if the answer element is mandatory; otherwise false.
    -   extended: Boolean. True if the answer element extends another field; otherwise false.
    -   local: Boolean. Used for internal purposes.
    -   sys\_class\_name: String. Used for internal purposes.
    -   reference: String. Reference table used if the answer element type is reference.
    -   dependent\_on: String. Field that document ID and choice answer elements depend on.
    -   data\_structure: String. Used for internal purposes.
    -   readonly: Boolean. True if the input is read-only; otherwise false.
    -   id: String. Sys\_id of the input from the Answer elements \[sys\_decision\_multi\_result\_element\] table.
    -   type\_label: String. Answer element data type label.
    -   table: String. Reference field table if the answer element type is reference.
    -   order: Number. Order of the answer elements.
    -   ref\_qual: String. Condition applied to the reference table.
    -   reference\_display: String. Used for internal purposes.
    -   comments: Description of the answer element.
    -   choiceOption: String. Method for users to see a list of suggested values.
    -   label: String. Label of the answer element record.
    -   hint: String. Hint text used to help users understand the answer element required.
    -   name: String. Internal name of the answer element record.
    -   attributes: Array. Field attributes that apply to the answer element record.
    -   maxsize: Number. Maximum number of characters allowed in the field.
    -   columnName: String. Name of the answer element.
-   domain: String. Domain in which the decision table is visible.
-   answerType: String. Used for internal purposes.
-   questions: Array. Decision records from the Decision \[sys\_decision\_question\] table associated with the decision table. Decision records contain these key-value pairs.
    -   defaultAnswer: Boolean. True if this decision is the default for the decision table; otherwise false.
    -   condition: String. Conditions required to reach this decision. The fields available for the condition are the decision inputs that are associated with this decision table.
    -   answer: Object. Answer record associated with the decision. Answer objects contain these key-value pairs.
        -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
            -   answerElementName: String. Name of the answer element.
            -   label: String. Answer record label.
            -   table: String. Table of the answer element if the answer element is a Reference type.
            -   type: String. Type of the answer element.
            -   valid: Boolean. True if the record exists in the system; otherwise false.
            -   value: String. Value of the answer element.
        -   label: String. Answer record label.
        -   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
        -   valid: Boolean. True if the record exists in the system; otherwise false.
        -   value: String. Sys\_id of the answer record.
        -   table: String. Table containing the answer record.
    -   decisionTable: String. Sys\_id of the decision table from the Decision Tables \[sys\_decision\] table associated with the decision.
    -   domain: String. Domain in which the decision is visible.
    -   active: Boolean. True if the decision record is active; otherwise false.
    -   id: String. Sys\_id of the decision record from the Decision \[sys\_decision\_question\] table.
    -   label: String. Label for the decision record.
    -   order: Number. Order in which the system evaluates decisions.
-   accessibleFrom: String. Scopes that have access to the record.
-   name: String. Internal name of the decision table record.
-   active: Boolean. True if the decision table record is active; otherwise false.
-   multipleAnswerSupported: Boolean. True if the decision table support multiple answers; otherwise false.
-   id: String. Sys\_id of the decision table record.
-   label: String. Label of the decision table record.
-   answerTable: Object. Answer table associated with the decision table.
    -   displayValue: String. Display name of the table that contains answer records.
    -   value: String. Internal name of the table that contains answer records.
-   conditions: Array. Conditions in the Decision \[sys\_decision\_question\_list\] table. Applicable only for decision tables created or edited in Decision Builder. Each entry contains the following key value pairs.
    -   decisionInput: String. Sys\_id of the corresponding decision input. Listed in the Decision Inputs \[sys\_decision\_input\] table.
    -   sysId: String. Sys\_id of the condition record.
    -   defaultOperator: String. Default operator for the condition.
    -   typeName: String. Name of the condition type.
    -   description: String. Description of the condition.
    -   label: String. Label of the condition.
    -   type: String. Sys\_id of the condition type.
    -   reference: String. Reference table used if the condition type is reference.
    -   field: String. Field of the condition if the condition is dot-walked from an input of type reference.
    -   decisionTable: String. Sys\_id of the decision table from the Decision Tables \[sys\_decision\] table.
    -   fieldLabel: String. Field label of the condition if the condition is dot-walked from an input of type reference.
    -   scope: String. Scope of the condition.
    -   domain: String. Domain in which the condition is visible.
    -   typeLabel: String. Label of the condition type.
    -   fieldParentTable: Table name of the condition field. Value returns if the condition is dot-walked to a non-reference field from a reference input.
    -   order: Number. Order of the condition.

 Format: JSON

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var response = dt.getAll();
gs.info(JSON.stringify(response));
```

Output:

```
{"result": [
  {
    "distinctAnswers": [{
      "valid": true,
      "label": "Assignment Group Manager Approval",
      "value": "5684821db701230034d1da23ee11a94d",
      "table": "chg_approval_def"
    }],
    "referenceQualifier": "",
    "inputs": [
      {
        "searchField": null,
        "defaultValue": "0",
        "show_ref_finder": false,
        "use_dependent": false,
        "type": "integer",
        "mandatory": false,
        "extended": false,
        "local": false,
        "sys_class_name": "",
        "reference": "",
        "dependent_on": "",
        "data_structure": "",
        "readonly": false,
        "id": "eca52ca7b701230034d1da23ee11a95a",
        "type_label": "Integer",
        "table": "",
        "order": 100,
        "ref_qual": "",
        "reference_display": "",
        "choiceOption": "",
        "label": "CI Count",
        "hint": "",
        "name": "ci_count",
        "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
        "maxsize": 40,
        "columnName": ""
      },
      {
        "searchField": "number",
        "defaultValue": "",
        "show_ref_finder": false,
        "use_dependent": false,
        "type": "reference",
        "mandatory": false,
        "extended": false,
        "local": false,
        "sys_class_name": "",
        "reference": "change_request",
        "dependent_on": "",
        "data_structure": "",
        "readonly": false,
        "id": "1395e8a7b701230034d1da23ee11a9b6",
        "type_label": "Reference",
        "table": "",
        "order": 100,
        "ref_qual": "",
        "reference_display": "Change Request",
        "choiceOption": "",
        "label": "Change request",
        "hint": "",
        "name": "change_request",
        "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
        "maxsize": 32,
        "columnName": ""
      }
    ],
    "domain": "global",
    "answerType": "reference",
    "questions": [{
      "defaultAnswer": false,
      "condition": "ci_count>=1000^EQ",
      "answer": {
        "valid": true,
        "label": "Assignment Group Manager Approval",
        "value": "5684821db701230034d1da23ee11a94d",
        "table": "chg_approval_def"
      },
      "decisionTable": "e49568a7b701230034d1da23ee11a913",
      "domain": "global",
      "active": true,
      "state": null,
      "id": "2a36eca7b701230034d1da23ee11a961",
      "label": "Mandatory Approval if 1000 CIs or more",
      "order": 0
    }],
    "accessibleFrom": "public",
    "name": "Example Standard Change Policy",
    "active": true,
    "id": "e49568a7b701230034d1da23ee11a913",
    "label": "",
    "answerTable": {
      "displayValue": "Change Approval Definition",
      "value": "chg_approval_def"
    }
  },
  {
    "distinctAnswers": [
      {
        "valid": true,
        "label": "CAB Approval",
        "value": "45358a5db701230034d1da23ee11a938",
        "table": "chg_approval_def"
      },
      {
        "valid": true,
        "label": "Assignment Group Manager Approval",
        "value": "5684821db701230034d1da23ee11a94d",
        "table": "chg_approval_def"
      },
      {
        "valid": true,
        "label": "Assignment Group Approval",
        "value": "dc95ca5db701230034d1da23ee11a9e9",
        "table": "chg_approval_def"
      }
    ],
    "referenceQualifier": "",
    "inputs": [
      {
        "searchField": null,
        "defaultValue": "false",
        "show_ref_finder": false,
        "use_dependent": false,
        "type": "boolean",
        "mandatory": false,
        "extended": false,
        "local": false,
        "sys_class_name": "",
        "reference": "",
        "dependent_on": "",
        "data_structure": "",
        "readonly": false,
        "id": "c0a7869db701230034d1da23ee11a9e7",
        "type_label": "True/False",
        "table": "",
        "order": 100,
        "ref_qual": "",
        "reference_display": "",
        "choiceOption": "",
        "label": "Manager approved",
        "hint": "",
        "name": "manager_approved",
        "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
        "maxsize": 40,
        "columnName": ""
      },
      {
        "searchField": "number",
        "defaultValue": "",
        "show_ref_finder": false,
        "use_dependent": false,
        "type": "reference",
        "mandatory": false,
        "extended": false,
        "local": false,
        "sys_class_name": "",
        "reference": "change_request",
        "dependent_on": "",
        "data_structure": "",
        "readonly": false,
        "id": "23164e5db701230034d1da23ee11a9c5",
        "type_label": "Reference",
        "table": "",
        "order": 100,
        "ref_qual": "",
        "reference_display": "Change Request",
        "choiceOption": "",
        "label": "Change request",
        "hint": "",
        "name": "change_request",
        "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
        "maxsize": 32,
        "columnName": ""
      }
    ],
    "domain": "global",
    "answerType": "reference",
    "questions": [
      {
        "defaultAnswer": false,
        "condition": "change_request.state=-3^change_request.riskIN2,3^NQchange_request.state=-3^change_request.assignment_group.managerISEMPTY^EQ",
        "answer": {
          "valid": true,
          "label": "CAB Approval",
          "value": "45358a5db701230034d1da23ee11a938",
          "table": "chg_approval_def"
        },
        "decisionTable": "5b06ce5db701230034d1da23ee11a965",
        "domain": "global",
        "active": true,
        "state": null,
        "id": "10284a9db701230034d1da23ee11a9c1",
        "label": "Requires CAB Approval",
        "order": 0
      },
      {
        "defaultAnswer": false,
        "condition": "change_request.state=-3^change_request.risk=4^manager_approved=false^EQ",
        "answer": {
          "valid": true,
          "label": "Assignment Group Manager Approval",
          "value": "5684821db701230034d1da23ee11a94d",
          "table": "chg_approval_def"
        },
        "decisionTable": "5b06ce5db701230034d1da23ee11a965",
        "domain": "global",
        "active": true,
        "state": null,
        "id": "88e6829db701230034d1da23ee11a9a9",
        "label": "Low Risk Manager approval",
        "order": 0
      },
      {
        "defaultAnswer": false,
        "condition": "change_request.state=-4^EQ",
        "answer": {
          "valid": true,
          "label": "Assignment Group Approval",
          "value": "dc95ca5db701230034d1da23ee11a9e9",
          "table": "chg_approval_def"
        },
        "decisionTable": "5b06ce5db701230034d1da23ee11a965",
        "domain": "global",
        "active": true,
        "state": null,
        "id": "a436029db701230034d1da23ee11a989",
        "label": "Assess Technical Approvals",
        "order": 0
      }
    ],
    "accessibleFrom": "public",
    "name": "Normal Change Policy",
    "active": true,
    "id": "5b06ce5db701230034d1da23ee11a965",
    "label": "",
    "answerTable": {
      "displayValue": "Change Approval Definition",
      "value": "chg_approval_def"
    }
  },
 
]}
```

## DecisionTableAPI - getAnswers\(String decisionID\)

Returns the answers associated with the specified decision table. An answer is a record on any table associated with a Decision \[sys\_decision\_question\] record.

|Name|Type|Description|
|----|----|-----------|
|decisionID|String|Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.|

<table id="table_phm_m5c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Answer records associated with the decision table. Each record contains these key-value pairs: -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
    -   answerElementName: String. Name of the answer element.
    -   label: String. Answer record label.
    -   table: String. Table of the answer element if the answer element is a Reference type.
    -   type: String. Type of the answer element.
    -   valid: Boolean. True if the record exists in the system; otherwise false.
    -   value: String. Value of the answer element.
-   label: String. Answer record label.
-   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
-   valid: Boolean. True if the record exists in the system; otherwise false.
-   value: String. Sys\_id of the answer record.
-   table: String. Table containing the answer record.

 Format: JSON

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var response = dt.getAnswers("3c4464a7b701230034d1da23ee11a993");
gs.info(JSON.stringify(response));
```

Output:

```
{
 "result": [
  {
   "answerElementValues": [
    {
     "valid": true,
     "answerElementName": "u_user",
     "label": "Abel Tuter",
     "value": "62826bf03710200044e0bfc8bcbe5df1",
     "table": "sys_user"
   }],
  "valid": true,
  "multipleAnswerRecord": true,
  "label": "User: Abel Tuter",
  "value": "76e19cd953d7011097a3ddeeff7b122c",
  "table": "sys_decision_multi_result"
  },
 ]
}
```

## DecisionTableAPI - getDecision\(String decisionID, Map inputs\)

Evaluates a decision table based on the provided inputs and returns an answer. If no inputs are provided, returns the first default answer found.

### Input and condition behavior

When `getDecision()` executes, the Decision Table engine evaluates the provided input values against the configured conditions and returns the matching result rows.

For inputs of type Date / Time, values must be provided in the internal ServiceNow datetime format:

```
yyyy-MM-dd HH:mm:ss

```

The system evaluates Date / Time values as absolute date-time values. The system doesn't apply time zone information during evaluation.

### Between operator behavior for Date / Time inputs

When a condition uses the between operator with a Date / Time input, the system compares the input value directly to the configured start and end values.

The comparison:

-   Uses the literal datetime values provided
-   Ignores user, system, or session timezone adjustments
-   Evaluates boundary values exactly as the condition defines them

Script example to normalize inputs to UTC before running `getDecision()`:

```
// Normalize a user-provided datetime to UTC before calling getDecision()
var gdt = new GlideDateTime();
gdt.setDisplayValue("2025-04-07 09:00:00"); // user-local display value

var inputs = {
    effective_time: gdt.getValue() // UTC value: yyyy-MM-dd HH:mm:ss
};

var dt = new sn_dt.DecisionTableAPI();
var result = dt.getDecision("my_decision_table", inputs);
```

<table id="table_e3m_w5c_hhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.

</td></tr><tr><td>

inputs

</td><td>

Map

</td><td>

Optional. Input values for the Decision Inputs \[sys\_decision\_input\] table associated with the provided decision table. Use the value of the **Column name** field as the key. The data type of the value must match the Decision Input **Type** field. If no inputs are provided, returns the first default answer found.**Note:** All inputs and column names must follow the following format:

-   be all lower case and prefixed with a `u_`
-   blank spaces are replaced with `_`

For example,

-   Input name: Incident
-   Input technical name: u\_incident
-   Result column name: Assignment Group
-   Result column technical name: u\_assignment\_group

For more information, see [Make Decisions from JavaScript with the DecisionTableAPI - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/make-decisions-from-javascript-with-the-decisiontableapi/ta-p/2620035)

</td></tr></tbody>
</table><table id="table_f3m_w5c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

GlideRecord

</td><td>

The correctly evaluated Answer record associated with the decision table. An answer record is a record from the table defined in the Decision \[sys\_decision\_question\] record **Answer table** field. -   If no inputs are provided, returns the first default answer found. If no default or correctly evaluated answers are found, returns an error.
-   If the decision table supports multiple answers, each answer is listed in the **result\_elements** field.

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var inputs = new Object();
inputs['u_age'] = 25;
var response = dt.getDecision('26eea7a9dba07300efc65404ce961961', inputs);
var user = response.result_elements.u_user;
```

## DecisionTableAPI - getDecisions\(String decisionID, Map inputs\)

Evaluates a decision table based on the provided inputs and returns all correctly evaluated answers. If no inputs are provided, returns all default answers.

### Input and condition behavior

When `getDecision()` executes, the Decision Table engine evaluates the provided input values against the configured conditions and returns the matching result rows.

For inputs of type Date / Time, values must be provided in the internal ServiceNow datetime format:

```
yyyy-MM-dd HH:mm:ss

```

The system evaluates Date / Time values as absolute date-time values. The system doesn't apply time zone information during evaluation.

### Between operator behavior for Date / Time inputs

When a condition uses the between operator with a Date / Time input, the system compares the input value directly to the configured start and end values.

The comparison:

-   Uses the literal datetime values provided
-   Ignores user, system, or session timezone adjustments
-   Evaluates boundary values exactly as the condition defines them

Script example to normalize inputs to UTC before running `getDecision()`:

```
// Normalize a user-provided datetime to UTC before calling getDecision()
var gdt = new GlideDateTime();
gdt.setDisplayValue("2025-04-07 09:00:00"); // user-local display value

var inputs = {
    effective_time: gdt.getValue() // UTC value: yyyy-MM-dd HH:mm:ss
};

var dt = new sn_dt.DecisionTableAPI();
var result = dt.getDecision("my_decision_table", inputs);
```

<table id="table_e3m_w5c_hhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.

</td></tr><tr><td>

inputs

</td><td>

Map

</td><td>

Optional. Input values for the Decision Inputs \[sys\_decision\_input\] table associated with the decision table. If you provide no inputs, returns all default answers.**Note:** All inputs and column names must follow this format:

-   Use all lowercase and prefix with u\_
-   Replace blank spaces with \_

For example,

-   Input name: Incident
-   Input technical name: u\_incident
-   Result column name: Assignment Group
-   Result column technical name: u\_assignment\_group

For more information, see [Make Decisions from JavaScript with the DecisionTableAPI - Workflow Automation CoE](https://www.servicenow.com/community/workflow-automation-articles/make-decisions-from-javascript-with-the-decisiontableapi/ta-p/2620035)

</td></tr></tbody>
</table><table id="table_tg2_y5c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Array

</td><td>

List of answer records in GlideRecord format. An answer record is a record on any table associated with a Decision \[sys\_decision\_question\] record. -   If you provide no inputs, returns all default answers.
-   If the system finds no default or correctly evaluated answers, returns an error.
-   If the decision table supports multiple answers, the **result\_elements** field lists each answer.

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var input = new Object();
input['u_age'] = 25;
var response = dt.getDecisions('5b06ce5db701230034d1da23ee11a965', input);
var firstRecord = response[0];
var user = firstRecord.result_elements.u_user;
```

## DecisionTableAPI - getDecisionTable\(String decisionID\)

Returns a single decision table from the Decision Tables \[sys\_decision\] table.

|Name|Type|Description|
|----|----|-----------|
|decisionID|String|Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.|

<table id="table_b3y_g5c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Decision table from the Decision Tables \[sys\_decision\] table. Each decision table contains these key-value pairs. -   distinctAnswers: Array. Answer records associated with the decision table. Each record contains these key-value pairs.
    -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
        -   answerElementName: String. Name of the answer element.
        -   label: String. Answer record label.
        -   table: String. Table of the answer element if the answer element is a Reference type.
        -   type: String. Type of the answer element.
        -   valid: Boolean. True if the record exists in the system; otherwise false.
        -   value: String. Value of the answer element.
    -   label: String. Answer record label.
    -   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
    -   valid: Boolean. True if the record exists in the system; otherwise false.
    -   value: String. Sys\_id of the answer record.
    -   table: String. Table containing the answer record.
-   referenceQualifier: String. Used for internal purposes.
-   inputs: Array. Decision inputs from the Decision Inputs \[sys\_decision\_input\] table associated with the decision table. Each record contains these key-value pairs.
    -   searchField: String. Used for internal purposes.
    -   defaultValue: String. Default value for the input.
    -   show\_ref\_finder: Boolean. Used for internal purposes.
    -   use\_dependent: Boolean. Used for internal purposes.
    -   type: String. Input data type.
    -   mandatory: Boolean. True if the input is mandatory; otherwise false.
    -   extended: Boolean. True if the input extends another field; otherwise false.
    -   local: Boolean. Used for internal purposes.
    -   sys\_class\_name: String. Used for internal purposes.
    -   reference: String. Reference table used if the input type is reference.
    -   dependent\_on: String. Field that document ID and choice inputs depend on.
    -   data\_structure: String. Used for internal purposes.
    -   readonly: Boolean. True if the input is read-only; otherwise false.
    -   id: String. Sys\_id of the input from the Decision Inputs \[sys\_decision\_input\] table.
    -   type\_label: String. Input data type label.
    -   table: String. Reference field table if the input type is reference.
    -   order: Number. Order in which the system evaluates inputs.
    -   ref\_qual: String. Condition applied to the reference table.
    -   reference\_display: String. Used for internal purposes.
    -   choiceOption: String. Method for users to see a list of suggested values.
    -   label: String. Label of the input record.
    -   hint: String. Hint text used to help users understand the input required.
    -   name: String. Internal name of the input record.
    -   attributes: Array. Field attributes that apply to the input record.
    -   maxsize: Number. Maximum number of characters allowed in the field.
    -   columnName: String. Name of the input.
-   answerElements: Array. Answer elements from the Answer elements \[sys\_decision\_multi\_result\_element\] table associated with the decision table. Each record contains these key-value pairs.
    -   searchField: String. Used for internal purposes.
    -   defaultValue: String. Default value for the answer element.
    -   show\_ref\_finder: Boolean. Used for internal purposes.
    -   use\_dependent: Boolean. Used for internal purposes.
    -   type: String. Answer element data type.
    -   mandatory: Boolean. True if the answer element is mandatory; otherwise false.
    -   extended: Boolean. True if the answer element extends another field; otherwise false.
    -   local: Boolean. Used for internal purposes.
    -   sys\_class\_name: String. Used for internal purposes.
    -   reference: String. Reference table used if the answer element type is reference.
    -   dependent\_on: String. Field that document ID and choice answer elements depend on.
    -   data\_structure: String. Used for internal purposes.
    -   readonly: Boolean. True if the input is read-only; otherwise false.
    -   id: String. Sys\_id of the input from the Answer elements \[sys\_decision\_multi\_result\_element\] table.
    -   type\_label: String. Answer element data type label.
    -   table: String. Reference field table if the answer element type is reference.
    -   order: Number. Order of the answer elements.
    -   ref\_qual: String. Condition applied to the reference table.
    -   reference\_display: String. Used for internal purposes.
    -   comments: Description of the answer element.
    -   choiceOption: String. Method for users to see a list of suggested values.
    -   label: String. Label of the answer element record.
    -   hint: String. Hint text used to help users understand the answer element required.
    -   name: String. Internal name of the answer element record.
    -   attributes: Array. Field attributes that apply to the answer element record.
    -   maxsize: Number. Maximum number of characters allowed in the field.
    -   columnName: String. Name of the answer element.
-   domain: String. Domain in which the decision table is visible.
-   answerType: String. Used for internal purposes.
-   questions: Array. Decision records from the Decision \[sys\_decision\_question\] table associated with the decision table. Decision records contain these key-value pairs.
    -   defaultAnswer: Boolean. True if this decision is the default for the decision table; otherwise false.
    -   condition: String. Conditions required to reach this decision. The fields available for the condition are the decision inputs that are associated with this decision table.
    -   answer: Object. Answer record associated with the decision. Answer objects contain these key-value pairs.
        -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
            -   answerElementName: String. Name of the answer element.
            -   label: String. Answer record label.
            -   table: String. Table of the answer element if the answer element is a Reference type.
            -   type: String. Type of the answer element.
            -   valid: Boolean. True if the record exists in the system; otherwise false.
            -   value: String. Value of the answer element.
        -   label: String. Answer record label.
        -   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
        -   valid: Boolean. True if the record exists in the system; otherwise false.
        -   value: String. Sys\_id of the answer record.
        -   table: String. Table containing the answer record.
    -   decisionTable: String. Sys\_id of the decision table from the Decision Tables \[sys\_decision\] table associated with the decision.
    -   domain: String. Domain in which the decision is visible.
    -   active: Boolean. True if the decision record is active; otherwise false.
    -   id: String. Sys\_id of the decision record from the Decision \[sys\_decision\_question\] table.
    -   label: String. Label for the decision record.
    -   order: Number. Order in which the system evaluates decisions.
-   accessibleFrom: String. Scopes that have access to the record.
-   name: String. Internal name of the decision table record.
-   active: Boolean. True if the decision table record is active; otherwise false.
-   multipleAnswerSupported: Boolean. True if the decision table support multiple answers; otherwise false.
-   id: String. Sys\_id of the decision table record.
-   label: String. Label of the decision table record.
-   answerTable: Object. Answer table associated with the decision table.
    -   displayValue: String. Display name of the table that contains answer records.
    -   value: String. Internal name of the table that contains answer records.
-   conditions: Array. Conditions in the Decision \[sys\_decision\_question\_list\] table. Applicable only for decision tables created or edited in Decision Builder. Each entry contains the following key value pairs.
    -   decisionInput: String. Sys\_id of the corresponding decision input. Listed in the Decision Inputs \[sys\_decision\_input\] table.
    -   sysId: String. Sys\_id of the condition record.
    -   defaultOperator: String. Default operator for the condition.
    -   typeName: String. Name of the condition type.
    -   description: String. Description of the condition.
    -   label: String. Label of the condition.
    -   type: String. Sys\_id of the condition type.
    -   reference: String. Reference table used if the condition type is reference.
    -   field: String. Field of the condition if the condition is dot-walked from an input of type reference.
    -   decisionTable: String. Sys\_id of the decision table from the Decision Tables \[sys\_decision\] table.
    -   fieldLabel: String. Field label of the condition if the condition is dot-walked from an input of type reference.
    -   scope: String. Scope of the condition.
    -   domain: String. Domain in which the condition is visible.
    -   typeLabel: String. Label of the condition type.
    -   fieldParentTable: Table name of the condition field. Value returns if the condition is dot-walked to a non-reference field from a reference input.
    -   order: Number. Order of the condition.

 Format: JSON

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var response = dt.getDecisionTable("3c4464a7b701230034d1da23ee11a993");
gs.info(JSON.stringify(response));

```

Output:

```
"distinctAnswers": [{
    "valid": true,
    "label": "CAB Approval",
    "value": "45358a5db701230034d1da23ee11a938",
    "table": "chg_approval_def"
  }],
  "referenceQualifier": "",
  "inputs": [{
    "searchField": "number",
    "defaultValue": "",
    "show_ref_finder": false,
    "use_dependent": false,
    "type": "reference",
    "mandatory": false,
    "extended": false,
    "local": false,
    "sys_class_name": "",
    "reference": "change_request",
    "dependent_on": "",
    "data_structure": "",
    "readonly": false,
    "id": "634420a7b701230034d1da23ee11a94f",
    "type_label": "Reference",
    "table": "",
    "order": 100,
    "ref_qual": "",
    "reference_display": "Change Request",
    "choiceOption": "",
    "label": "Change request",
    "hint": "",
    "name": "change_request",
    "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
    "maxsize": 32,
    "columnName": ""
  }],
  "domain": "global",
  "answerType": "reference",
  "questions": [{
    "defaultAnswer": true,
    "condition": "change_request.state=-3^EQ",
    "answer": {
      "valid": true,
      "label": "CAB Approval",
      "value": "45358a5db701230034d1da23ee11a938",
      "table": "chg_approval_def"
    },
    "decisionTable": "3c4464a7b701230034d1da23ee11a993",
    "domain": "global",
    "active": true,
    "state": null,
    "id": "2764a4a7b701230034d1da23ee11a989",
    "label": "Requires CAB Approval",
    "order": 0
  }],
  "accessibleFrom": "public",
  "name": "Emergency Change Policy",
  "active": true,
  "id": "3c4464a7b701230034d1da23ee11a993",
  "label": "",
  "answerTable": {
    "displayValue": "Change Approval Definition",
    "value": "chg_approval_def"
  }
}

```

## DecisionTableAPI - getInputs\(String decisionID\)

Returns the decision inputs from the Decision Inputs \[sys\_decision\_input\] table associated with the passed in decision table.

|Name|Type|Description|
|----|----|-----------|
|decisionID|String|Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.|

<table id="table_v5w_35c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Decision inputs from the Decision Inputs \[sys\_decision\_input\] table associated with the decision table. You can find the inputs associated with a decision table using the Decision Inputs related list in the Decision Tables \[sys\_decision\] table. Inputs contain these key-value pairs. -   searchField: String. Used for internal purposes.
-   defaultValue: String. Default value for the input.
-   show\_ref\_finder: Boolean. Used for internal purposes.
-   use\_dependent: Boolean. Used for internal purposes.
-   type: String. Input data type.
-   mandatory: Boolean. True if the input is mandatory; otherwise false.
-   extended: Boolean. True if the input extends another field; otherwise false.
-   local: Boolean. Used for internal purposes.
-   sys\_class\_name: String. Used for internal purposes.
-   reference: String. Reference table used if the input type is reference.
-   dependent\_on: String. Field that document ID and choice inputs depend on.
-   data\_structure: String. Used for internal purposes.
-   readonly: Boolean. True if the input is read-only; otherwise false.
-   id: String. Sys\_id of the input from the Decision Inputs \[sys\_decision\_input\] table.
-   type\_label: String. Input data type label.
-   table: String. Reference field table if the input type is reference.
-   order: Number. Order in which the system evaluates inputs.
-   ref\_qual: String. Condition applied to the reference table.
-   reference\_display: String. Used for internal purposes.
-   choiceOption: String. Method for users to see a list of suggested values.
-   label: String. Label of the input record.
-   hint: String. Hint text used to help users understand the input required.
-   name: String. Internal name of the input record.
-   attributes: Array. Field attributes that apply to the input record.
-   maxsize: Number. Maximum number of characters allowed in the field.
-   columnName: String. Name of the input.

 Format: JSON

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var response = dt.getInputs("3c4464a7b701230034d1da23ee11a993");
gs.info(JSON.stringify(response));
```

Output:

```
{"result": [{
  "searchField": "number",
  "defaultValue": "",
  "show_ref_finder": false,
  "use_dependent": false,
  "type": "reference",
  "mandatory": false,
  "extended": false,
  "local": false,
  "sys_class_name": "",
  "reference": "change_request",
  "dependent_on": "",
  "data_structure": "",
  "readonly": false,
  "id": "634420a7b701230034d1da23ee11a94f",
  "type_label": "Reference",
  "table": "",
  "order": 100,
  "ref_qual": "",
  "reference_display": "Change Request",
  "choiceOption": "",
  "label": "Change request",
  "hint": "",
  "name": "change_request",
  "attributes": {"element_mapping_provider": "com.glide.decision_table.data.DecisionTableVariableMapper"},
  "maxsize": 32,
  "columnName": ""
}]}
```

## DecisionTableAPI - getQuestions\(String decisionID\)

Returns the decisions from the Decision \[sys\_decision\_question\] table associated with the passed in decision table.

|Name|Type|Description|
|----|----|-----------|
|decisionID|String|Sys\_id of the Decision Table record from the Decision Tables \[sys\_decision\] table.|

<table id="table_zjb_l5c_hhb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Decisions from the Decision \[sys\_decision\_question\] table associated with the decision table. You can find the decisions associated with a decision table using the Decisions related list in the Decision Tables \[sys\_decision\] table. Decision records contain these key-value pairs.-   defaultAnswer: Boolean. True if this decision is the default for the decision table; otherwise false.
-   condition: String. Conditions required to reach this decision. The fields available for the condition are the decision inputs that are associated with this decision table.
-   answer: Object. Answer record associated with the decision. Answer objects contain these key-value pairs.
    -   answerElementValues: Array. Answer element values associated with the answer record. Each record contains these key-value pairs:
        -   answerElementName: String. Name of the answer element.
        -   label: String. Answer record label.
        -   table: String. Table of the answer element if the answer element is a Reference type.
        -   type: String. Type of the answer element.
        -   valid: Boolean. True if the record exists in the system; otherwise false.
        -   value: String. Value of the answer element.
    -   label: String. Answer record label.
    -   multipleAnswerRecord: Boolean. True if this is a multiple answer record; otherwise false.
    -   valid: Boolean. True if the record exists in the system; otherwise false.
    -   value: String. Sys\_id of the answer record.
    -   table: String. Table containing the answer record.
-   decisionTable: String. Sys\_id of the decision table from the Decision Tables \[sys\_decision\] table associated with the decision.
-   domain: String. Domain in which the decision is visible.
-   active: Boolean. True if the decision record is active; otherwise false.
-   id: String. Sys\_id of the decision record from the Decision \[sys\_decision\_question\] table.
-   label: String. Label for the decision record.
-   order: Number. Order in which the system evaluates decisions.

 Format: JSON

</td></tr></tbody>
</table>```
var dt = new sn_dt.DecisionTableAPI();
var response = dt.getQuestions("3c4464a7b701230034d1da23ee11a993");
gs.info(JSON.stringify(response));

```

Output:

```
{"result": [{
  "defaultAnswer": true,
  "condition": "change_request.state=-3^EQ",
  "answer": {
    "valid": true,
    "label": "CAB Approval",
    "value": "45358a5db701230034d1da23ee11a938",
    "table": "chg_approval_def"
  },
  "decisionTable": "3c4464a7b701230034d1da23ee11a993",
  "domain": "global",
  "active": true,
  "state": null,
  "id": "2764a4a7b701230034d1da23ee11a989",
  "label": "Requires CAB Approval",
  "order": 0
}]}
```

## DecisionTableAPI - updateAnswerElement\(String answerElementID, Object answerElement\)

Updates a record in the Result \[sys\_decision\_multi\_result\_element\] table.

<table id="table_bzf_nyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

answerElementID

</td><td>

String

</td><td>

Sys\_id of the answer element record.Table: Result Elements \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

answerElement

</td><td>

Object

</td><td>

Key-value pairs to update the answer element record.```
{   
   comments: "String", 
   label: "String",    
   maxsize: Number
}
```

</td></tr><tr><td>

answerElement.comments

</td><td>

String

</td><td>

Optional. Description of the answer element.

</td></tr><tr><td>

answerElement.label

</td><td>

String

</td><td>

Optional. Label of the answer element record.

</td></tr><tr><td>

answerElement.maxsize

</td><td>

Number

</td><td>

Optional. Maximum number of characters allowed in the answer element field. Use this property only if **answerElement.type** is `String`.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the answer element updated in the Result Elements \[sys\_decision\_multi\_result\_element\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates the label and comments for an answer element.

```
var answerElementID = '51c707803d0b9910f8776a598af91217';
var answerElement = {
   label: 'Product',	
   comments: 'hello'
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateAnswerElement(answerElementID, answerElement);
gs.info('Status - ' + response.status);
gs.info('Result Element label changed to - ' + response.record.getValue('label'));
```

Output:

```
Status - Success
Result Element label changed to - Product
```

## DecisionTableAPI - updateChoice \(String choiceID, Object choice\)

Updates a record in the Choices \[sys\_choice\] table.

<table id="table_zcq_rzg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

choiceID

</td><td>

String

</td><td>

Sys\_id of the choice record. Table: Choices \[sys\_choice\]

</td></tr><tr><td>

choice

</td><td>

Object

</td><td>

Key-value pairs to update the choice record.```
{
   label: "String",
   order: Number,
   value: "String"
}
```

</td></tr><tr><td>

choice.label

</td><td>

String

</td><td>

Optional. Label of the choice.

</td></tr><tr><td>

choice.order

</td><td>

Number

</td><td>

Optional. Order of the choice.

</td></tr><tr><td>

choice.value

</td><td>

String

</td><td>

Optional. Value of the choice.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the choice updated in the Choices \[sys\_choice\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates the label, value, and order for a choice.

```
var choiceID = '4532db883d0b9910f8776a598af912e7';
var choices = {
   label: 'Delhi',
   value: 'del',
   order: 50
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateChoice(choiceID, choices);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

## DecisionTableAPI - updateCondition\(String conditionID, Object condition\)

Updates a record in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.

<table id="table_rrf_hyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

conditionID

</td><td>

String

</td><td>

Sys\_id of the decision condition record. Table: Decision Conditions \[sn\_decision\_table\_decision\_condition\]

</td></tr><tr><td>

condition

</td><td>

Object

</td><td>

Key-value pairs to update the decision condition record.```
{   
   defaultOperator: "String", 
   description: "String",    
   label: "String"
}
```

</td></tr><tr><td>

condition.defaultOperator

</td><td>

String

</td><td>

Optional. Default operator for the condition. For a list of valid operators, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

condition.description

</td><td>

String

</td><td>

Optional. Description of the condition.

</td></tr><tr><td>

condition.label

</td><td>

String

</td><td>

Optional. Label of the decision condition record.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the decision condition updated in the Decision Conditions \[sn\_decision\_table\_decision\_condition\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates a decision condition.

```
var conditionID = 'c9530f4c3dc79910f8776a598af912f1';
var condition = {
   defaultOperator: '!=',
   label: 'Active Incident',
   description: 'Check if the incident is active'
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateCondition(conditionID, condition);
gs.info('Status - ' + response.status);
gs.info('Condition label changed to - ' + response.record.getValue('label'));
```

Output:

```
Status - Success
Condition label changed to - Active Incident
```

## DecisionTableAPI - updateDecisionTable\(String decisionID, Object decisionTable\)

Updates a record in the Decision Tables \[sys\_decision\] table.

<table id="table_pnx_vxg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

decisionID

</td><td>

String

</td><td>

Sys\_id of the decision table record.Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

decisionTable

</td><td>

Object

</td><td>

Key-value pairs to update the decision table record.```
{
  "accessibleFrom": "String",
  "name": "String"
}
```

</td></tr><tr><td>

decisionTable.accessibleFrom

</td><td>

String

</td><td>

Optional. Scopes that have access to the decision table record.Valid values:

-   package\_private
-   public

</td></tr><tr><td>

decisionTable.name

</td><td>

String

</td><td>

Optional. Name of the decision table.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the decision table.Data type: GlideRecord

Table: Decision Tables \[sys\_decision\]

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates a decision table.

```
var decisionID = 'a1f6e14c3d039910f8776a598af9129d';
var decisionTable = {
   name: 'Emergency Change Request',    
   accessibleFrom: 'public',
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateDecisionTable(decisionID, decisionTable);
gs.info('Status -' + response.status);
gs.info('Decision Table sys id - ' + response.record.getValue('sys_id'));
```

Output:

```
Status - Success
Decision Table sys id - a1f6e14c3d039910f8776a598af9129d
```

## DecisionTableAPI - updateInput\(String inputID, Object input\)

Updates a record in the Decision Inputs \[sys\_decision\_input\] table.

<table id="table_zzd_dyg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputID

</td><td>

String

</td><td>

Sys\_id of the decision input record.Table: Decision Inputs \[sys\_decision\_input\]

</td></tr><tr><td>

input

</td><td>

Object

</td><td>

Key-value pairs to update a decision input record.

 ```
{
   active: Boolean,
   defaultValue: "String",
   label: "String",
   mandatory: Boolean,
   maxsize: Number,
   order: Number,
   readonly: Boolean
}
```

</td></tr><tr><td>

input.active

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the decision input record is active.

 Valid values:

-   true: The decision input record is active.
-   false: The decision input record is not active.

</td></tr><tr><td>

input.defaultValue

</td><td>

String

</td><td>

Optional. Default value for the input.

</td></tr><tr><td>

input.label

</td><td>

String

</td><td>

Optional. Label of the decision input record.

</td></tr><tr><td>

input.mandatory

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the input is mandatory.

 Valid values:

-   true: The input is mandatory.
-   false: The input is not mandatory.

</td></tr><tr><td>

input.maxsize

</td><td>

Number

</td><td>

Optional. Maximum number of characters allowed in the input field. Use this property only if **input.type** is `String`.

</td></tr><tr><td>

input.order

</td><td>

Number

</td><td>

Optional. Order of the input.

</td></tr><tr><td>

input.readonly

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the input is read-only.

 Valid values:

-   true: The input is read-only.
-   false: The input is not read-only.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the decision input updated in the Decision Inputs \[sys\_decision\_input\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates a decision input.

```
var inputID = 'e862f1803dc39910f8776a598af912da';
var input = {
   label: 'Item name',
   defaultValue: 'Apple',
   maxsize: 100,
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateInput(inputID, input);
gs.info(JSON.stringify(response));
gs.info('Status - ' + response.status);
gs.info('Input label changed to - ' + response.record.getValue('label'));

```

Output:

```
Status - Success
Input label changed to - Item name
```

## DecisionTableAPI - updateQuestion\(String questionID, Object question\)

Updates a record in the Decisions \[sys\_decision\_question\] table.

<table id="table_c4l_syg_qvb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

questionID

</td><td>

String

</td><td>

Sys\_id of the question record.Table: Decisions \[sys\_decision\_question\]

</td></tr><tr><td>

question

</td><td>

Object

</td><td>

Key-value pairs to update the question record.```
{
  "active": Boolean,
  "answer": [Array],
  "condition": "String",
  "defaultAnswer": Boolean,
  "label": "String",
  "order": Number
}
```

</td></tr><tr><td>

question.active

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether the question record is active.

 Valid values:

-   true: The question record is active.
-   false: The question record isn't active.

</td></tr><tr><td>

question.answer

</td><td>

Array

</td><td>

Optional. List of possible answers to the question.For a single result table, the array can only have one object. For a multi-result table, the array can have multiple objects.

```
[
  {
    "name": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

question.answer.name

</td><td>

String

</td><td>

Optional. Name of the answer element.Table: Result Elements \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

question.answer.value

</td><td>

String

</td><td>

Optional. Value of the answer element.Table: Result Elements \[sys\_decision\_multi\_result\_element\]

</td></tr><tr><td>

question.condition

</td><td>

String

</td><td>

Optional. Conditions required to reach this question.The fields available for the conditions are the decision inputs that are associated with the decision table.

For more information about creating conditions, see [Operators available for filters and queries](https://www.servicenow.com/docs/access?context=r_OpAvailableFiltersQueries&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

question.defaultAnswer

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether this question is the default question for the decision table.Valid values:

-   true: The question is the default question.
-   false: The question isn't the default question.

</td></tr><tr><td>

question.label

</td><td>

String

</td><td>

Optional. Label of the question record.

</td></tr><tr><td>

question.order

</td><td>

Number

</td><td>

Optional. Order of the question.

</td></tr></tbody>
</table><table id="table_ps1_bgn_lvb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Information about the status of the API request.```
{
  "errors": [Array],
  "record": GlideRecord,
  "status": "String"
}
```

</td></tr><tr><td>

&lt;Object&gt;.errors

</td><td>

Error information.Data type: Array of Objects

```
"errors": [
  {
    "message": "String",
    "type": "String
  }
]
```

</td></tr><tr><td>

&lt;Object&gt;.errors.message

</td><td id="errors-message-entry">

Error message.Data type: String

</td></tr><tr><td>

&lt;Object&gt;.errors.type

</td><td id="errors-type-entry">

Type of error.Possible value: INTERNAL\_ERROR

Data type: String

</td></tr><tr><td>

&lt;Object&gt;.record

</td><td>

GlideRecord reference to the question updated in the Decisions \[sys\_decision\_question\] table.Data type: GlideRecord

</td></tr><tr><td>

&lt;Object&gt;.status

</td><td>

Status of the API request.Possible values:

-   Failure
-   Success

Data type: String

</td></tr></tbody>
</table>This example updates a question record.

```
var questionId = '70381fcc3d0b9910f8776a598af91219';
var questions = {
   condition: 'u_item=Laptop^u_price>1800^EQ',
   answer:[
      {
         name: 'u_discount',
         value: '40',
      },
      {
         name: 'u_seller',
         value: '02826bf03710200044e0bfc8bcbe5d64',
      },
   ],
   active: true,
   order: 3000
};

var dt = new sn_dt.DecisionTableAPI();
var response = dt.updateQuestion(questionId, questions);
gs.info('Status - ' + response.status);
```

Output:

```
Status - Success
```

