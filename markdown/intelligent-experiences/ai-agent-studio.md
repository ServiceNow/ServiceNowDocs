---
title: AI Agent Studio
description: Create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ai-agent-studio.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Agentic AI, AI agents]
breadcrumb: [Explore, Now Assist AI agents, Enable AI experiences]
---

# AI Agent Studio

Create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

AI Agent Studio description and example guided setups for agents and agentic workflows 

## AI Agent Studio overview

With the AI Agent Studio application, you can create, manage, or test AI agents and agentic workflows all in one place. To enable the agentic AI experience, you must first install Now Assist AI agents. For more information, see [Install Now Assist AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/install-ai-agents-plugins.md).

The Overview page has three sections where you can find the information that you must understand, begin, and continue developing AI agents and agentic workflows. When you first go to the AI Agent Studio, tour points are available to guide you through the experience.

In the Ready-made agentic workflows and AI agents section, you can find the templates and ready-made AI agents and agentic workflows that you can incorporate as-is or in custom workflows that you create. You can even explore more templates to find the ones that best fit your needs.

In the Recent agentic workflows and AI agents activity section, you can find the agentic workflows or AI agents that have been created or configured most recently. On both List views, you can create, duplicate, or delete agentic workflows or AI agents. The tab also includes a link to the AI Agents Dashboard where you can review the details about AI agent usage and performance.

The third section is a card to open a modal with a journey checklist that describes the steps to incorporate the AI agents into your workflows successfully and a video that provides an overview of the AI agents and workflows to get you started. Select **View steps** to open this section.

The following example shows the Overview page of AI Agent Studio.

\[Omitted image "aia-studio-overview.png"\] Alt text: AI Agent Studio overview page.

## Managing agentic workflows and AI agents

From the AI Agent Studio Create and manage page, you can create, duplicate, or manage the existing agentic workflows and AI agents. This page has two tabs, one for agentic workflows and one for AI agents. You can edit the columns of the List view to change what information is displayed. You can also search or filter the Lists to find the agentic workflows and AI agents that you're looking for quickly. By selecting the name of the agentic workflow or AI agent, you can open Guided Setup to configure or reconfigure the agentic workflow or AI agent.

The following example shows the AI Agent Studio create and manage page after several Now Assist applications are installed.

\[Omitted image "aia-create-manage.png"\] Alt text: AI Agent Studio create and manage page.

## Agentic AI activity

The activity page contains execution logs for both agentic workflows and AI agents. The list allows you to filter based on various fields, including the version. For more information on creating multiple versions of the **List of steps** field, see [Version control for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/version-control.md).

The following example shows several execution logs in AI Agent Studio.

\[Omitted image "ais-activity.png"\] Alt text: AI Agent Studio activity page with list of AI agent and agentic workflow executions.

## Testing agentic AI

From the AI Agent Studio testing page, you can review the different tests for your AI agents and agentic workflows, both manual and automated. You can test the performance of your agentic AI by simulating a single execution manually, or you can use [automated agentic evaluations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/execute-aia-eval.md) for testing multiple executions. Single tests are best for evaluating whether the AI agent or agentic workflow does what you expect it to. Agentic evaluations are better at finding underlying patterns and trends that may not be noticeable one execution at a time.

**Note:** The testing feature does not support the Now Assist panel assistance for live agent interactions. To connect to a live agent, use Now Assist in Virtual Agent instead. Otherwise, during live agent chat sessions, requester and agent users may be logged out unexpectedly due to sessions expiring prematurely.

There are two types of manual tests you can do: **AI agent or agentic workflow** to test execution or **Test access** to test security controls. You can view your executed tests in the two tabs of the testing page. For manual execution tests, you can select the reply button to repeat the test. You can open the full details page of an automated test by selecting the test's name in the list in the **Automated** tab.

The following example shows the inputs for a Generate Resolution Plan agentic workflow testing setup of AI Agent Studio.

\[Omitted image "aia-test-page-new.png"\] Alt text: AI Agent Studio testing home page

\[Omitted image "aia-test-playground.png"\] Alt text: AI Agent Studio testing playground

## AI Agent Studio settings

From the AI Agent Studio Settings page, you can enable Now Assist Guardian for your AI agents. By using Now Assist Guardian, you can configure:

-   [Offensiveness detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-aia-na-guardian.md)
-   [Prompt injection attempt decision](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-aia-na-guardian.md)
-   [Long-term memory for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/long-term-memory-aia.md)

The following image shows the AI Agent Studio settings.

\[Omitted image "aia-settings-new.png"\] Alt text: AI Agent Studio settings page.

## AI Agent Analytics dashboard

From the AI Agent Analytics dashboard, you can review the vital statistics about your AI agents and agentic workflows. You can see the data about the number of agents and agentic workflows used, time-to-resolution efficiency gain, and the number of executions.

The following example shows the overview page for the AI Agent Analytics dashboard.

\[Omitted image "ais-analytics-dashboard.png"\] Alt text: AI Agent Analytics dashboard overview page.

