---
title: Generative AI skills
description: Activate, configure, and manage the generative AI skills that enhance productivity across your workflows, and build custom skills for your organization's unique requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-generative-ai-skills.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [generative AI skills, Now Assist skills, Now Assist AI assets, Now Assist Skill Kit, Now Assist Admin console, custom skills]
breadcrumb: [Enable AI Experiences]
---

# Generative AI skills

Activate, configure, and manage the generative AI skills that enhance productivity across your workflows, and build custom skills for your organization's unique requirements.

## Generative AI

Generative AI skills apply large language models to your enterprise data to complete a single task within a workflow, such as summarizing a record or drafting a reply. To learn what they are, why they matter, and when to use them rather than an AI agent, see [About generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-understanding-generative-ai-skills.md).

## ServiceNow AI assets

AI assets are the building blocks that skills and agents use, including prompts, tools, and configurations. Some skills and agents are turned on by default when you install a product, so reviewing your active assets after installation is an important early step. To check which assets are on by default, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md)

## Generative AI skills

A skill delivers a generative AI feature plus the use case to the user. Skills are organized by the workflows they serve: IT Service Management, Customer Service Management, HR Service Delivery, and others. When you activate a product for a specific workflow, the associated skills become available. ServiceNow products provide features and skills tailored to meet the needs of users in different workflows.

**Note:** Start with high-impact, low-complexity skills like incident summarization or case summarization. These provide immediate value with minimal behavioral change required from your users.

To find the skills available for each workflow and activate the ServiceNow products that deliver them, see [Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skills/now-assist-skills.md).

## AI Skill Kit

AI Skill Kit is a development environment for building custom generative AI skills. A skill is a self-contained unit of generative AI functionality that runs a prompt against an LLM and returns a response. Skills can gather data using tools before the prompt runs, and can be deployed to the ServiceNow Otto panel, UI actions, flow actions, virtual assistants, and UI Builder.

Each skill is made up of a prompt \(the instruction template sent to the LLM\), inputs \(data passed in when the skill is triggered\), outputs \(the structured data the skill returns\), optional tools \(utilities that gather additional context before the prompt executes\), and deployment settings that control where the skill is available. AI developers create and test skills in AI Skill Kit, then publish them for a Now Assist admin to activate in AI Admin Hub.

To build, test, and publish custom skills with their own prompts, inputs, outputs, and deployment targets, see [AI Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-skill-kit/now-assist-skill-kit-landing.md).

## AI Admin Hub

The AI Admin Hub is where admins manage generative AI on the instance. Administrators install plugins, manage skills, choose which skills to turn on and which users can access them, and analyze usage and performance. The console provides a unified view of all active skills across your instance, making it straightforward to see what is running, where it is running, and how users are interacting with it. To install plugins, choose which skills are on and who can use them, and analyze usage across your instance, see [AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platform-now-assist-landing.md).

## ServiceNow AI Lens

ServiceNow AI Lens uses generative AI to read visual data — images, screenshots, scanned handwritten notes, and documents — extract the information it contains, and auto-fill forms with that data. Users can capture or upload content from a browser or the desktop application, preview what ServiceNow AI Lens extracts, and create or update records without manual data entry. ServiceNow AI Lens is a skill that administrators enable in the AI Admin Hub.

To scan images and documents, extract the data they contain, and auto-fill forms, see [ServiceNow AI Lens](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-lens/servicenow-lens-landing-page.md).

