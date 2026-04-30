---
title: Customize Now Assist context menu for skills
description: If you have the admin role, you can customize a Now Assist for Customer Service Management \(CSM\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.
locale: en-US
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Configure, Now Assist for CSM, Customer Service Management]
---

# Customize Now Assist context menu for skills

If you have the admin role, you can customize a Now Assist for Customer Service Management \(CSM\) skill so that agents can use the generative AI skills in CSM Configurable Workspace and in Core UI.

## Before you begin

Role required: admin

**Note:**

The Now Assist context menu configuration is accessible through the Now Assist Experiences in Now Assist Admin console. After activating the relevant skills, users are prompted to visit the Case NACM Config however, in the base system , configuration is already active. By default, it is configured to use extended tables for the resolution notes and activity response generation skill that is provided in the base system.

Case NACM Config is currently only available for resolution notes and activity response generation skill.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

2.  Select Now Assist context menu.

3.  Open the **Configuration** tab to view all the existing configurations.

4.  Find the configuration name **Case NACM Config**.

5.  Under Action, select the ![More actions](../image/csm-ws-dashboards-more-actions-icon.png)icon

6.  Select **Edit configuration**.

7.  In the guided setup, go to **General details** and customize the table name.

8.  Select the **Record form fields** for table form use cases.

    The form fields are active for close notes, additional comment and work notes.

9.  Select **Save and continue**.

10. Select **Configure Experience**, to configure the actions for the context menu trigger button and dialog.

    There are separate configurations for close notes, additional comment and work notes. Default action configured is **Generate resolution notes**.

    1.  Configure the **Actions** to **Generate resolution notes**, **Shorten** and **Elaborate**.
    2.  Configure the **Refinement actions** to **Shorten** and **Elaborate**.
    3.  Configure the **Actions for generated content** to **Insert**.
    In the preview you can see how the Now Assist context menu button will look like after configuration.

    By default, the **Enable support for extended tables** toggle is turned on and this configuration is shipped as active in the base system. This is to support sparkle on extended table on same field. Once the skill is active, this experience is available.

11. Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default roles n\_customerservice\_agent and sn\_customerservice.consumer\_agent automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they are updated automatically by a script.
    -   If new roles are created after the upgrade, you can manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still must manually select it in **Select Display** to make it active.

12. **Select Display** to determine where to display the Case NACM Config.

    -   Select In-product desktop to show Case NACM Config in all customer products on forms and workspaces.
    -   Select roles for whom NACM config will be displayed.
13. In**Review and Activate** select **Activate** to activate Now Assist context menu for the skill.

    A record with the specific usage conditions can be selected from the dropdown to test the configuration.

    Now Assist context menu has been successfully activated.

14. Select **Return to Customer** to complete and save this section.


