---
title: Configure device actions
description: Configure device actions that end users can trigger to maintain optimal device and application performance even when no issues are detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/configuring-dex-self-service-device-actions.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Device actions, Configuring DEX Self-service, Configure, Digital End-User Experience, IT Service Management]
---

# Configure device actions

Configure device actions that end users can trigger to maintain optimal device and application performance even when no issues are detected.

## Before you begin

Make sure that the Agent Client Collector \(ACC\) agent is deployed on the target end user devices.

Role required: sn\_dex.admin

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Self-Service** &gt; **Device Actions**.

2.  Select **New** to add a device action or open an existing device action record to modify its details.

3.  On the DEX Self-service device action form, select the issue configuration to be linked with the action.

    1.  In the **DEX Self-service issue config** field, select the Unlock DEX Self-service issue config icon \[Omitted image "icon-unlock-visible-fields.png"\] Alt text:.

    2.  In the **Select target record** field, select the Lookup using list icon \[Omitted image "icon-magnifying-glass-blue.png"\] Alt text:.

    3.  From the DEX Self-service issue configs list, select an issue configuration.

    4.  Select the Lock DEX Self-service issue config icon \[Omitted image "icon-lock-visible-fields.png"\] Alt text:.

4.  On the form, fill in the remaining fields.

    **Note:** For a description of the field values, see [DEX Self-service device action form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/dex-self-service-device-actions-form.md).

5.  Select **Submit** to add new device actions, and **Update** to modify existing device actions.


**Related topics**  


[Custom device action example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/example-device-action.md)

