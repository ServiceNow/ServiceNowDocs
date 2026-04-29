---
title: DynamicTranslation - Client
description: The DynamicTranslation API provides methods that translate text, in real time, into multiple languages using translation service providers. This API is available for both standard clients and Angular-based Service Portal clients.Detects the language of the passed in text.Detects the languages of the passed in text strings.Translates the passed in text to one or more languages.Translates the passed in text strings to one or more languages.Determines whether the various methods in the DynamicTranslation API are enabled for a translation service.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 24
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# DynamicTranslation- Client

The DynamicTranslation API provides methods that translate text, in real time, into multiple languages using translation service providers. This API is available for both standard clients and Angular-based Service Portal clients.

In addition, you can use this API to detect the language of a specific string and check whether the DynamicTranslation methods are enabled for a translation service. Use this API to create a seamless localization experience for your user interface, enabling one interface to service multiple countries.

Currently this API supports two translation service providers: Microsoft Azure Translator Service and Google Cloud Translator Service. You can also configure other translation services within your instance and then use the DynamicTranslation API to translate your text.

To use this API you must activate the Dynamic Translation plugin. For information on this plugin and additional information on Dynamic Translation, refer to [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US). Also, to use this API in a Service Portal widget, you must inject the dynamicTranslation service into the widget client script function.

**Note:** The name of the class to use in Service Portal clients is dynamicTranslation, while the name of the class to use in standard clients is DynamicTranslation.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## DynamicTranslation - getDetectedLanguage\(String text, Object parms\)

Detects the language of the passed in text.

If you pass in a translator, the method uses that translation service to detect the source language. Otherwise, the detection is performed by the default translation service. Ensure that the text strings that you provide contain enough verbiage to enable proper language detection.

In addition to the detected language, the response contains a confidence level of the detection, along with other possible language alternatives. If a translator is not passed in, the method also returns the default translation service used to detect the language.

<table id="table_rym_ftl_thb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

text

</td><td>

String

</td><td>

Text to use to detect the language.

</td></tr><tr><td>

parms

</td><td>

Object

</td><td>

Optional. JSON object that contains additional translation parameters.```
"parms": {
  "translator": "String"
}
```

</td></tr><tr><td>

parms.translator

</td><td>

String

</td><td>

Translation service to use to detect the language of a string. Translation services are configured under the **Translator Configuration** menu.Possible values - not case-sensitive:

-   Google
-   Microsoft
-   IBM
-   &lt;custom&gt;

**Note:** To use custom translation services you must first configure the translation service in your instance. For details, see [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Default: Translation service configured in the Translator Configuration \[sn\_dt\_translator\_configuration\] table.

Table: Translator Configuration \[sn\_dt\_translator\_configuration\]

</td></tr></tbody>
</table><table id="table_sym_ftl_thb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="detections_alternatives-row-dynTran"><td>

alternatives

</td><td>

Array of objects that describe other languages that might also be a match.Data type: Array

 ```
"alternatives": [
  {
    "code": "String",
    "confidence": "String",
    "name": "String"
  }
]
```

</td></tr><tr id="detections_alternatives_code-row-dynTran"><td>

alternatives.code

</td><td>

Language code of the alternative language.Data type: String

</td></tr><tr id="detections_alternatives_conf-row-dynTran"><td>

alternatives.confidence

</td><td>

Float value indicating the confidence level of the alternative language. Value is between zero and one. The lower the value, the lower the confidence level.Data type: String

</td></tr><tr id="detections_alternatives_name-row-dynTran"><td>

alternatives.name

</td><td>

Language code of the alternative language.Data type: String

</td></tr><tr id="detections_detectedLanguage-row-dynTran"><td>

detectedLanguage

</td><td>

Description of the detected language.Data type: Object

 ```
"detectedLanguage": {
  "code": "String",
  "confidence": "String",
  "name": "String"
}
```

</td></tr><tr id="detections_detectedLanguage_code-row-dynTran"><td>

detectedLanguage.code

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr id="detections_detectedLanguage_confidence-row-dynTran"><td>

detectedLanguage.confidence

</td><td>

Float value indicating the confidence level of the alternative language. Value is between zero and one. The lower the value, the lower the confidence level.Data type: String

</td></tr><tr id="detections_detectedLanguage_name-row-dynTran"><td>

detectedLanguage.name

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr id="translator-row-dynTran"><td>

translator

</td><td>

Translation service used to detect the language.Data type: String

</td></tr><tr><td>

Error messages

</td><td>

The following are error messages that the method may return and indications as to the error's root cause. -   Text \("text" field\) is missing or invalid. \(40000\): The text to detect the language is either missing or not a string.
-   Dynamic Translation plugin is not installed. \(40001\): The Dynamic Translation API was invoked without activating the com.glide.dynamic\_translation plugin. For information on activating this plugin, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator \("translator" field\) is invalid. \(40003\): The passed in **translator** parameter is not a string.
-   &lt;translator&gt; translator is not configured. \(40004\): The specified translation service is not configured in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is inactive. \(40005\): The specified translation service is not set to **Active** in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Additional parameters are invalid. \(40006\): The additional parameters that were passed are not an object.
-   Maximum time limit has been exceeded. \(40009\): The operation took longer than the defined timeout value specified in the Translation Configuration. Default: 40 seconds
-   Default translator is not configured for detection. \(40011\): The default translation service has not been specified for language detection in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is not configured for detection. \(40013\): The specified translation service is not configured for language detection in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Unknown error occurred. \(40051\): Default error thrown when the error doesn't fall in to any other category.
-   Text \("text" field\) has exceeded its maximum length. \(40052\): The text that was passed in for language detections exceeds the maximum length supported by the corresponding translation service.
-   Request is not authorized because credentials are missing or invalid \(40055\): The credentials configured for the translation service in Connections &amp; Credentials are not valid. For information on connections and credentials, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>This example shows code that detects a string in English using IBM's translation service in a standard client script.

```
var detectedResponse = DynamicTranslation.getDetectedLanguage('Please detect the language of this text', {"translator":'IBM'}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
```

Output:

```
detectedResponse {
  detectedLanguage:
    { "code": "en", "confidence": "1", "name": "en" }
  alternatives: 
    [
      { "code": "vi", "confidence": "0.86", "name": "vi" },
      { "code": "id", "confidence": "0.86", "name": "id" }
    ]                  
 }
```

This example shows a client script that throws an error when an invalid translation service is passed in.

```
var detectedResponse = DynamicTranslation.getDetectedLanguage('Please detect the language of this text', {"translator":123}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
```

Output:

```
{"code":"40003","message":"Translator (\"translator\" field) is invalid"}
```

This example shows code that detects a string in English using IBM's translation service in a Service Portal widget client script. Note that the name of the class is `dynamicTranslation` not `DynamicTranslation`.

```
var detectedResponse = dynamicTranslation.getDetectedLanguage('Please detect the language of this text', {"translator":'IBM'}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
```

Output:

```
detectedResponse {
  detectedLanguage:
    { "code": "en", "confidence": "1", "name": "en" }
  alternatives: 
    [
      { "code": "vi", "confidence": "0.86", "name": "vi" },
      { "code": "id", "confidence": "0.86", "name": "id" }
    ]                  
 }
```

This example shows a Service Portal widget client script that throws an error when an invalid translation service is passed in.

```
var detectedResponse = dynamicTranslation.getDetectedLanguage('Please detect the language of this text', {"translator":123}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
```

Output:

```
{"code":"40003","message":"Translator (\"translator\" field) is invalid"}
```

## DynamicTranslation - getDetectedLanguages\(Array texts, Object parms\)

Detects the languages of the passed in text strings.

If you pass in a translator, the method uses that translation service to detect the source language. Otherwise, the detection is performed by the default translation service. Ensure that the text strings that you provide contain enough verbiage to enable proper language detection.

In addition to the detected language, the response contains a confidence level of the detection, along with other possible language alternatives. If a translator is not passed in, the method also returns the default translation service used to detect the language.

When calling this method from a portal client script, use the class name dynamicTranslation; such as dynamicTranslation.getTranslations\(\). When calling it from a platform client script, use the class name DynamicTranslation; such as DynamicTranslation.getTranslations\(\).

<table id="table_rlv_w4r_nnb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

parms

</td><td>

Object

</td><td>

Optional. JSON object that contains additional translation parameters.```
"parms": {
  "translator": "String"
}
```

</td></tr><tr><td>

parms.translator

</td><td>

String

</td><td>

Translation service to use to detect the language of a string. Translation services are configured under the **Translator Configuration** menu.Possible values - not case-sensitive:

-   Google
-   Microsoft
-   IBM
-   &lt;custom&gt;

**Note:** To use custom translation services you must first configure the translation service in your instance. For details, see [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Default: Translation service configured in the Translator Configuration \[sn\_dt\_translator\_configuration\] table.

Table: Translator Configuration \[sn\_dt\_translator\_configuration\]

</td></tr><tr><td>

texts

</td><td>

Array

</td><td>

List of text strings to use to detect the language\(s\).

</td></tr></tbody>
</table><table id="table_slv_w4r_nnb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

detections

</td><td>

Language detection of text strings.Data type: Object

```
"detections": {
  "alternatives": [Array],
  "detectedLanguage": {Object},
  "isError": Boolean
}
```

</td></tr><tr><td>

detections.alternatives

</td><td>

Array of objects that describe other languages that might also be a match.Data type: Array

 ```
"alternatives": [
  {
    "code": "String",
    "confidence": "String",
    "name": "String"
  }
]
```

</td></tr><tr><td>

detections.alternatives.code

</td><td>

Language code of the alternative language.Data type: String

</td></tr><tr><td>

detections.alternatives.confidence

</td><td>

Float value indicating the confidence level of the alternative language. Value is between zero and one. The lower the value, the lower the confidence level.Data type: String

</td></tr><tr><td>

detections.alternatives.name

</td><td>

Language code of the alternative language.Data type: String

</td></tr><tr><td>

detections.detectedLanguage

</td><td>

Description of the detected language.Data type: Object

 ```
"detectedLanguage": {
  "code": "String",
  "confidence": "String",
  "name": "String"
}
```

</td></tr><tr><td>

detections.detectedLanguage.code

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr><td>

detections.detectedLanguage.confidence

</td><td>

Float value indicating the confidence level of the alternative language. Value is between zero and one. The lower the value, the lower the confidence level.Data type: String

</td></tr><tr><td>

detections.detectedLanguage.name

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr><td>

detections.isError

</td><td>

Flag that indicates whether the detection of language for the text resulted in an error.Valid values:

-   true: Error encountered.
-   false: Language detection was successful.

Data type: Boolean

</td></tr><tr><td>

status

</td><td id="status-entry-dynTran">

Status of the response to the method call.Possible values:

-   Error
-   Partial
-   Success

Data type: String

</td></tr><tr><td>

translator

</td><td id="translator-entry-dynTran">

Translation service used to detect the language.Data type: String

</td></tr><tr><td>

Error messages

</td><td>

The following are error messages that the method may return and indications as to the error's root cause. -   Text \("text" field\) is missing or invalid. \(40000\): The text to detect the language is either missing or not a string.
-   Dynamic Translation plugin is not installed. \(40001\): The Dynamic Translation API was invoked without activating the com.glide.dynamic\_translation plugin. For information on activating this plugin, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator \("translator" field\) is invalid. \(40003\): The passed in **translator** parameter is not a string.
-   &lt;translator&gt; translator is not configured. \(40004\): The specified translation service is not configured in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is inactive. \(40005\): The specified translation service is not set to **Active** in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Additional parameters are invalid. \(40006\): The additional parameters that were passed are not an object.
-   Maximum time limit has been exceeded. \(40009\): The operation took longer than the defined timeout value specified in the Translation Configuration. Default: 40 seconds
-   Request failed with multiple errors. \(40010\): Multiple errors occurred in the language detection call. For more information, refer to the response for each individual text string.
-   Default translator is not configured for detection. \(40011\): The default translation service has not been specified for language detection in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is not configured for detection. \(40013\): The specified translation service is not configured for language detection in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator configuration version is invalid. Migrate to v3. \(40014\): The associated version of the Translator Configuration for the specified translation service does not support the specified text translation method. For more information, see [Migrate to version v3 of a translator configuration](https://www.servicenow.com/docs/access?context=migrate-v3-dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Unknown error occurred. \(40051\): Default error thrown when the error doesn't fall in to any other category.
-   Text \("text" field\) has exceeded its maximum length. \(40052\): The text that was passed in for language detections exceeds the maximum length supported by the corresponding translation service.
-   Request is not authorized because credentials are missing or invalid \(40055\): The credentials configured for the translation service in Connections &amp; Credentials are not valid. For information on connections and credentials, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>This example shows code from a portal client script that detects English as the language of the passed-in strings using the Microsoft translation service.

```
var detectedResponse = dynamicTranslation.getDetectedLanguages(["First text string language to detect", "Second text string language to detect"], {"translator": "Microsoft"}).then(function(res) {console.log(res);}, function(res) {console.log(res);});
gs.info(JSON.stringify(detectedResponse));

```

Output

```
{
  "translator":"Microsoft",
  "status":"Success",
  "detections":[
    {
      "isError":false,
      "detectedLanguage":{"name":"en", "code":"en", "confidence":"1"},
      "alternatives":[
        {"name":"id", "code":"id", "confidence":"0.83"},
        {"name":"ms", "code":"ms", "confidence":"0.83"}
      ]
    },
    {
      "isError":false,
      "detectedLanguage":{"name":"en", "code":"en", "confidence":"1"},
      "alternatives":[
        {"name":"fr", "code":"fr", "confidence":"0.83"},
        {"name":"id", "code":"id", "confidence":"0.83"}
      ]
    }
  ]
}
```

This example shows code in a portal client script that returns a Partial status when two text strings are passed in and one of them is invalid. To use this code example in a platform client script, change `dynamicTranslation.getDetectedLanguages` to `DynamicTranslation.getDetectedLanguages`.

```
var detectedResponse = dynamicTranslation.getDetectedLanguages(["First text string language to detect", ""], {"translator": "Microsoft"}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
gs.info(JSON.stringify(detectedResponse));
```

Output

```
{
  "translator":"Microsoft",
  "status":"Partial",
  "detections":[
    {
      "isError":false,
      "detectedLanguage":{"name":"en", "code":"en", "confidence":"1"},
      "alternatives":[
        {"name":"id", "code":"id", "confidence":"0.83"},
        {"name":"ms", "code":"ms", "confidence":"0.83"}
      ]
    },
    {
      "isError":true,
      "code":"40000",
      "message":"Text is missing or invalid"
    }
  ]
}
```

This example shows code from a portal client script that throws an error when an invalid translation service is passed in. To use this code example for a platform client script, change `dynamicTranslation.getDetectedLanguages` to `DynamicTranslation.getDetectedLanguages`.

```
var detectedResponse = dynamicTranslation.getDetectedLanguages(["First text string language to detect", "Second text string language to detect"], {"translator": "123"}).then(function(res) {console.log(res); }, function(res) {console.log(res); } );
gs.info(JSON.stringify(detectedResponse));
```

Output

```
{"code":"40003","message":"Translator (\"translator\" field) is invalid","status":"Error"}
```

## DynamicTranslation - getTranslation\(String textToTranslate, Object parms\)

Translates the passed in text to one or more languages.

The method uses translation services, such as Microsoft Azure Translator Service and Google Cloud Translator Service, to perform the translation. If you do not pass in translation parameters, the method uses the system default.

<table id="table_bzb_4zk_thb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

textToTranslate

</td><td>

String

</td><td>

Text to translate.

</td></tr><tr><td>

parms

</td><td>

Object

</td><td>

Optional. JSON object that contains additional translation parameters.```
"parms": {
  "additionalParameters": {Object},
  "sourceLanguage": "String",
  "targetLanguages": [Array],
  "translator": "String"
}
```

</td></tr><tr><td>

parms.additionalParameters

</td><td>

Object

</td><td>

Optional. Array of JSON objects. Each object contains key-value pairs that provide additional information for performing the translation.```
"additionalParameters": {
  "parameterName": "String",
  "parameterValue": "String"
}
```

</td></tr><tr><td>

parms.additionalParameters.parameterName

</td><td>

String

</td><td>

Optional. Key name.Valid values:

textype: Type of text to translate. For Microsoft Azure Translator Service only.

</td></tr><tr><td>

parms.additionalParameters.parameterValue

</td><td>

String

</td><td>

Optional. Value of the associated key.Valid values:

-   html: HTML text string
-   plain: Standard text string

Default: plain

</td></tr><tr><td>

parms.sourceLanguage

</td><td>

String

</td><td>

Optional. Language code of the source text.Default: Translation service detects the source language.

</td></tr><tr><td>

parms.targetLanguages

</td><td>

Array

</td><td>

Optional. List of language codes to use to translate the text. The method returns translated text for each language code.Default: User preferred language.

</td></tr><tr><td>

parms.translator

</td><td>

String

</td><td>

Optional. Translation service to use to translate the text \(not case-sensitive\).Valid values:

 -   Google
-   Microsoft
-   IBM
-   &lt;custom&gt;

 **Note:** To use custom translation services you must first configure the translation service in your instance. For details, see [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

 Default: Translation service configured in the Translator Configuration \[sn\_dt\_translator\_configuration\] table.

</td></tr></tbody>
</table><table id="table_czb_4zk_thb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr id="detections_detectedLanguage-row-dynTran"><td>

detectedLanguage

</td><td>

Description of the detected language.Data type: Object

 ```
"detectedLanguage": {
  "code": "String",
  "name": "String"
}
```

</td></tr><tr id="detections_detectedLanguage_code-row-dynTran"><td>

detectedLanguage.code

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr id="detections_detectedLanguage_name-row-dynTran"><td>

detectedLanguage.name

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr><td>

translations

</td><td id="translations-trans-entry-dynTrans">

List that describe the language translations.Data type: Array of Objects

```
translations": [
  {
    "targetLanguage": "String",
    "translatedText": "String"
  }
]
```

</td></tr><tr><td>

translations.targetLanguage

</td><td id="trans_trg_lang-trans-entry-dynTrans">

Language code to which the source text was translated.Data type: String

</td></tr><tr><td>

translations.translatedText

</td><td id="trans_transText-trans-entry-dynTrans">

Translated text.Data type: String

</td></tr><tr id="translator-row-dynTran"><td>

translator

</td><td>

Translation service used to detect the language.Data type: String

</td></tr><tr><td>

Error messages

</td><td>

The following are error messages that the method may return and indications as to their root cause. -   Text \("text" field\) is missing or invalid. \(40000\): The text to translate is either missing or not a string.
-   Dynamic Translation plugin is not installed. \(40001\): The Dynamic Translation API was invoked without activating the com.glide.dynamic\_translation plugin. For information on activating this plugin, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Default translator is not configured for translation. \(40002\): No translation service is selected as the default translation service in the Translator Configurations. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator \("translator" field\) is invalid. \(40003\): The passed in **translator** parameter is not a string.
-   &lt;translator&gt; translator is not configured. \(40004\): The specified translation service is not configured in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is inactive. \(40005\): The specified translation service is not set to **Active** in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Additional parameters are invalid. \(40006\): The additional parameters that were passed are not an object.
-   Target languages \("targetLanguages" field\) are invalid. \(40007\): The **targetLanguages** parameter is passed in the call but is not valid for one of the following reasons:

    -   Value isn't an array
    -   Array is empty
    -   One or multiple of the entries is not a string
-   Source language \("sourceLanguage" field\) is invalid. \(40008\): The **sourceLanguage** parameter is passed in the call but the value is not a String.
-   Maximum time limit has been exceeded. \(40009\): The operation took longer than the defined timeout value specified in the Translation Configuration. Default: 40 seconds
-   &lt;translator&gt; translator is not configured for translation. \(40012\): The specified translation service is not configured for text translation in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Unknown error occurred. \(40051\): Default error thrown when the error doesn't fall in to any other category.
-   Text \("text" field\) has exceeded its maximum length. \(40052\): The text that was passed in to translate exceeds the maximum length supported by the corresponding translation service.
-   Source language is invalid. \(40053\): The passed in **sourceLanguage** parameter contains a language code that is not supported by the corresponding translation service.
-   Target language is invalid. \(40054\): One or more of the language codes passed in the **targetLanguages** parameter is not supported by the corresponding translation service.
-   Request is not authorized because credentials are missing or invalid \(40055\): The credentials configured for the translation service in Connections &amp; Credentials are not valid. For information on connections and credentials, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Text cannot be translated to target languages. \(40056\): The specified translation service is not able to translate the passed in text into the specified target languages.

</td></tr></tbody>
</table>This example shows the translation of plain text content from English \(detected\) into French and Italian using Microsoft's translation service in a standard client script.

```
DynamicTranslation.getTranslation("Translate this text using platform from client", {
  "targetLanguages": ["fr", "it"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});

```

Response:

```

{"translations":[
    {
      "targetLanguage":"it",
      "translatedText":"Tradurre questo testo utilizzando la piattaforma dal client"
    },
    {
      "targetLanguage":"fr",
      "translatedText":"Traduire ce texte en utilisant la plate-forme du client"
    }
  ],
  "translator":"Microsoft",
  "detectedLanguage":{"code":"en","name":"en"}
}
```

This example shows a client script that throws an error when an invalid target language is passed in.

```
DynamicTranslation.getTranslation("Translate this text using platform from client", {
  "targetLanguages": ["123"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});

```

Response:

```
{"code":"40054","message":"Target language is invalid"}
```

This example shows the translation of plain text content from English \(detected\) into French and Italian using Microsoft's translation service in a Service Portal widget client script. Note that the name of the class is `dynamicTranslation` not `DynamicTranslation`.

```
dynamicTranslation.getTranslation("Translate this text using platform from client", {
  "targetLanguages": ["fr", "it"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});

```

Response:

```

{"translations":[
    {
      "targetLanguage":"it",
      "translatedText":"Tradurre questo testo utilizzando la piattaforma dal client"
    },
    {
      "targetLanguage":"fr",
      "translatedText":"Traduire ce texte en utilisant la plate-forme du client"
    }
  ],
  "translator":"Microsoft",
  "detectedLanguage":{"code":"en","name":"en"}
}
```

This example shows a Service Portal widget client script that throws an error when an invalid target language is passed in

```
dynamicTranslation.getTranslation("Translate this text using platform from client", {
  "targetLanguages": [123],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});

```

Response:

```
{"code":"40054","message":"Target language is invalid"}
```

## DynamicTranslation - getTranslations\(Array texts, Object parms\)

Translates the passed in text strings to one or more languages.

The method uses translation services, such as Microsoft Azure Translator Service and Google Cloud Translator Service, to perform the translation. If you do not pass in translation parameters, the method uses the system default.

When calling this method from a portal client script, use the class name dynamicTranslation; such as dynamicTranslation.getTranslations\(\). When calling it from a platform client script, use the class name DynamicTranslation; such as DynamicTranslation.getTranslations\(\).

<table id="table_bzb_4zk_thb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

texts

</td><td>

Array

</td><td>

List of text stings to translate.

</td></tr><tr><td>

parms

</td><td>

Object

</td><td>

Optional. JSON object that contains additional translation parameters.```
"parms": {
  "additionalParameters": {Object},
  "sourceLanguage": "String",
  "targetLanguages": [Array],
  "translator": "String"
}
```

</td></tr><tr><td>

parms.additionalParameters

</td><td>

Object

</td><td>

Optional. Array of JSON objects. Each object contains key-value pairs that provide additional information for performing the translation.```
"additionalParameters": {
  "parameterName": "String",
  "parameterValue": "String"
}
```

</td></tr><tr><td>

parms.additionalParameters.parameterName

</td><td>

String

</td><td>

Optional. Key name.Valid values:

textype: Type of text to translate. For Microsoft Azure Translator Service only.

</td></tr><tr><td>

parms.additionalParameters.parameterValue

</td><td>

String

</td><td>

Optional. Value of the associated key.Valid values:

-   html: HTML text string
-   plain: Standard text string

Default: plain

</td></tr><tr><td>

parms.sourceLanguage

</td><td>

String

</td><td>

Optional. Language code of the source text.Default: Translation service detects the source language.

</td></tr><tr><td>

parms.targetLanguages

</td><td>

Array

</td><td>

Optional. List of language codes to use to translate the text. The method returns translated text for each language code.Default: User preferred language.

</td></tr><tr><td>

parms.translator

</td><td>

String

</td><td>

Optional. Translation service to use to translate the text \(not case-sensitive\).Valid values:

 -   Google
-   Microsoft
-   IBM
-   &lt;custom&gt;

 **Note:** To use custom translation services you must first configure the translation service in your instance. For details, see [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

 Default: Translation service configured in the Translator Configuration \[sn\_dt\_translator\_configuration\] table.

</td></tr></tbody>
</table><table id="table_czb_4zk_thb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td id="status-entry-dynTran">

Status of the response to the method call.Possible values:

-   Error
-   Partial
-   Success

Data type: String

</td></tr><tr><td>

translations

</td><td>

List that describe the language translations.Data type: Array

```
translations": [
  {
    "isError": Boolean;
    "detectedLanguage": {Object},
    "textTranslations": [Array]
  }
]
```

</td></tr><tr><td>

translations.isError

</td><td>

Flag that indicates whether the translation of the text resulted in an error.Valid values:

-   true: Error encountered.
-   false: Text translation was successful.

 Data type: Boolean

</td></tr><tr id="detections_detectedLanguage-row-dynTran"><td>

translations.detectedLanguage

</td><td>

Description of the detected language.Data type: Object

```
"detectedLanguage": {
  "code": "String",
  "name": "String"
}
```

</td></tr><tr id="detections_detectedLanguage_code-row-dynTran"><td>

translations.detectedLanguage.code

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr id="detections_detectedLanguage_name-row-dynTran"><td>

translations.detectedLanguage.name

</td><td>

Language code of the detected language.Data type: String

</td></tr><tr><td>

textTranlations

</td><td>

Description of the language used to translate the text string.Data type: Array of Objects

```
"textTranslation": {
  "targetLanguage": "String",
  "translatedText": "String"
}
```

</td></tr><tr><td>

textTranslations.targetLanguage

</td><td>

Language code to which the source text was translated.Data type: String

</td></tr><tr><td>

textTranslations.translatedText

</td><td>

Translated text.Data type: String

</td></tr><tr id="translator-row-dynTran"><td>

translator

</td><td>

Translation service used to translate the text.Data type: String

</td></tr><tr><td>

Error messages

</td><td>

The following are error messages that the method may return and indications as to their root cause. -   Text \("text" field\) is missing or invalid. \(40000\): The text to translate is either missing or not a string.
-   Dynamic Translation plugin is not installed. \(40001\): The Dynamic Translation API was invoked without activating the com.glide.dynamic\_translation plugin. For information on activating this plugin, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Default translator is not configured for translation. \(40002\): No translation service is selected as the default translation service in the Translator Configurations. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator \("translator" field\) is invalid. \(40003\): The passed in **translator** parameter is not a string.
-   &lt;translator&gt; translator is not configured. \(40004\): The specified translation service is not configured in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   &lt;translator&gt; translator is inactive. \(40005\): The specified translation service is not set to **Active** in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Additional parameters are invalid. \(40006\): The additional parameters that were passed are not an object.
-   Target languages \("targetLanguages" field\) are invalid. \(40007\): The **targetLanguages** parameter is passed in the call but is not valid for one of the following reasons:

    -   Value isn't an array
    -   Array is empty
    -   One or multiple of the entries is not a string
-   Source language \("sourceLanguage" field\) is invalid. \(40008\): The **sourceLanguage** parameter is passed in the call but the value is not a String.
-   Maximum time limit has been exceeded. \(40009\): The operation took longer than the defined timeout value specified in the Translation Configuration. Default: 40 seconds
-   Request failed with multiple errors. \(40010\): Multiple errors occurred in the language detection call. For more information, refer to the response for each individual text string.
-   &lt;translator&gt; translator is not configured for translation. \(40012\): The specified translation service is not configured for text translation in the Translator Configuration. For information on creating/modifying a translator configuration, see [Create a translator configuration](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Translator configuration version is invalid. Migrate to v3. \(40014\): The associated version of the Translator Configuration for the specified translation service does not support the specified text translation method. For more information, see [Migrate to version v3 of a translator configuration](https://www.servicenow.com/docs/access?context=migrate-v3-dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Unknown error occurred. \(40051\): Default error thrown when the error doesn't fall in to any other category.
-   Text \("text" field\) has exceeded its maximum length. \(40052\): The text that was passed in to translate exceeds the maximum length supported by the corresponding translation service.
-   Source language is invalid. \(40053\): The passed in **sourceLanguage** parameter contains a language code that is not supported by the corresponding translation service.
-   Target language is invalid. \(40054\): One or more of the language codes passed in the **targetLanguages** parameter is not supported by the corresponding translation service.
-   Request is not authorized because credentials are missing or invalid \(40055\): The credentials configured for the translation service in Connections &amp; Credentials are not valid. For information on connections and credentials, see [Dynamic translation overview](https://www.servicenow.com/docs/access?context=dynamic-translation&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Text cannot be translated to target languages. \(40056\): The specified translation service is not able to translate the passed in text into the specified target languages.

</td></tr></tbody>
</table>This example shows code in a portal client script that translates a list of text strings into French and Italian using the Microsoft translation service.

```
dynamicTranslation.getTranslations(["Translate first text using portal from client", "Translate second text using portal from client"], {
  "targetLanguages": ["fr", "it"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});
```

Response:

```
{
  "translations":[
    {
      "isError":false,
      "textTranslations":[
        {
          "targetLanguage":"it",
          "translatedText":"Tradurre il primo testo utilizzando il portale dal client"
        },
        {
          "targetLanguage":"fr",
          "translatedText":"Traduire le premier texte à l'aide du portail à partir du client"
        }
      ],
      "detectedLanguage": {"name":"en", "code":"en"}
    },
    {
      "isError":false,
      "textTranslations":[
        {
          "targetLanguage":"it",
          "translatedText":"Traduci il secondo testo utilizzando il portale dal client"
        },
        {
          "targetLanguage":"fr",
          "translatedText":"Traduire le deuxième texte à l'aide du portail à partir du client"
        }
      ],
      "detectedLanguage": {"name":"en", "code":"en"}
    }
  ],
  "translator":"Microsoft",
  "status":"Success"
}
```

This example shows a portal client script that returns a Partial status when one of the two passed in text strings is invalid. To use this code example for a platform client script, change `dynamicTranslation.getTranslations` to `DynamicTranslation.getTranslations`.

```
dynamicTranslation.getTranslations(["Translate first text using portal from client", ""], {
  "targetLanguages": ["fr", "it"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": "Microsoft"
 }).then(function(res){console.log(res);}, function(res){console.log(res);});
```

Response:

```
{
  "translations":[
    {
      "isError":false,
      "textTranslations":[
        {
          "targetLanguage":"it",
          "translatedText":"Tradurre il primo testo utilizzando il portale dal client"
        },
        {
          "targetLanguage":"fr",
          "translatedText":"Traduire le premier texte à l'aide du portail à partir du client"
        }
      ],
      "detectedLanguage":{"name":"en", "code":"en"}
    },
    {
      "isError":true,
      "code":"40000",
      "message":"Text is missing or invalid"
    }
  ],
 "translator":"Microsoft",
 "status":"Partial"
}
```

This example shows a portal client script that throws an error when an invalid translation service is passed in. To use this code example for a platform client script, change `dynamicTranslation.getTranslations` to `DynamicTranslation.getTranslations`.

```
dynamicTranslation.getTranslations(["Translate first text using portal from client", "Translate second text using portal from client"], {
  "targetLanguages": ["fr", "it"],
  "additionalParameters": [{
    "parameterName": "texttype",
    "parameterValue": "plain"
  }],
  "translator": 123
 }).then(function(res){console.log(res);}, function(res){console.log(res);});
```

Response:

```
{"code":"40003","message":"Translator (\"translator\" field) is invalid","status":"Error"}
```

## DynamicTranslation - isEnabled\(String translator\)

Determines whether the various methods in the DynamicTranslation API are enabled for a translation service.

If you pass in a specific translation service, the method checks the method activation for that translation service; otherwise the method checks the default translation service.

When calling this method from a portal client script, use the class name dynamicTranslation; such as dynamicTranslation.isEnabled\(\). When calling it from a platform client script, use the class name DynamicTranslation; such as DynamicTranslation.isEnabled\(\).

<table id="table_qx5_nwl_thb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

translator

</td><td>

String

</td><td>

Optional. Translation service to use to verify whether the methods are active. Translation services are configured under the Translator Configuration menu.Possible values - not case-sensitive:

-   Google
-   Microsoft
-   IBM
-   &lt;custom&gt;

**Note:** To use custom translation services you must first configure the translation service in your instance. For details, see [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Default: Default translation service.

</td></tr></tbody>
</table><table id="table_rx5_nwl_thb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

batchDetection

</td><td>

Flag that indicates whether the getDetectedLanguages\(\) method is enabled.Possible values:

-   false: Disabled
-   true: Enabled

Data type: Boolean

</td></tr><tr><td>

batchTranslation

</td><td>

Flag that indicates whether the getTranslations\(\) method is enabled.Possible values:

-   false: Disabled
-   true: Enabled

Data type: Boolean

</td></tr><tr><td>

detection

</td><td>

Flag that indicates whether the getDetectedLanguage\(\) method is enabled.Possible values:

-   false: Disabled
-   true: Enabled

Data type: Boolean

</td></tr><tr><td>

translation

</td><td>

Flag that indicates whether the getTranslation\(\) method is enabled.Possible values:

-   false: Disabled
-   true: Enabled

Data type: Boolean

</td></tr><tr><td>

Error messages

</td><td>

The following are error messages that the API may return and indications as to their root cause.-   Translator \("translator" field\) is invalid. \(40003\): The passed in **translator** parameter is not a string.

</td></tr></tbody>
</table>This example shows a client script that checks whether the DynamicTranslation methods are enabled for the Microsoft translation service. To use this code example for a platform client script, change `DynamicTranslation.getTranslations` to `dynamicTranslation.getTranslations`.

```
DynamicTranslation.isEnabled('Microsoft').then(function(res){console.log(res);}, function(res){console.log(res);});
```

Output:

```
{"detection":true,"batchTranslation":true,"batchDetection":true,"translation":true}
```

This example shows a client script that throws an error when an invalid translation service is passed in. To use this code example for a platform client script, change `DynamicTranslation.getTranslations` to `dynamicTranslation.getTranslations`.

```
DynamicTranslation.isEnabled(123).then(function(res){console.log(res);}, function(res){console.log(res);});
```

Output:

```
{"code":"40003","message":"Translator (\"translator\" field) is invalid"}
```

