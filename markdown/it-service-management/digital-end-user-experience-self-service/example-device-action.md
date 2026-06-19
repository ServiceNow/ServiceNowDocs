---
title: Custom device action example
description: Example of creating a device action that enables end users to reconnect to their VPN on Windows devices and restore access to internal resources from Employee Center without contacting the service desk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/example-device-action.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: reference
last_updated: "2026-05-15"
reading_time_minutes: 2
breadcrumb: [Reference, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Custom device action example

Example of creating a device action that enables end users to reconnect to their VPN on Windows devices and restore access to internal resources from Employee Center without contacting the service desk.

## Example configuration

Creating a device action requires configuring an issue configuration, a remedial action, and a device action record.

-   Issue configuration to identify a VPN connectivity issue on Windows devices and enabled for end users.

    For more information, see [Create DEX Self-service issue configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/create-dex-self-service-issue-configs.md).

    |Field|Value|
    |-----|-----|
    |Title|`VPN connectivity issue`|
    |Action Applicability|`Device actions`|
    |Category|`Network stability`|
    |Subcategory|`VPN connectivity`|
    |Type|`Device`|
    |Device OS|`Windows`|
    |User applicability|`End user`|
    |Enabled in DEX Now Assist topic|Selecting this check box enables you to view this issue in Now Assist Virtual Agent.|
    |Enabled in EC Self-service|Selecting this check box enables you to view this issue in Employee Center.|
    |Evaluation metric|`Device VPN status`|
    |Evaluation criteria|Metric configuration ID and the value.|
    |Issue Description|`VPN connection has dropped on the device.`|
    |Resolution|`snc11002`|

    For a description of all field values, see [DEX Self-service issue configuration form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/dex-self-service-issue-config-form.md).

-   A remedial action that defines the flow or script that reconnects the VPN on the device. For more information, see [Create a remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/create-remedial-action.md).
-   A device action that groups the issue configuration and the remedial action under a single label, which end users see in Employee Center.

    For more information, see [Configure device actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/configuring-dex-self-service-device-actions.md).

    |Field|Value|
    |-----|-----|
    |DEX Self-service issue config|Select the issue configuration you created. For example, VPN connectivity issue.|
    |Quick action label|`Reconnect VPN`|
    |Active|Select the check box.|

    For a description of all field values, see [DEX Self-service device action form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/dex-self-service-device-actions-form.md).


When an end user selects the **Reconnect VPN** device action from the Employee Center, the remedial action linked to the device action runs on the device and restores the VPN connection.

