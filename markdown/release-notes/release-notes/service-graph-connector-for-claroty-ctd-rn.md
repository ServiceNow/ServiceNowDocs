---
title: Service Graph Connector Integration for Claroty CTD release notes
description: The ServiceNow Service Graph Connector Integration for Claroty CTD application automates the import of detected devices and Claroty CTD sites. Service Graph Connector Integration for Claroty CTD was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-23"
reading_time_minutes: 2
---

# Service Graph Connector Integration for Claroty CTD release notes

The ServiceNow® Service Graph Connector Integration for Claroty CTD application automates the import of detected devices and Claroty CTD sites. Service Graph Connector Integration for Claroty CTD was enhanced and updated in the Xanadu release.

## Service Graph Connector Integration for Claroty CTD highlights for the Xanadu release

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Filter out empty rack slots to help avoid importing blank rack slots into the ServiceNow. Configuration Management Database \(CMDB\).
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new ire\_criterion\_attribute attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Clean the serial record entries from the Source \[sys\_object\_source\] table using a fix script.
-   Ensure that your Operational Technology \(OT\) devices are categorized under the Industrial product model category with the enhanced Service Graph Connector Integration for Claroty CTD application.

See [Service Graph Connector Integration for Claroty CTD](https://www.servicenow.com/docs/access?context=sgc-cmdb-integration-claroty-ctd&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US) for more information.

**Important:** Service Graph Connector Integration for Claroty CTD is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Use the **Claroty CTD SGC Class Mappings** table to view the available class mappings and targeted CMDB classes.

-   **[Avoid importing empty rack slots](https://www.servicenow.com/docs/access?context=configuring-sgc-claroty-ctd-guided-setup&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    During import, empty rack slots are removed to avoid importing them into the CMDB.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version of your Service Graph Connector Integration for Claroty CTD devices.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The ire\_criterion\_attribute acts as a criterion attribute for an OT entity-related entry and helps avoid entity update issues.

-   **[Clean up serial number data](https://www.servicenow.com/docs/access?context=sgc-claroty-ctd-classes&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Clean up the serial number \[cmdb\_serial\_number\] records imported into the Source \[sys\_object\_source\] table from the Service Graph Connector Integration for Claroty CTD with a fixed script. This script establishes that a null pointer exception doesn't occur when the serial number and MAC address are the same. The script runs automatically when the plugin is upgraded.

-   **[Categorize your OT devices into the industrial product model category](https://www.servicenow.com/docs/access?context=model-categories-for-ot&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    The enhanced Service Graph Connector Integration for Claroty CTD creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.


## Activation information

Install Service Graph Connector Integration for Claroty CTD by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Claroty CTD v5.1 is also supported for the Service Graph Connector Integration for Claroty CTD application.

## Related ServiceNow applications and features

-   **[CMDB CI Class Models](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Operational Technology classes are imported with the Configuration Management Database \(CMDB\) configuration item \(CI\) classes.

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=xanadu&pubname=xanadu-operational-technology&ft:locale=en-US)**

    Integrate Claroty CTD with the ServiceNow Operational Technology Manager application to import detected devices and Claroty CTD sites, including sensors and NIDS appliances.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

