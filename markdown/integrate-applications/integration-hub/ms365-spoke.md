---
title: Microsoft Dynamics 365 Spoke
description: Use Microsoft Dynamics 365 spoke to manage users and activities in Dynamics 365.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Microsoft Dynamics 365 Spoke

Use Microsoft Dynamics 365 spoke to manage users and activities in Dynamics 365.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Microsoft Graph: v1.0 and Microsoft Dynamics 365: v9.0, but may be compatible with later versions.

## Spoke version

Microsoft Dynamics 365 v1.0.8 is the latest version.

## Spoke requirements

-   Ensure that you have Global Administrator and Microsoft Dynamics 365 Administrator role in Microsoft Admin Centre.
-   You must create an OAuth 2.0 app in Azure AD and generate the OAuth 2.0 token.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Dynamics 365 spoke provides actions to automate Microsoft Dynamics 365 tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|User Management|Look up Users Stream|Retrieves all users in an organisation.|
|Look up Dynamics CRM Users Stream|Retrieves details of all users with access to Microsoft Dynamics CRM system.|
|Look up Dynamics Object Schema \(Dynamic\)|Retrieves the list of fields for the specified entity name to be used as dynamic input.|
|SKU Management|Look up Subscribed SKUs|Retrieves all subscriptions that an organization has acquired.|
|Audit Management|Look up Audit Log Stream|Retrieves all audit logs in the system.|
|Activity Pointer Management|Look up Activity Pointers Stream|Retrieves all the calendar activities performed.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Microsoft Dynamics 365](https://www.servicenow.com/docs/access?context=integrating-with-microsoft365&version=yokohama&pubname=yokohama-it-asset-management&section=setup-ms-dynamics-365&ft:locale=en-US) and [Set up Microsoft Azure Active Directory](https://www.servicenow.com/docs/access?context=integrating-with-microsoft365&version=yokohama&pubname=yokohama-it-asset-management&section=setup-ms-azure-ad&ft:locale=en-US).

This spoke requires the Integration Hub subscription. For details, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md)

## Supported versions

This spoke was built for Microsoft Graph: v1.0 and Microsoft 365 Dynamics: v9.0, but may be compatible with later versions.

## Spoke requirements

-   Ensure that you have Global Administrator and Microsoft Dynamics 365 Administrator role in Microsoft Admin Centre.
-   You must create an OAuth 2.0 app in Azure AD and generate the OAuth 2.0 token.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Microsoft Dynamics 365 spoke provides actions to automate Microsoft 365 tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|User Management|Look up Users Stream|Retrieves all users in an organisation.|
|SKU Management|Look up Subscribed SKUs|Retrieves all subscriptions that an organization has acquired.|
|Audit Management|Look up Audit Log Stream|Retrieves all audit logs in the system.|
|Activity Pointer Management|Look up Activity Pointers Stream|Retrieves all the calendar activities performed.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Microsoft Dynamics 365](https://www.servicenow.com/docs/access?context=integrating-with-microsoft365&version=yokohama&pubname=yokohama-it-asset-management&section=setup-ms-dynamics-365&ft:locale=en-US).

