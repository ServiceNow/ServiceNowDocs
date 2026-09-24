---
title: Enable a DEX remedial action for L1 IT Service Desk AI Specialist
description: Add the sn\_dex.ai\_user role to a Digital End-User Experience \(DEX\) remedial action so the L1 IT Service Desk AI Specialist can automatically trigger it when a device issue is detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/enable-dex-action-l1-specialist.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Enable a DEX remedial action for L1 IT Service Desk AI Specialist

Add the sn\_dex.ai\_user role to a Digital End-User Experience \(DEX\) remedial action so the L1 IT Service Desk AI Specialist can automatically trigger it when a device issue is detected.

## Before you begin

Make sure that a Proactive Engagement resolution is linked to the remedial action you want the L1 IT Service Desk AI Specialist to trigger. For more information, see [Configuring Proactive Engagement resolutions with DEX](https://www.servicenow.com/docs/r/it-service-management/proactive-engagement/configuring-metric-rule.html).

**Note:**

-   Some remedial actions are enabled for the L1 IT Service Desk AI Specialist in the base system. For more information, see .
-   These remedial actions are applicable for actionable resolutions and can be triggered from the actionable resolutions tab in the performance section.
-   The sys\_ids of remedial actions that don't require employee consent before the AI Specialist triggers them must be added to the **sn\_itsm\_aia.consent\_bypass\_actions** system property. For more information, see [Employee consent for device remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/collect-emp-consent.md).

Role required: sn\_reacf.sn\_remedial\_action\_admin

## Procedure

1.  Navigate to **All** &gt; **Remedial Actions Framework** &gt; **Administration** &gt; **Remedial actions**.

2.  On the Remedial Actions page, select the remedial action you want to enable for the L1 IT Service Desk AI Specialist.

3.  On the Remedial Action form, select the **Remedial Action Roles** tab.

4.  Select **New**.

5.  Select the **sn\_dex.ai\_user** role.

6.  Select **Submit**.


