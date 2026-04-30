---
title: Configure Sidebar Summarization
description: Configure sidebar summarization to generate summaries of sidebar discussions for quick agent understanding, allowing for faster collaboration.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 2
breadcrumb: [Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Configure Sidebar Summarization

Configure sidebar summarization to generate summaries of sidebar discussions for quick agent understanding, allowing for faster collaboration.

## Before you begin

Role required: admin

Sidebar summarization is generated from the information within selected tables containing specific case, incident, or interaction information.

## Procedure

1.  Navigate to **Admin &gt; Now Assist Admin &gt; Skills**.

2.  Select the **Customer** workflow, and **CSM** as the product.

3.  Activate Skill for the **Sidebar Summarization** skill.

    Each skill has a guided setup with multiple steps. A check symbol next to each step indicates whether its setup is complete, partially complete, or incomplete. After configuring a step, select **Save and continue** to move forward, or **Back** to return to a previous step.

4.  Select **Define triggers** and switch the toggles to choose how and when the summarization is configured.

    |Trigger|Description|
    |-------|-----------|
    |Quick action|Sidebar summary that is generated when the live agent performs the `/summarize` quick action.|

    You can also select toggle a property that controls how a sidebar summary is displayed.

    |Property|Description|
    |--------|-----------|
    |Bulleted list|Sidebar summary as an unordered list.|

5.  Select **Choose tables** to select the tables from which summaries for Sidebar discussions are generated.

    |Label|Name|
    |-----|----|
    |Change Phase|change\_phase|
    |Change Request|change\_request|
    |IMAC|change\_request\_imac|
    |Change Task|change\_task|
    |Chat Queue Entry|chat\_queue\_entry|
    |Incident|incident|
    |Incident Task|incident\_task|
    |Interaction|interaction|
    |Knowledge Feedback Task|kb\_feedback\_task|
    |Problem|problem|
    |Problem Task|problem\_task|
    |Request|sc\_request|
    |Requested Item|sc\_req\_item|
    |Catalog Task|sc\_task|
    |Standard Change Proposal|std\_change\_proposal|

6.  Select **Define access** to determine who can access this skill.

    By selecting specific roles, you're controlling who can use it. The roles you choose will also be available in the next step **Select display**.

    Default and Custom Roles:

    -   If no changes are made, the default role sn\_esm\_agent will automatically appear in **Define Access** and **Select Display**.
    -   If custom roles were added before the upgrade, they’ll be updated automatically by a script.
    -   If new roles are created after the upgrade, you’ll need to manually add them in both the **Define Access** and **Select Display**.

        **Note:** In the **Select Display** step, you can only choose roles that were added in the **Define Access** step. If you add a role in **Define Access**, you still need to manually select it in **Select Display** to make it active.

7.  Toggle **Select display** to determine if sidebar summarization appears in In-product desktop, displaying Now Assist skills on forms and workspaces.

8.  After selecting **Review and Activate** to examine changes, select **Done** to close the sidebar summarization generation settings.

9.  Select **Activate** to turn on the skill for agents and complete the configuration.


