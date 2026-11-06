---
title: \(Legacy\) Using Issue Auto Resolution
description: You can proactively deflect issues and expedite the resolution process for your agent and user with the Issue Auto Resolution \(IAR\) application. Through machine learning and Natural Language Understanding \(NLU\), users get immediate self-service and can access Virtual Agent topics, Knowledge articles, and catalog items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/auto-resolution-va.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Case and incident deflection for NLU, Exploring other Virtual Agent NLU features, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Using Issue Auto Resolution

You can proactively deflect issues and expedite the resolution process for your agent and user with the Issue Auto Resolution \(IAR\) application. Through machine learning and Natural Language Understanding \(NLU\), users get immediate self-service and can access Virtual Agent topics, Knowledge articles, and catalog items.

Starting with the Brazil release, Issue Auto Resolution is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## How Issue Auto Resolution works

When a user creates an issue, the Issue Auto Resolution application uses machine learning and NLU to identify the criticality of the issue, the intent, and an appropriate Virtual Agent topic for an automatic resolution. If a Virtual Agent topic isn’t found, Issue Auto Resolution does an AI Search to return the most appropriate Knowledge articles, FAQs, or catalog content. The deflection content is then delivered to the user through the configured response channel, such as email, short messaging service \(SMS\), or Virtual Agent.

## Issue Auto Resolution Admin Console

As an administrator, you use the IAR Admin Console to set up the Issue Auto Resolution application, review how configurations may perform based on historical data \(simulations\), and track performance. You can also see the total cases processed, the solutions identified by the Issue Auto Resolution application, and the cases closed by the user.

To view the IAR Admin Console, navigate to **All****&gt; Issue Auto Resolution****&gt; Overview**. The Overview page contains an FAQ section that provides tips for how certain features work. You can also find a section where you can upgrade your IAR.

## Issue Auto Resolution with custom NLU models

For information about using a custom NLU model and intents with Issue Auto Resolution, see the following post in ServiceNow Community: [https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-configure-custom-intents-for-issue-auto-resolution-iar/ta-p/2638545](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-configure-custom-intents-for-issue-auto-resolution-iar/ta-p/2638545).

## Issue Auto Resolution agentic workflows

To learn more about the agentic workflows for Issue Auto Resolution for ITSM and HR Service Delivery, see [Issue Auto Resolution for ITSM Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-va-auto-resolution.md) and [Issue Auto Resolution for HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/issue-auto-resolution-hr.md).

-   **[\(Legacy\) Configure and run an Issue Auto Resolution simulation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-ar-simulations.md)**  
Use the incident data from your organization to run simulations from the matching intents that the Issue Auto Resolution application based its predictions on from the case descriptions.
-   **[\(Legacy\) Issue Auto Resolution configuration settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/iar-channels.md)**  
Learn about the different configuration settings that you can use for the Issue Auto Resolution \(IAR\) application. For example, you can see the status of your Issue Auto Resolution configurations and decide to turn off or edit each configuration setting to fit your organization's needs.
-   **[\(Legacy\) Issue Auto Resolution diagnostic chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/iar-diagnostic-chat.md)**  
Admin users can initiate a chat conversation to troubleshoot the settings and functionality of Issue Auto Resolution if an issue arises that wasn't addressed as expected.

**Parent Topic:**[\(Legacy\) Case and incident deflection in Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/case-incident-deflection-virtual-agent-nlu.md)

