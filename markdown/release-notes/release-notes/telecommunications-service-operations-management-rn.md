---
title: Telecommunications Service Operations Management \(TSOM\) release notes
description: The ServiceNow Telecommunications Service Operations Management \(TSOM\) application helps service providers enhance operational efficiency and network reliability. The application provides visibility into network infrastructure and streamlining data accuracy across systems. The features are designed to support proactive issue detection, reduce downtime risk, and enable faster, data-driven decisions—empowering organizations to deliver more reliable services. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Telecommunications Service Operations Management \(TSOM\) release notes

The ServiceNow® Telecommunications Service Operations Management \(TSOM\) application helps service providers enhance operational efficiency and network reliability. The application provides visibility into network infrastructure and streamlining data accuracy across systems. The features are designed to support proactive issue detection, reduce downtime risk, and enable faster, data-driven decisions—empowering organizations to deliver more reliable services. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Australia release.

## Telecommunications Service Operations Management highlights for the Australia release

-   Gain comprehensive SD-WAN visibility with new Telecom Discovery connectors for Cisco Meraki and Fortinet FortiManager.
-   Extend discovery pattern capabilities with support for switch stacks, card models, lifecycle attributes, and improved error handling.
-   Monitor SD-WAN health in real-time with new Telecom Event and Metric connectors that enable intelligent event categorization, correlation, and KPI aggregation.

See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecommunications-service-operations-management&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US) for more information.

**Important:** Telecommunications Service Operations Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   ****

    Gain full visibility into your SD-WAN landscape with automated discovery and mapping for Cisco Meraki and Fortinet FortiManager.


-   ** Customize Fortinet license expiration date storage using scripted extension points**

    By default, the Fortinet SD-WAN connector stores license expiration dates as separate CI key value pairs per device. You can override this behavior using a scripted extension point to implement alternative storage logic.


-   **Configure allowlists to scope connector polling**

    Connector instances for Cisco Meraki and Fortinet now support allowlists to limit polling to specific organizations or ADOMs. When configured, the connector polls only the listed entities, allowing large deployments to distribute collection across multiple connector instances and MID Servers.


## Changed in this release

-   **SD-WAN Discovery connectors [SD-WAN data model](https://www.servicenow.com/docs/access?context=sd-wan-data-model&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

    Enable comprehensive SD-WAN visibility by leveraging new Telecom Discovery connectors. Standardize data processing through the SD-WAN Data Model integrated into the Telecom Discovery Builder Framework ETL pipeline.


-   **[Discrepancy identification – types of discrepancies](https://www.servicenow.com/docs/access?context=discrepancy-identification-types-of-discrepancies&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

    Enhance discovery accuracy and data quality with SD-WAN-specific discrepancy audits that validate discovery results against the CMDB. Reconcile discrepancies manually or automatically using the remediation engine. When the audit detects a newly discovered CI not present in the CMDB, a single follow-on task is created at the equipment level for streamlined resolution.


## Activation information

Install Telecommunications Service Operations Management applications and plugins by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **[New plugins](https://www.servicenow.com/docs/access?context=configuring-tsom&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

    The following plugins are new in Australia:

    -   TSOM Event Management Connectors \(sn\_tsom\_em\_connectors\): TSOM Assurance Connectors for events and metrics

    -   TSOM Event Management Core \(sn\_tsom\_em\_core\): TSOM AssuranceCore features

-   **[Renamed or changed plugins](https://www.servicenow.com/docs/access?context=configuring-tsom&version=australia&pubname=australia-telecom-service-ops&ft:locale=en-US)**

    The following plugins were renamed or changed in Australia:

    Service Graph Connector for Meraki \(sn\_tsom\_meraki\_connector\):The application has been renamed to Service Graph Connector for Meraki Telco SD-WAN.


## Related ServiceNow applications and features

-   **[ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)**

    The ServiceNow®ITOM AIOps application includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

