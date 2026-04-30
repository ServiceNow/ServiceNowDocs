---
title: Custom licensing for ISV applications
description: Monitor the usage of ISV applications with Subscription Management. Create a definition for your store application with the metadata you want collected. After publishing the application with the definition to the store, Usage Analytics runs and aggregates your defined metrics.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Custom licensing for ISV applications

Monitor the usage of ISV applications with Subscription Management. Create a definition for your store application with the metadata you want collected. After publishing the application with the definition to the store, Usage Analytics runs and aggregates your defined metrics.

## Overview of custom licensing

Applications that you create with the can be published to the ServiceNow Store. Monitor the usage of your applications with custom licensing.

You can use custom licensing on ISV applications that you publish to the ServiceNow Store if they meet the following criteria:

-   The application is licensable.
-   The application is not scoped in ServiceNow or Global.
-   The application has a capacity subscription model.

Custom licensing functions through the usage analytics \(com.glide.usageanalytics\) and scoped app author \(com.sn\_appauthorr\) plugins. These plugins are active by default in the App Engine. Additionally, your instance must be connected to an application repository or application store instance.

## Custom license definitions

Custom licensing is achieved by creating a definition. A definition is a set of licensing metrics that you define based on what usage information you want to collect for your application. See [Create a definition for your store application](../task/create-definition-store-apps.md).

-   **[Create a definition for your store application](../task/create-definition-store-apps.md)**  
Create a definition for your store app to define the licensing metrics you want collected.

**Parent Topic:**[Application sharing](c_SharingApplications.md)

