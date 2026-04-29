---
title: Configure the Investigative case narrative refinement skill in Now Assist for Public Sector Digital Services \(PSDS\)
description: Activate and customize the Investigative case narrative refinement skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that investigators can use the generative AI skills in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-04"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist skills, Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure the Investigative case narrative refinement skill in Now Assist for Public Sector Digital Services \(PSDS\)

Activate and customize the Investigative case narrative refinement skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that investigators can use the generative AI skills in CSM Configurable Workspace.

## About this task

The Investigative Case Management Case narrative refinement skill helps investigators refine a investigative case narrative or case summary for tone, length, and clarity. By activating and using this configuration, investigators can adjust the case summary or narrative with one of several options: Casual, Formal, Shorten, or Elaborate.

## Before you begin

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. The default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills, agents, or agentic workflows are turned on automatically.

-   **Existing customers who are upgrading \(starting with Australia Patch 4\)**

    There is no change to skills, agents, or agentic workflows that are currently enabled and customized.

    An AI asset is turned on if:

    -   The Now Assist plugin is installed, but the asset was never turned on.
    -   An admin has never adjusted roles for the skill.
    An AI asset is not turned on if:

    -   The asset was previously turned on, and then turned off again.
    -   An admin has adjusted roles for the asset.

For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

-   Confirm that the following applications and plugins are installed:

    -   Now Assist for Public Sector Digital Services \(PSDS\)
    -   Investigative Case Management
    **Note:** Now Assist Admin Console \(sn\_nowassist\_admin\) and Now Assist for Platform \(sn\_genai\_platform\) plugins must be installed.

-   Perform this task in your ServiceNow instance, ensuring the Now Assist for Public Sector Digital Services \(PSDS\) Application scope is selected.
-   Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Experiences**.

2.  In the side panel workflow list, select **Now Assist Context Menu**, and select the Configurations related list.

3.  Select **ICM Case Narrative**.

4.  Select the more actions \(![](../image/more-actions-na-psds.png)\) icon for that record, and select **Activate** or **Deactivate**.

    **Note:** This configuration is Activated by Default.

    ![Case narrative refinement Al skill configuration list that displays the skill already activated.](../image/psds-cns-configure.png)

5.  To edit the configurations of this skill, select **Edit Configurations**.

6.  In the workflow side panel, select Configure Experience.

    Here, you can change the default actions for the skill when the AI sparkle icon \(![](../../../common/image/icon-ai-sparkle.png)\) context menu is selected in the case narrative field. You can also add and configure tones as necessary for the case narrative output. Tones such as Casual, Formal, Shorten and Elaborate are selected by default.

7.  Select **Save and Continue** whenever prompted.

8.  Verify that the skill is activated and configured by going to an Investigative case narrative field and opening the Now Assist Context menu.

    ![Case narrative refinement Al skill is active.](../image/psds-narrative-skill-activated.png)


