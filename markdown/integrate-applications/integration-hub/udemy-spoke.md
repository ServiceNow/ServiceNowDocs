---
title: Udemy Spoke
description: Manage the courses on the Udemy platform from your ServiceNow instance. For example, get the details of all the courses on Udemy by executing a spoke action from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Udemy Spoke

Manage the courses on the Udemy platform from your ServiceNow instance. For example, get the details of all the courses on Udemy by executing a spoke action from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Udemy spoke v1.0.2 is the latest version.

## Supported versions

This spoke was built for Udemy API version v2, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation. To get help on the licenses, contact your account manager.

## Spoke actions

The Udemy spoke actions automate how you manage the courses on the Udemy platform. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Default|Look up Courses Stream|Gets the details of the courses on Udemy. For example, course length, description, video duration, and the course title.|
|Learning Management|Look up Course Synchronization Stream|Retrieves details of the courses. For example, course title, description, and duration. If the action is successfully executed, the status is "Success", or else, the status is "Failure" and an appropriate error code is shown.|
|Look up Course Synchronization Token|Retrieves the synchronization token to fetch the next set of updated or created course.|
|Look up User Course Activity Stream|Retrieves the data on the progress made by the course subscriber.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.

For information about setting up the spoke, see [Set up the Udemy spoke](../task/setup-udemy-spk.md#).

For information about setting up the spoke, see [Set up the Udemy spoke](../task/setup-udemy-spk.md#)

