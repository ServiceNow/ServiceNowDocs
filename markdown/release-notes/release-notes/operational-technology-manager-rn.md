---
title: Operational Technology Manager release notes
description: The ServiceNow Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so you can build foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Operational Technology Manager release notes

The ServiceNow® Operational Technology Manager application enables you to aggregate Operational Technology \(OT\) device data from multiple sources so you can build foundational data relationships in the Industrial solution. Operational Technology Manager was enhanced and updated in the Australia release.

## Operational Technology Manager highlights for the Australia release

-   Get a deeper look into your OT network with the OT network map in the Industrial Workspace, where you can view a site, its subnets, and the OT devices in each subnet.
-   Keep your OT device data updated by using the Configuration Management Database \(CMDB\) OT class model updates and UI enhancements.

See for [Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/operational-technology-manager.md) more information.

**Important:** Operational Technology Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Operational Technology Network Map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/industrial-workspace/utilizing-ot-network-map.md)**

    Use the OT network map available in the Industrial Workspace to view the subnets of a site and the OT devices in each subnet.

-   **[CMDB OT class model updates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models-operation-technology.md)**

    Configure for your OT devices with the following CMDB OT class model updates:

    -   The IP Network Subnets related list was added to IT devices in the OT view to show all the subnets related to the device and show IP Network subnets for the selected OT device.
    -   The IP Network Subnets related list was added to the following CMDB classes:

        -   cmdb\_ci\_display
        -   cmdb\_ci\_firewall\_network
        -   cmdb\_ci\_security
        -   cmdb\_ci\_ids\_network
        -   cmdb\_ci\_imaging
        -   cmdb\_ci\_unclassed\_hardware
        -   cmdb\_ci\_multimedia
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_computer
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hardware
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_iot
        -   cmdb\_ci\_ip\_firewall
        -   cmdb\_ci\_ip\_router
        -   cmdb\_ci\_ip\_switch
        -   cmdb\_ci\_linux\_server
        -   cmdb\_ci\_monitor\_control
        -   cmdb\_ci\_netgear
        -   cmdb\_ci\_ot
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_printer
        -   cmdb\_ci\_protocol\_converter
        -   cmdb\_ci\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
        -   cmdb\_ci\_win\_server
    -   You can now view the OT device details for the following CMDB classes:
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_hyper\_v\_server
    -   Because the OT device details are included in the form view of the CMDB class table, the **OT device details** tab was removed for the following CMDB classes:
        -   cmdb\_ci\_aix\_server
        -   cmdb\_ci\_hpux\_server
        -   cmdb\_ci\_pc\_hardware
        -   cmdb\_ci\_hyper\_v\_server
        -   cmdb\_ci\_esx\_server
        -   cmdb\_ci\_solaris\_server
        -   cmdb\_ci\_unix\_server
        -   cmdb\_ci\_ups
    -   Admins can edit the protection policy for an OT View rule for all CMDB classes.

## UI changes

-   **[Automated IT OT Bulk Conversion name change](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/automatically-convert-it-records-to-ot-devices.md)**

    The Automated IT OT Bulk Conversion menu item was replaced with Automated IT OT Bulk Contextualization on the ServiceNow AI Platform.

-   **[Banner messages for the Bulk Update Ruleset for Reassigning IT to OT feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/automatically-convert-it-records-to-ot-devices.md)**

    A banner message was modified during the Bulk Update Ruleset for Reassigning IT to OT feature process to reflect the correct information when you use this feature.

-   **[IP Network Subnets related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/ot-assets-related-links-and-lists.md)**

    The IP Network Subnets list was added for OT devices so you can see all subnets the selected OT device is associated with.

-   **[VLAN related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/ot-assets-related-links-and-lists.md)**

    The VLAN related list was added to the OT device form view to show the VLANs associated with a device.


## Changed in this release

-   **[Use CMDB groups to add OT context to IT CIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/use-cmdb-groups-it-ot-conversion.md)**

    When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than one CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/operational-technology-manager/use-cmdb-groups-it-ot-conversion.md)**

    The **Automated IT OT Bulk Contextualization - Using CMDB groups** scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **[Admin role dependency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md)**

    Several new granular admin roles were added to enable developers to complete administrative configuration tasks without requiring the full admin role.


## Removed in this release

-   The **New** button was removed from the following related lists for users with read-only access to a site:
    -   Network Adapters
    -   Memory Modules
    -   Software Installed
    -   IP Addresses

## Activation information

Install Operational Technology Manager by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CMDB CI Class Models app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models/cmdb-ci-class-models.md)**

    The CMDB CI Class Models store application enables Operational Technology Manager to import and classify device data in ServiceNow. The Operational Technology Manager application automatically installs the latest version of the OT extension classes, available in the CMDB CI Class Models application in the ServiceNow Store.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

