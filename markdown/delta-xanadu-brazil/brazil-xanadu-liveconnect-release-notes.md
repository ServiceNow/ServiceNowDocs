---
title: Combined Live Connect release notes for upgrades from Xanadu to Brazil
description: Consolidated page of all release notes for Live Connect from Xanadu to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-brazil/brazil-xanadu-liveconnect-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Live Connect release notes for upgrades from Xanadu to Brazil

Consolidated page of all release notes for Live Connect from Xanadu to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Live Connect release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Live Connect to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Upgrade information**

ServiceNow provided customers with a free SOAP-based ODBC client. If you have an active RaptorDB Professional entitlement, you can migrate to the REST-based Live Connect client by completing the required configuration on both the server and client sides. For more information, see [Configure](https://www.servicenow.com/docs/access?context=configuring-sql-api&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Live Connect.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

The following features are new in this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **[Enable OAuth for Live Connect](https://www.servicenow.com/docs/access?context=enable-oauth-for-live-connect&family=brazil&ft:locale=en-US)**

Connect third-party ODBC and JDBC clients to ServiceNow using OAuth credentials to meet FedRamp compliance requirements and enable secure multi-factor authentication workflows. OAuth provides modern, encrypted authentication aligned with security standards and reduces credential exposure in transit.

-   **Pyramid Analytics integration**

Use Pyramid Analytics as your analytics layer for ServiceNow operational data with native SQL connectivity through JDBC drivers. Build interactive dashboards and reports without data duplication and leverage advanced analytics capabilities on live data.

-   **Product renamed from SQL API to Live Connect**

The product formerly known as SQL API is now called Live Connect. The product name was updated across all client-facing interfaces, documentation, installers, and connection wizards for consistency and clarity. Your existing integrations continue to work without changes.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Live Connect features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

The following UI changes are in this release.

</td></tr><tr><td>

Brazil

</td><td>

-   **Authentication method support**

OAuth is now the recommended authentication method for all ODBC and JDBC connections. Basic Authentication continues to be supported but will be gradually phased out in future releases.

-   **Client tool compatibility**

JDBC driver support was expanded to enable compatibility with Pyramid Analytics and other enterprise analytics platforms. All ODBC and JDBC-compliant tools can now connect using OAuth authentication.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Live Connect features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Live Connect features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Live Connect.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Live Connect is a ServiceNow feature that is available with the activation of Live Connect plugin \(com.glide.rest.sqlapiserver\). The ServiceNow instance requires RaptorDB Professional entitlement to activate the Live Connect server-side plugin.

The Live Connect client drivers are freely available for download by anyone with a valid account to the ServiceNow Store. However, the Live Connect client would not be able to connect to the ServiceNow instance until the server-side plugin is enabled. For more information, see [Install Live Connect on your ServiceNow instance](https://www.servicenow.com/docs/access?context=install-sql-api-plugin&family=australia&ft:locale=en-US).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Live Connect we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Additional requirements**

You must download the SQL API ODBC and JDBC drivers on your client machine. These drivers enable your BI tools and data analysis platforms to connect to your ServiceNow data and run the Live Connect queries. You can download the ODBC and JDBC drivers from ServiceNow Store.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Live Connect we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Browser requirements**

Live Connect is a backend connectivity layer with no browser-specific requirements. Browser compatibility depends on the third-party client tools used to connect to Live Connect.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Live Connect, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Accessibility information**
    -   Live Connect is a backend connectivity layer with no direct user interface.
    -   Accessibility of query results depends on the third-party client tools used to connect to Live Connect.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Live Connect we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **Localization information**

Live Connect operates independently of language settings. Data returned through Live Connect reflects the language settings of the queried tables.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Live Connect we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   Query your ServiceNow data directly without replicating it to external repositories or data warehouses.
-   Access data using read-only operations to avoid unintended changes to your ServiceNow records. Allow access only to the desired tables.
-   Integrate standard BI platforms such as Power BI, DBvisualizer, and other ODBC or JDBC-compatible tools directly with your ServiceNow data.
-   Merge your ServiceNow data with external datasets in your analytical platforms for comprehensive analysis.
-   Write targeted SQL queries to retrieve only the data you need, reducing network overhead on data pipeline and data transformation, and improving performance.

 For more information, see [Access your ServiceNow data using Live Connect](https://www.servicenow.com/docs/r/api-reference/web-services/accessing-your-servicenow-data-using-sql-api.html).

 **Important:** Live Connect is available in the ServiceNow Store. For details, see the Activation information section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-xanadu-brazil/rn-combined-intro.md)

