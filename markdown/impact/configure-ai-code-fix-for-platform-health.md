---
title: Configure real-time code resolution with AI
description: Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-ai-code-fix-for-platform-health.html
release: australia
topic_type: task
last_updated: "2026-07-15"
reading_time_minutes: 1
breadcrumb: [Configure Scan Engine parameters, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure real-time code resolution with AI

Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

Real-time messaging enforcement can be disabled on the Scan Engine properties page. When enforcement is disabled, users see the messaging but aren't required to make corrections for Act and Recommend findings.

Visibility of real-time messaging can also be configured to limit which users receive finding notifications. You can restrict messaging to a specific group.

## About this task

The following are minimum prerequisites:

-   Install and configure the Impact Store App. See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md) for details.
-   Scan Engine configured: See [Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-initial-scan-engine-settings.md) for details.
-   Now Assist for Impact, version 3.03: See [Activate Now Assist Skills for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/activate-now-assist-skills-in-now-assist-for-impact.md) for details.
-   Now Assist for Platform, version 11.01

## Procedure

1.  Set system to enforce real-time validation.
2.  Navigate to Scan Engine Properties System properties \(`sn_se_properties.list`\).

3.  On the Real Time Scanning related list, set **Enforce real-time validation** to true

    Real-time Messaging must be activated, as the feature is tied to findings being present.

4.  Activate the ServiceNow Otto for Setup Skill for Fix code in real-time.
5.  Navigate to **All** &gt; **ServiceNow Otto for Setup** &gt; **Skills**.

6.  On the Skills tab, select **Impact** from the navigation menu.

7.  On the Code Fix tile, select **Activate skill.**

    The button on the tile updates to **Deactivate skill** when the option has been selected and the status will show **Active**.

8.  Set the `sn_impact_gen_ai.ai_fix.enabled` property to true.

    **Note:** Enables the **Generate fixes with AI** button to display on script records.

9.  Navigate to **ALL** &gt; **System Properties** &gt; **sn\_impact\_gen\_ai.ai\_fix.enabled** &gt; **.**

10. Set the value to `true`.

    This value is set to `false` by default.

11. Assign users to have access to the Fix code in real-time panel.
12. Navigate to **All****sys\_user\_role.list**.

13. In the roles table search for `sn_impact_gen` and select the `sn_impact_gen_ai.ai_fix_user` role from the table to open the role details.

14. Assign the `sn_impact_gen_ai_.ai_fix_user` role to relevant users or groups.


**Parent Topic:**[Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-scan-engine-properties.md)

