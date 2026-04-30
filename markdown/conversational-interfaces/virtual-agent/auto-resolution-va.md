---
title: Using Issue Auto Resolution
description: You can proactively deflect issues and expedite the resolution process for your agent and user with the Issue Auto Resolution \(IAR\) application. Through machine learning and Natural Language Understanding \(NLU\), users get immediate self-service and can access Virtual Agent topics, Knowledge articles, and catalog items.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-10-24"
reading_time_minutes: 2
breadcrumb: [Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Using Issue Auto Resolution

You can proactively deflect issues and expedite the resolution process for your agent and user with the Issue Auto Resolution \(IAR\) application. Through machine learning and Natural Language Understanding \(NLU\), users get immediate self-service and can access Virtual Agent topics, Knowledge articles, and catalog items.

## How Issue Auto Resolution works

When a user creates an issue, the Issue Auto Resolution application uses machine learning and NLU to identify the criticality of the issue, the intent, and an appropriate Virtual Agent topic for an automatic resolution. If a Virtual Agent topic isn’t found, Issue Auto Resolution does an AI Search to return the most appropriate Knowledge articles, FAQs, or catalog content. The deflection content is then delivered to the user through the configured response channel, such as email, short messaging service \(SMS\), or Virtual Agent.

## Issue Auto Resolution Admin Console

As an administrator, you use the IAR Admin Console to set up the Issue Auto Resolution application, review how configurations may perform based on historical data \(simulations\), and track performance. You can also see the total cases processed, the solutions identified by the Issue Auto Resolution application, and the cases closed by the user.

To view the IAR Admin Console, navigate to **All****&gt; Issue Auto Resolution****&gt; Overview**. The Overview page contains an FAQ section that provides tips for how certain features work. You can also find a section where you can upgrade your IAR.

## Issue Auto Resolution with custom NLU models

For information about using a custom NLU model and intents with Issue Auto Resolution, see the following post in ServiceNow Community: [https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-configure-custom-intents-for-issue-auto-resolution-iar/ta-p/2638545](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-configure-custom-intents-for-issue-auto-resolution-iar/ta-p/2638545).

## Issue Auto Resolution agentic workflows

To learn more about the agentic workflows for Issue Auto Resolution for ITSM and HR Service Delivery, see [Issue Auto Resolution for ITSM Virtual Agent](https://www.servicenow.com/docs/access?context=itsm-va-auto-resolution&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) and [Issue Auto Resolution for HR Service Delivery](https://www.servicenow.com/docs/access?context=issue-auto-resolution-hr&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

-   **[Configure and run an Issue Auto Resolution simulation](../task/configure-ar-simulations.md)**  
Use the incident data from your organization to run simulations from the matching intents that the Issue Auto Resolution application based its predictions on from the case descriptions.
-   **[Issue Auto Resolution configuration settings](iar-channels.md)**  
Learn about the different configuration settings that you can use for the Issue Auto Resolution \(IAR\) application. For example, you can see the status of your Issue Auto Resolution configurations and decide to turn off or edit each configuration setting to fit your organization's needs.
-   **[Issue Auto Resolution diagnostic chat](iar-diagnostic-chat.md)**  
Admin users can initiate a chat conversation to troubleshoot the settings and functionality of Issue Auto Resolution if an issue arises that wasn't addressed as expected.

**Parent Topic:**[Building and deploying Virtual Agent](using-virtual-agent.md)

