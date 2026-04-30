---
title: Configure Fix code in real-time for Platform Health
description: Follow these steps to configure Fix code in real-time for Impact Platform Health.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [Fix code in real-time with Now Assist, Scan Engine, Platform Health, Using Impact, Impact]
---

# Configure Fix code in real-time for Platform Health

Follow these steps to configure Fix code in real-time for Impact Platform Health.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

## About this task

The following are minimum prerequisites:

-   Install and configure the Impact Store App. See [Configure the Impact Store Application](configuring-impact-platform.md) for details.
-   Scan Engine configured: See [Activate Scan Engine and review settings](../task/configure-initial-scan-engine-settings.md) for details.
-   Now Assist for Impact, version 3.03: See [Activate Now Assist skills in Now Assist for Impact](activate-now-assist-skills-in-now-assist-for-impact_0.md) for details.
-   Now Assist for Platform, version 11.01

## Procedure

1.  Set system to enforce real-time validation.
2.  Navigate to Scan Engine Properties System properties \(`sn_se_properties.list`\).

3.  On the Real Time Scanning related list, set **Enforce real-time validation** to true

    Real Time Messaging must be activated, as the feature is tied to findings being present.

4.  Activate the Now Assist Skill for Fix code in real-time.
5.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

6.  On the Now Assist Skills tab, select **Impact** from the navigation menu.

7.  On the Code Fix tile, select **Activate skill.**

    ![The Now Assist Admin Console with the Impact Code Fix activation tile displayed.](../image/impact-activate-skill-now-assist-adminpanel.png)

    The button on the tile updates to **Deactivate skill** when the option has been selected and the status will show **Active**.

8.  Set the `sn_impact_gen_ai.ai_fix.enabled` property to true.

    **Note:** Enables the Fix with Now Assist button to display on script records.

9.  Navigate to **ALL** &gt; **System Properties** &gt; **sn\_impact\_gen\_ai.ai\_fix.enabled** &gt; **.**

10. Set the value to `true`.

    This value is set to `false` by default.

11. Assign users to have access to the Fix code in real-time panel.
12. Navigate to **All****sys\_user\_role.list**.

13. In the roles table search for `sn_impact_gen` and select the `sn_impact_gen_ai.ai_fix_user` role from the table to open the role details.

14. Assign the `sn_impact_gen_ai_.ai_fix_user` role to any users or groups to use the Gen AI feature.


