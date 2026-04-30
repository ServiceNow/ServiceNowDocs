---
title: Industrial Process Manager release notes
description: The ServiceNow Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-21"
reading_time_minutes: 3
---

# Industrial Process Manager release notes

The ServiceNow® Industrial Process Manager application enables your teams to map and visualize the industrial equipment models and associated production processes at individual facilities. Industrial Process Manager was enhanced and updated in the Xanadu release.

## Industrial Process Manager highlights for the Xanadu release

-   Organize your Operational Technology \(OT\) device data by capturing the mapped equipment model entity for an OT device.
-   View the relationships between devices and other configuration items \(CIs\) with the Unified Map experience in the Industrial Workspace.
-   Add Operational Technology \(OT\) devices to an equipment model entity by using the IP address.
-   Change the **Entity name** and **Parent** fields of an equipment model entity to keep your equipment model entity information up to date after you create it.

See [Industrial Process Manager](https://www.servicenow.com/docs/access?context=industrial-process-manager-overview&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US) for more information.

**Important:** Industrial Process Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Industrial Process Manager to Xanadu

The Industrial Process Manager application now has a dependency with the Operational Technology Service Management applications, which include Operational Technology Incident Management and Operational Technology Change Management. To install Industrial Process Manager on your instance, one of the following SKUs is required:

-   Operational Technology Visibility SKU
-   Operational Technology Service Management SKU
-   Any custom SKU that entitles Industrial Process Manager

## New in the Xanadu release

-   **[Capture the mapped equipment model entity for your OT devices](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Organize your OT device data efficiently by adding the primary equipment model entity for your OT devices. You can also automatically update the primary equipment model entity for your existing devices.

-   **[Use the Unified Map experience in the Industrial Workspace](https://www.servicenow.com/docs/access?context=unified-maps-experience-iw&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    View the relationships between OT devices and other CIs with the Unified Map experience. You can also view related items, such as OT incidents and change requests.

-   **[Map discovery detected devices using the Automated Mapping Across Zone-based IP Network Groups \(AMAZING\) feature](https://www.servicenow.com/docs/access?context=automatedly-map-all-ot-assets&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Map Discovery detected devices that have an IP address on their Network Adapter record using the AMAZING feature.

-   **[Add OT devices to an equipment model entity by IP address](https://www.servicenow.com/docs/access?context=view-ot-assets-equipment-model-entity&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    When you manually add OT devices to the Mapped OT Devices related list in the Equipment Model Manager on the Industrial Workspace, you can add an OT device by its IP address.

-   **[Update the entity name or parent of an equipment model entity](https://www.servicenow.com/docs/access?context=update-the-name-or-parent-equipment-model-entity&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Update the **Entity name** or **Parent** fields in an equipment model entity record as needed to help keep your equipment model information up to date.


## UI changes

-   **[Mapped equipment model entity column](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The Mapped equipment model entity column was added to the Industrial Workspace list views for OT devices.

-   **[Mapped OT Devices list](https://www.servicenow.com/docs/access?context=view-all-mapped-ot-devices&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The Mapped OT Devices list is now available in the Industrial Workspace list view so you can view the mapping between an equipment model entity and an OT device.

-   **[ISA Hierarchy search bar](https://www.servicenow.com/docs/access?context=search-equipment-model-entities&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    A search bar was added to the ISA Hierarchy in the Industrial Workspace so you can search for equipment model entity names.

-   **[__View OT Unified Map__ button](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The **View OT Unified Map** button was added to the equipment model entity record in the Industrial Workspace to access the Unified Map.

-   **[__View OT Unified Map__ button](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The **View OT Unified Map** button was added to OT incident records, OT change request records, and remediation task records to access the Unified Map associated with the opened record.

-   **[Industrial Process Health icon](https://www.servicenow.com/docs/access?context=view-ot-unified-map&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The Industrial Process Health icon \(![Industrial Process Health icon](../image/industrial-process-health-icon.png)\) was added to OT incident records, OT change request records, and remediation task records to access the Unified Map in the record side panel.

-   **[Parent field changed to Parent entity in the Equipment Model Entity record](https://www.servicenow.com/docs/access?context=create-entity-new-equipment-model&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The **Parent** field is changed to **Parent entity** in the Equipment Model Entity record on the ServiceNow AI Platform.


## Activation information

Install Industrial Process Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Industrial Process Manager is automatically installed with Operational Technology Incident Management and Operational Technology Change Management.

## Related ServiceNow applications and features

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The ServiceNow Operational Technology Manager enables you to aggregate OT device data from multiple sources so that you can build the foundational data relationships used in the Industrial solution.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

