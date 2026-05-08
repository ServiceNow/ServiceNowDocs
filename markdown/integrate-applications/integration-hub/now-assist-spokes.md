---
title: Now Assist for Integration Hub
description: Use the ServiceNow Now Assist AI agents to mimic human-like intelligence by using Large Language Models \(LLMs\) to perform tasks that range from simple automated responses to complex problem-solving. Utilize the conversational ability of Integration Hub spoke actions.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build integrations, Integration Hub, Workflow Data Fabric]
---

# Now Assist for Integration Hub

Use the ServiceNow Now Assist AI agents to mimic human-like intelligence by using Large Language Models \(LLMs\) to perform tasks that range from simple automated responses to complex problem-solving. Utilize the conversational ability of Integration Hub spoke actions.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store.

## Capabilities

AI agents are autonomous systems that interact with their environment to gather data, make decisions, and complete tasks that would otherwise need to be completed by a human. Now Assist products provide AI agents that are tailored to meet the needs of users in different workflows. You can take actions to drive towards a specific goal, such as resolving an incident or a case by providing a set of instructions to the AI agents.

Perform business actions through conversational interface like Now Assist. Unlock the interactive conversational experience to automate your business workflows.

## Dependency

Before using Now Assist for Integration Hub, confirm that you are using the latest Now Assist for platform version.

## Supported version

The Now Assist for Integration Hub application is supported on Xanadu Patch 7 and later releases.

**Important:** Ensure that you install the latest available version of the Now Assist for Integration Hub application.

## Application version

Now Assist for Integration Hub v2.2.0 is the latest version.

## Activation of the application

The Now Assist for Integration Hub application requires these subscriptions:

-   Now Assist for Platform \(sn\_genai\_platform\) subscription
-   An Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

After installing the Now Assist for Integration Hub application, you can use the available AI agents and configure the available conversational spoke actions.

-   See Now Assist AI agents to learn about AI agents.
-   See Conversational subflows to learn more about configuring the conversational settings.
-   See Conversational actions to learn more about creating and configuring the conversational skill from Workflow Studio.
-   See  in Now Assist skills in the Platform workflow to learn more about conversation experience and skills.

## Available AI agents

This application provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

Available AI agent includes, [Meeting scheduler AI agent](../reference/meeting-scheduler-ai-agent.md) that can be used to organize Zoom or Teams meetings and create regular calendar events. This AI agent retrieves details of available rooms, details of the relevant users you want to invite such as, email address and timezone, finds an available time slot, creates a calendar event, and generates a Zoom URL for the meeting.

## Role masking

Agentic workflows and their AI agents use role masking to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

**Parent Topic:**[Building integrations in Integration Hub](building-integrations-ih.md)

