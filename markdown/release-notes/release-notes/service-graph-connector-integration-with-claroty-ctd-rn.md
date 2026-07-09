---
title: Service Graph Connector Integration for Claroty CTD release notes
description: The ServiceNow Service Graph Connector Integration for Claroty CTD application automates the import of detected devices and Claroty CTD sites. Service Graph Connector Integration for Claroty CTD was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-23"
reading_time_minutes: 2
---

# Service Graph Connector Integration for Claroty CTD release notes

The ServiceNow® Service Graph Connector Integration for Claroty CTD application automates the import of detected devices and Claroty CTD sites. Service Graph Connector Integration for Claroty CTD was enhanced and updated in the Yokohama release.

## Service Graph Connector Integration for Claroty CTD highlights for the Yokohama release

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Filter out empty rack slots to help avoid importing blank rack slots into the ServiceNow. Configuration Management Database \(CMDB\).
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new ire\_criterion\_attribute attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Clean the serial record entries from the Source \[sys\_object\_source\] table using a fix script.

See [Service Graph Connector Integration for Claroty CTD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/sgc-cmdb-integration-claroty-ctd.md) for more information.

**Important:** Service Graph Connector Integration for Claroty CTD is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[View the class mappings available for the Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/sgc-claroty-ctd-classes.md)**

    Use the **Claroty CTD SGC Class Mappings** table to view the available class mappings and targeted CMDB classes.

-   **[Avoid importing empty rack slots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/configuring-sgc-claroty-ctd-guided-setup.md)**

    During import, empty rack slots are removed to avoid importing them into the CMDB.

-   **[Capture firmware version of devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/sgc-claroty-ctd-classes.md)**

    Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version of your Service Graph Connector Integration for Claroty CTD devices.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/sgc-claroty-ctd-classes.md)**

    The ire\_criterion\_attribute acts as a criterion attribute for an OT entity-related entry and helps avoid entity update issues.

-   **[Clean up serial number data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/sgc-claroty-ctd-classes.md)**

    Clean up the serial number \[cmdb\_serial\_number\] records imported into the Source \[sys\_object\_source\] table from the Service Graph Connector Integration for Claroty CTD with a fixed script. This script establishes that a null pointer exception doesn't occur when the serial number and MAC address are the same. The script runs automatically when the plugin is upgraded.


## Activation information

Install Service Graph Connector Integration for Claroty CTD by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** Claroty CTD v5.1 is also supported for the Service Graph Connector Integration for Claroty CTD application.

## Related ServiceNow applications and features

-   **[CMDB CI Class Models store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/cmdb-ci-class-models.md)**

    Operational Technology classes are imported with the Configuration Management Database \(CMDB\) configuration item \(CI\) classes.

-   **[Operational Technology Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/operational-technology-manager.md)**

    Integrate Claroty CTD with the ServiceNow® Operational Technology Manager application to import detected devices and Claroty CTD sites, including sensors and NIDS appliances.


**Parent Topic:**[Operational Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/operational-technology-rn-landing.md)

