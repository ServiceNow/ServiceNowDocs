---
title: Industrial Process Manager release notes
description: The ServiceNow Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Industrial Process Manager release notes

The ServiceNow® Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Australia release.

## Industrial Process Manager highlights for the Australia release

-   View both unmapped and all Operational Technology \(OT\) devices in separate tabs while mapping them to equipment model entities for an organized view of your OT devices.
-   Visualize your OT network using the OT Network Map.
-   Automatically create a location for equipment model entities to visualize your location hierarchy.
-   Use the updated Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature to uniquely identify OT devices during equipment model entity mapping.

See for Industrial Process Manager more information.

**Important:** Industrial Process Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Discovered subnets supported by the AMAZING feature**

    Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **Map OT devices to equipment model entities from the Equipment Model Manager**

    Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **Generate a location hierarchy**

    Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **Use the OT Network Map to visualize your OT network**

    Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.


## UI changes

-   **Additional fields in the OT Subnet Mapping table**

    The following fields were added for equipment model entity mapping:

    -   Subnet
    -   Managed Network
    -   VLAN ID
-   **OT Discovered Subnets table**

    The OT Discovered Subnets table was added to the ServiceNow AI Platform and contains the discovered subnets in your OT network.

    To access the table, navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** and select **OT Discovered Subnets**.

-   **Discovered Subnet value added to the OT Subnet Mapping table**

    A Discovered Subnet value was added to the **Type** field in the OT Subnet Mapping table on the ServiceNow AI Platform to identify which mappings were done with discovered subnets.

-   **Updated OT device mapping to equipment model entities in the Industrial Workspace**

    You can now map OT devices to multiple equipment model entities. When you navigate to the Equipment Model Manager and select the **Mapped OT Devices** tab in an equipment model record, you can select the **Map OT Device** button. In the Add OT Devices page, you can select the devices you want to map in both the **Unmapped OT Devices** tab and the **All Devices** tab. Then you can select the equipment model entities to map your devices to.

-   **Location Validation Map tab**

    The **Location Validation Map** tab was added to the Equipment Model Manager of the Industrial Workspace so you can view a node map that displays the location hierarchy and validation status of an equipment model entity.


## Changed in this release

-   **Admin role dependency**

    Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


## Activation information

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **Operational Technology Manager**

    The ServiceNow Operational Technology Manager enables you to aggregate OT device data from multiple sources so that you can build the foundational data relationships used in the Industrial solution.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

