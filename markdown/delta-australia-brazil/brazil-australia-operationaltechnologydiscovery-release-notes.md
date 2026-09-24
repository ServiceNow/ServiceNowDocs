---
title: Combined Operational Technology Discovery release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Operational Technology Discovery from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-operationaltechnologydiscovery-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Operational Technology Discovery release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Operational Technology Discovery from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Operational Technology Discovery release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Operational Technology Discovery to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Operational Technology Discovery.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Create a backup for the Console](https://www.servicenow.com/docs/access?context=create-console-backup-concept&family=australia&ft:locale=en-US)**

To support disaster recovery, the Discovery Console for OT generates backup files containing restore data, configuration, and logs.

-   **[Install containerized OT Discovery packages](https://www.servicenow.com/docs/access?context=install-containerized-ot-discovery-packages&family=australia&ft:locale=en-US)**

Containerized versions of the Console and the Collector are available to download from the OT Discovery Downloads page. For more information, see [Air-gapped networks and OT Discovery installation](https://www.servicenow.com/docs/access?context=air-gapped-networks-installation&family=australia&ft:locale=en-US).

-   **[Generate a certificate](https://www.servicenow.com/docs/access?context=generate-new-certificate-discovery-for-ot&family=australia&ft:locale=en-US)**

You can now select the link **Download Console Certificate Bundle \(.ZIP\)**. The bundle contains the Console certificate and the web browser certificate. These certificates establish trust between these applications and confirm their communications are secure and encrypted.

-   **[Set up Microsoft Entra ID](https://www.servicenow.com/docs/access?context=users-entra-id-setup&family=australia&ft:locale=en-US)**

The Entra ID integration enables you to log in to the Console using your organization's Microsoft Entra ID cloud identity access management \(IAM\) credentials. This eliminates managing separate usernames and passwords within the application. This integration supports secure authentication using Microsoft Entra ID, improving the user experience and aligning with enterprise identity management practices.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Operational Technology Discovery features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Edit an Appliance](https://www.servicenow.com/docs/access?context=edit-an-appliance&family=australia&ft:locale=en-US)**

Navigate to the Appliances page where the individual Sensors and Collectors with their status and location are displayed. The page displays the component type, its endpoint, and CPU usage. Select the appliance name to see its details and additional settings.

-   **[Filter for Host Status](https://www.servicenow.com/docs/access?context=results-filter-host-status&family=australia&ft:locale=en-US)**

In the Scan Results filtering types, the **Host Status** helps you view query results based on whether the queried host was **Up** or **Down**. This filter is derived from the Nmap XML status field inside the Raw scan output.


 -   **[Requirements for Discovery Console for OT installation](https://www.servicenow.com/docs/access?context=reqs-ot-console-installation&family=australia&ft:locale=en-US)**

The required dependency version changed from .NET 8 to .NET 10.


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Operational Technology Discovery features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Operational Technology Discovery features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

Starting with the Australia release, Operational Technology Discovery is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

 -   Service Graph Connector for ServiceNow OT Discovery \(com.sn\_otdiscsgc\)
-   Discovery Console
-   Discovery Sensor
-   Discovery Collector

</td></tr><tr><td>

Brazil

</td><td>

-   **Operational Technology Discovery**

Starting with the Brazil release, Operational Technology Discovery is being prepared for future deprecation. It will be hidden and no longer available for installation but will continue to be supported. For more information, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


</td></tr></tbody>
</table>## Activation information

Review information on how to activate Operational Technology Discovery.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **Activation information**

Install the following Operational Technology Discovery applications using the Service Graph Connector for ServiceNow OT Discovery Guided Setup page. You must install the Service Graph Connector for ServiceNow OT Discovery before installing the following applications:

    -   Discovery Console
    -   Discovery Sensor
    -   Discovery Collector
Install Operational Technology Discovery by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).


**Note:** Operational Technology Discovery is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Operational Technology Discovery we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Operational Technology Discovery we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Operational Technology Discovery, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Operational Technology Discovery we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Operational Technology Discovery we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

**Important:** Operational Technology Discovery is being prepared for future deprecation. For more information, see the "Deprecated in this release" section of these release notes.

 -   Create a backup ZIP file of the Console database from the Console web interface.
-   Use Entra ID integration to log in to the Console with your organization's Microsoft Entra ID.
-   Use the updated Console UI for an enhanced Appliances page.
-   Identify open ports using the enhanced Open Port section of the Assets page.

 For more information, see [Operational Technology Discovery](https://www.servicenow.com/docs/access?context=operational-technology-discovery-landing&family=australia&ft:locale=en-US).

</td></tr><tr><td>

Brazil

</td><td>

**Important:** Operational Technology Discovery is being prepared for future deprecation. For more information, see [Version 1.0.7](https://www.servicenow.com/docs/access?context=operational-technology-discovery-rn-2026-09&family=brazil&ft:locale=en-US).

 -   Discover, monitor, and query devices in your OT environment with the Discovery Console.
-   Access enhanced scanning and query functionality to manage assets in your OT environment with the Discovery Sensor.
-   Create an inventory of assets in your OT environment with the Discovery Collector.
-   Import data from a connected OT Discovery environment and use the Integration Hub ETL framework with the Service Graph Connector for ServiceNow OT Discovery.

 See [Operational Technology Discovery](https://www.servicenow.com/docs/access?context=operational-technology-discovery-landing&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

