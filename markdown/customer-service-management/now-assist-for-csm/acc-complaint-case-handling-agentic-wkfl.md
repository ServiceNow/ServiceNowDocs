---
title: Configure the Accelerate Complaint Case Handling agentic workflow
description: Configure the Accelerate Complaint Case Handling agentic workflow by defining key requirements and security controls. The workflow is then tested and made available through various channels.
locale: en-US
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Accelerate complaint case handling collection, Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Configure the Accelerate Complaint Case Handling agentic workflow

Configure the Accelerate Complaint Case Handling agentic workflow by defining key requirements and security controls. The workflow is then tested and made available through various channels.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage.**.

2.  Select **Accelerate Complaint Case Handling**.

3.  Define the key requirements.

    For more information on defining key requirements, refer to [General guidelines for creating AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=gg-creating-aia&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

    1.  Write a clear description and list of steps.

    2.  Add AI agents that can perform these steps or ask Now Assist to suggest AI agents.

    3.  From the list, select any LLM providers that this agentic workflow does not support.

    4.  Select **Save and continue**.

4.  Define the security controls for this workflow.

    1.  Define user access.

        These include the following:

        -   Any authenticated user: Any logged-in user can access this AI agent.
        -   Users with specific roles: select specific roles that can access this AI agent.
        -   Public: anyone can access this AI agent, even if they are not logged in.
    2.  Define data access: Select the user identity type this agentic workflow will run as.

        These include the following:

        -   Dynamic user: This can be the sys\_user of a trigger, agentic workflow, or user that passes its roles to this AI agent.
        -   AI user: This is a type of sys\_user only for agentic workflows and AI agents, with pre-defined roles.
    3.  Select **Save and continue**.

5.  Add triggers.

    You can add triggers if you want an agentic workflow or AI agent to launch according to pre-defined rules, and you want to spare your users the effort of reaching out for help, add a trigger.

    If you do not add triggers, the workflow executes only in response to users' requests for help.

6.  Select channels and status.

    Select the channels where you want this agentic workflow to be available for users.

    -   Engage via the Now Assist panel: When users send a message to Now Assist, they can discover and use this workflow.

    -   Engage via UI actions on specific records: When users select a UI action displayed on certain records, this workflow is activated.
7.  Select **Save and test**.


