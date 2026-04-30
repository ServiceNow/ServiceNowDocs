---
title: Industrial Process Manager release notes
description: The ServiceNow Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-04"
reading_time_minutes: 5
---

# Industrial Process Manager release notes

The ServiceNow® Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Zurich release.

## Industrial Process Manager highlights for the Zurich release

-   View both unmapped and all Operational Technology \(OT\) devices in separate tabs while mapping them to equipment model entities for an organized view of your OT devices.
-   Visualize your OT network using the OT Network Map.
-   Automatically create a location for equipment model entities to visualize your location hierarchy.
-   Use the updated Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature to uniquely identify OT devices during equipment model entity mapping.
-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on the Operational Technology \(OT\) devices.

See [Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US) for more information.

**Important:** Industrial Process Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Discovered subnets supported by the AMAZING feature](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the AMAZING feature, which uses discovered subnets, to identify OT devices and assign them to the correct equipment model entity during OT subnet mapping.

-   **[Map OT devices to equipment model entities from the Equipment Model Manager](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Map OT devices to equipment model entities using the **Unmapped OT Devices** and the **All Devices** tabs in the Equipment Model Manager of the Industrial Workspace.

-   **[Generate a location hierarchy](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Generate a complete location hierarchy for an ISA equipment model entity tree when no locations exist to establish location references that match the ISA hierarchy.

-   **[Use the OT Network Map to visualize your OT network](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Visualize your OT network, subnets, and device-to-device connections with the OT Network Map in the Industrial Workspace.

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the Favorite icon \(![](../image/mark-as-favorite.png)\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.


## UI changes

-   **[Additional fields in the OT Subnet Mapping table](https://www.servicenow.com/docs/access?context=create-a-new-ot-subnet-mapping-record&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The following fields were added for equipment model entity mapping:

    -   Subnet
    -   Managed Network
    -   VLAN ID
-   **[OT Discovered Subnets table](https://www.servicenow.com/docs/access?context=automate-mappings-between-ot-assets-and-equipment-model-entity&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The OT Discovered Subnets table was added to the ServiceNow AI Platform and contains the discovered subnets in your OT network.

    To access the table, navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager** and select **OT Discovered Subnets**.

-   **[Discovered Subnet value added to the OT Subnet Mapping table](https://www.servicenow.com/docs/access?context=create-a-new-ot-subnet-mapping-record&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    A Discovered Subnet value was added to the **Type** field in the OT Subnet Mapping table on the ServiceNow AI Platform to identify which mappings were done with discovered subnets.

-   **[Updated OT device mapping to equipment model entities in the Industrial Workspace](https://www.servicenow.com/docs/access?context=map-ot-devices-in-iw&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    You can now map OT devices to multiple equipment model entities. When you navigate to the Equipment Model Manager and select the **Mapped OT Devices** tab in an equipment model record, you can select the **Map OT Device** button. In the Add OT Devices page, you can select the devices you want to map in both the **Unmapped OT Devices** tab and the **All Devices** tab. Then you can select the equipment model entities to map your devices to.

-   **[Location Validation Map tab](https://www.servicenow.com/docs/access?context=create-location-hierarchy-isa&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The **Location Validation Map** tab was added to the Equipment Model Manager of the Industrial Workspace so you can view a node map that displays the location hierarchy and validation status of an equipment model entity.


## Changed in this release

-   **Admin role dependency**

    Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.

-   **[Viewing multiple records at once in the Equipment Model Manager](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


## Activation information

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)**

    The ServiceNow Operational Technology Manager enables you to aggregate OT device data from multiple sources so that you can build the foundational data relationships used in the Industrial solution.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

