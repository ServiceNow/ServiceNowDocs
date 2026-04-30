---
title: Enable DEX Self-service for issue configurations
description: Enable issue resolutions for DEX Self-service to enable end users to self-solve device, application, and connectivity issues.
locale: en-US
release: yokohama
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Configuring Digital End-user Experience Self-service, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Enable DEX Self-service for issue configurations

Enable issue resolutions for DEX Self-service to enable end users to self-solve device, application, and connectivity issues.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Self-Service** &gt; **Issue Configurations**.

    The base system issue configurations are displayed.

    The default value for the **Enabled in EC self-service** and **Enabled in DEX Now Assist topic** columns is **false**.

2.  Open an issue configuration record.

3.  Select the **Enabled in EC self-service** check box to enable the issue in Employee Center portal and Desktop Assistant.

4.  Select the **Enabled in DEX Now Assist topic** check box to enable the issue in Now Assist for ITSM.

    The ITSM Virtual Agent enables you to check your device's health using prebuilt Large Language Model \(LLM\) topic conversation. For more information, see [ITSM Virtual Agent pre-built LLM topics](../../now-assist-itsm/concept/itsm-va-prebuilt-topics.md).

5.  Verify that the issue code in the **Resolution** field is active.

    1.  Select the reference icon near the **Resolution** field.

    2.  On the Issue Registry preview pop-up, confirm that the **Active** check box is selected.

    3.  If the **Active** check box isn’t selected, activate the issue resolution.

        For information about how to activate an issue resolution, see [Activate Proactive Engagement resolutions for DEX Self-service](activate-proactive-engage-resolutions.md).

6.  Select **Update**.


