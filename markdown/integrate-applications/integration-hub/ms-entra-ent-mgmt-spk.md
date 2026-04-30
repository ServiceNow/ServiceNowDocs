---
title: Microsoft Entra Entitlement Management Spoke
description: Retrieves details of access packages and access package assignments in Microsoft Entra Entitlement Management from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Microsoft Entra Entitlement Management Spoke

Retrieves details of access packages and access package assignments in Microsoft Entra Entitlement Management from your ServiceNow instance.

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Microsoft Entra Entitlement Management v1.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Microsoft Entitlement Management account requirements

The Microsoft Entitlement Management spoke requires creating a custom app on your Microsoft Entra account to generate OAuth 2.0 tokens. See: [Create a custom application in Azure portal](../task/setup-entra-entitlement-spk.md#).

## Spoke actions

The Microsoft Entra Entitlement Management spoke provides actions to automate entitlement management tasks when events occurs in your ServiceNow instance. Available actions include:

**Note:** To use the actions, ensure that you provide at least one of the required permissions.

|Category|Action|Description|Permissions Required \(from least to most privileged\)|
|--------|------|-----------|------------------------------------------------------|
|Access Package Assignment Management|Look up Access Package Assignment|Retrieves the details of the specified access package assignment.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Look up Access Package Assignments Stream|Retrieves the list of all the assignments \(both active and expired\) that the caller has access to read, across all catalogs and access packages.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Look up Access Package Assignments Stream by User|Retrieves the list of all the assignments \(active and expired\) that the caller has access to read, across all catalogs and access packages where the signed-in user is the target. Signed-in user is the user whose Entra credentials were used while generating the token.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|Not supported|
|Access Package Management|Look up Access Package|Retrieves the details of the specified access package.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Look up Access Packages Stream|Retrieves the list of all access packages across all catalogs.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Look up Access Packages Stream by User|Retrieves the list of all access packages across all catalogs for which the signed-in user is allowed to submit access requests. Signed-in user is the user whose Entra credentials were used while generating the token.|Delegated \(work or school account\)|EntitlementManagement.Read.All, EntitlementManagement.ReadWrite.All|
|Delegated \(personal Microsoft account\)|Not supported|
|Application|Not supported|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

