---
title: Explore AI Agent Studio
description: Create, manage, and test AI agents and agentic workflows in one centralized space to build self-executing solutions that help you achieve your business goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-agent-studio-new.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 5
keywords: [Agentic AI, AI agents, Agentic workflows]
breadcrumb: [AI Agent Studio, Enable AI experiences]
---

# Explore AI Agent Studio

Create, manage, and test AI agents and agentic workflows in one centralized space to build self-executing solutions that help you achieve your business goals.

## AI Agent Studio overview

With the AI Agent Studio, you can create, manage, and test AI agents and agentic workflows all in one place. To enable the agentic AI experience, you must first install AI agents. For more information, see [Install ServiceNow Otto AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-ai-agents-plugins.md).

The AI Agent Studio home page provides an overview of your agentic AI environment with recently edited items and a library of prebuilt automations. From the home page, you can access the Library of prebuilt automations, which includes featured items, AI agents for tasks, and agentic workflows for processes.

\[Omitted image "ai-agent-studio-new.png"\] Alt text: AI Agent Studio home page showing Design AI agents using your enterprise data with recently edited items and library of prebuilt automations.

## Automation opportunities

The AI Agent Studio home page also lists automation opportunities identified from your instance data, each with an estimated cost saving and time saving. You can use the list to decide which automations to build first.

Cost and time saving estimates are derived from the number of records analyzed for the opportunity, the average handling time for those records, and a standard labor rate. The figure is an annualized projection rather than a measured result, and it is rounded for display. Read the inputs before treating a figure as a business case: a large headline number usually reflects a high record volume rather than a large saving on any single record.

If you select **View all automation opportunities**, you can sort the list by column and filter it by estimated cost saving and estimated time saved.

Selecting an opportunity displays a preview that summarizes the AI agent, including possible tools. The count is the number of tools the opportunity is expected to require, not the number that already exist on your instance. The preview also lists resolution steps for the task being automated. These are evidence that the task can be automated. They are not an implementation plan, and they are not the full AI agent instructions. You can make edits to the instructions during the build process.

Building from an opportunity opens the guided setup with the opportunity context applied.

## Managing agentic workflows and AI agents

From the Agentic solutions section in AI Agent Studio, you can create, duplicate, or manage existing AI agents and agentic workflows. The Agentic solutions page contains tabs for Recently edited, AI agents, Agentic workflows, and AI specialists. You can customize the list view columns to display the information that matters most to you. Search and filter options enable you to quickly find the agentic AI assets you're looking for. By selecting the name of an AI agent or agentic workflow, you can open the guided setup to configure or reconfigure it.

The tabs are scoped by type: AI agents lists individual agents, Agentic workflows lists workflows, AI specialists lists role-level solutions, and Recently edited lists items you have opened or changed regardless of type. You can also search for an agentic AI asset by name on any tab.

\[Omitted image "aia-studio-agentic-solutions-tab.png"\] Alt text: AI Agent Studio Agentic solutions tab displaying list of AI agents with name, description, agent type, tools, created by, updated, model support, application, and status columns.

## Node map view

When you select an AI agent or agentic workflow from the Agentic solutions list, you're taken to the node map view. In the node map, you can see the structure of your agentic AI asset. For agentic workflows, the node map displays all the AI agents that make up the workflow. For AI agents, the node map displays all the tools configured for that agent.

From the node map, you can select the edit icon on any node to configure that agentic workflow, AI agent, or tool individually. You can also edit the name and description of your agentic AI asset by selecting the more options icon. The more options icon also allows you to add AI agents to agentic workflows and tools to AI agents to extend their functionalities.

\[Omitted image "ai-agent-studio-new-node-map.png"\] Alt text: AI Agent Studio node map view showing Major Incident Detection Agent with three tools connected as child nodes.

## Activity tracking

From the Activity section in AI Agent Studio, you can view execution logs for both AI agents and agentic workflows. The activity page allows you to track trends in how your agentic AI assets perform. You can filter executions and automated evaluations by various fields to analyze performance patterns. For comprehensive insights into AI agent and agentic workflow usage and performance, access the AI Agent Analytics dashboard.

Runs that are still in progress, including queued test runs, appear here with their current status. Use this section to confirm what is still running if the test panel does not make that clear.

## Testing agentic AI

You can manually test individual AI agents and agentic workflows from their guided setup, or use automated evaluations to assess performance across multiple executions. Manual tests are best for verifying that an AI agent or agentic workflow behaves as expected on a single test record. Automated evaluations are better at identifying underlying patterns and trends that might not be visible in individual executions.

An automated evaluation runs the asset against test scenarios you select and returns a result for each scenario plus an aggregate view across the run. Decide what you are measuring, and what score you would accept, before configuring one.

## AI Agent Studio settings

From the Settings section in AI Agent Studio, you can configure AI Guardian and manage AI agent capabilities. Configure the following settings:

-   Offensiveness detection and Prompt injection protection
-   [Long-term memory for AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/long-term-memory-aia.md)
-   User facts and preferences for knowledge retention
-   External AI agent settings for discoverability and communication
-   Model provider configuration for LLM selection

