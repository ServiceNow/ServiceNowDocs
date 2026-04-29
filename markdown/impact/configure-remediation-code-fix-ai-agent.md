---
title: Configure Remediate Scan Engine findings with Now Assist
description: Follow these steps to configure the Remediate Scan Engine findings with Now Assist feature for Impact Platform Health.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remediate Scan Engine findings with Now Assist, Now Assist for Platform Health, Platform Health, Using Impact, Impact]
---

# Configure Remediate Scan Engine findings with Now Assist

Follow these steps to configure the Remediate Scan Engine findings with Now Assist feature for Impact Platform Health.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## About this task

The following are minimum prerequisites:

-   Install and configure the Impact Store App. See [Configure the Impact Store Application](../concept/configuring-impact-platform.md) for details.
-   Scan Engine configured: See [Activate Scan Engine and review settings](configure-initial-scan-engine-settings.md) for details.
-   Now Assist for Impact v.3.03: See [Activate Now Assist skills in Now Assist for Impact](../concept/activate-now-assist-skills-in-now-assist-for-impact_0.md) for details.
-   Now Assist for ServiceNow AI Platform v11.0.1

## Procedure

1.  Activate the Now Assist Skill for Resolve Scan Engine findings:

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

3.  On the Now Assist Skills tab, select **Impact** from the navigation menu.

4.  On the Code Fix tile, select **Activate skill.**

    ![The Now Assist Admin Console with the Impact Code Fix activation tile displayed.](../image/impact-activate-skill-now-assist-adminpanel.png)

    The button on the tile updates to **Deactivate skill** when the option has been selected and the status will show **Active**.

5.  Set the `sn_impact_gen_ai.ai_fix.enabled` property to true:
6.  Navigate to **All** &gt; **System Properties** &gt; **sn\_se\_properties.list** &gt; **Scan Engine Properties** &gt; **.**

7.  Set the **sn\_impact\_gen\_ai.ai\_fix.enabled** value to `true`.**.**

    This value is set to `false` by default.

    ![System property to enable the gen_ai.ai_fix.enabled functionality.](../image/code-fix-ai-sys-property.png)

8.  Assign users to have access to the Resolve Scan Engine findings panel:
9.  Navigate to **All****sys\_user\_role.list**.

10. In the roles table search for and assign the `sn_impact_code_fix_ai.ai_user` role to relevant users or groups.


