---
title: Create agentic workflows, agents, and skills
description: Build custom agentic workflows, AI agents, and skills for your applications using automated generation tools with Build Agent. You can streamline development by creating the necessary instructions, tools, and access controls based on your requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/create-custom-ai-agent.html
release: zurich
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use, Build Agent, Agentic development on the ServiceNow AI Platform, Developing your application, Building applications]
---

# Create agentic workflows, agents, and skills

Build custom agentic workflows, AI agents, and skills for your applications using automated generation tools with Build Agent. You can streamline development by creating the necessary instructions, tools, and access controls based on your requirements.

## Before you begin

Skills must be published before they can be used as a tool by another skill.

**Note:** Check your entitlements to determine whether you have access to agentic workflows, agents, and skills in Build Agent.

Role required: admin

## About this task

For details on creating agentic workflows, agents, and skills, see [Agentic workflows, agents, and skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ba-about-creating-in-app-agents.md).

## Procedure

1.  Navigate to **All** &gt; **App Development** &gt; **ServiceNow Studio**.

    You can also open Build Agent in the ServiceNow IDE if you prefer a more code-centric experience.

    The Build Agent chat panel opens by default in new ServiceNow Studio sessions. If the panel isn't open, select **Open Build Agent** from the status bar in the lower corner of your browser. You can also select the Sparkle icon \[Omitted image "ba-sns-ai-sparkle.png"\] Alt text: in the application banner.\[Omitted image "sn-studio-access-build-agent.png"\] Alt text: If Build Agent isn't open, open it from the status bar in the corner of your browser.

2.  Select your application from the Build Agent chat panel drop-down list.

3.  Prompt to add AI to your app in one of two ways.

    -   Enter a prompt describing the agentic workflow, agent, or skill that you want to create. For example:
        -   To create an agentic workflow: `Create an onboarding agentic workflow for contractors featuring three sequential AI agents:`
            -   `Intake Agent: Validates requests, conducts online background checks, verifies budget, and calculates costs using web searches and scripts.`
            -   `Background Check Agent: Assesses risk and performs tiered checks on identity, employment, credit, and references. Also verifies credentials and identifies necessary training.`
            -   `Provisioning Agent: Evaluates access needs, assigns equipment, generates credentials, provisions system access, finds training resources, and sends welcome packages.`
        -   To create an agent: `Create a Swag Fulfillment AI agent that can review and approve swag requests. The agent must review incoming swag requests, check inventory availability for all requested items, approve requests autonomously, update inventory, and request records when taking actions.`
        -   To create a skill: `Create a summarization skill that summarizes travel requests and provides approval suggestions based on the company's travel policy.`
        -   If you don't know what agents or skills you need: `Analyze my application. Review the tables, fields, business rules, and workflows. Identify the most repetitive manual tasks that fulfillers perform and suggest which ones could benefit from AI agent or skill.`
    -   Select the **Add AI to my app** button and follow the prompts.

        \[Omitted image "ba-add-ai-button.png"\] Alt text: Now Assist chat panel with the Add AI to button highlighted.

        **Note:**

        -   Depending on your licensing, the button may not be available.
        -   You must be on Australia Patch 3 or higher for the button to appear.
4.  Review and approve the plan by selecting **Approve plan**.

    \[Omitted image "ba-add-skill-1.png"\] Alt text: Five-step plan for creating a swag management application

    Build Agent starts creating the agentic workflow, agent, or skill, along with its instructions, tools, access control lists \(ACLs\), and supporting scripts.

5.  When the build is complete, confirm the installation.

    Build Agent deploys the workflow, agent, or skill to the development environment.


## What to do next

After Build Agent generates agents and skills, complete the following steps to move them from creation to production.

1.  Test each skill in Now Assist Skill Kit to validate prompt behavior against sample records and review output quality before publishing.
2.  Test the agent in AI Agent Studio to validate the end-to-end workflow and confirm that tool invocations work correctly.
3.  Activate triggers in AI Agent Studio. Triggers are not activated automatically and must be enabled separately after generation.
4.  Deploy the custom app with its agents and skills as a standard update set.

**Parent Topic:**[Use Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/use-build-agent.md)

**Related topics**  


[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/ai-agent-studio.md)

[Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/configure-next-best-action-agent.md)

[Manually test the execution of an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/test-ai-agent.md)

[Exploring Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit/exploring-now-assist-skill-kit.md)

[Test a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit/test-prompt-template.md)

