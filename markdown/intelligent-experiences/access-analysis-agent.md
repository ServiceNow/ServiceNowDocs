---
title: Access Analysis AI Agent
description: The Access Analysis Agent lets you ask whether a user, group, or role can access something on your ServiceNow instance. It uses guided, conversational workflows in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/access-analysis-agent.html
release: brazil
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [IT Service Management AI agents, IT Service Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Access Analysis AI Agent

The Access Analysis Agent lets you ask whether a user, group, or role can access something on your ServiceNow instance. It uses guided, conversational workflows in the ServiceNow Otto® panel.

## Access Analysis Agent overview

The agent evaluates whether a user, group, or role can access a table, record, field, Client Callable Script Include, UI page, AI agent, or Agentic Workflow. It returns one of three results:

|Result|What it means|
|------|-------------|
|**Passed**|The entity has access. The agent names the ACL \(or ACLs\) that grant it.|
|**Blocked**|The entity does not have access. The agent names the specific ACL, role, security attribute, or condition that's stopping it.|
|**Undefined**|No ACL evaluated the operation at all, so the platform's default behavior applies. This is different from Blocked — there's no rule actively denying it, there's simply no rule granting it either.|

The agent may ask clarifying questions before it evaluates anything. It never guesses at which record you meant.

Once enabled, the Access Analysis Agent supports:

-   Reading the table, record, or user you're currently viewing so you can ask an access question right from that page without naming or navigating to it
-   Evaluating whether a user can access a resource
-   Evaluating whether a group can access a resource
-   Evaluating whether a role can access a resource
-   Answering questions that cover more than one operation on the same entity and resource in one response
-   Evaluating access to AI agents and Agentic Workflows themselves, not just traditional tables and fields
-   Saving completed evaluations so you can find and review them again later

## Prerequisites and setup

Ensure the following requirements are met before using the AI agent:

-   Access Analyzer is installed on your instance and active.
-   The Access Analysis Agent is installed on your instance.
-   AI Agent Studio is available on your instance.
-   The Now Assist panel is available on your instance.
-   You are signed in with a role that has access to the agent. For more information, see [Required role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/access-analysis-agent.md) below.

## Required role

Required role: `access_analyzer_admin` or `user_admin`.

Unlike some Now Assist agents that are open to every session role, the Access Analysis Agent is gated behind two specific roles: `access_analyzer_admin` and `user_admin` roles. These roles keep the agent's use in line with who already has visibility into ACL structure and security configuration on your instance.

Within that gate, the agent evaluates access using the permissions your current session already holds when it looks up the underlying records. It does not escalate or borrow elevated privileges to answer your question.

## Accessing the Access Analysis Agent

To confirm the agent is installed and see its configuration:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Go to the **AI Agents** tab.
3.  Select **Access Analysis Agent**.

To start using the agent day to day, open the Now Assist panel from the sidebar on any ServiceNow page and start a new interaction. See the procedures below for how to phrase your questions.

## Evaluate whether a user, group, or role can access a resource

Use this operation to check whether users can access a table, record, field, Client Callable Script Include, UI page, AI agent, or Agentic Workflow.

1.  Ask the agent your question, naming the user, group, or role and the resource you're asking about. For example:
    -   "What can user ABC access?"
    -   "Can user ABC access resource X?"
    -   "Does the ITIL group have write access to changes?"
    -   "What can the itil role do on the incident table?"
2.  If the agent can't uniquely identify the entity or resource you named, it asks a clarifying question. If your question matches more than one type of entity, the agent lists each match with its type and asks you to confirm.
3.  The agent returns a Passed, Blocked, or Undefined result, along with the specific ACL, role, security attribute, or condition that determined the outcome.

**Note:** You can ask about more than one type of access in the same question, for example both read and write access to the same resource, or a full breakdown of everything a role can do on a table.

## Learn why an operation was blocked

Use this operation when you already know an operation is blocked and want the specific reason, rather than re-asking the original question.

1.  After receiving a Blocked result, ask a follow-up like "Why is user ABC blocked from report\_view on incidents?"
2.  The agent identifies the specific ACL, data condition, security attribute, or role gap that caused the block and explains it in plain language.

## Ask about access without leaving the page you're on

Use this operation to ask about access while viewing a record, list, or user, without typing out what you're asking about.

1.  While viewing a record, list, or user page, open the ServiceNow Otto® panel. Ask your access question without naming a resource, for example: "Can user ABC access this?".
2.  The agent uses the page you're viewing as the resource for the evaluation.

**Note:** If you name a resource directly in your question, the agent uses that resource instead of the page you're viewing. Because the page you're on can change between questions, the agent runs a fresh evaluation rather than reusing an earlier answer, even if you ask what looks like the same question twice in one conversation.

## Review a past evaluation

Use this operation to find an access evaluation you ran previously, instead of running it again.

1.  Open the Now Assist panel.
2.  Ask the agent to show your previous evaluations, or reference the user, group, or role from an earlier question.

The agent retrieves the saved result from your earlier evaluation.

**Parent Topic:**[IT Service Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/itsm-ai-agents-overview.md)

