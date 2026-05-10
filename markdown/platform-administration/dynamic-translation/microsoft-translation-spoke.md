---
title: Microsoft Azure Translator Service spoke
description: Microsoft Azure Translator Service spoke provides subflows and actions to detect and translate user-entered text, using the Microsoft machine translation service. Dynamic Translation supports detection and translation of single texts and multiple texts.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Microsoft Azure Translator Service spoke

Microsoft Azure Translator Service spoke provides subflows and actions to detect and translate user-entered text, using the Microsoft machine translation service. Dynamic Translation supports detection and translation of single texts and multiple texts.

Configure Microsoft as a third-party machine translation provider in the Dynamic Translation app. 

## Activation

Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) or the Microsoft Azure Translator Service Spoke plugin \(com.glide.microsoft\_translation\_spoke\).

## Subscription

This spoke requires any ServiceNow subscription that is Professional or above, and includes Dynamic Translation.

## Supported versions

API version v3 and v4.

## Spoke subflows

The spoke provides subflows in the Published state to integrate with Microsoft translation service. These subflows can be used as part of other subflows and flows.

|Subflow|Description|
|-------|-----------|
|Detect Language \[detect\_language\_v3\]|Contains a set of inputs, actions, and output to detect the language of the input text. Releases before Xanadu Patch 3 use v3 flows.|
|Detect Language V4 \[detect\_language\_v4\]|Contains a set of inputs, actions, and output to detect the language of the input text. Releases from Xanadu Patch 3 use v4 flows. For more information about v4 flows, see [Migrate customized Translator Configurations to v4 flows](../task/migrate-v4-dynamic-translation.md).|
|Translate Text \[translate\_text\_v3\]|Contains a set of inputs, actions, and outputs to translate the input text to multiple languages. This subflow uses v3 for releases before and after Xanadu Patch 3.|

## Spoke actions

The spoke provides actions to integrate with Microsoft translation services.

|Action|Description|
|------|-----------|
|Detect Language \[detect\_language\_v3\]|Detects the language of the input text.|
|Translate Text \[translate\_text\_v3\]|Translates the input text to multiple languages.|

## Microsoft account requirements

Ensure that you are registered with Microsoft and obtain the credential information. For more information, see [Microsoft](https://docs.microsoft.com/en-in/) documentation.

For information on Microsoft Translator Text API, see the [Microsoft](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/) documentation.

## Connection and credential alias requirements

IntegrationHub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Credentials and connection information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

To use the spoke connection aliases, create an associated connection record and a credential record for each alias.

This spoke uses the MicrosoftTranslation alias \(sn\_ms\_trans\_spoke.MicrosoftTranslation\) to authorize actions.

The following are the connection alias requirements.

-   Connection type: HTTP
-   Connection URL: For example, `https://api.cognitive.microsofttranslator.com`.

    **Note:** The URL provided here is a sample only. Microsoft translation customers may need to use custom API URLs or virtual network type API URLs, even when they do not subscribe to a virtual network. Microsoft customers who use multi-service or regional translation services also need to know their Ocp-Apim-Subscription-Region attribute, and their API URL may contain a regional reference. Check your Azure portal for this information. Refer to the [Microsoft](https://learn.microsoft.com/en-us/azure/ai-services/translator/reference/v3-0-reference) documentation for further details.


Perform the following tasks to connect to the Microsoft machine translation service.

1.  [Create a credential for the MicrosoftTranslation alias](../task/create-credential-ms-translation.md)  
Authorize actions of Microsoft Azure Translator Service spoke by creating a credential for the MicrosoftTranslation connection and credential alias.
2.  [Create a connection for the MicrosoftTranslation alias](../task/create-connection-ms-translation.md)  
Connect to the Microsoft translation service by creating a connection. Provide information that is used by HTTP\(s\) actions or activities to connect to that service.
3.  [Activate the Microsoft translator configuration](../task/activate-ms-translator-config.md)  
Make the Microsoft translation service available for use by activating the Microsoft translator configuration.

**Parent Topic:**[Integration with other translation services](integration-with-other-translation-services.md)

