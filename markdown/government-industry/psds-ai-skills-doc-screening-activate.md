---
title: Activate the Document screening Al skill in Now Assist for PSDS
description: Activate the Document screening Al skill to use Now Assist for PSDS gen-AI to screen documents in the Social Benefits Playbook, classifying document types, validating them against what's expected for the case, flagging issues and providing clear explanations, and giving agents Al-composed messages to send back to constituents with specific resubmission instructions.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activate Now Assist skills, Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Activate the Document screening Al skill in Now Assist for PSDS

Activate the Document screening Al skill to use Now Assist for PSDS gen-AI to screen documents in the Social Benefits Playbook, classifying document types, validating them against what's expected for the case, flagging issues and providing clear explanations, and giving agents Al-composed messages to send back to constituents with specific resubmission instructions.

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

-   Confirm that the following applications and plugins are installed:

    -   Now Assist in Document Intelligence \(sn\_docintel\_gen\_ai\)
    -   Document Processor \(sn\_doc\_processor\)
    -   Service Applicant Information \(sn\_svc\_appl\_info\)
    -   Now Assist for Public Sector Digital Services \(PSDS\)
    -   Social Benefits Playbook, Grants Management, **or** License and Permit Playbook
    For more information on configuring Now Assist in Document Intelligence, see Configuring Now Assist in Document Intelligence.

-   Perform this task in your ServiceNow instance, ensuring the Now Assist for Public Sector Digital Services \(PSDS\) Application scope is selected.
-   Role required: admin

**Note:** Now Assist Admin Console \(sn\_nowassist\_admin\) and Now Assist for Platform \(sn\_genai\_platform\) plugins must be installed.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Now Assist Skills**.

2.  In the workflow list, select **Customer** &gt; **PSDS**.

3.  On the card for the Document screening Al skill, select **Turn on**.

    ![Document screening Al skill card that displays the skill to be turned on.](../image/psds-activate-doc-screening-skill.png)

4.  Configure user access on the pop-up modal to specify who can utilize this skill.

    Access control lists \(ACLs\) are implemented to identify the users permitted to access this skill, and are generated automatically\).

5.  Select **Turn on**.

6.  In the dialog box, select **Back to skills**.

7.  Verify that the skill is activated on the Document Screening Al skill card.

    ![Document screening Al skill is active.](../image/psds-doc-screening-skill-activated.png)


