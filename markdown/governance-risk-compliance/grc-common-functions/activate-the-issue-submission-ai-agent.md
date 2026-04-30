---
title: Activate the Report a GRC issue AI agent
description: Configure and activate the report a GRC issue AI agent to guide employees in reporting GRC issues from the Employee Center with clarity and context.
locale: en-US
release: yokohama
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-11-15"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, report a GRC issue]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate the Report a GRC issue AI agent

Configure and activate the report a GRC issue AI agent to guide employees in reporting GRC issues from the Employee Center with clarity and context.

## Before you begin

Install the Now Assist for Integrated Risk Management \(IRM\) plugin \(sn\_irm\_gen\_ai\), and ensure that they are upto date.

Role required: sn\_nowassist\_admin.nsa\_admin or sn\_aia.admin.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  In the Recent agentic workflows and AI agents activity section, select **AI agents**.

3.  From the list of available AI agents, select **Report a GRC issue**.

    ![](../../grc-common-workspace/image/report-a-grc-issue.png)

4.  Select the Define the specialty section, review the fields, and confirm that the AI agent meets your requirements.

    If it doesn't meet your requirements, you can edit the AI agent. To modify the report a GRC issue AI agent, [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

5.  Select the Add tools and information section to review the skills, scripts, and tools available for the AI agent to perform its role.

6.  Select the Define Security Controls section to review:

    -   User access: Users who can access and interact with the AI agent \(an ACL is generated automatically\).
    -   Data access: The user identity that the agent runs as, which determines roles and data access permissions.
7.  Select **Add triggers** and configure conditions that start the AI agent.

    Triggers can include record conditions, schedules, or inbound email.

    For more information, see [Add a trigger to an AI agent](https://www.servicenow.com/docs/access?context=add-trigger-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

8.  Select **Channels and status** to choose the channels where this AI agent will be available for users to initiate interactions, and set its availability status.

    For more information, see [Select channels and status for an AI agent](https://www.servicenow.com/docs/access?context=channels-access-aia&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

9.  Select **Save and test**.

    The Test one example of behavior page opens where you can test how the AI agent completes a task.


## What to do next

Use the Testing playground to [Manually test the execution of an AI agent](https://www.servicenow.com/docs/access?context=test-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) using example utterances.

If activation fails, check roles and skill configuration.

**Related topics**  


[Post activation indexing and customization](post-activation-indexing-and-customization_0.md)

[Report a GRC issue](report-a-grc-issue.md)

