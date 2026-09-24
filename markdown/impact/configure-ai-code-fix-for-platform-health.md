---
title: Configure real-time code resolution with AI
description: Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-ai-code-fix-for-platform-health.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure Scan Engine parameters, Activate Scan Engine and review settings, Impact Guided Setup, Configuring Impact, Impact]
---

# Configure real-time code resolution with AI

Follow these steps to configure real-time code resolution with AI suggested fixes for Impact Platform Health.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

Real-time messaging enforcement can be disabled on the Scan Engine properties page. When enforcement is disabled, users see the messaging but aren't required to make corrections for Act and Recommend findings.

Visibility of real-time messaging can also be configured to limit which users receive finding notifications. You can restrict messaging to a specific group.

## About this task

The following are minimum prerequisites:

-   Install and configure the Impact Store App. See [Configuring Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-impact-platform.md) for details.
-   Scan Engine configured: See [Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-initial-scan-engine-settings.md) for details.
-   Now Assist for Impact, version 3.03: See [Activate Now Assist Skills for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/activate-now-assist-skills-in-now-assist-for-impact.md) for details.
-   Now Assist for Platform, version 11.01

## Procedure

1.  Set system to enforce real-time validation.
2.  Navigate to **All** &gt; **** &gt; **Impact** &gt; **** &gt; **Configuration** &gt; **Scan Engine Properties**.

3.  On the **Real Time Scanning** related list, select **Enforce real-time validation**.

    Real-time Messaging must not be disabled, as the feature is tied to findings being present for either All users or Only users with role scan\_engine\_user.

    \[Omitted image "real-time-messaging-enabled.png"\] Alt text: Real time messaging visiblity enabled options.

4.  Activate the ServiceNow Otto for Setup Skill for Fix code in real-time. See [Activate Now Assist Skills for Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/activate-now-assist-skills-in-now-assist-for-impact.md) for additional information.
5.  Navigate to **All** &gt; **ServiceNow Otto for Setup** &gt; **Skills**.

6.  On the Skills tab, select **Impact** from the navigation menu.

7.  On the Code Fix tile, select **Activate skill.**

    The button on the tile updates to **Deactivate skill** when the option has been selected and the status will show **Active**.

8.  Select the `sn_impact_gen_ai.ai_fix.enabled` property.

    **Note:** Enables the **Generate fixes with AI** button to display on script records.

9.  Navigate to **ALL** &gt; **System Properties** &gt; **sn\_impact\_gen\_ai.ai\_fix.enabled** &gt; **.**

10. Set the value to `true`.

    This value is disabled by default.

11. Assign users to have access to the Fix code in real-time panel. See [Roles installed with Impact](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/impact-roles.md) for details.
12. Navigate to **All****sys\_user\_role.list**.

13. Assign the role to relevant users or groups.


**Parent Topic:**[Configure Scan Engine parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-scan-engine-properties.md)

