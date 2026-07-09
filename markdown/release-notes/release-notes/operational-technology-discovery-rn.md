---
title: Operational Technology Discovery release notes
description: The Operational Technology Discovery application give the user visibility into their Operational Technology environment and discovers the enviroments assets. Operational Technology Discovery is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-06-30"
reading_time_minutes: 2
---

# Operational Technology Discovery release notes

The Operational Technology Discovery application give the user visibility into their Operational Technology environment and discovers the enviroments assets. Operational Technology Discovery is a new application in the Zurich release.

## Operational Technology Discovery highlights for the Zurich release

-   The Discovery Console for OT provides situational awareness of your OT environment. This awareness starts at the HumanMachine Interface \(HMI Purdue Reference Model Levels 2 and 3\) and goes down to the field devices \(Level 0\) through the Console Network and Sensors.
-   The Discovery Sensor for OT executes the discovery of devices and creates the OT environment of device inventory.
-   The Service Graph Connector for ServiceNow OT Discovery imports data from a connected OT environment and leverages the Integration Hub ETL framework to import CMDB.
-   TheOT Discovery Collector delivers native OT protocol support without requiring any appliance, making it fast to implement and easy to scale.

**Important:** Operational Technology Discovery is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Operational Technology Discovery features

-   **Consistent experience**

    With the Discovery Console for OT interface, the user has a consistent experience across the application. The Console Home page provides easy access to your assets, auto queries, variable sets, sensors, and sites

-   **Communicates with Service Graph Connector for ServiceNow OT Discovery**

    The Console API has mechanisms to communicate with the Service Graph Connector for ServiceNow OT Discovery and can ingest the data from the Console into the ServiceNow CMDB.

-   **Automatic asset queries**

    The Auto Query functionality provides automatic asset queries for the Discovery Console for OT in a scheduled fashion The auto queries are classified into Simplified and Advanced.

-   **Auto Query credentials to access Sites**

    With the Console Variable sets, the user can setup required credentials and manage them per site level.

-   **Create OT environment parameters**

    You can create sites, associate Network zones and ranges to define scope of your OT network for discovery to query. You can create ignore ranges as well and select assets that must be excluded from a query.

-   **Additional OT Components**

    You can monitor and manage the configuration and health of the Discovery Sensor for OT and OT Discovery Collector used for discovery purposes from the Discovery Console for OT.


## Activation information

Install Operational Technology Discovery by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related Discovery for Operational Technology \(OT\) applications and features

-   **Service Graph Connector for ServiceNow OT Discovery**

    In your ServiceNow instance, you can navigate to the Service Graph Connector forServiceNow OT Discovery Guided Setup page and use the OT Discovery link to access installation packages.


**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/operational-technology-rn-landing.md)

