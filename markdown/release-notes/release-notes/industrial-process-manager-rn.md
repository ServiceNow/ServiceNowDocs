---
title: Industrial Process Manager release notes
description: The ServiceNow Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-22"
reading_time_minutes: 5
---

# Industrial Process Manager release notes

The ServiceNow® Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Yokohama release.

## Industrial Process Manager highlights for the Yokohama release

-   Identify sites on your equipment model entity that aren't in use with a new **Operational Status** field value in the Industrial Workspace.
-   Filter out **Not in use** or **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value.
-   Sort equipment model entities for a Site using the new value **Processing Order**.
-   View the **Daily Activity** tab for a summarized version of the previous day's activities on Operational Technology \(OT\) devices.
-   Organize your OT device data by capturing the mapped equipment model entity for an OT device.
-   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.

See [Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

**Important:** Industrial Process Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Set the operational status for equipment model entity sites](https://www.servicenow.com/docs/access?context=equipment-model-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Set equipment model entity sites to not in use in the Industrial Workspace by selecting the **Not in use** value for the **Operational Status** field.

-   **[Filter out Not in use and Retired equipment model entities from view](https://www.servicenow.com/docs/access?context=filter-out-non-operational-equipment-model-entities&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Filter out **Not in use** and **Retired** equipment model entities in the Industrial Workspace using the **Operational Status** field value for a site.

-   **[Add child equipment model entities to a Favorites view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Use the Favorite icon \(![](../image/mark-as-favorite.png)\) to add a child equipment model entity as a favorite in the Equipment Model Manager on the Industrial Workspace. You can then use the **Show Favorites** toggle to display them.

-   **[Assign Processing Order to sort equipment model entities in a site](https://www.servicenow.com/docs/access?context=view-child-entities-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Use the **Processing Order** field to assign values to an equipment model entity that determines their functional importance in a site.

-   **[The Daily Activity tab in the Equipment Model view in the Industrial Workspace](https://www.servicenow.com/docs/access?context=view-ot-eme-daily-summary&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    View the list of previous day's activities on the **Daily Activity** tab of an OT device. The activities include adding an OT device and changing the field-level attributes for existing OT devices. For example, IP address, Device Criticality, and more.

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map Discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.


## UI changes

-   **[Not in use value for the Operational Status field](https://www.servicenow.com/docs/access?context=equipment-model-workspace&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **Not in use** value was added as an **Operational Status** field option in an equipment model entity site record in the Industrial Workspace.

-   **[All OT Devices by Managed Network list](https://www.servicenow.com/docs/access?context=view-ot-devices-managed-by-network&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The All OT Devices by Managed Network list was added to the Industrial Process Manager module on the ServiceNow AI Platform.

-   **[Favorite icon in the Equipment Model Manager of the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    In the Equipment Model Manager on the Industrial Workspace, the Favorite icon \(![](../image/mark-as-favorite.png)\) was added to add child equipment model entities as a favorite in your system.

-   **[Show Favorites toggle in the in the Equipment Model Manager of the Industrial Workspace](https://www.servicenow.com/docs/access?context=favorite-child-equipment-model-entity&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    In the Equipment Model Manager on the Industrial Workspace, you can switch on the **Show Favorites** toggle to view only your favorite equipment model entities. The **Show Favorites** toggle focuses your UI view on specific equipment model entities to help you stay on track while making changes in the Equipment Model Manager.

-   **[List expansion during equipment model entity search in the Equipment Model Manager of the Industrial Workspace](https://www.servicenow.com/docs/access?context=search-equipment-model-entities&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    When you use the search function to find an equipment model entity, the list expands to show and highlight the search entity.

-   **[Mapped equipment model entity column](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Mapped equipment model entity column was added to the Industrial Workspace list views for OT devices.

-   **[Mapped OT Devices list](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Mapped OT Devices list is now available in the Industrial Workspace list view so you can view the mapping between an equipment model entity and an OT device.

-   **[ISA Hierarchy search bar](https://www.servicenow.com/docs/access?context=search-equipment-model-entities&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    A search bar was added to the ISA Hierarchy in the Industrial Workspace so you can search for equipment model entity names.

-   **[__View OT Unified Map__ button](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **View OT Unified Map** button was added to the equipment model entity record in the Industrial Workspace to access the Unified Map.

-   **[__View OT Unified Map__ button](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The **View OT Unified Map** button was added to OT incident records, OT change request records, and remediation task records to access the Unified Map associated with the opened record.

-   **[Industrial Process Health icon](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The Industrial Process Health icon \(![Industrial Process Health icon](../image/industrial-process-health-icon.png)\) was added to OT incident records, OT change request records, and remediation task records to access the Unified Map in the record side panel.


## Changed in this release

-   **[Viewing multiple records at once in the Equipment Model Manager](https://www.servicenow.com/docs/access?context=managing-equipment-models-after-data-import&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    In the Equipment Model Manager of the Industrial Workspace, view multiple records and keep the record context available instead of only viewing one record at a time. When creating or opening multiple records, the records open in single row of tabs at the same level so you can navigate back to other opened records.


## Activation information

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The ServiceNow Operational Technology Manager enables you to aggregate OT device data from multiple sources so that you can build the foundational data relationships used in the Industrial solution.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

