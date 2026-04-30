---
title: GeniusResultContext - Scoped
description: The GeniusResultContext API provides methods for retrieving search query information from the context of a Genius Result configuration.Retrieves search result documents from the search query that triggers your Genius Result configuration.Retrieves the original search terms from the search query that triggers your Genius Result configuration.Retrieves NLU model prediction results for the search query that triggers your Genius Result configuration.
locale: en-US
release: zurich
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GeniusResultContext- Scoped

The GeniusResultContext API provides methods for retrieving search query information from the context of a Genius Result configuration.

You can use search query details retrieved with this API to populate Genius Result answer objects created with the [GeniusResultAnswer](../../GeniusResultAnswerScoped/concept/GeniusResultAnswerScopedAPI.md#) API.

Use this API in Genius Result server-side scripts with the `sn_ais` namespace identifier. For more information on scripting logic for Genius Results, see [Create a new Genius Result configuration](https://www.servicenow.com/docs/access?context=create-genius-results-config-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## GeniusResultContext - getMatchingDocuments\(\)

Retrieves search result documents from the search query that triggers your Genius Result configuration.

Use this method in a Genius Result configuration's response processor script to retrieve field values from search result documents returned by the search query that triggers your Genius Result. You can populate Genius Result answers with fields from the search result documents using GeniusResultAnswer API methods.

**Note:** This method returns no results when invoked in an **AI Search request processor** script, since the script is executed before AI Search computes results for the triggering search query. Don't use this method in your request processor scripts.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_fhg_4gr_ywb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Array\]

</td><td>

Array of objects in which each object represents a search result document that matched the search query.

 Data type: Array

 ```
[
  {
    ".score": Number,
    ".table": "String",
    ".text": "String",
    ".title": "String",
    ".url": "String",
    "class_name": "String",
    "sys_id": "String",
    "<field_name>": <field_value>
  }
]
```

 **Note:** Depending on the search query, some of the search result document's AI Search index fields may appear in the object in addition to the listed name-value pairs.

</td></tr><tr><td>

\[Array\]..score

</td><td>

Relevancy score computed for the search result document in the context of the search query.

 Data type: Number

 **Note:** The name for this name-value pair begins with a period to distinguish it from the AI Search index's **score** common field.

</td></tr><tr><td>

\[Array\]..table

</td><td>

Name of the ServiceNow AI Platform table that the search result document was indexed from.

 Data type: String

 **Note:** The name for this name-value pair begins with a period to distinguish it from the AI Search index's **table** common field.

</td></tr><tr><td>

\[Array\]..text

</td><td>

Indexed text from the search result document.

 Data type: String

 **Note:** The name for this name-value pair begins with a period to distinguish it from the AI Search index's **text** common field.

</td></tr><tr><td>

\[Array\]..title

</td><td>

Indexed title for the search result document.

 Data type: String

 **Note:** The name for this name-value pair begins with a period to distinguish it from the AI Search index's **title** common field.

</td></tr><tr><td>

\[Array\]..url

</td><td>

URL for the search result document.

 Data type: String

 **Note:** The name for this name-value pair begins with a period to distinguish it from the AI Search index's **url** common field.

</td></tr><tr><td>

\[Array\].class\_name

</td><td>

The child class that the search result document belongs to. For more information on table child classes, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

 Data type: String

</td></tr><tr><td>

\[Array\].sys\_id

</td><td>

Sys\_id for the search result document.

 Data type: String

</td></tr><tr><td>

\[Array\].&lt;field\_name&gt;

</td><td>

AI Search index field from the search result document.

 Data type: The data type of the AI Search index field.

</td></tr></tbody>
</table>This **AI Search response processor** script retrieves up to three search result documents matched by the search query and checks whether any of them is from the Knowledge \[kb\_knowledge\] table. If it finds a search result document from the Knowledge table, the function adds that document's fields to the GeniusResultAnswer object so the UI can display them to the user.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();
  var matchingDocuments = context.getMatchingDocuments();
  if (matchingDocuments.length > 1) {
    for (var i = 0; i < 3; i++) {
      var currentDocument = matchingDocuments[i];
      if (currentDocument['.table'] == 'kb_knowledge') {
        var gr = new GlideRecord("kb_knowledge");
        if (gr.get(currentDocument['sys_id'])) {
          answer.addDataMap({
            "number": currentDocument['number'],
            "url": currentDocument['.url'],
            "title": currentDocument['.title']
          });
        }
      }
      break;
    }
  }
  return answer;
}
```

## GeniusResultContext – getOriginalSearchPhrase\(\)

Retrieves the original search terms from the search query that triggers your Genius Result configuration.

You can use retrieved search terms to populate Genius Result answers using GeniusResultAnswer API methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_e5s_ntm_qnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

Original terms from the search query.

 Data type: String

</td></tr></tbody>
</table>This **AI Search request processor** script gets the search query's original terms and uses them as the query terms for a new snippet search.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  var searchPhrase = context.getOriginalSearchPhrase();
  answer.setSearchPhrase(searchPhrase);
  answer.snippetSearch(true);

  return answer;
}
```

## GeniusResultContext – getPredictionResult\(\)

Retrieves NLU model prediction results for the search query that triggers your Genius Result configuration.

Use this method in a Genius Result configuration's request or response processor script to retrieve the intent detected for the triggering search query. You can populate Genius Result answers with details from the detected intent using GeniusResultAnswer API methods.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_ajs_4tm_qnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\[Array\]

</td><td>

Array of objects in which each object represents an NLU model intent prediction result for the search query.

 Data type: Array

 ```
[
  {
    "intentName": "String",
    "result": {Object},
    "solutionName": "String"
  }
]
```

</td></tr><tr><td>

\[Array\].intentName

</td><td>

Name of the NLU model intent detected in the search query.

 Data type: String

</td></tr><tr><td>

\[Array\].result

</td><td>

Object representing the NLU model intent prediction result for the search query.

 Data type: Object

 ```
"result": {
  "application": {Object},
  "result": {Object},
  "solutionLabel": "String",
  "solutionName": "String",
  "solutionType": "String",
  "type": "String",
  "version": Number
}
```

</td></tr><tr><td>

\[Array\].result.application

</td><td>

Object containing metadata for the search application that produced the prediction result.

 Data type: Object

 ```
"application": {
  "language": "String",
  "type": "String"
}
```

</td></tr><tr><td>

\[Array\].result.application.language

</td><td>

Language context for the ServiceNow AI Platform application that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.application.type

</td><td>

Type of the ServiceNow AI Platform application that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result

</td><td>

Object including details for the NLU model intent prediction result.

 Data type: Object

 ```
"result": {
  "entities": [Array],
  "intentName": "String",
  "intents": [Array],
  "nluModelName": "String",
  "score": Number
}
```

</td></tr><tr><td>

\[Array\].result.result.entities

</td><td>

Array of objects in which each object represents an NLU model intent entity detected in the search query.

 Data type: Array

 ```
"entities": [
  {
    "matchingSegments": [Array],
    "name": "String",
    "parts": [Array],
    "score": Number,
    "startingPosition": Number,
    "value": "String"
  }
]
```

</td></tr><tr><td>

\[Array\].result.result.entities.matchingSegments

</td><td>

Array of objects in which each object represents a matching segment of the detected NLU entity.

 Data type: Array

 ```
"matchingSegments": [
  {
    "directMatch": Boolean
    "meta": {Object},
    "value": "String"
  }
]
```

</td></tr><tr><td>

\[Array\].result.result.entities.matchingSegments.directMatch

</td><td>

Flag that indicates whether the NLU entity matching segment represents an exact match for the entity value.

</td></tr><tr><td>

\[Array\].result.result.entities.matchingSegments.meta

</td><td>

Object containing key-value pair fields representing metadata for the NLU entity matching segment.

 Data type: Object

 ```
"meta": {
  "augmentedBy": "String",
  "colMeta:first_name": "String",
  "colMeta:last_name": "String",
  "compositionStrategy": "String",
  "fieldName": "String",
  "searchPreProcessors": "String",
  "SUB_PHRASE.penalty": "String",
  "tableName": "String"
}
```

</td></tr><tr><td>

\[Array\].result.result.entities.matchingSegments.value

</td><td>

String value of the NLU entity matching segment.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.entities.name

</td><td>

Name for the detected NLU entity, in `entity:[NLU_model].[intent].[entity_type]` format.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.entities.parts

</td><td>

Array of objects in which each object represents an NLU entity part found in the prediction result.

 Data type: Array

 ```
"parts": [
  {
    "meta": {Object},
    "value": "String"
  }
]
```

</td></tr><tr><td>

\[Array\].result.result.entities.parts.meta

</td><td>

Object containing key-value pair fields representing metadata for the NLU entity part.

 Data type: Object

 ```
"meta": {
  "augmentedBy": "String",
  "colMeta:name": "String",
  "compositionStrategy": "String",
  "fieldName": "String",
  "searchPreProcessors": "String",
  "SUB_PHRASE.penalty": "String",
  "tableName": "String"
}
```

</td></tr><tr><td>

\[Array\].result.result.entities.parts.value

</td><td>

String value of the NLU entity part.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.entities.score

</td><td>

Numeric score from 0 through 1 indicating confidence for the detected NLU entity.

 Data type: Number

</td></tr><tr><td>

\[Array\].result.result.entities.startingPosition

</td><td>

Numeric index for the character position in the search query at which the detected NLU entity begins.

 Data type: Number

</td></tr><tr><td>

\[Array\].result.result.entities.value

</td><td>

String value of the NLU detected in the search query.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.intentName

</td><td>

Name of the NLU model intent detected in the search query.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.intents

</td><td>

Array of objects in which each object represents a nested NLU model intent detected in the search query.

 Nested intent objects include the same parameter names and data types as the parent NLU model intent object.

 Data type: Array

 ```
"intents": [
  {
    "entities": [Array],
    "intentName": "String",
    "intents": [Array],
    "nluModelName": "String",
    "score": Number
  }
]
```

</td></tr><tr><td>

\[Array\].result.result.nluModelName

</td><td>

Name of the NLU model that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.result.score

</td><td>

Numeric score from 0 through 1 indicating confidence for the NLU model prediction result.

 Data type: Number

</td></tr><tr><td>

\[Array\].result.solutionLabel

</td><td>

Label for the NLU model that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.solutionName

</td><td>

Name for the NLU model that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.solutionType

</td><td>

Type for the NLU model that produced the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.type

</td><td>

Type of the prediction result.

 Data type: String

</td></tr><tr><td>

\[Array\].result.version

</td><td>

Version of the NLU model that produced the prediction result.

 Data type: Number

</td></tr><tr><td>

\[Array\].solutionName

</td><td>

Name of the NLU model that produced the prediction result.

 Data type: String

</td></tr></tbody>
</table>This **AI Search request processor** script checks whether the search query includes an NLU model prediction result. When it finds a prediction result, it adds the matching segments from all detected catalogItem entities as search terms.

```
function process(context) {
  var answer = new sn_ais.GeniusResultAnswer();

  answer.setTable('sc_cat_item');
  answer.setSearchLimit(2);
  var predictionResult = context.getPredictionResult();
  if (predictionResult && predictionResult.length == 1) {
    var detail = predictionResult[0];
    if (detail['result'] && detail['result']['entities']) {
      var entities = detail['result']['entities'];
      for (var i = 0; i < entities.length; i++) {
        if (entities[i]['name'].endsWith('catalogItem')) {
          var matchingSegments = entities[i]['matchingSegments'];
          for (var j = 0; j < matchingSegments.length; j++)
            answer.addSearchPhrases([matchingSegments[j]['value']]);
        }
      }
    }
  }

  return answer;
}
```

