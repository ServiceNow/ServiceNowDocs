---
title: Telecommunications Service Operations Management \(TSOM\) release notes
description: The ServiceNow Telecommunications Service Operations Management application provides visibility into network infrastructure to help maintain data accuracy across systems and deliver more reliable services. It supports proactive issue detection, reduces downtime risk, and enables faster, data-driven decisions.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Telecommunications Service Operations Management \(TSOM\) release notes

The ServiceNow® Telecommunications Service Operations Management application provides visibility into network infrastructure to help maintain data accuracy across systems and deliver more reliable services. It supports proactive issue detection, reduces downtime risk, and enables faster, data-driven decisions.

## Telecommunications Service Operations Management highlights for the Australia release

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   Reduce API call volume and enforce per-API scheduling constraints for Meraki and Fortinet pull connectors with new granularity and schedule window controls.
-   Define custom KPI calculations on top of raw metrics using the metric aggregation scripted extension point.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Gain comprehensive SD-WAN visibility with new Telecom Discovery connectors for Cisco Meraki and Fortinet FortiManager.
-   Extend discovery pattern capabilities with support for switch stacks, card models, life-cycle attributes, and improved error handling.
-   Monitor SD-WAN health in real time with new Telecom Event and Metric connectors that enable intelligent event categorization, correlation, and KPI aggregation.

See [Telecommunications Service Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management.md) for more information.

**Important:** Telecommunications Service Operations Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   **[Granularity support for pull connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/pull-connector-granularity.md)**

    Configure granularity and polling schedule constraints on Meraki and Fortinet pull connector instances to reduce API call volume and align data sampling with source system capabilities. Per-connector validation prevents unsupported values for metrics collection schedules and granularity windows. For valid values per connector and API type, see [Pull connector granularity constraints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/pull-connector-granularity-constraints.md).

-   **Discover VeloCloud SD-WAN inventory from both Partner \(MSP\) and Operator accounts**

    The Service Graph Connector automatically detects whether the supplied credentials belong to an Enterprise Proxy \(partner\) account or a direct operator account, so the same scheduled import works for either topology without configuring the discovery mode.

-   **[Pagination for Meraki metrics requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/meraki-pull-connector-pagination.md)**

    Meraki pull connector metrics requests now follow API pagination links automatically, ensuring complete data retrieval for large organizations where a single API response does not return all available records.

-   **[Metric aggregation scripted extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/metric-aggregation-scripted-extension.md)**

    Define custom KPI calculations on top of raw metrics using the `TSOMMetricAggregator` scripted extension point. Formulas can combine raw and transformed metrics, apply temporal aggregation operators \(`avg`, `max`, `min`, `p95`\) and spatial aggregation across matching resources, and attach user-defined labels to calculated KPIs.


[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   **[Elastic connector for MPN alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/set-up-connector-instance-nokia-mpn.md)**

    Collect fault management alarm data from a Mobile Private Network \(MPN\) Elastic index and forward events to Event Management by configuring a connector instance.

-   **[Elastic connector for MPN metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/configure-mpn-connectors-for-events-and-metrics.md)**

    The MPN connector now supports flexible metrics collection and network-level aggregation for MPN environments.

-   **[MPN data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/mpn-data-model.md)**

    Model your MPN topology in the CMDB with new CI classes and relationships for physical hardware and virtual network functions. The expanded data model captures connectivity between physical objects \(servers, firewalls, and appliances\) and virtual network functions \(UPF, UDM, and 5G core functions\). MPN infrastructure can be represented, related, and reported on alongside your telecom service operations data.

-   **Network Packet Broker CI class**

    Model network packet broker devices in the CMDB with the new Network Packet Broker class \(`cmdb_ci_network_packet_broker`\), a child of Telco Equipment \(`cmdb_ci_telco_equipment`\). Network packet brokers sit between network TAPs or SPAN ports and your security and monitoring tools, aggregating, filtering, and distributing traffic so each tool receives only the data it needs. Example devices include the Iris Packet Broker IPB220 and IPB420, and APCON IntellaFlex XR monitoring switches.

-   **[Bind MPN metrics to configuration items automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/metric-to-ci-binding-tsom-sgc.md)**

    The MPN pull connector now ships with a preconfigured event field mapping rule that binds collected metrics to CMDB configuration items automatically. The rule uses a scripted extension to resolve the CI from event fields such as name, distinguished name, serial number, and hardware ID.

-   **[KPI aggregation capability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/nokia-mpn-formula-engine.md)**

    Use the Formula Engine to process raw KPI formulas into formatted expressions, which are stored in the Formatted KPI Formula field and validated for balanced parentheses before the metric calculation engine references them.


[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   **[Customize Fortinet license expiration date storage using scripted extension points](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/configure-fortinet-allowlist.md)**

    By default, the Fortinet SD-WAN connector stores license expiration dates as separate CI key value pairs per device. You can override this behavior and implement alternative storage logic by using a scripted extension point.

-   **[Configure allowlists to scope connector polling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/configuring-allowlist.md)**

    Limit polling to specific organizations or ADOMs through allowlists on connector instances for Cisco Meraki and Fortinet.


[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


## Changed in this release

-   **[Now LLM service deprecation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[SD-WAN Discovery connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/sd-wan-data-model.md)**

    Enable comprehensive SD-WAN visibility by using new Telecom Discovery connectors. Standardize data processing through the SD-WAN Data Model integrated into the Telecom Discovery Builder Framework ETL pipeline.


-   **[Discrepancy identification – types of discrepancies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/discrepancy-identification-types-of-discrepancies.md)**

    Enhance discovery accuracy and data quality with SD-WAN-specific discrepancy audits that validate discovery results against the CMDB. Reconcile discrepancies manually or automatically using the remediation engine. When the audit detects a newly discovered CI not present in the CMDB, a single follow-on task is created at the equipment level for resolution.


## Activation information

Install Telecommunications Service Operations Management \(TSOM\) applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **[New plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/configuring-tsom.md)**

    The following plugins are new in Australia:

    -   TSOM Event Management Connectors \(sn\_tsom\_em\_conns\): TSOM Assurance Connectors for events and metrics

    -   TSOM Event Management Core \(sn\_tsom\_em\_core\): TSOM Assurance Core features

-   **[Renamed or changed plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/configuring-tsom.md)**

    The following plugins were renamed or changed in Australia:

    Service Graph Connector for Fortinet \(sn\_tsom\_fortinet\_connector\):The application has been renamed to Service Graph Connector for Fortinet Telco SD-WAN.

    Service Graph Connector for VeloCloud \(sn\_tsom\_vcloud\_connector\):The application has been renamed to Service Graph Connector for VeloCloud Telco SD-WAN.

    Service Graph Connector for Meraki \(sn\_tsom\_meraki\_connector\):The application has been renamed to Service Graph Connector for Meraki Telco SD-WAN.


## Related ServiceNow applications and features

-   **[ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-health-landing-page.md)**

    The ServiceNow®ITOM AIOps application includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/technology-industry-rn-landing.md)

