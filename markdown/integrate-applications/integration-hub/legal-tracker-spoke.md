---
title: Legal Tracker Spoke
description: Legal Tracker spoke enables a seamless integration of the Thomson Reuters Legal Tracker application with a ServiceNow instance to enable legal departments to create matters for Outside Firm and Outside Counsel Engagements and to track spends.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Legal Tracker Spoke

Legal Tracker spoke enables a seamless integration of the Thomson Reuters Legal Tracker application with a ServiceNow® instance to enable legal departments to create matters for Outside Firm and Outside Counsel Engagements and to track spends.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Legal Tracker spoke v1.0.2 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow® IntegrationHub Action Step — REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow® IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow® IntegrationHub Action Template — Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

Legal Tracker API \(REST API v1\)

## Spoke actions

Legal Tracker provides actions to automate the tasks in the following table when events occur in your ServiceNow instance.

**Note:** To avoid unauthorized access, make sure that the required users have the least privileges for the spoke actions.

|Category|Action|Description|
|--------|------|-----------|
|User Management|Look up Users Stream|Retrieves all users in the current company.|
|Company List|Look up Companies Stream|Retrieves a list of companies accessible to current user.|
|Location Management|Look up Countries Stream|Queries for countries based on an OData filter query.|
|Data Warehouse Access Management|Look up Organizational units Stream|Retrieves all Organizational units.|
|Look up Practice groups Stream|Retrieves all Practice Groups.|
|Look up Substantive law Stream|Retrieves all Substantive Laws.|
|Accounts Payable Data Exchange Management|Look up AP Routes Stream|Retrieves all AP Routes available for user.|
|Matter Management|Create Matter|Creates a matter record on the Legal Tracker application.|
|Look up Matter status|Retrieves the existing status for a matter by the matter ID.|
|Look up Matter Budgets|Retrieves information about a matter budget identified by the matter ID, source, firmID, and firmType.|
|Look up Matters Stream|Retrieves a list of matters.|
|Look up Matter by ID|Retrieves information about a matter by Matter ID.|
|Look up Templates|Retrieves a list of matter templates.|
|Look up Template Types|Retrieves a list of types for matter template.|
|Look up Matter Fields by ID|Retrieves a Matter Field by Field ID.|
|Look up Matter Financials|Retrieves the total spending and budget information for a matter in the matter's configured currency.|

## Spoke user roles

The Legal Tracker Spoke user \[sn\_legal\_trckr\_spk.user\] is available when the Legal Tracker spoke is installed. The role is required for users accessing Legal Tracker.

## Legal Tracker online account requirements

The Legal Tracker spoke requires a Legal Tracker account to generate OAuth 2.0 tokens.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Legal Tracker spoke](../task/setup-legal-tracker-spoke.md#).

