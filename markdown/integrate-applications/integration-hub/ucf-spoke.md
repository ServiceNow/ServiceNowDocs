---
title: UCF Spoke
description: Manage processes to collect and coordinate the compliance requirements applicable to your organization from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# UCF Spoke

Manage processes to collect and coordinate the compliance requirements applicable to your organization from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

UCF spoke v1.1.0 is the latest version.

## Supported version

This spoke was built for UCF v2.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke requirements

-   Common Control Hub \(CCH\) account
-   CCH administrator credentials

## Spoke actions

The UCF spoke provides actions to automate UCF tasks when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Content Record Management|Get Authority Documents|Retrieves authority documents that are downloaded from the UCF Common Controls Hub.|
|Get Citation Control Objective Mapping|Retrieves the Citation and Control objective mapping information.|
|Get Citation Documents|Retrieves the citations that are downloaded from the UCF Common Controls Hub.|
|Get Control Objective Documents|Retrieves the citation to controls that are downloaded from the UCF Common Controls Hub.|
|Metadata Retrieval|Get Authority Document List|Retrieves the current user's authority document lists.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the UCF spoke](../task/setup-ucf-spoke.md#).

