---
title: Create a custom device action
description: Create a custom device action to provide a self-service option for end users to maintain optimal device and application performance even when no issues are detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/create-dss-device-action.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2026-05-15"
reading_time_minutes: 1
breadcrumb: [Device actions, Configure, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Create a custom device action

Create a custom device action to provide a self-service option for end users to maintain optimal device and application performance even when no issues are detected.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Create an issue configuration.

    For more information, see [Create DEX Self-service issue configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/create-dex-self-service-issue-configs.md).

2.  Enable the issue configuration for DEX Self-service.

    For more information, see [Enable issue configurations for DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/enable-dex-self-service-issues.md).

3.  Create a remedial action.

    For more information, see [Create a remedial action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/create-remedial-action.md).

4.  Create a device action.

    For more information, see [Configure device actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/configuring-dex-self-service-device-actions.md).

    **Note:** Only issue configurations linked to a supported remedial action are available when creating device actions.

5.  Verify the configuration.

    1.  Access an interface that supports self-service using device actions.

        For example, Employee Center.

    2.  Locate the new device action.

    3.  Select the device action and confirm if the correct remediation is triggered and the action completes without errors.


**Related topics**  


[Custom device action example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-self-service/example-device-action.md)

