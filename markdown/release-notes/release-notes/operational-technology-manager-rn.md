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

See for [Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=australia&pubname=australia-operational-technology&ft:locale=en-US) more information.

**Important:** Operational Technology Manager is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Operational Technology Network Map](https://www.servicenow.com/docs/access?context=utilizing-ot-network-map&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    Use the OT network map available in the Industrial Workspace to view the subnets of a site and the OT devices in each subnet.

-   **[CMDB OT class model updates](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models-operation-technology&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

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

-   **[Automated IT OT Bulk Conversion name change](https://www.servicenow.com/docs/access?context=automatically-convert-it-records-to-ot-devices&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    The Automated IT OT Bulk Conversion menu item was replaced with Automated IT OT Bulk Contextualization on the ServiceNow AI Platform.

-   **[Banner messages for the Bulk Update Ruleset for Reassigning IT to OT feature](https://www.servicenow.com/docs/access?context=automatically-convert-it-records-to-ot-devices&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    A banner message was modified during the Bulk Update Ruleset for Reassigning IT to OT feature process to reflect the correct information when you use this feature.

-   **[IP Network Subnets related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    The IP Network Subnets list was added for OT devices so you can see all subnets the selected OT device is associated with.

-   **[VLAN related list](https://www.servicenow.com/docs/access?context=ot-assets-related-links-and-lists&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    The VLAN related list was added to the OT device form view to show the VLANs associated with a device.


## Changed in this release

-   **[Use CMDB groups to add OT context to IT CIs](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    When you use CMDB groups to add OT context to IT CIs, you can no longer create an Automated IT OT Bulk Contextualization record with more than one CMDB group.

-   **[Automated IT OT Bulk Contextualization - Using CMDB groups scheduled job](https://www.servicenow.com/docs/access?context=use-cmdb-groups-it-ot-conversion&version=australia&pubname=australia-operational-technology&ft:locale=en-US)**

    The **Automated IT OT Bulk Contextualization - Using CMDB groups** scheduled job can only process 10,000 CIs at one time. If you have more than 10,000 CIs, the remaining CIs will be processed in the next job run.

-   **[Admin role dependency](https://www.servicenow.com/docs/access?context=granular-admin-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

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

-   **[CMDB CI Class Models app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    The CMDB CI Class Models store application enables Operational Technology Manager to import and classify device data in ServiceNow. The Operational Technology Manager application automatically installs the latest version of the OT extension classes, available in the CMDB CI Class Models application in the ServiceNow Store.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

