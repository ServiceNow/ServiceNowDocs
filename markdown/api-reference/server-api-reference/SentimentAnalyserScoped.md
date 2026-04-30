---
title: SentimentAnalyser - Scoped
description: The SentimentAnalyser script include provides methods to perform sentiment analysis on a string value.Creates an instance of the SentimentAnalyser class with the default connector configuration that is used for sentiment analysis.Creates an instance of the SentimentAnalyser class with the specified connector configuration that is used for sentiment analysis.Performs sentiment analysis on the specified text.Performs sentiment analysis on an array of strings.Performs sentiment analysis on an array of strings in the specified language.Performs sentiment analysis on a specified text and language.Returns the GlideRecord of the specified connector configuration.Returns the GlideRecord of the default connector configuration.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# SentimentAnalyser- Scoped

The SentimentAnalyser script include provides methods to perform sentiment analysis on a string value.

You should use this script include in a script that is treated as an admin-executing script. For example, use the Sentiment Analysis script includein a script action or scheduled job.

To use this class in a scoped application, use the `sn_nlp_sentiment` namespace identifier. The Sentiment Analysis plugin \(com.snc.sentiment\_analysis\) must be enabled to access the SentimentAnalyser API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## SentimentAnalyser - SentimentAnalyser\(\)

Creates an instance of the SentimentAnalyser class with the default connector configuration that is used for sentiment analysis.

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
```

## SentimentAnalyser - SentimentAnalyser\(GlideRecord configGR\)

Creates an instance of the SentimentAnalyser class with the specified connector configuration that is used for sentiment analysis.

|Name|Type|Description|
|----|----|-----------|
|configGR|GlideRecord|GlideRecord object of a connector configuration.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser(configGR);
```

## SentimentAnalyser - analyze\(String inputText\)

Performs sentiment analysis on the specified text.

|Name|Type|Description|
|----|----|-----------|
|inputText|String|Text on which sentiment analysis should be performed.|

|Type|Description|
|----|-----------|
|JSON object|Result of the sentiment analysis specifying the status, score, normalised score, sys\_id of the relevant connector configuration, and error message.|

```

        var sa = new sn_nlp_sentiment.SentimentAnalyser();
        var result = sa.analyze ("Example string");
```

Output:

```
{"status": "Success", "score": "0.7", "normalizedScore": "0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", "errorMessage":""}
```

## SentimentAnalyser - analyzeMultiple\(Array inputTextArray\)

Performs sentiment analysis on an array of strings.

|Name|Type|Description|
|----|----|-----------|
|inputTextArray|Array|Array of text \(string\) on which to perform sentiment analysis.|

|Type|Description|
|----|-----------|
|JSON Array|An array that gives the result of the sentiment analysis performed on multiple texts specifying the status, score, normalized score, sys\_id of the relevant connector configuration, and error message.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
var result = sa.analyzeMultiple (["Example string1","Example string2"]);
```

Output:

```
[{"text": "I am happy","result": {Success", "score": "0.7", "normalizedScore": "0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", "errorMessage":""}},{"text": "I am not happy","result": {Success", "score": "-0.7", "normalizedScore": "-0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", "errorMessage":""}}]
```

## SentimentAnalyser - analyzeMultipleWithLanguage\(Array inputTextArray, String language\)

Performs sentiment analysis on an array of strings in the specified language.

|Name|Type|Description|
|----|----|-----------|
|inputTextArray|Array|Array of text \(string\) on which to perform sentiment analysis.|
|language|String|Language for the input text. This can very for different sentiment services.|

|Type|Description|
|----|-----------|
|JSON Array|An array with the result of the sentiment analysis performed on multiple texts of the mentioned language, specifying the status, score, normalized score, sys\_id of the relevant connector configuration, and error message.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
var result = sa.analyzeMultipleWithLanguage (["Example string1","Example string2"], "en");
```

Output:

```
[{"text": "I am happy","result": {Success", "score": "0.7", "normalizedScore": "0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", "errorMessage":""}},{"text": "I am not happy","result": {Success", "score": "-0.7", "normalizedScore": "-0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", "errorMessage":""}}]
```

## SentimentAnalyser - analyzeWithLanguage\(String inputText, String language\)

Performs sentiment analysis on a specified text and language.

|Name|Type|Description|
|----|----|-----------|
|inputText|String|Text on which to perform sentiment analysis.|
|language|String|Language for the input text. This can vary for different sentiment services.|

|Type|Description|
|----|-----------|
|JSON object|Result of the sentiment analysis specifying the status, score, normalized score, sys\_id of the relevant connector configuration, and error message.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
var result = sa.analyze ("Example string", "en");
```

Output:

```
{"status": "Success", "score": "0.7", "normalizedScore": "0.7", "connectorConfig": "10932aa773101300734e234ffff6a777", errorMessage":""}
```

## SentimentAnalyser - getConnectorByName\(String connectorName\)

Returns the GlideRecord of the specified connector configuration.

|Name|Type|Description|
|----|----|-----------|
|connectorName|String|Name of the connector configuration.|

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord of the specified connector configuration.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
var connector = sa.getConnectorByName("xxx");
```

Output:

```
GlideRecord object of the connector configuration with name "xxx", null if no connector is named as "xxx".

```

## SentimentAnalyser - getDefaultConnector\(\)

Returns the GlideRecord of the default connector configuration.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|GlideRecord|GlideRecord of the default connector configuration.|

```
var sa = new sn_nlp_sentiment.SentimentAnalyser();
var defaultConnector = sa.getDefaultConnector();
```

