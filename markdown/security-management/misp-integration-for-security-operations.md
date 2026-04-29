---
title: MISP integration for Security Operations
description: With MISP integration for Security Operations, you can investigate security incidents with sighting searches, observable enrichment, and create or update events in MISP. Using MISP, you can investigate targeted attacks faster, improve the detection ratio, and reduce the number of false positives in your environment.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# MISP integration for Security Operations

With MISP integration for Security Operations, you can investigate security incidents with sighting searches, observable enrichment, and create or update events in MISP. Using MISP, you can investigate targeted attacks faster, improve the detection ratio, and reduce the number of false positives in your environment.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## MISP Overview

MISP, which stands for Malware Information Sharing Platform, lets you exchange and share threat intelligence and Indicators of Compromise \(IoCs\) about the targeted malware and attacks within your community of trusted members. You can also share MISP information with private or open communities. By exchanging MISP information, you can investigate targeted attacks faster, improve the detection ratio, and reduce the number of false positives in your environment.

## MISP and Security Operations

See the following example to learn how the MISP information flows with Security Operations applications.

![How MISP integrates with the Security Operations applications.](../image/misp-overview.png "MISP and Security Operations overview")

## Key features

This integration includes the things that you can do with the MISP key features:

-   [Connect to private and public MISP instances](../task/install-and-configure-misp.md#table_kyc_qbg_pa1).
-   [Support manual and automatic sighting search of observables](sightings-searches-in-misp.md#).
-   [Run sighting search from case management](sightings-searches-in-misp.md#).
-   [Report or update sightings to an attribute](sightings-searches-in-misp.md#):
    -   Report an observable as a sighting \(global\)
    -   Report an observable as a false positive \(global\)
    -   Report an observable as expired
-   [Support manual and automatic observable enrichment](observable-enrichment-in-misp.md#). Results include the MISP attribute and event information that is associated with the observables.
-   Attribute enrichment in MISP which includes adding or updating [tags](observable-enrichment-in-misp.md#), [galaxies](observable-enrichment-in-misp.md#), or [comments](observable-enrichment-in-misp.md#).
-   [Event creation in MISP from SIR](events-in-misp.md#): Supports manual and the automatic creation of events in MISP from SIR.
-   Update a MISP event from SIR which includes adding or updating [tags](events-in-misp.md#), [galaxies](events-in-misp.md#), or [attributes](events-in-misp.md#).
-   [Add security incident associated observables as attributes to a MISP event](events-in-misp.md#).
-   [Auto-extract MITRE-ATT&amp;CK™ information from MISP attributes](../task/rollup-mitre-information-using-misp-enrichment-results.md) and associate the information to SIR security incidents.
-   [Automatically add SIR MITRE-ATT&amp;CK™ information as galaxies to a MISP event](../task/review-the-misp-integration-settings.md#ul_pf2_41x_nqb).

## Key concepts

This integration includes the following key concepts that you must know:

-   MISP is a Threat intelligence platform \(TIP\). You use TIPs to collect, correlate, categorize, share, and integrate security threat data in real time to support the prioritization of actions and aid in attack prevention, detection, and response.
-   MISP is a Threat Intelligence Management \(TIM\). You use TIMs to turn threat data into threat intelligence through context and to automatically prioritize threats by user-defined scoring and relevance.
-   MISP Data layer
    -   Events are encapsulations for contextually linked information.
    -   Attributes are individual data points, which can be indicators or supporting data.
    -   Objects are custom template attribute compositions.
    -   Object references are the relationships between the other building blocks.
    -   Sightings are time-specific occurrences of a detected data-point.
-   MISP Context layer
    -   Tags are labels that are attached to events or attributes and may come from taxonomies.
    -   Galaxy-clusters are knowledge base items that you can use to label events or attributes that come from galaxies.
    -   Cluster relationships denote pre-defined relationships between clusters.
-   Indicators contain a pattern that you can use to detect suspicious or malicious cyber activity.
-   Attributes in MISP can be network indicators \(IP address\), system indicators \(a string in memory\), or even bank account details. The attributes in MISP are known as observables in other SIEMs or formats such as STIX.
    -   A type describes the attribute. For example, MD5 or a URL.
    -   The attribute category describes an attribute. For example, a payload delivery.
    -   An IDS tag determines if an attribute can be automatically used for detection.

**Note:** For more information about MISP concepts, see the [MISP Documentation website](https://www.misp-project.org/documentation/)

## How your organization can benefit from MISP integration for Security Operations

Security analysts must gain and maintain situational awareness of the threat landscape, which means that they must manually consolidate and integrate an overwhelming amount of threat data. Gathering, consolidating, and integrating this data takes valuable time, which slows the detection and analysis of threats. MISP integration for Security Operations enables analysts to detect more threats and respond quicker by integrating the MISP security intelligence into an existing ServiceNow AI Platform instance.

By using the MISP integration for Security Operations, your organization can do the following actions:

-   Enable your security analysts to respond quickly and with the right context.
-   Improve your security team's efficiency by automating the incident flows for detecting and containing threats.
-   Reduce manual research time and enable security analysts to operationalize and curate indicators from within the ServiceNow AI Platform.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|MISP documentation website|[MISP Documentation website](https://www.misp-project.org/documentation/)|
|ServiceNow product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

-   **[MISP administration](misp-administration.md)**  
You can set up MISP integration in the ServiceNow AI Platform to perform a sighting search, observable enrichment, and to create and update events in MISP.
-   **[Using MISP to investigate and analyze threats](using-misp-to-detect-and-analyze-threats.md)**  
You can use the MISP data across the ServiceNow AI Platform Threat Intelligence module and the ServiceNow AI Platform SIR module to investigate and analyze threats to your organization.

**Parent Topic:**[Threat Intelligence integrations](../../threat-intelligence/concept/threat-intelligence-integrations.md)

