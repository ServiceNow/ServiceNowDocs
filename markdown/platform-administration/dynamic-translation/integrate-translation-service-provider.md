---
title: Integrate with a translation service provider
description: Integrate with a third-party translation provider of your choice for machine translation of user-generated text.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-11-03"
reading_time_minutes: 4
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Integrate with a translation service provider

Integrate with a third-party translation provider of your choice for machine translation of user-generated text.

## Before you begin

-   Create an account with your third-party translation service provider, and obtain the connection and credentials needed for integration.
-   Role required: admin

## About this task

By default Dynamic Translation provides partially preconfigured translator records for several third party services. However, you can also create your own custom integration for a different service provider.

Custom integrations require you to create subflows for language detection and translation, including actions, in Workflow Studio.

Use default subflows as examples when you build your own subflows. For example:

-   Detect Language \[detect\_language\_v4\]
-   Translate Text \[translate\_text\_v3\]

For background information, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) and [Migrate customized Translator Configurations to v4 flows](migrate-v4-dynamic-translation.md).

## Procedure

1.  Confirm your application scope, then navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**, and select **New**.

    To map error codes try using actions in subflows. For example, the Translate Text subflow has a Translate Text action. On that action, you can select **Open in Action Designer**. In the **Action Outline** section of the Action Designer, you can select **Error Evaluation**. You can overwrite the default error status that a step produces at runtime by entering new status code and status message values. See [Action error evaluation](https://www.servicenow.com/docs/access?context=action-error-evaluation&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    1.  Map error codes from your machine translation provider to the error codes and standardized error messages supported by ServiceNow.

        |Error code|Error message|
        |----------|-------------|
        |40050|Error code to populate error messages from the machine translation provider instead of standardized error messages.|
        |40051|Unknown error occurred.|
        |40052|Text \('text' field\) has exceeded its maximum length.|
        |40053|Source language is invalid.|
        |40054|Target language is invalid.|
        |40055|Request is not authorized because credentials are missing or invalid.|
        |40056|Text cannot be translated to target languages.|

    2.  Ensure that the inputs and output fields are in the following format for subflows.

<table id="table_z5q_q5t_23b"><thead><tr><th>

Field name

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Inputs

</td></tr><tr><td>

texts

</td><td>

Input texts whose language should be detected.Version v3 supports bulk detection \(detection of multiple texts input in a single string\). With the Xanadu Patch 3 release, version v4 supports [Exclusion Framework](../concept/dyn-translation-exclusion-framework.md) as well as bulk detection.

</td><td>

Array.String

</td></tr><tr><td class="sub-head" colspan="3">

Outputs

</td></tr><tr><td>

detections

</td><td>

Information about the code and confidence of the languages detected by the translator and their respective alternatives, error codes, and error messages.-   Code: Language code of the detected language as specified by the translation service provider.
-   Confidence: Value that indicates the confidence in the result. The value is between zero and one. A low value indicates a low confidence.
 For example, French text with confidence of 0.93

```
{ 'code' : 'fr',  'confidence' : '0.93'  }
```

 For more information refer to the getDetectedLanguages section of [DynamicTranslation - Scoped](https://www.servicenow.com/docs/access?context=DynamicTranslation&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td><td>

Array.Object. Each element of the Object is a String value.

</td></tr><tr><td>

status

</td><td>

Status of the request.

</td><td>

Choice

</td></tr></tbody>
</table><table id="table_cgx_ntt_23b"><thead><tr><th>

Field name

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Inputs

</td></tr><tr><td>

texts

</td><td>

Texts to be translated.Version v3 and above support bulk translation \(translation of multiple texts input in a single string\).

</td><td>

Array.String

</td></tr><tr><td>

target\_languages

</td><td>

Array of language codes to which the text needs to be translated.For example,

```
['fr','it']
```

</td><td>

Array String. Each element of the array is a String value.

</td></tr><tr><td>

source\_language

</td><td>

Language code of the source text.For example,

```
en
```

</td><td>

String

</td></tr><tr><td>

additional\_parameters

</td><td>

Array of additional parameters. For example,

```
[{'parameter_name': 'textType', 'parameter_value': 'html'}]
```

</td><td>

Array.Object. Each element of the array is an Object with String values.

</td></tr><tr><td class="sub-head" colspan="3">

Outputs

</td></tr><tr><td>

translations

</td><td>

Translated texts in the specified target languages. Each element of the array is an Object containing target language and the translated text.For example,

```
[ 
{'target_language':'fr', 'translated_text':'Bonjour'}, 
{'target_language':'it', 'translated_text':'ciao'} 
]

```

 For more information refer to the getTranslations section of [DynamicTranslation - Scoped](https://www.servicenow.com/docs/access?context=DynamicTranslation&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

</td><td>

Array.Object. Each element of the array is an Object with String values.

</td></tr><tr><td>

status

</td><td>

Status of the request.

</td><td>

Choice

</td></tr></tbody>
</table>        **Note:** Ensure that the **Run As** field is set to **User who initiates session** in the flow properties.

2.  [Create a custom translator configuration](create-custom-translator.md) for your service provider in the Translator Configurations table, and set the record to active.

    When you create the record in the Translator Configurations table, search for the subflows you created in the previous step..

3.  If your instance is on Xanadu Patch 3 or higher, and you intend to use Exclusion Framework, enter your translation provider's exclusion tags in the Exclusion Provider Pattern table.

    Refer to your provider's documentation to obtain these tags. For more information about entering the tags, see [Add an Exclusion Provider Pattern](dyn-translation-exclusion-provider.md).

4.  Create a language code mapping to associate your provider's language codes to ServiceNow language codes.

    For more information, see [Create a language code mapping](create-language-code-mapping.md).


## What to do next

For information about APIs, see [DynamicTranslation API](../concept/dyn-translation-apis.md).

-   **[Create a custom translator configuration](create-custom-translator.md)**  
Configure Dynamic Translation for a third-party machine translation provider of your choice.

**Parent Topic:**[Integration with other translation services](../concept/integration-with-other-translation-services.md)

