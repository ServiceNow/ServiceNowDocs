---
title: Telecommunications Service Operations Management \(TSOM\) release notes
description: The ServiceNow Telecommunications Service Operations Management \(TSOM\) application enables you to monitor the health of your networks and services so that you can prevent potential downtime. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Yokohama release by adding a new capability called TSOM Visibility, which includes Telecom Discovery and Reconciliation functionality.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
---

# Telecommunications Service Operations Management \(TSOM\) release notes

The ServiceNow® Telecommunications Service Operations Management \(TSOM\) application enables you to monitor the health of your networks and services so that you can prevent potential downtime. Telecommunications Service Operations Management \(TSOM\) was enhanced and updated in the Yokohama release by adding a new capability called TSOM Visibility, which includes Telecom Discovery and Reconciliation functionality.

## Telecommunications Service Operations Management \(TSOM\) highlights for the Yokohama release

-   Perform deep network discovery of your networks via the Simple Network Management Protocol \(SNMP\) and command-line interface \(CLI\) by using Pattern-based Discovery.
-   Integrate with the Nokia Altiplano Service Graph Connector to discover the access network.
-   Handle Discrepancy Identification and Reconciliation between your discovered and inventoried data.

See [Telecommunications Service Operations Management](https://www.servicenow.com/docs/access?context=telecom-service-operations-mgt-overview&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US) for more information.

**Important:** Telecommunications Service Operations Management \(TSOM\) is available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Telecommunications Service Operations Management \(TSOM\) to Yokohama

After installing Telecommunications Service Operations Management TSOM, any customized IRE identification rules applied to interface cards, slots, sub-slots and network interfaces may be affected. You must review and validate the rules to ensure proper functionality.

## New in the Yokohama release

-   **[Pattern-based direct discovery using CLI and SNMP](https://www.servicenow.com/docs/access?context=telecom-discovery-tsom-visibility&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

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
-   **[Nokia Altiplano SGC integration](https://www.servicenow.com/docs/access?context=service-graph-connector-for-nokia-altiplano&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

    With Nokia Altiplano SGC integration, you can:

    -   Support discovery of physical Gigabit Passive Optical Network \(GPON\) network information by integrating with the Nokia Altiplano Service Graph Connector.
    -   Enable scheduled and on-demand discovery.
    -   Support the multi-instance integration of the Nokia Altiplano Service Graph Connector.
-   **[Discrepancy identification and reconciliation](https://www.servicenow.com/docs/access?context=telecom-reconciliation&version=yokohama&pubname=yokohama-telecom-service-ops&ft:locale=en-US)**

    Identify the discrepancies between your inventoried and discovered data in the following cases:

    -   -   Model mismatch.
-   Model relationship mismatch.
-   Entities not discovered in the current run but discovered in the previous run.
-   Slots-occupied discrepancy.
-   Most recent discovery not updated.
-   Incorrect number of relationships.
    -   Support a framework to automatically create tasks for reconciling discrepancies.

## Activation information

Install Telecommunications Service Operations Management by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The Event Management application helps you to identify health issues across the datacenter on a single management console. It provides alert aggregation and root cause analysis \(RCA\) for discovered services, application services, and automated alert groups. Event Management is available as a separate subscription from the rest of the ServiceNow AI Platform®.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)

