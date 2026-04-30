---
title: XTM Translation Management System spoke
description: The XTM Translation Management System spoke provides subflows and actions to localize the artifacts using the XTM translation management system service.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# XTM Translation Management System spoke

The XTM Translation Management System spoke provides subflows and actions to localize the artifacts using the XTM translation management system service.

Activate the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) to activate the XTM Translation Management System Spoke for localization Framework \(com.glide.localization\_framework.xtm\_spoke\).

## Subscription

The XTM TMS spoke requires any ServiceNow subscription that is Standard or above and includes the Localization Framework.

## Supported versions

Version v1.

## Spoke Subflows

The spoke provides subflows in the Published state to integrate with the XTM TMS service. These subflows can be used as part of other subflows and flows.

|Subflow|Description|
|-------|-----------|
|Request Translations \[request\_translations\]|Contains set of inputs and outputs to request translations of the artifacts.|
|Retrieve Translations \[retrieve\_translations\]|Contains set of inputs and outputs to retrieve translations of the translated artifacts.|

## Spoke actions

The spoke provides actions to integrate with the XTM TMS service.

|Action|Description|
|------|-----------|
|Create Project \[create\_project\]|Creates a project on XTM for translation.|
|Get Project Details \[get\_xtm\_tms\_project\_details\]|Fetches the project's details for the translation request.|
|Get Translated File \[get\_translated\_file\_from\_xtm\_tms\]|Fetches the translated file from XTM TMS after translations.|

## XTM Translation Management System account requirements

Ensure that you are registered with XTM TMS and obtain the credential information. For more information, see [XTM](https://go.xtm.cloud/ServiceNow) documentation.

## Connection and Credential alias requirements

The IntegrationHub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Connections and Credentials Information](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

To use the spoke connection aliases, use an associated connection record and a credential record created with the XTM TMS spoke installation.

This spoke uses the XTM TMS alias \(sn\_xtm\_spoke.XTM\_TMS\) to authorize actions.

The following are the connection alias requirements.

-   Connection type: HTTP
-   Connection URL: For example, `https://languagecloud.sdl.com`. This is a sample URL. Users can have a different URL based on their geographical preference.

See [Configure XTM TMS in the Localization Framework](../task/configure-xtm-tms.md) to connect to the XTM TMS services and use them to localize the artifacts.

**Parent Topic:**[Translation Management System configurations](tms-configuration.md)

