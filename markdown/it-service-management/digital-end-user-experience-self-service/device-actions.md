---
title: Device actions
description: Device actions enable end users to fix common device and application issues on DEX monitored devices. Selecting a device action runs the associated fix on the device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/device-actions.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: concept
last_updated: "2026-05-14"
reading_time_minutes: 4
breadcrumb: [Configure, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Device actions

Device actions enable end users to fix common device and application issues on DEX monitored devices. Selecting a device action runs the associated fix on the device.

As an administrator, you can create and configure device actions, define which device issues each action addresses, and control where the actions are available to users.

## Device action components

Each device action is made up of three connected components:

-   Device action: Represents a user-facing action used to resolve a device or application issue.
-   Issue configuration: Defines a device or application issue, evaluation metrics and criteria, device operating system \(OS\), user applicability, availability across interfaces, and issue resolution.

    Only eligible configurations are available for selection when creating a device action. An issue configuration is not eligible if it is already associated with another device action, is not enabled for end users, is linked to an unsupported resolution type, or uses an unsupported engagement type.

-   Resolution: Defines how the issue is resolved when the device action is triggered and is configured in Proactive Engagement.

All three components must be configured and connected for a device action to work correctly. If the issue configuration or resolution is missing, the device action is visible but inactive.

For a list of device actions available by default, see [Base system device actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/base-sys-device-actions.md).

## Device action roles and user availability

Device action creation and management require the following roles:

|Role|Description|
|----|-----------|
|sn\_dex.admin|Can create, view, update, and delete device actions and issue configurations.|
|sn\_dex\_self\_serv.user|Can view and trigger device actions in supported interfaces.|

Action visibility in the interface is determined by the user applicability setting in the issue configuration. For more information, see [Create DEX Self-service issue configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/create-dex-self-service-issue-configs.md).

## Device action availability

Device actions are available in the following interfaces, based on the issue configuration settings:

-   Employee Center: The self-service portal where employees can select, confirm, and track device actions. It is enabled by default. For more information, see [Check device health using Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/check-your-device-s-using-employee-center.md).

    This interface is enabled by default.

-   Now Assist: The Virtual Agent chat interface. This option is inactive by default and must be enabled for each device action.

    Device actions can be triggered through Virtual Agent conversations when enabled. This allows end users to initiate actions within guided interactions. For more information, see [Check device health using Now Assist for ITSM Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/check-your-device-s-health-using-now-assist-for-itsm.md).

-   DEX Desktop Assistant: A desktop application that provides employees access to self-service options, device health checks, and support resources. For more information, see [Setting up DEX Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/config-dex-desktop-exp.md) and [Check device health using Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/check-your-device-s-health-using-desktop-assistant.md).

Device action availability for Employee Center and Now Assist is configured on the issue configuration associated with the device action. For more information, see [Enable issue configurations for DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/enable-dex-self-service-issues.md).

For availability in Desktop Assistant, set up and log in to Desktop Assistant. For more information, see [Setting up DEX Desktop Assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/config-dex-desktop-exp.md).

## Device action user experience

When a device action is selected, the following user experience is consistent across interfaces:

1.  The end user selects a device action from a supporting interface and confirms the action when prompted.
2.  A progress indicator displays while the action runs.
3.  The status of the action indicated success, failure, or an error message if the device is offline.

**Related topics**  


[Base system device actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/base-sys-device-actions.md)

[Configure device actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/configuring-dex-self-service-device-actions.md)

[Create a custom device action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/create-dss-device-action.md)

[Device action access and approval control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/device-action-access-approval.md)

[Custom device action example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/example-device-action.md)

[Device action execution states and offline behavior](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/device-actions-states.md)

[Device action diagnosis and checks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/device-actions-issues.md)

