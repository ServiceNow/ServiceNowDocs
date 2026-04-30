---
title: Atlassian Administration Spoke
description: The Atlassian Administration spoke provides actions to view and analyze meaningful usage data for Atlassian Administration subscriptions. The spoke downloads subscription information and usage, pulls group details, and removes users from a group.Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Atlassian Administration Spoke

The Atlassian Administration spoke provides actions to view and analyze meaningful usage data for Atlassian Administration subscriptions. The spoke downloads subscription information and usage, pulls group details, and removes users from a group.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Atlassian Administration v1, but may be compatible with later versions.

## Spoke requirements

-   Atlassian Administration account
-   Atlassian Administration Role required: Organization admin
-   API Key to authenticate the ServiceNow instance.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Workflow Studio - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

## Spoke subflows

The Atlassian Administration spoke provides sample subflows to demonstrate automating Atlassian Administration tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Pull Atlassian Group Details|This subflow retrieves all Group Details from Atlassian Administration such as group product and site details.|

## Spoke actions

The Atlassian Administration spoke provides actions to automate Atlassian Administration tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Group Management|Look up Organization Groups Stream|Retrieves information about groups, users, and roles assignments.|
|User Management|Look up Organization Users Stream|Retrieves information about users, groups, and product last access.|
|Remove User from Group|Removes given user from a group in the Atlassian Administration instance.|

## Spoke module

The Atlassian Administration spoke adds the Atlassian Administration application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Groups|Contains data related to groups.|
|Product and Site Details|Contains data related to product and site.|
|Group Product Site Role Details|Contains data related to site roles for product groups.|

## Spoke user roles

The Atlassian Administration spoke provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
|Atlassian Admin \(sn\_atlassian\_spoke.atlassian\_admin\)|Creates connections for the Atlassian Administration application.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.



