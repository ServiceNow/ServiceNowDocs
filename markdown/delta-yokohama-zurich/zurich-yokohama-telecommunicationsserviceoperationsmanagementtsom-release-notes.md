---
title: Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-telecommunicationsserviceoperationsmanagementtsom-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 7
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Service Operations Management \(TSOM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Service Operations Management \(TSOM\) to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

After installing Telecommunications Service Operations Management TSOM, any customized IRE identification rules applied to interface cards, slots, sub-slots and network interfaces may be affected. You must review and validate the rules to ensure proper functionality.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Telecommunications Service Operations Management \(TSOM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Pattern-based direct discovery using CLI and SNMP](https://servicenow-staging.fluidtopics.net/access?context=telecom-discovery-tsom-visibility&family=yokohama&ft:locale=en-US)**

Use pattern-based direct discovery to do the following tasks:

    -   Support deep network discovery of your physical network elements by using CLI and SNMP.
    -   Enable pattern-based discovery for any network elements that support SNMP standard MIBs.
    -   Provide a framework to enable custom Management Information Base \(MIB\)-based discovery.
    -   Enable both scheduled and quick discovery of standalone network elements.
    -   Support the following Cisco and Juniper routers and switches:
        -   Cisco ASR1K
        -   Cisco 7613
        -   Cisco Nexus 9000
        -   Cisco Nexus 3548
        -   Juniper Mx80
        -   Juniper MX104
        -   Juniper MX240
        -   Juniper MX480
-   **[Nokia Altiplano SGC integration](https://servicenow-staging.fluidtopics.net/access?context=service-graph-connector-for-nokia-altiplano&family=yokohama&ft:locale=en-US)**

With Nokia Altiplano SGC integration, you can:

    -   Support discovery of physical Gigabit Passive Optical Network \(GPON\) network information by integrating with the Nokia Altiplano Service Graph Connector.
    -   Enable scheduled and on-demand discovery.
    -   Support the multi-instance integration of the Nokia Altiplano Service Graph Connector.
-   **[Discrepancy identification and reconciliation](https://servicenow-staging.fluidtopics.net/access?context=telecom-reconciliation&family=yokohama&ft:locale=en-US)**

Identify the discrepancies between your inventoried and discovered data in the following cases:

    -   -   Model mismatch.
-   Model relationship mismatch.
-   Entities not discovered in the current run but discovered in the previous run.
-   Slots-occupied discrepancy.
-   Most recent discovery not updated.
-   Incorrect number of relationships.
    -   Support a framework to automatically create tasks for reconciling discrepancies.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Telecom Discovery Builder framework](https://servicenow-staging.fluidtopics.net/access?context=exploring-the-telco-generic-schema-etl-framework&family=zurich&ft:locale=en-US)**

Leverage a standardized Extract, Transform, Load \(ETL\) framework to streamline the processing and storage of telecom network data on the ServiceNow AI Platform.

This reusable framework simplifies implementation by removing the need to manually build ETLs. It enables you to focus on connectivity logic while confirming consistent and reliable mapping of network elements such as equipment, cards, ports, LAGs, logical ports, and logical connections into predefined CMDB structures.

Use Telecom Discovery Builder Framework to do the following:

    -   Simplify data transformation tasks by duplicating the common ETL and configuring essential fields and settings for specific connector applications.
    -   Deploy new Service Graph Connector \(SGC\) using existing ETLs to maintain consistent data transformation practices.
    -   Help to ensure data integrity and support the automatic creation of TNI Entities through configured Before and After scripts.
    -   The standardized CMDB/TNI data model enables ETL reusability across multiple connectors.
    -   Allocate predefined storage locations for both physical and logical inventory elements.
    -   Maintain consistent data model hierarchies across connectors to support unified network inventory management.
    -   Improve Discovery SGC quality by providing an OOTB Data Source Validation tools.
-   **[Identify and reconcile discrepancies](https://servicenow-staging.fluidtopics.net/access?context=exploring-telecom-reconciliation&family=zurich&ft:locale=en-US)**

Use enhanced discrepancy identification and reconciliation features to keep your discovery data accurate and up to date on the ServiceNow AI Platform. These features give you better control over detected changes and improve overall audit performance.

    -   Identify attribute value mismatches during discovery, such as bandwidth changes on ports \(for example, from 10 Mbps to 100 Mbps\).
    -   Display previous and current attribute values, enabling you to decide whether to accept the new value, retain the old one, or manually raise a remediation task.
    -   Detect discrepancies in logical entities alongside physical entities for comprehensive discrepancy management for newly discovered logical network elements.
    -   Generate audit results using filtering conditions—such as specific IP ranges, device vendors, or port types—to focus on relevant subsets of data and significantly enhance audit performance and usability.
-   **[Fault Management: Events and alerts](https://servicenow-staging.fluidtopics.net/access?context=fault-management-events-and-alerts&family=zurich&ft:locale=en-US)**

You can monitor your SD-WAN network health and resolve issues faster with automated alerts and event detection.

    -   Detect and resolve SD-WAN network issues faster with automated alerts and event monitoring.
    -   Configure customizable event rules to detect SD-WAN device issues in real time.

-   **[Added Service Graph Connector for Cisco Meraki and Fortinet](https://servicenow-staging.fluidtopics.net/access?context=configuring-cisco-meraki-service-graph-connector&family=zurich&ft:locale=en-US)**

The following capabilities have been added to Cisco Meraki and Fortinet:

    -   Provides a centralized management of physical infrastructure and logical network relationships within the ServiceNow AI Platform®.
    -   Supports automated, telecom-aware discovery and real-time CMDB synchronization, along with visual network mapping, guided setup, and a dashboard for monitoring integration health.
-   **[Granular admin roles](https://servicenow-staging.fluidtopics.net/access?context=exploring-the-telco-generic-schema-etl-framework&family=zurich&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for TSOM without requiring the full admin role.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Telecommunications Service Operations Management \(TSOM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Telecom Discovery via Nokia Altiplano](https://servicenow-staging.fluidtopics.net/access?context=service-graph-connector-for-nokia-altiplano&family=zurich&ft:locale=en-US)**

Nokia Altiplano SGC enables you to do the following:

    -   Discover logical inventory for Nokia Altiplano such as logical ports, LAGs, and logical connections.
    -   Enable customers to manage both physical infrastructure and logical network relationships on the ServiceNow AI Platform.
    -   Store logical elements in the CMDB, improving visibility and traceability across the network.
    -   Use the generic Extract, Transform, Load \(ETL\) framework provided by ServiceNow to integrate with Nokia Altiplano, significantly reducing development effort.
-   **[Discrepancy identification](https://servicenow-staging.fluidtopics.net/access?context=discrepancy-identification-types-of-discrepancies&family=zurich&ft:locale=en-US)**

Use the enhanced audit and reconciliation logic to do the following:

    -   Detect mismatches in logical elements such as logical ports, LAGs, and connections.
    -   Filter audit results by IP range, device type, or vendor to focus on relevant subsets of data.
    -   Enhance audit performance, usability, and customer satisfaction by reducing unnecessary processing.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Telecommunications Service Operations Management \(TSOM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Telecommunications Service Operations Management \(TSOM\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   The two previous Extract, Transform, Load \(ETLs\) for Optical Line Terminal \(OLT\) and Optical Network Unit \(ONU\) have been merged into a unified ETL that supports both physical and logical data and have been deprecated and phased out.
-   The previous Service Operation CMDB Compliance Audit has been deprecated and replaced by the Telecom Discrepancy Audit.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Telecommunications Service Operations Management \(TSOM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Telecommunications Service Operations Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Telecommunications Service Operations Management applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Telecommunications Service Operations Management \(TSOM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Telecommunications Service Operations Management \(TSOM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Telecommunications Service Operations Management \(TSOM\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Telecommunications Service Operations Management \(TSOM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Telecommunications Service Operations Management \(TSOM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Perform deep network discovery of your networks via the Simple Network Management Protocol \(SNMP\) and command-line interface \(CLI\) by using Pattern-based Discovery.
-   Integrate with the Nokia Altiplano Service Graph Connector to discover the access network.
-   Handle Discrepancy Identification and Reconciliation between your discovered and inventoried data.

 See [Telecommunications Service Operations Management](https://servicenow-staging.fluidtopics.net/access?context=telecom-service-operations-mgt-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Simplify connector build and data transformation by leveraging the reusable, standardized Telecom Discovery Builder Framework across multiple telecom data sources.
-   Discover logical network elements from Nokia Altiplano using the enhanced Service Graph Connector for unified network visibility on the ServiceNow AI Platform.
-   Detect discrepancies in both logical and physical entities, including attribute value mismatches, and improve audit accuracy using targeted filters.

 See [Telecommunications Service Operations Management](https://servicenow-staging.fluidtopics.net/access?context=telecommunications-service-operations-management&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

