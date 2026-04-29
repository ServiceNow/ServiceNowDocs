---
title: GeniusResultAnswer - Scoped
description: The GeniusResultAnswer API provides methods for creating an answer object in a Genius Result configuration's processor scripts. Answers created with this API define search requests or key-value pair maps that can populate Genius Result answer cards.Defines a Genius Result answer with arbitrary key-value pair fields in your Genius Result configuration's AI Search response processor script. You can utilize any public ServiceNow AI Platform API to generate these fields.Adds terms to the search query defined in your Genius Result configuration's AI Search request processor script.Specifies an encoded search query in your Genius Result configuration's AI Search request processor script. Results from this encoded search query are displayed as Genius Result answer cards.Limits the maximum number of results returned for the search query defined in your Genius Result configuration's AI Search request processor script. By default, the search query returns up to three results.Specifies terms for the search query defined in your Genius Result configuration's AI Search request processor script.Limits the search query defined in a Genius Result configuration's AI Search request processor script to a specific table. The query only returns search results from the specified table as Genius Result answer cards.Specifies whether to perform typo handling auto-correction \(spell checking\) for the search query defined in a Genius Result configuration's AI Search request processor script.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GeniusResultAnswer- Scoped

The GeniusResultAnswer API provides methods for creating an answer object in a Genius Result configuration's processor scripts. Answers created with this API define search requests or key-value pair maps that can populate Genius Result answer cards.

You can populate the answer object with query details retrieved from the context of the Genius Result configuration using the [GeniusResultContext](../../GeniusResultContextScoped/concept/GeniusResultContextScopedAPI.md#) API.

The GeniusResultAnswer API methods you need to invoke to create your answer object depend on which AI Search Genius Result Configuration form field you're using for your script:

-   If you're scripting in a Genius Result configuration's **AI Search request processor** field, you need to invoke the setTable\(\) method and one of the setSearchPhrase\(\), addSearchPhrases\(\), or setEncodedQuery\(\) methods. All other methods are optional except for addDataMap\(\), which is not relevant for this use case.
-   If you're scripting in a Genius Result configuration's **AI Search response processor** field, you need to invoke the addDataMap\(\) method. No other methods are relevant for this use case.

Use this API in Genius Result server-side scripts with the `sn_ais` namespace identifier. For more information on scripting logic for Genius Results, see [Create a new Genius Result configuration](https://www.servicenow.com/docs/access?context=create-genius-results-config-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GeniusResultAnswer – addDataMap\(Object map\)

Defines a Genius Result answer with arbitrary key-value pair fields in your Genius Result configuration's **AI Search response processor** script. You can utilize any public ServiceNow AI Platform API to generate these fields.

**Note:** When scripting in a Genius Result configuration's **AI Search response processor** field, you need to invoke this method. If you don't invoke this method, the Genius Result returns no answers when triggered.

You can add multiple field maps to a single **AI Search response processor** script by invoking this method more than once. Each field map populates a separate Genius Result answer card.

<table id="table_bp3_3xm_qnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

map

</td><td>

Object

</td><td>

Defines an arbitrary set of key-value pair fields for addition to the search query response from AI Search. All field values must be Strings.

 ```
{
  "fieldName1": String,
  "fieldName2": String
}
```

</td></tr></tbody>
</table><table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search response processor** script adds custom title and URL key-value pair fields to the answer object for display on a Genius Result answer card.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  var customFieldMap = {
    "title": "My custom Genius Result answer",
    "url": "https://example.com/myGeniusResultLink"
  }

  answer.addDataMap(customFieldMap);

  return answer;
}
```

## GeniusResultAnswer – addSearchPhrases\(Array searchPhrases\)

Adds terms to the search query defined in your Genius Result configuration's **AI Search request processor** script.

**Note:** When scripting in a Genius Result configuration's **AI Search request processor** field, you must invoke the setTable\(\) method and one of the setSearchPhrase\(\), addSearchPhrases\(\), or setEncodedQuery\(\) methods. If you don't invoke both of the required methods, your Genius Result returns no answers when triggered.

<table id="table_tn5_jxm_qnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

searchPhrases

</td><td>

Array

</td><td>

Array of arbitrary Strings to add as search terms for the search query defined in your Genius Result configuration's **AI Search request processor** script. AI Search treats these search terms as if separated by the OR operator.

 Example:

```
[
  "Term": String,
  "Quoted phrase": String
]
```

</td></tr></tbody>
</table><table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search request processor** script constructs a search query for records on the User \[sys\_user\] table that contain the terms `Beth` or `Anglin`.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sys_user');
  answer.addSearchPhrases(['Beth','Anglin']);

  return answer;
}
```

## GeniusResultAnswer – setEncodedQuery\(String query\)

Specifies an encoded search query in your Genius Result configuration's **AI Search request processor** script. Results from this encoded search query are displayed as Genius Result answer cards.

**Note:** When scripting in a Genius Result configuration's **AI Search request processor** field, you need to invoke the setTable\(\) method and one of the setSearchPhrase\(\), addSearchPhrases\(\), or setEncodedQuery\(\) methods. If you don't invoke both of the required methods, your Genius Result returns no answers when triggered.

|Name|Type|Description|
|----|----|-----------|
|query|String|Encoded search query to send to AI Search from your Genius Result configuration's **AI Search request processor** script.|

<table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search request processor** script constructs an encoded search query against the User \[sys\_user\] table. The final query joins together multiple subqueries generated from entities detected in the user's original search query.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sys_user');
  answer.setSearchLimit(2);
  answer.spellCheck(false);
  var queries = [];
  var matchingSegments;
  var predictionResult = context.getPredictionResult();
  if (predictionResult && predictionResult.length == 1) {
    var detail = predictionResult[0];
    if (detail['result'] && detail['result']['entities']) {
      var entities = detail['result']['entities'];
      for (var i = 0; i < entities.length; i++) {
        if (entities[i]['name'].endsWith('personName')) {
          matchingSegments = entities[i]['matchingSegments'];
          for (var j = 0; j < matchingSegments.length; j++)
            answer.addSearchPhrases([matchingSegments[j]['value']]);
        } else if (entities[i]['name'].endsWith('cityLocation')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('location.nameLIKE' + matchingSegments[0]['value']);
        } else if (entities[i]['name'].endsWith('departmentName')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('department.nameLIKE' + matchingSegments[0]['value']);
        } else if (entities[i]['name'].endsWith('jobTitle')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('titleLIKE' + matchingSegments[0]['value']);
        }
      }
    }
  }

  if (queries.length > 0)
    answer.setEncodedQuery(queries.join('^'));

  return answer;
}
```

## GeniusResultAnswer – setSearchLimit\(Number searchLimit\)

Limits the maximum number of results returned for the search query defined in your Genius Result configuration's **AI Search request processor** script. By default, the search query returns up to three results.

<table id="table_yq1_lxm_qnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

searchLimit

</td><td>

Number

</td><td>

Positive integer value for the maximum number of search results to return for the search query defined in your Genius Result configuration's **AI Search request processor** script. Values above 3 have no effect.

 Default: 3

</td></tr></tbody>
</table><table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search request processor** script searches for records from the Catalog Item \[sc\_cat\_item\] table that contain the term `laptop` and returns a maximum of two results.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sc_cat_item');
  answer.setSearchPhrase('laptop');
  answer.setSearchLimit(2);

  return answer;
}
```

## GeniusResultAnswer – setSearchPhrase\(String searchPhrase\)

Specifies terms for the search query defined in your Genius Result configuration's **AI Search request processor** script.

**Note:** When scripting in a Genius Result configuration's **AI Search request processor** field, you need to invoke the setTable\(\) method and one of the setSearchPhrase\(\), addSearchPhrases\(\), or setEncodedQuery\(\) methods. If you don't invoke both of the required methods, your Genius Result returns no answers when triggered.

<table id="table_icm_lxm_qnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

searchPhrase

</td><td>

String

</td><td>

Terms to use for the search query defined in your Genius Result configuration's **AI Search request processor** script.

 If you want to retain the search terms from the query that triggered the Genius Result configuration, set this parameter to the String value returned by the GeniusResultContext.getOriginalSearchPhrase\(\) method.

</td></tr></tbody>
</table><table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search request processor** script constructs a search query for records from the User \[sys\_user\] table that contain the term `Anglin`.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sys_user');
  answer.setSearchPhrase('Anglin');

  return answer;
}
```

## GeniusResultAnswer – setTable\(String table\)

Limits the search query defined in a Genius Result configuration's **AI Search request processor** script to a specific table. The query only returns search results from the specified table as Genius Result answer cards.

**Note:** When scripting in a Genius Result configuration's **AI Search request processor** field, you need to invoke this method and one of the setSearchPhrase\(\), addSearchPhrases\(\), or setEncodedQuery\(\) methods. If you don't invoke both of the required methods, your Genius Result returns no answers when triggered.

|Name|Type|Description|
|----|----|-----------|
|table|String|ServiceNow AI Platform table name. Only indexed records on this table are returned as results for the search query defined in your Genius Result configuration's **AI Search request processor** script.|

<table id="id_qyq_cg4_vnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="GRAnswer-returns-Boolean-row"><td>

Boolean

</td><td>

Flag that indicates whether invocation of the method succeeded.

 Valid values:

-   true: Invocation of the method succeeded.
-   false: Invocation of the method failed.

</td></tr></tbody>
</table>This **AI Search request processor** script constructs a search query for records from the User \[sys\_user\] table that contain the term `Anglin`.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sys_user');
  answer.setSearchPhrase('Anglin');

  return answer;
}
```

## GeniusResultAnswer – spellCheck\(Boolean spellCheck\)

Specifies whether to perform typo handling auto-correction \(spell checking\) for the search query defined in a Genius Result configuration's **AI Search request processor** script.

If you don't invoke this method in your Genius Result configuration's **AI Search request processor** script, the defined search query inherits the typo handling flag from the search query that triggers the Genius Result configuration.

<table id="table_j1x_x14_vnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

spellCheck

</td><td>

Boolean

</td><td>

Flag that indicates whether to perform typo handling auto-correction for the search query defined in your Genius Result configuration's **AI Search request processor** script.

 Valid values:

-   true: Perform typo handling auto-correction for the search query.
-   false: Bypass typo handling auto-correction for the search query.

 Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This **AI Search request processor** script disables typo handling auto-correction for its search query against the User \[sys\_user\] table.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sys_user');
  answer.setSearchLimit(2);
  answer.spellCheck(false);
  var queries = [];
  var matchingSegments;
  var predictionResult = context.getPredictionResult();
  if (predictionResult && predictionResult.length == 1) {
    var detail = predictionResult[0];
    if (detail['result'] && detail['result']['entities']) {
      var entities = detail['result']['entities'];
      for (var i = 0; i < entities.length; i++) {
        if (entities[i]['name'].endsWith('personName')) {
          matchingSegments = entities[i]['matchingSegments'];
          for (var j = 0; j < matchingSegments.length; j++)
            answer.addSearchPhrases([matchingSegments[j]['value']]);
        } else if (entities[i]['name'].endsWith('cityLocation')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('location.nameLIKE' + matchingSegments[0]['value']);
        } else if (entities[i]['name'].endsWith('departmentName')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('department.nameLIKE' + matchingSegments[0]['value']);
        } else if (entities[i]['name'].endsWith('jobTitle')) {
          matchingSegments = entities[i]['matchingSegments'];
          if (matchingSegments && matchingSegments.length > 0)
            queries.push('titleLIKE' + matchingSegments[0]['value']);
        }
      }
    }
  }

  if (queries.length > 0)
    answer.setEncodedQuery(queries.join('^'));

  return answer;
}
```

