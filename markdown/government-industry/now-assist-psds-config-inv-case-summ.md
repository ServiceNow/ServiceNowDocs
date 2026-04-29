---
title: Configure the Investigative case summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)
description: Activate and customize the Investigative case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that investigators can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist skills, Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure the Investigative case summarization skill in Now Assist for Public Sector Digital Services \(PSDS\)

Activate and customize the Investigative case summarization skill in the Now Assist for Public Sector Digital Services \(PSDS\) application so that investigators can use the generative AI skills in CSM Configurable Workspace and in Public Sector Digital Services Core UI.

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

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  In the workflow list, select **Customer** &gt; **PSDS**.

3.  On the card for the Investigative case summarization Al skill, select **Activate Skill**.

    ![Investigative case summarization Al skill card that displays the skill to be activated.](../image/psds-nowassist-ics-activate.png)

4.  In the General details section, select **Save and continue**.

5.  In the View input section, select **Save and continue**.

6.  In the Customize prompt section, select **Save and continue**.

7.  Define how the skill is available to your users.

8.  Configure user access on the pop-up modal to specify who can utilize this skill.

    Access control lists \(ACLs\) are implemented to identify the users permitted to access this skill, and are generated automatically.

9.  Toggle the Display property to **On** in the In-product card and Now Assist panel to configure where to display the case summarization.

    This is what allows the case summarization card to show in the Investigative Case Management workspace page.

10. Review your choices and select **Activate** to complete the skill customization.

11. Verify that the skill is activated on the Investigative case summarization skill card.

    ![Document screening Al skill is active.](../image/psds-doc-screening-skill-activated.png)


