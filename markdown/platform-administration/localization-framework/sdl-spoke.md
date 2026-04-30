---
title: RWS Translation Management System spoke
description: The RWS Translation Management System spoke provides subflows and actions to localize the artifacts using the RWS translation management system service.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2025-04-10"
reading_time_minutes: 2
breadcrumb: [Translation Management System configurations, Localization Framework settings, Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# RWS Translation Management System spoke

The RWS Translation Management System spoke provides subflows and actions to localize the artifacts using the RWS translation management system service.

Activate the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\) to activate the RWS Translation Management System Spoke for Localization Framework \(com.glide.localization\_framework.rws\_spoke\).

## Subscription

The RWS TMS spoke requires any ServiceNow subscription that is Standard or above and includes the Localization Framework.

## Supported versions

Version v1.

## Spoke Subflows

The spoke provides subflows in the Published state to integrate with the RWS TMS service. These subflows can be used as part of other subflows and flows.

|Subflow|Description|
|-------|-----------|
|Request Translations \[request\_translations\]|Contains set of inputs and outputs to request translations of the artifacts.|
|Retrieve Translations \[retrieve\_translations\]|Contains set of inputs and outputs to retrieve translations of the translated artifacts.|

## Spoke actions

The spoke provides actions to integrate with the RWS TMS service.

|Action|Description|
|------|-----------|
|Create Project \[create\_project\_on\_sdl\]|Creates a project on RWS for translation.|
|Get Project Details \[get\_sdl\_project\_details\]|Fetches the project's details for the translation request.|
|Get Translated File \[get\_translated\_file\_from\_sdl\]|Fetches the translated file from RWS TMS after translations.|
|Mark File As Complete \[complete\_file\_on\_sdl\]|Marks the file as complete, after getting the translated content.|
|Upload File \[upload\_file\_on\_sdl\_tms\]|Sends a file to RWS for translations.|

## RWS Translation Management System account requirements

Ensure that you are registered with RWS TMS and obtain the credential information. For more information on RWS Managed Translation API, see [RWS](https://www.rws.com) documentation.

## Connection and Credential alias requirements

The IntegrationHub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you do not need to update any actions that use the connection. For more information, see [Connections and Credentials Information](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

To use the spoke connection aliases, use an associated connection record and a credential record created with the RWS spoke installation.

This spoke uses the RWS TMS alias \(sn\_sdl\_spoke.RWS\_TMS\) to authorize actions.

The following are the connection alias requirements.

-   Connection type: HTTP
-   Connection URL: For example, `https://languagecloud.sdl.com`. This is a sample URL. Users can have a different URL based on their geographical preference.

See [Configure RWS TMS in the Localization Framework](../task/configure-sdl-tms.md) to connect to the RWS TMS services and use them to localize the artifacts.

**Parent Topic:**[Translation Management System configurations](tms-configuration.md)

