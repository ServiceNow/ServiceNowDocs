---
title: Create agentic workflows, agents, and skills
description: Build custom agentic workflows, AI agents, and skills for your applications using automated generation tools with Build Agent. You can streamline development by creating the necessary instructions, tools, and access controls based on your requirements.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Create agentic workflows, agents, and skills

Build custom agentic workflows, AI agents, and skills for your applications using automated generation tools with Build Agent. You can streamline development by creating the necessary instructions, tools, and access controls based on your requirements.

## Before you begin

If Now Assist for App Engine is not installed, then install it. For more information, see [Installing Now Assist for App Engine](../../app-engine-studio/task/install-now-assist-for-app-engine.md).

Verify that you have access to ServiceNow Studio or the ServiceNow IDE.

**Note:** Your licensing depending on whether you can work with agentic workflows, agents, and skills in Build Agent.

Skills must be published before they can be used as a tool by another skill.

Role required: admin

## About this task

Build Agent currently supports the following tool creation:

-   Skills:
    -   WebSearch
    -   Script - Inline
    -   Script - Explicit
    -   Now Assist Skill
    -   FlowAction\*
    -   SubFlow\*
-   Agents:
    -   Subflow
    -   Flow Action
    -   WebSearch
    -   Now Assist Skill
    -   Record Operations
    -   Script
    -   Catalog Item
    -   Conversational Topic

\*You can only use FlowActions and Subflows that are already part of your app scope, as Build Agent reuses existing FlowActions and Subflows instead of creating new ones.

Build Agent can recommend in-app agents tailored to specific application use cases.

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the corner of your browser. ![If Build Agent isn't open, open it from the status bar in the corner of your browser.](../../servicenow-studio/image/sn-studio-access-build-agent.png)

2.  Select your application from the Build Agent chat panel drop-down list.

3.  Enter a prompt describing the agentic workflow, agent, or skill that you want to create.

    For example:

    -   To create an agentic workflow: `Create an onboarding agentic workflow for contractors featuring three sequential AI agents:`
        -   `Intake Agent: Validates requests, conducts online background checks, verifies budget, and calculates costs using web searches and scripts.`
        -   `Background Check Agent: Assesses risk and performs tiered checks on identity, employment, credit, and references. Also verifies credentials and identifies necessary training.`
        -   `Provisioning Agent: Evaluates access needs, assigns equipment, generates credentials, provisions system access, finds training resources, and sends welcome packages.`
    -   To create an agent: `Create a Swag Fulfillment AI agent that can review and approve swag requests. The agent must review incoming swag requests, check inventory availability for all requested items, approve requests autonomously, update inventory, and request records when taking actions.`
    -   To create a skill: `Create a summarization skill that summarizes travel requests and provides approval suggestions based on the company’s travel policy.`
    Build Agent scans the application files, users, roles, permissions, and tables to endure that the requested skill or agent doesn't already exist. It then presents a plan that can include research, design, implementation, testing, and deployment phases. The plan can identify the key tools the agent needs, such as tools for checking inventory, updating requests, calculating costs, and logging decisions.

4.  Review and approve the plan by selecting **Approve plan**.

    ![Five-step plan for creating a swag management application](../image/ba-add-skill-1.png "Plan to create a skill")

    Build Agent starts creating the agentic workflow, agent or skill, along with its instructions, tools, access control lists \(ACLs\), and supporting scripts.

5.  When the build is complete, confirm the installation.

    Build Agent deploys the workflow, agent, or skill to the development environment.


## What to do next

-   If you have created an agentic workflow or agent, go to AI Agent Studio to review its properties, check triggers, and test it with the built-in tools.

    **Note:** The agent is published immediately. However, you must activate the associated triggers separately in AI Agent Studio.

-   If you have created a skill, use the Now Assist Skill Kit to test the agent with the built-in tools, make necessary changes, and publish the skill.

**Parent Topic:**[Use Build Agent](use-build-agent.md)

**Related topics**  


[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-agent-studio.md)

[Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md)

[Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-agent.md)

[Exploring Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/exploring-now-assist-skill-kit.md)

[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)

