---
title: Telecommunications Service Operations Management \(TSOM\) release notes
description: The ServiceNow Telecommunications Service Operations Management \(TSOM\) application provides visibility into network infrastructure and enables service providers to streamline data accuracy across systems. It supports proactive issue detection, reduces downtime risk, and enables faster, data-driven decisions. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Telecommunications Service Operations Management \(TSOM\) release notes

The ServiceNow® Telecommunications Service Operations Management \(TSOM\) application provides visibility into network infrastructure and enables service providers to streamline data accuracy across systems. It supports proactive issue detection, reduces downtime risk, and enables faster, data-driven decisions. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Zurich release.

## Telecommunications Service Operations Management \(TSOM\) highlights for the Zurich release

-   Simplify connector build and data transformation by leveraging the reusable, standardized Telecom Discovery Builder Framework across multiple telecom data sources.
-   Discover logical network elements from Nokia Altiplano using the enhanced Service Graph Connector for unified network visibility on the ServiceNow AI Platform.
-   Detect discrepancies in both logical and physical entities, including attribute value mismatches, and improve audit accuracy using targeted filters.

See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecommunications-service-operations-management&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US) for more information.

**Important:** Telecommunications Service Operations Management \(TSOM\) applications and plugins are available in ServiceNow Store. For details, see the "Activation information" section of this release notes.

## New in the Zurich release

-   **[Telecom Discovery Builder framework](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

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
-   **[Telecom Discrepancy Identification and Reconciliation](https://www.servicenow.com/docs/access?context=exploring-telecom-reconciliation&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    Use enhanced discrepancy identification and reconciliation features to keep your discovery data accurate and up to date on the ServiceNow AI Platform. These features give you better control over detected changes and improve overall audit performance.

    -   Identify attribute value mismatches during discovery, such as bandwidth changes on ports \(for example, from 10 Mbps to 100 Mbps\).
    -   Display previous and current attribute values, enabling you to decide whether to accept the new value, retain the old one, or manually raise a remediation task.
    -   Detect discrepancies in logical entities alongside physical entities for comprehensive discrepancy management for newly discovered logical network elements.
    -   Generate audit results using filtering conditions—such as specific IP ranges, device vendors, or port types—to focus on relevant subsets of data and significantly enhance audit performance and usability.
-   **[Fault Management: Events and alerts](https://www.servicenow.com/docs/access?context=fault-management-events-and-alerts&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    You can monitor your SD-WAN network health and resolve issues faster with automated alerts and event detection.

    -   Detect and resolve SD-WAN network issues faster with automated alerts and event monitoring.
    -   Configure customizable event rules to detect SD-WAN device issues in real time.

-   **[Added Service Graph Connector for Cisco Meraki and Fortinet](https://www.servicenow.com/docs/access?context=configuring-cisco-meraki-service-graph-connector&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    The following capabilities have been added to Cisco Meraki and Fortinet:

    -   Provides a centralized management of physical infrastructure and logical network relationships within the ServiceNow AI Platform®.
    -   Supports automated, telecom-aware discovery and real-time CMDB synchronization, along with visual network mapping, guided setup, and a dashboard for monitoring integration health.
-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=exploring-the-telco-generic-schema-etl-framework&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    The granular admin role enables developers and administrators to complete administrative configuration tasks for TSOM without requiring the full admin role.


## Changed in this release

-   **[Telecom Discovery via Nokia Altiplano](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    Nokia Altiplano SGC enables you to do the following:

    -   Discover logical inventory for Nokia Altiplano such as logical ports, LAGs, and logical connections.
    -   Enable customers to manage both physical infrastructure and logical network relationships on the ServiceNow AI Platform.
    -   Store logical elements in the CMDB, improving visibility and traceability across the network.
    -   Use the generic Extract, Transform, Load \(ETL\) framework provided by ServiceNow to integrate with Nokia Altiplano, significantly reducing development effort.
-   **[Discrepancy identification](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&version=zurich&pubname=zurich-telecom-service-ops&ft:locale=en-US)**

    Use the enhanced audit and reconciliation logic to do the following:

    -   Detect mismatches in logical elements such as logical ports, LAGs, and connections.
    -   Filter audit results by IP range, device type, or vendor to focus on relevant subsets of data.
    -   Enhance audit performance, usability, and customer satisfaction by reducing unnecessary processing.

## Deprecations

-   The two previous Extract, Transform, Load \(ETLs\) for Optical Line Terminal \(OLT\) and Optical Network Unit \(ONU\) have been merged into a unified ETL that supports both physical and logical data and have been deprecated and phased out.
-   The previous Service Operation CMDB Compliance Audit has been deprecated and replaced by the Telecom Discrepancy Audit.

## Activation information

Install Telecommunications Service Operations Management applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

The following plugins are new in Zurich:

-   TSOM Event Management Connectors \(sn\_tsom\_em\_connectors\): TSOM Assurance Connectors for events and metrics

-   TSOM Event Management Core \(sn\_tsom\_em\_core\): TSOM AssuranceCore features

-   Service Graph Connector for Fortinet \(sn\_tsom\_fortinet\_connector\): Service Graph Connector for Fortinet
-   Service Graph Connector for Meraki \(sn\_tsom\_meraki\_connector\): Service Graph Connector for Meraki

## Related ServiceNow applications and features

-   **[ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The ServiceNow®ITOM AIOps application includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

