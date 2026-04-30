---
title: IBM Watson Language Translator Service spoke
description: With the Xanadu release, the IBM Watson Language Translator Service Spoke is no longer available because it has been deprecated. This information is provided for legacy context. The spoke provided subflows and actions to dynamically translate user-entered texts and to detect the language of user-entered texts using the IBM translation service.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2025-01-06"
reading_time_minutes: 2
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# IBM Watson Language Translator Service spoke

With the Xanadu release, the IBM Watson Language Translator Service Spoke is no longer available because it has been deprecated. This information is provided for legacy context. The spoke provided subflows and actions to dynamically translate user-entered texts and to detect the language of user-entered texts using the IBM translation service.

Integrate Dynamic Translation with IBM translation service.

**Important:** IBM announced the deprecation of the IBM Watson Translator Service for IBM Cloud in all regions. As of December 10, 2024, the service is withdrawn entirely and no longer available to any customers. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

## Activation

With the Xanadu release, the IBM Watson Language Translator Service Spoke is deprecated and is no longer available.

Before deprecation, this spoke was activated with the Dynamic Translation plugin \(com.glide.dynamic\_translation\) or the IBM Watson Language Translator Service Spoke plugin \(com.glide.ibm\_translation\_spoke\).

## Subscription

This spoke required any ServiceNow subscription that is Professional or above, and includes Dynamic Translation.

## Supported versions

API version v3.

## Spoke subflows

The spoke provided subflows in the Published state to integrate with the IBM Watson Language translation services. These subflows could be used as part of other subflows and flows.

|Subflow|Description|
|-------|-----------|
|Detect Language \[detect\_language\_v3\]|Contains a set of inputs, actions, and output to detect the language of the input text.|
|Translate Text \[translate\_text\_v3\]|Contains a set of inputs, actions, and outputs to translate the input text to multiple languages.|

## Spoke actions

The spoke provided actions to integrate with IBM translation services.

|Action|Description|
|------|-----------|
|Detect Language \[detect\_language\_v3\]|Detects the language of the input text.|
|Translate Text \[translate\_text\_v3\]|Translates the input text to multiple languages.|

## IBM account requirements

For information on the IBM Language Translator API and the notice of deprecation, see the [IBM](https://cloud.ibm.com/apidocs/language-translator) documentation.

## Connection and credential alias requirements

IntegrationHub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

This spoke used the IBMTranslation alias \(sn\_ibm\_trans\_spoke.IBMTranslation\) to authorize actions.

The following were the connection alias requirements.

-   Connection type: HTTP
-   Connection URL: Base URL provided by IBM to connect to the language translator service. Users can have a different URL based on their geographical preference.

**Parent Topic:**[Integration with other translation services](integration-with-other-translation-services.md)

