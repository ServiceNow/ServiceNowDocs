---
title: Google Cloud Translator Service Spoke
description: Provides subflows and actions to dynamically translate the user-entered text, and to detect the language of the text using the Google translation service.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration with other translation services, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Google Cloud Translator Service Spoke

Provides subflows and actions to dynamically translate the user-entered text, and to detect the language of the text using the Google translation service.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription

This spoke requires one of the following subscriptions:

-   Any ServiceNow subscription that is Professional or above, and includes Dynamic Translation.
-   Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

See the [Google Cloud Translator Service Spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6b0f258a73623300395108b24ff6a734/) in ServiceNow Store.

## Supported versions

Google Translate API version v3.

## Scope of the spoke in the Dynamic Translation framework

To use Google Cloud Translator Service spoke in the Dynamic Translation framework, ensure that the spoke is installed in ServiceNow Store and the Dynamic Translation plugin is active. For more information, see [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md).

## Spoke flows

This spoke has no sample flows.

## Spoke subflows

The Google Cloud Translator Service spoke provides subflows in the Published state to integrate with the Google translation service. These subflows can be used as part of other subflows and flows.

|Subflow|Description|
|-------|-----------|
|Detect Language|Contains a set of inputs, actions, and outputs to detect the language of the input text.|
|Translate Text To Multiple Languages|Contains a set of inputs, actions, and outputs to translate the input text to multiple languages.|

## Spoke actions

The Google Cloud Translator Service spoke provides actions to integrate with the Google translation service. Available actions include:

|Action|Description|
|------|-----------|
|Detect Language|Detects the language of the input text.|
|Translate Text To Single Language|Translates the input text to a single language.|
|Translate Text To Multiple Languages|Translates the input text to multiple languages.|

## Google account requirements

The Google Cloud Translator Service spoke requires configuring your Google Cloud account to generate an OAuth 2.0 JWT Bearer Grant token.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

This spoke uses the GoogleTranslation alias record \(sn\_google\_trans.GoogleTranslation\) to authorize actions. For information about setting up the spoke, see [Set up the Google Cloud Translator Service spoke](../task/setup-google-translator.md).

-   **[Set up the Google Cloud Translator Service spoke](../task/setup-google-translator.md)**  
Integrate your Google account with your ServiceNow instance.

**Parent Topic:**[Integration with other translation services](../../dynamic-translation/concept/integration-with-other-translation-services.md)

