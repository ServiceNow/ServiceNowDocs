---
title: Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes
description: The ServiceNow Service Graph Connector for Microsoft Defender for IoT \(Azure\) application automates the import of devices and sensor appliances. Service Graph Connector for Microsoft Defender for IoT \(Azure\) was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-03"
reading_time_minutes: 2
---

# Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes

The ServiceNow® Service Graph Connector for Microsoft Defender for IoT \(Azure\) application automates the import of devices and sensor appliances. Service Graph Connector for Microsoft Defender for IoT \(Azure\) was enhanced and updated in the Yokohama release.

## Service Graph Connector for Microsoft Defender for IoT \(Azure\) highlights for the Yokohama release

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new **ire\_criterion\_attribute** attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
-   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance automatically using the **Site Map** table.

See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://www.servicenow.com/docs/access?context=integration-sgc-microsoft-defender-iot-azure&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US) for more information.

**Important:** Service Graph Connector for Microsoft Defender for IoT \(Azure\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[View the class mappings available for the Service Graph Connector](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    View the available class mappings and targeted CMDB classes on the MSFT D4IoT Azure SGC Class Mappings page.

-   **[Capture firmware version of devices](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Firmware versions of your Service Graph Connector for Microsoft Defender for IoT \(Azure\) devices are captured in the Firmware Installation \[cmdb\_firmware\_install\] table.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://www.servicenow.com/docs/access?context=sgc-microsoft-d4iot-azure-classes&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The ire\_criterion\_attribute identifies configuration items \(CIs\) for an OT entity-related entry and helps avoid entity update issues.

-   **[Actively scan device data from Microsoft Defender for IoT with the Site Mappings table](https://www.servicenow.com/docs/access?context=actively-scan-device-data-msft-azure&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    Access the Site Mappings table to actively scan devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance.


## Activation information

Install Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    Operational Technology classes are imported with the Configuration Management Database \(CMDB\) configuration item \(CI\) classes.

-   **[Operational Technology Manager](https://www.servicenow.com/docs/access?context=operational-technology-manager&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)**

    The ServiceNow Operational Technology Manager enables you to aggregate OT device data from multiple sources so you can build the foundational data relationships used in the Industrial solution.

-   **[Industrial Core](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Use the Industrial Core application to package prerequisite tables for integrations and OT licensing. The Industrial Core application serves as a centralized solution for OT-specific utilities and data model changes.


**Parent Topic:**[Operational Technology release notes](operational-technology-rn-landing.md)

