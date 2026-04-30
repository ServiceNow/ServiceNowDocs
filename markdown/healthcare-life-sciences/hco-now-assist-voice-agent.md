---
title: Care Team Operations Case Creation Voice AI agent
description: Use the Care Team Operations Case Creation Voice AI agent to create support request cases through conversational voice calls.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Using Agentic AI in Now Assist for Healthcare Operations, Now Assist for Healthcare Operations, Healthcare and Life Sciences]
---

# Care Team Operations Case Creation Voice AI agent

Use the Care Team Operations Case Creation Voice AI agent to create support request cases through conversational voice calls.

## Before you begin

Role required: sn\_hco.care\_team\_member or sn\_hco.care\_team\_manager

## About this task

he Care Team Operations Case Creation Voice AI agent lets users create support request cases entirely through voice commands. The agent asks clarifying questions to gather the context needed for case creation, then confirms case details before ending the call.

**Note:** The Care Team Operations plugin for the relevant request type must be installed before the agent can create cases.

The following Care Team Operations plugins are supported:

-   Care Team Operations for Biomed.

-   Care Team Operations for Environmental Services.

-   Care Team Operations for Facilities.

-   Care Team Operations for Healthcare IT.


To integrate this agent with supported third-party CCaaS \(Contact Center as a Service\) providers, see [Integrating voice assistant with CCaaS provider](https://www.servicenow.com/docs/access?context=integrating-voice-service-with-ccaas-providers&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

For more information on setting up Voice AI Agents, see [Deploy AI voice agents](https://www.servicenow.com/docs/access?context=deploy-ai-agents-for-voice&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Once CCaaS has been configured, call your configured telephone number to reach the agent.

2.  When prompted, say how the agent can help you — for example, "I need to submit a Care Team Operations request", "I need help with CTO", or simply “CTO”.

    **Note:**

    These trigger phrases can be configured to your use case. For information on updating these, see [Configure Care Team Operations Case Creation Voice AI agent triggers](hco-now-assist-cto-voice-triggers.md).

3.  Enter your PIN when the agent requests it.

4.  Answer any follow-up questions, providing relevant context about the issue.

5.  Review the case details the agent reads backthen confirm to create the case or say no to have the agent make corrections.

6.  Once the case is created and the agent confirms the details, end the call when prompted.


