---
title: LEAP AI agent
description: Enhance IT operations with AI-driven, autonomous artifact creation such as problem records, knowledge base articles, and playbooks using LEAP AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/leap-ai-agent.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-06-30"
reading_time_minutes: 2
keywords: [LEAP AI agent, knowledge base article, problem record, AIOps LEAP]
breadcrumb: [Explore, Learning Enhanced Automation Platform \(LEAP\), ITOM Visibility, IT Operations Management]
---

# LEAP AI agent

Enhance IT operations with AI-driven, autonomous artifact creation such as problem records, knowledge base articles, and playbooks using LEAP AI agent.

**Important:**

Generative AI may produce inaccurate or incomplete information. Always validate AI-generated content before you publish or act on it.

## Generate LEAP artifacts

|AI agent|AI agent role|
|--------|-------------|
|LEAP AI agent|Uses the automation opportunities created by LEAP analysis, and creates artifacts \(problem records, knowledge base articles, or playbooks\) requested by users.|

**Important:** This AI agent is turned on by default. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## What the LEAP AI agent does

The LEAP AI agent autonomously scans active automation opportunities and acts on the ones that have resolution steps, so that IT operations teams spend less time triggering automation manually. The agent provides the following capabilities:

-   **Create knowledge base articles**

    The agent is triggered when resolution steps for automation opportunities are generated successfully to document and generate a draft knowledge base article that includes the automation opportunity title, resolution steps, and related incident context. You review the draft and publish it. Each published article remains traceable to its source automation opportunity. The agent doesn't create a knowledge base for an automation opportunity that is already linked to an open KB.

-   **Create problem records**

    The agent is triggered when resolution steps for automation opportunities are generated successfully and automatically creates a problem record. Each problem record is populated with the related incident count, the automation opportunity detail, and the associated resolution notes, which mirrors the manual **Create Problem** action. The agent doesn't create a problem record for an automation opportunity that is already linked to an open problem. Each problem record remains traceable to its source automation opportunity.


## Eligibility thresholds

An automation opportunity is eligible for knowledge base article and problem record creation when it has a minimum of 15 incidents or a severity of Critical or High. You can change the incident count threshold \(default: 15\) and the severity threshold \(default: Critical and High\) on the LEAP Settings page. For the list of settings, see [LEAP settings fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-settings-fields.md).

## Identify AI-created artifacts

Artifacts that the LEAP AI agent creates are marked with an AI indicator on the home page and the automation opportunity details page, so that you can tell AI-created artifacts apart from those created manually. For more information, see [LEAP AI indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-ai-indicators.md).

## Activate or deactivate the LEAP AI agent

The LEAP AI agent is active by default. To change the activation status, navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**, select the LEAP AI agent, then go to **Agent** &gt; **Select channels and status** and toggle the **activation status** control.

-   Active: The agent scans automation opportunities and creates artifacts automatically.
-   Inactive: The agent stops scanning automation opportunities and no longer creates artifacts.

