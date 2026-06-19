---
title: Recommended Actions for Service
description: Use Recommended Actions for Customer Service to display relevant actions to agents based on the context of a record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/ra-csm-configure.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Recommended Actions for Service

Use Recommended Actions for Customer Service to display relevant actions to agents based on the context of a record.

**Important:** Starting with v31.0, the Recommended Actions for Customer Service plugin has been renamed to Recommended Actions for Service.

The Recommended Actions for Service application displays recommendations for case records in CSM Configurable Workspace. Agents can take the actions provided by the recommendations to help customers and resolve their issues. Agents can also use this application to perform an AI search to find relevant resources.

The Recommended Actions for Service application provides predefined guidances and recommendation context records tailored for Customer Service Management. It also provides workspace configurations that automatically display recommended actions and search results in the contextual side panel.

For more information about recommended actions and AI search results, see [Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/configure-nba.md).

## Context records

The Recommended Actions for Service application provides context records for the Case and Interaction tables. A [context](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-contexts.md) enables agents to see recommendations for records from a specific table when certain rules are met.

-   [Case Context record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-context-records.md)
-   [Interaction Context record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-context-records.md)

## Guidances

The Recommended Actions for Service application includes custom guidances for the following tables:

-   [Knowledge](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-custom-guidances.md)
-   [Case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-custom-guidances.md)
-   [Incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-custom-guidances.md)
-   [Problem](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-custom-guidances.md)
-   [Change Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/ra-csm-custom-guidances.md)

These guidances enable search results from the corresponding search source tables for the Case Context record. Customer service agents can see these results in the Recommended Actions tab in the contextual side panel.

## Plugin

The Recommended Actions for Service application \(sn\_cs\_nb\_action\) is available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

This application has a dependency on the Recommended Actions application.

## Request apps from the ServiceNow Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

