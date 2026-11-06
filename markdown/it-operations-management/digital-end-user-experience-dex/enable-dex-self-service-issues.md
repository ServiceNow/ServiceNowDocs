---
title: Enable issue configurations for DEX Self-service
description: Enable issue resolutions for DEX Self-service so that end users can resolve device, application, and connectivity issues on their own.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/enable-dex-self-service-issues.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring DEX Self-service, Configure, Digital End-User Experience, IT Operations Management]
---

# Enable issue configurations for DEX Self-service

Enable issue resolutions for DEX Self-service so that end users can resolve device, application, and connectivity issues on their own.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  Navigate to **All** &gt; **Digital Experience Self-Service** &gt; **Issue Configurations**.

    The base system issue configurations are displayed.

    The default value for the **Enabled in EC self-service** and **Enabled in DEX Now Assist topic** columns is false.

2.  Open an issue configuration record.

3.  Select the **Enabled in EC self-service** check box to enable the issue in the Employee Center portal and Desktop Assistant.

4.  Select the **Enabled in DEX Now Assist topic** check box to enable the issue in ServiceNow Otto for ITSM.

    The ITSM Virtual Agent enables you to check your device's health using a prebuilt large language model \(LLM\) topic conversation. For more information, see [ITSM Virtual Agent pre-built LLM topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-va-prebuilt-topics.md).

5.  Verify that the issue code in the **Resolution** field is active.

    1.  Select the reference icon near the **Resolution** field.

    2.  In the Issue Registry preview pop-up window, confirm that the **Active** check box is selected.

    3.  If the **Active** check box isn’t selected, activate the issue resolution.

        For information about how to activate an issue resolution, see [Activate Proactive Engagement resolutions for DEX Self-service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/activate-proactive-engage-resolutions.md).

6.  Select **Update**.


