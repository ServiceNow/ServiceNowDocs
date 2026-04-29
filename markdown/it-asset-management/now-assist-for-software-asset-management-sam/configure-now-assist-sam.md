---
title: Configuring Now Assist for Software Asset Management \(SAM\)
description: If you have the admin role, you can configure the Now Assist for Software Asset Management \(SAM\) application to use generative AI skills in the Software Asset Workspace.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Configuring Now Assist for Software Asset Management \(SAM\)

If you have the admin role, you can configure the Now Assist for Software Asset Management \(SAM\) application to use generative AI skills in the Software Asset Workspace.

## Before you begin

Role required: admin

## About this task

Starting with the Zurich Patch 4 release, generative AI skills for Now Assist for SAM are automatically activated on your instance by default and require no configuration. However, if you deactivate a skill, you need to manually reactivate that skill by following the specified procedure.

## Procedure

1.  Install the Now Assist for Software Asset Management \(SAM\) plugin \(sn\_now\_assist\_sam\).

2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** to access the **Now Assist Skills** tab of the Now Assist Admin console.

3.  Select **SAM** under the **Technology** workflow group.

4.  On the Now Assist skills for SAM page, select **Activate skill** for the skill that you would like to activate.

    The page for the skill that you activated opens with the General details section highlighted.

5.  In the General details section, select **Save and continue**.

    The settings in the General details section are read-only.

6.  In the Select display section, select **Display**.

    ![Display mode option.](../image/now-assist-sam-display.png)

    When selected, the skill is displayed on forms and workspaces.

    The sam\_user role is the default role for viewing the skill. You can add additional roles if you want to.

    Custom role configurations for accessing generative AI skills are preserved. For example, if you added an alternative role such as the sam\_admin role instead of the default sam\_user role, the sam\_admin role will retain access, while the sam\_user role will lose access, as per the custom configuration.

7.  Select **Save and continue**.

8.  In the Review and activate section, review your choices and select **Activate**.

    The Successfully activated message box opens and the skill is activated. You're ready to use the skill in the Software Asset Workspace. For details on using the skills, see [Using generative AI skills in Now Assist for SAM](../concept/using-now-assist-sam.md).


-   **[Skill inputs and triggers for Now Assist for Software Asset Management \(SAM\)](../reference/now-assist-sam-skills-inputs.md)**  
Get a quick overview of the skill inputs and triggers for Now Assist for Software Asset Management \(SAM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

**Parent Topic:**[Now Assist for Software Asset Management \(SAM\)](../concept/now-assist-sam.md)

