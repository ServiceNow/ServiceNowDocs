---
title: Live Connect release notes
description: Live Connect \(formerly SQL API\) provides read-only SQL access to your ServiceNow tables through ODBC and JDBC drivers. You can write queries, build reports, and analyze data in your existing tools while your security controls continue to apply. See the following sections for release notes by version.Live Connect was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/live-connect-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Live Connect, SQL API, ODBC, JDBC, OAuth, analytics, Live Connect, SQL API, OAuth, ODBC, JDBC, Pyramid Analytics, authentication]
breadcrumb: [ServiceNow AI Platform capabilities release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Live Connect release notes

Live Connect \(formerly SQL API\) provides read-only SQL access to your ServiceNow® tables through ODBC and JDBC drivers. You can write queries, build reports, and analyze data in your existing tools while your security controls continue to apply. See the following sections for release notes by version.

## About Live Connect

-   Provides read-only SQL access to authorized tables through ODBC and JDBC drivers.
-   Enables direct queries from external analytics and business intelligence tools without data synchronization.
-   Supports OAuth authentication for secure, FedRamp-compliant connections.
-   Integrates with enterprise analytics platforms such as Pyramid Analytics, Power BI, and Tableau.

See [Access your ServiceNow data using Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.md) for more information.

## Activation and other requirements

-   **Activation information**

    Live Connect is a ServiceNow AI Platform capability that requires RaptorDB Professional and activation of the Live Connect plugin. Access is configured per user account \(service or personal\). To make tables available for querying, you must add the `egress_sql` access control to each table.

-   **Additional requirements**
    -   ODBC or JDBC drivers must be installed on client systems.
    -   User accounts must be configured with appropriate table access controls.

## Accessibility and localization

-   **Accessibility information**
    -   Live Connect is a backend connectivity layer with no direct user interface.
    -   Accessibility of query results depends on the third-party client tools used to connect to Live Connect.
-   **Localization information**

    Live Connect is operates independently of language settings. Data returned through Live Connect reflects the language settings of the queried tables.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## Brazil Early Availability

Live Connect was enhanced and updated in the Brazil release.

### What's new

-   **[Enable OAuth for Live Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/enable-oauth-for-live-connect.md)**

    Connect third-party ODBC and JDBC clients to ServiceNow using OAuth credentials to meet FedRamp compliance requirements and enable secure multi-factor authentication workflows. OAuth provides modern, encrypted authentication aligned with security standards and reduces credential exposure in transit.

-   **Pyramid Analytics integration**

    Use Pyramid Analytics as your analytics layer for ServiceNow operational data with native SQL connectivity through JDBC drivers. Build interactive dashboards and reports without data duplication and leverage advanced analytics capabilities on live data.

-   **Product renamed from SQL API to Live Connect**

    The product formerly known as SQL API is now called Live Connect. The product name was updated across all client-facing interfaces, documentation, installers, and connection wizards for consistency and clarity. Your existing integrations continue to work without changes.


### What's changed

-   **Authentication method support**

    OAuth is now the recommended authentication method for all ODBC and JDBC connections. Basic Authentication continues to be supported but will be gradually phased out in future releases.

-   **Client tool compatibility**

    JDBC driver support was expanded to enable compatibility with Pyramid Analytics and other enterprise analytics platforms. All ODBC and JDBC-compliant tools can now connect using OAuth authentication.


