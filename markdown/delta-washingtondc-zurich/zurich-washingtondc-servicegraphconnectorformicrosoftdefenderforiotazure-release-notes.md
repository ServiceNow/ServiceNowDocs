---
title: Combined Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes for upgrades from Washington DC to Zurich
description: Consolidated page of all release notes for Service Graph Connector for Microsoft Defender for IoT \(Azure\) from Washington DC to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-washingtondc-zurich/zurich-washingtondc-servicegraphconnectorformicrosoftdefenderforiotazure-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes for upgrades from Washington DC to Zurich

Consolidated page of all release notes for Service Graph Connector for Microsoft Defender for IoT \(Azure\) from Washington DC to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Service Graph Connector for Microsoft Defender for IoT \(Azure\) release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Service Graph Connector for Microsoft Defender for IoT \(Azure\) to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Service Graph Connector for Microsoft Defender for IoT \(Azure\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   **[Categorize your OT devices into the industrial product model category](https://servicenow-staging.fluidtopics.net/access?context=model-categories-for-ot&family=washingtondc&ft:locale=en-US)**

The enhanced Service Graph Connector for Microsoft Defender for IoT \(Azure\) creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.

-   **[Troubleshooting the Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://servicenow-staging.fluidtopics.net/access?context=configuring-sgc-microsoft-d4iot-azure&family=washingtondc&ft:locale=en-US)**

Execute the scheduled job for validations and review the results to troubleshoot any issues by using the optional steps in the Troubleshooting the Service Graph Connector for Microsoft Defender for IoT \(Azure\) section of the Guided Setup.

-   **[Converting sensor ID to lowercase during devices import system property](https://servicenow-staging.fluidtopics.net/access?context=configuring-sgc-microsoft-d4iot-azure&family=washingtondc&ft:locale=en-US)**

Change the sensor ID value into lowercase letters to avoid issues with the import process by using the **Convert Sensor Names to lowercase during Devices Import \(sn\_msftd4iotazsgc.convert\_sensor\_names\_to\_lowercase\)** system property.

-   **[Filtering specific devices during import](https://servicenow-staging.fluidtopics.net/access?context=configuring-sgc-microsoft-d4iot-azure&family=washingtondc&ft:locale=en-US)**

Control what type of devices get imported by using the Filter Configuration for Devices Import section in the system properties.

-   **[Support for control module import](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=washingtondc&ft:locale=en-US)**

Import devices with the control module class to the CMDB and use the additional class mappings for the control modules.

-   **[Additional class mapping](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=washingtondc&ft:locale=en-US)**

Use the following additional class mappings to support more devices:

    -   Storage
    -   Wireless access point
    -   DB server
    -   IP telephone
    -   Multicast/broadcast
    -   Terminal station
    -   Door control panel
    -   IP camera

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Categorize your OT devices into the industrial product model category](https://servicenow-staging.fluidtopics.net/access?context=model-categories-for-ot&family=xanadu&ft:locale=en-US)**

The enhanced Service Graph Connector for Microsoft Defender for IoT \(Azure\) creates assets in the Industrial product model category for OT class devices. This enables compatibility with the Enterprise Asset Management product for full lifecycle management of OT class devices.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=yokohama&ft:locale=en-US)**

View the available class mappings and targeted CMDB classes on the MSFT D4IoT Azure SGC Class Mappings page.

-   **[Capture firmware version of devices](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=yokohama&ft:locale=en-US)**

Firmware versions of your Service Graph Connector for Microsoft Defender for IoT \(Azure\) devices are captured in the Firmware Installation \[cmdb\_firmware\_install\] table.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=yokohama&ft:locale=en-US)**

The ire\_criterion\_attribute identifies configuration items \(CIs\) for an OT entity-related entry and helps avoid entity update issues.

-   **[Actively scan device data from Microsoft Defender for IoT with the Site Mappings table](https://servicenow-staging.fluidtopics.net/access?context=actively-scan-device-data-msft-azure&family=yokohama&ft:locale=en-US)**

Access the Site Mappings table to actively scan devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance.


</td></tr><tr><td>

Zurich

</td><td>

-   **[View the class mappings available for the Service Graph Connector](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=zurich&ft:locale=en-US)**

View the available class mappings and targeted CMDB classes on the MSFT D4IoT Azure SGC Class Mappings page.

-   **[Capture firmware version of devices](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=zurich&ft:locale=en-US)**

Firmware versions of your Service Graph Connector for Microsoft Defender for IoT \(Azure\) devices are captured in the Firmware Installation \[cmdb\_firmware\_install\] table.

-   **[Use the ire\_criterion\_attribute in the OT Entity \[cmdb\_ot\_entity\] table](https://servicenow-staging.fluidtopics.net/access?context=sgc-microsoft-d4iot-azure-classes&family=zurich&ft:locale=en-US)**

The ire\_criterion\_attribute identifies configuration items \(CIs\) for an OT entity-related entry and helps avoid entity update issues.

-   **[Actively scan device data from Microsoft Defender for IoT with the Site Mappings table](https://servicenow-staging.fluidtopics.net/access?context=actively-scan-device-data-msft-azure&family=zurich&ft:locale=en-US)**

Access the Site Mappings table to actively scan devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance.


</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Service Graph Connector for Microsoft Defender for IoT \(Azure\) features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Service Graph Connector for Microsoft Defender for IoT \(Azure\) features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Service Graph Connector for Microsoft Defender for IoT \(Azure\) features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Service Graph Connector for Microsoft Defender for IoT \(Azure\).

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

Install ServiceNow® Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=washingtondc&ft:locale=en-US).

</td></tr><tr><td>

Xanadu

</td><td>

Install Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Service Graph Connector for Microsoft Defender for IoT \(Azure\) by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Service Graph Connector for Microsoft Defender for IoT \(Azure\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Service Graph Connector for Microsoft Defender for IoT \(Azure\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Service Graph Connector for Microsoft Defender for IoT \(Azure\), such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Service Graph Connector for Microsoft Defender for IoT \(Azure\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Service Graph Connector for Microsoft Defender for IoT \(Azure\) we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

-   Ensure that your Operational Technology \(OT\) devices are categorized under the Industrial product model category with the enhanced Service Graph Connector for Microsoft Defender for IoT \(Azure\) application.
-   Troubleshoot issues directly in the optional Guided Setup task.
-   Control which devices get imported by adding a filter during the import process.

 See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://servicenow-staging.fluidtopics.net/access?context=integration-sgc-microsoft-defender-iot-azure&family=washingtondc&ft:locale=en-US) for more information.

</td></tr><tr><td>

Xanadu

</td><td>

Ensure that your Operational Technology \(OT\) devices are categorized under the Industrial product model category with the enhanced Service Graph Connector for Microsoft Defender for IoT \(Azure\) application.

 See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://servicenow-staging.fluidtopics.net/access?context=integration-sgc-microsoft-defender-iot-azure&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new **ire\_criterion\_attribute** attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
-   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance automatically using the **Site Map** table.

 See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://servicenow-staging.fluidtopics.net/access?context=integration-sgc-microsoft-defender-iot-azure&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   View the class mappings available for the Service Graph Connector using the new Class Mappings menu
-   Use the Firmware Installation \[cmdb\_firmware\_install\] table to capture the firmware version.
-   Avoid OT entity update issues by using the new **ire\_criterion\_attribute** attribute on the OT Entity \[cmdb\_ot\_entity\] table.
-   Extend capabilities of the Service Graph Connector to import devices actively scanned by Microsoft Defender for IoT.
-   Ingest actively scanned devices from Microsoft Defender for IoT and assign them to a site in your ServiceNow instance automatically using the **Site Map** table.

 See [Service Graph Connector for Microsoft Defender for IoT \(Azure\)](https://servicenow-staging.fluidtopics.net/access?context=integration-sgc-microsoft-defender-iot-azure&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-washingtondc-zurich/rn-combined-intro.md)

