---
title: Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-telecommunicationsserviceoperationsmanagementtsom-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 10
breadcrumb: [Products combined by family]
---

# Combined Telecommunications Service Operations Management \(TSOM\) release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Telecommunications Service Operations Management \(TSOM\) from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Telecommunications Service Operations Management \(TSOM\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Telecommunications Service Operations Management \(TSOM\) to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

-   **[Telecom Discovery Builder framework](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&family=zurich&ft:locale=en-US)**

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
-   **[Identify and reconcile discrepancies](https://www.servicenow.com/docs/access?context=exploring-telecom-reconciliation&family=zurich&ft:locale=en-US)**

Use enhanced discrepancy identification and reconciliation features to keep your discovery data accurate and up to date on the ServiceNow AI Platform. These features give you better control over detected changes and improve overall audit performance.

    -   Identify attribute value mismatches during discovery, such as bandwidth changes on ports \(for example, from 10 Mbps to 100 Mbps\).
    -   Display previous and current attribute values, enabling you to decide whether to accept the new value, retain the old one, or manually raise a remediation task.
    -   Detect discrepancies in logical entities alongside physical entities for comprehensive discrepancy management for newly discovered logical network elements.
    -   Generate audit results using filtering conditions—such as specific IP ranges, device vendors, or port types—to focus on relevant subsets of data and significantly enhance audit performance and usability.
-   **[Fault Management: Events and alerts](https://www.servicenow.com/docs/access?context=fault-management-events-and-alerts&family=zurich&ft:locale=en-US)**

You can monitor your SD-WAN network health and resolve issues faster with automated alerts and event detection.

    -   Detect and resolve SD-WAN network issues faster with automated alerts and event monitoring.
    -   Configure customizable event rules to detect SD-WAN device issues in real time.

-   **[Added Service Graph Connector for Cisco Meraki and Fortinet](https://www.servicenow.com/docs/access?context=configuring-cisco-meraki-service-graph-connector&family=zurich&ft:locale=en-US)**

The following capabilities have been added to Cisco Meraki and Fortinet:

    -   Provides a centralized management of physical infrastructure and logical network relationships within the ServiceNow AI Platform®.
    -   Supports automated, telecom-aware discovery and real-time CMDB synchronization, along with visual network mapping, guided setup, and a dashboard for monitoring integration health.
-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&family=zurich&ft:locale=en-US)**

The granular admin role enables developers and administrators to complete administrative configuration tasks for TSOM without requiring the full admin role.


</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 4](https://www.servicenow.com/docs/access?context=australia-patch-4&family=australia&ft:locale=en-US)

-   **[Granularity support for pull connectors](https://www.servicenow.com/docs/access?context=pull-connector-granularity&family=australia&ft:locale=en-US)**

Configure granularity and polling schedule constraints on Meraki and Fortinet pull connector instances to reduce API call volume and align data sampling with source system capabilities. Per-connector validation prevents unsupported values for metrics collection schedules and granularity windows. For valid values per connector and API type, see [Pull connector granularity constraints](https://www.servicenow.com/docs/access?context=pull-connector-granularity-constraints&family=australia&ft:locale=en-US).

-   **[Discover VeloCloud SD-WAN inventory from both Partner \(MSP\) and Operator accounts](https://www.servicenow.com/docs/access?context=telecom-discovery-via-arista-velocloud&family=australia&ft:locale=en-US)**

The Service Graph Connector automatically detects whether the supplied credentials belong to an Enterprise Proxy \(partner\) account or a direct operator account. The same scheduled import works for either topology without configuring the discovery mode.

-   **[Pagination for Meraki metrics requests](https://www.servicenow.com/docs/access?context=meraki-pull-connector-pagination&family=australia&ft:locale=en-US)**

Meraki pull connector metrics requests now follow API pagination links automatically. This verifies complete data retrieval for large organizations.

-   **[Metric aggregation scripted extension](https://www.servicenow.com/docs/access?context=metric-aggregation-scripted-extension&family=australia&ft:locale=en-US)**

Define custom KPI calculations on top of raw metrics using the `TSOMMetricAggregator` scripted extension point. Formulas can combine raw and transformed metrics, apply temporal aggregation operators \(`avg`, `max`, `min`, `p95`\) and spatial aggregation across matching resources, and attach user-defined labels to calculated KPIs.


[Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

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


[Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-2&family=australia&ft:locale=en-US)

-   **[Customize Fortinet license expiration date storage using scripted extension points](https://www.servicenow.com/docs/access?context=configure-fortinet-allowlist&family=australia&ft:locale=en-US)**

By default, the Fortinet SD-WAN connector stores license expiration dates as separate CI key value pairs per device. You can override this behavior and implement alternative storage logic by using a scripted extension point.

-   **[Configure allowlists to scope connector polling](https://www.servicenow.com/docs/access?context=configuring-allowlist&family=australia&ft:locale=en-US)**

Limit polling to specific organizations or ADOMs through allowlists on connector instances for Cisco Meraki and Fortinet.


[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Telecommunications Service Operations Management \(TSOM\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

-   **[SD-WAN Discovery connectors](https://www.servicenow.com/docs/access?context=sd-wan-data-model&family=australia&ft:locale=en-US)**

Enable comprehensive SD-WAN visibility by using new Telecom Discovery connectors. Standardize data processing through the SD-WAN Data Model integrated into the Telecom Discovery Builder Framework ETL pipeline.


-   **[Types of discrepancies](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&family=australia&ft:locale=en-US)**

Enhance discovery accuracy and data quality with SD-WAN-specific discrepancy audits that validate discovery results against the CMDB. Reconcile discrepancies manually or automatically using the remediation engine. When the audit detects a newly discovered CI not present in the CMDB, a single follow-on task is created at the equipment level for resolution.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Telecommunications Service Operations Management \(TSOM\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Zurich

</td><td>

Install Telecommunications Service Operations Management applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

Install Telecommunications Service Operations Management \(TSOM\) applications and plugins by requesting them from ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Telecommunications Service Operations Management \(TSOM\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

