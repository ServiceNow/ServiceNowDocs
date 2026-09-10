---
title: Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-telecommunicationsserviceoperationsmanagementtsom-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 9
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Service Operations Management \(TSOM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Service Operations Management \(TSOM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Upgrade information**

After installing Telecommunications Service Operations Management TSOM, any customized IRE identification rules applied to interface cards, slots, sub-slots and network interfaces may be affected. You must review and validate the rules to ensure proper functionality.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Telecommunications Service Operations Management \(TSOM\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Pattern-based direct discovery using CLI and SNMP](https://www.servicenow.com/docs/access?context=telecom-discovery-tsom-visibility&family=yokohama&ft:locale=en-US)**

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
-   **[Nokia Altiplano SGC integration](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&family=yokohama&ft:locale=en-US)**

With Nokia Altiplano SGC integration, you can:

    -   Support discovery of physical Gigabit Passive Optical Network \(GPON\) network information by integrating with the Nokia Altiplano Service Graph Connector.
    -   Enable scheduled and on-demand discovery.
    -   Support the multi-instance integration of the Nokia Altiplano Service Graph Connector.
-   **[Discrepancy identification and reconciliation](https://www.servicenow.com/docs/access?context=telecom-reconciliation&family=yokohama&ft:locale=en-US)**

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

-   **[Fault Management: Events and alerts](https://www.servicenow.com/docs/access?context=fault-management-events-and-alerts&family=zurich&ft:locale=en-US)**

You can monitor your SD-WAN network health and resolve issues faster with automated alerts and event detection.

    -   Detect and resolve SD-WAN network issues faster with automated alerts and event monitoring.
    -   Configure customizable event rules to detect SD-WAN device issues in real time.

-   **[Added Service Graph Connector for Cisco Meraki and Fortinet](https://www.servicenow.com/docs/access?context=configuring-cisco-meraki-service-graph-connector&family=zurich&ft:locale=en-US)**

The following capabilities have been added to Cisco Meraki and Fortinet:

    -   Provides a centralized management of physical infrastructure and logical network relationships within the ServiceNow AI Platform®.
    -   Supports automated, telecom-aware discovery and real-time CMDB synchronization, along with visual network mapping, guided setup, and a dashboard for monitoring integration health.

</td></tr><tr><td>

Australia

</td><td>

-   **[Elastic connector for MPN alerts](https://www.servicenow.com/docs/access?context=set-up-connector-instance-nokia-mpn&family=australia&ft:locale=en-US)**

Collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management by configuring a connector instance.

-   **[Elastic connector for MPN metrics](https://www.servicenow.com/docs/access?context=configure-mpn-connectors-for-events-and-metrics&family=australia&ft:locale=en-US)**

The MPN connector now supports flexible metrics collection and network-level aggregation for MPN environments.

-   **[MPN data model](https://www.servicenow.com/docs/access?context=mpn-data-model&family=australia&ft:locale=en-US)**

Model your MPN topology in the CMDB with new CI classes and relationships for physical hardware and virtual network functions. The expanded data model captures connectivity between physical objects \(servers, firewalls, and appliances\) and virtual network functions \(UPF, UDM, and 5G core functions\). MPN infrastructure can be represented, related, and reported on alongside your telecom service operations data.

-   **[Network Packet Broker CI class](https://www.servicenow.com/docs/access?context=telecom-data-model&family=australia&ft:locale=en-US)**

Model network packet broker devices in the CMDB with the new Network Packet Broker class \(`cmdb_ci_network_packet_broker`\), a child of Telco Equipment \(`cmdb_ci_telco_equipment`\). Network packet brokers sit between network TAPs or SPAN ports and your security and monitoring tools. They aggregate, filter, and distribute traffic so each tool receives only the data it needs. Example devices include the Iris Packet Broker IPB220 and IPB420, and APCON IntellaFlex XR monitoring switches.

-   **[Bind MPN metrics to configuration items automatically](https://www.servicenow.com/docs/access?context=metric-to-ci-binding-tsom-sgc&family=australia&ft:locale=en-US)**

The MPN pull connector now ships with a preconfigured event field mapping rule that binds collected metrics to CMDB configuration items automatically. The rule uses a scripted extension to resolve the CI from event fields such as name, distinguished name, serial number, and hardware ID.

-   **[KPI aggregation capability](https://www.servicenow.com/docs/access?context=nokia-mpn-formula-engine&family=australia&ft:locale=en-US)**

Use the Formula Engine to process raw KPI formulas into formatted expressions. The expressions are stored in the Formatted KPI Formula field and validated for balanced parentheses before the metric calculation engine references them.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Telecommunications Service Operations Management \(TSOM\) features.

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

-   **[Telecom Discovery via Nokia Altiplano](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&family=zurich&ft:locale=en-US)**

Nokia Altiplano SGC enables you to do the following:

    -   Discover logical inventory for Nokia Altiplano such as logical ports, LAGs, and logical connections.
    -   Enable customers to manage both physical infrastructure and logical network relationships on the ServiceNow AI Platform.
    -   Store logical elements in the CMDB, improving visibility and traceability across the network.
    -   Use the generic Extract, Transform, Load \(ETL\) framework provided by ServiceNow to integrate with Nokia Altiplano, significantly reducing development effort.
-   **[Discrepancy identification](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&family=zurich&ft:locale=en-US)**

Use the enhanced audit and reconciliation logic to do the following:

    -   Detect mismatches in logical elements such as logical ports, LAGs, and connections.
    -   Filter audit results by IP range, device type, or vendor to focus on relevant subsets of data.
    -   Enhance audit performance, usability, and customer satisfaction by reducing unnecessary processing.

</td></tr><tr><td>

Australia

</td><td>

-   **[Now LLM service deprecation](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Telecommunications Service Operations Management \(TSOM\) features or functionality were removed.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Telecommunications Service Operations Management \(TSOM\) features or functionality were deprecated.

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

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

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

-   **Activation information**

Install Telecommunications Service Operations Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Telecommunications Service Operations Management applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Install Telecommunications Service Operations Management \(TSOM\) applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).


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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

</td></tr><tr><td>

Australia

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

 See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecom-service-operations-mgt-overview&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Simplify connector build and data transformation by leveraging the reusable, standardized Telecom Discovery Builder Framework across multiple telecom data sources.
-   Discover logical network elements from Nokia Altiplano using the enhanced Service Graph Connector for unified network visibility on the ServiceNow AI Platform.
-   Detect discrepancies in both logical and physical entities, including attribute value mismatches, and improve audit accuracy using targeted filters.

 See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecommunications-service-operations-management&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   Starting with Zurich Patch 12, ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   Reduce API call volume and enforce per-API scheduling constraints for Meraki and Fortinet pull connectors with new granularity and schedule window controls.
-   Define custom KPI calculations on top of raw metrics using the metric aggregation scripted extension point.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Gain comprehensive SD-WAN visibility with new Telecom Discovery connectors for Cisco Meraki and Fortinet FortiManager.
-   Extend discovery pattern capabilities with support for switch stacks, card models, life-cycle attributes, and improved error handling.
-   Monitor SD-WAN health in real time with new Telecom Event and Metric connectors that enable intelligent event categorization, correlation, and KPI aggregation.

 See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecommunications-service-operations-management&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

