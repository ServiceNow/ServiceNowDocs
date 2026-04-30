---
title: Mobile plugins
description: Learn about the plugins used to enable ServiceNow mobile on your instance.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Mobile plugins and upgrades, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile plugins

Learn about the plugins used to enable ServiceNow mobile on your instance.

## Core plugins

The following mobile plugins include the core functionality of ServiceNow mobile and the ability to interact with ServiceNow mobile apps. Plugins marked as base system plugins are automatically installed on your instance.

|Name|ID|Description|Base System|
|----|---|-----------|-----------|
|Mobile App Builder|sn\_mab|Enables the editing of mobile configurations via the Mobile App Builder.|Yes|
|Mobile App Builder API|sn\_mab\_api|API to enable the editing of mobile configurations via the Mobile App Builder.|Yes|
|Mobile Card Builder|sn\_mobile\_card\_bui|Enables the editing of mobile cards via the Mobile Card Builder.|Yes|
|ServiceNow Now Mobile app screens and launcher screens|sn\_me|Application and configurations required to setup the Now Mobile app.|No|

## Supporting plugins

These plugins are not required for ServiceNow mobile, but include extended functionality, such as offline mode, geolocation, and access to Virtual Agent.

|Name|ID|Description|Base System|
|----|---|-----------|-----------|
|SG Offline support|com.glide.sg.offline|Provides offline support for ServiceNow mobile.|No \(This plugin is automatically installed with the **Field Service Mobile** plugin\)|
|Service Management Geolocation|com.snc.service\_management.geolocation|Enables geolocation capabilities for Service Management|No \(This plugin is automatically installed with the **Field Service Mobile** plugin\)|
|Geolocation|com.snc.geolocation|Core geolocation capabilities|Yes|
|Glide Virtual Agent|com.glide.cs.chatbot|Virtual Agent platform and other necessary plugins|No|
|Mobile Publishing|com.glide.sn-mobile-whitelab|Enables you to publish secure and branded mobile applications that use your unique company identity and management method.|No|

## Activating plugins on your instance

Install a plugin by searching for the plugin name in you plugins list. For information on the plugin activation process, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Mobile plugins for Mobile Agent](sg-mobile-plugins-agent.md)**  
Use these plugins to extend functionality for the Mobile Agent app.
-   **[Mobile plugins for Now Mobile](sg-mobile-plugins-now.md)**  
Use these plugins to extend functionality for the Now Mobile app.

**Parent Topic:**[Mobile plugins and upgrades](../concept/plugins-upgrades.md)

