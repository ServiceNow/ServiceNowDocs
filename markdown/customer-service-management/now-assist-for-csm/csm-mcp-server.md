---
title: CSM MCP Server
description: The CSM MCP Server connects AI-enabled Model Context Protocol \(MCP\) client applications to your ServiceNow environment, enabling case management and generative AI skill features for customer service agents and managers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/csm-mcp-server.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [MCP Server, Model Context Protocol, agentic AI, Customer Service Management]
breadcrumb: [ServiceNow Otto for CSM, Customer Service Management]
---

# CSM MCP Server

The CSM MCP Server connects AI-enabled Model Context Protocol \(MCP\) client applications to your ServiceNow environment, enabling case management and generative AI skill features for customer service agents and managers.

The CSM MCP Server operates as a secure intermediary between any MCP client application and your ServiceNow instance. The server is registered as CSM MCP Server \(`sn_csm_mcp_server.csm_default`\) and is active by default. Customer service agents use subflows, actions, or AI skills through an MCP client such as Moveworks or Claude. The CSM MCP Server retrieves data live from the ServiceNow Customer Service Management environment and performs actions through natural language conversation.

## Key benefits

The CSM MCP Server provides the following benefits:

-   **Native tool exposure**

    External AI agents, LLM-based tools \(CLI, chat, etc\) can connect with and use ServiceNow capabilities as tools through MCP.

-   **Instant onboarding**

    Any generative or agentic AI platform can be connected in minutes with automated, authentication-compliant setup.

-   **Controlled access**

    All permissions, rules, and access controls that you set up are enforced, regardless of access channel.

-   **Complete observability and auditability**

    Usage, latency, and connection health across every server, tool, and client are available through AI Control Tower.


## CSM MCP Server capabilities

The CSM MCP Server currently exposes 6 tools: 2 case management tools and 4 generative AI skill tools. This is within the recommended range of 20-30 tools per MCP server for optimal performance and manageability.

Each tool carries platform-level annotations indicating the tool is read-only and whether the tool is available to all users or restricted by role.

## Case management tools

The CSM MCP Server handles these core subflows and actions for case management:

-   Gets a list of cases for given criteria or gets details of a specific case
-   Gets a list of case tasks for given criteria or details of specific case tasks
-   Retrieves case and case task details based on the case number

## AI skill tools

The CSM MCP Server handles these AI skill tools:

-   Summarizes case activity, key actions, and current status
-   Generates a draft resolution notes entry for the case
-   Evaluates the sentiment of a CSM case using the Sentiment Analysis generative AI skill. Returns sentiment score, trend, and reasoning. Enforces record-level read access before invoking the skill.
-   Generates an AI-drafted activity response for a CSM case using the Activity Response Generation skill. Supports three response modes: Respond, Follow-Up, Summarize.

## Supported MCP primitives

The CSM MCP Server supports the tools primitive only. This MCP server does not support resources or prompt primitives. This means:

-   Resources unavailable: Claude can't retrieve live ServiceNow data \(such as records, Snowflake analytics, or Seismic assets\) to pass into MCP tool calls. All tool execution must rely on data provided explicitly in the conversation.
-   Prompt primitives unavailable: Claude can't use prebuilt or dynamic prompt templates to adapt its reasoning based on context. Tool behavior remains consistent across all invocations, regardless of the task or situation.

The resources and prompts primitives aren't supported. This is a deliberate design decision driven by prompt injection attack risk mitigation.

## Supervised and autonomous execution

Whether a tool call runs in supervised or autonomous mode is a setting controlled by the connecting MCP client, not a setting available at the MCP server level. For example, this setting is configured in Claude desktop when you add a third-party MCP server \(like GitHub or Slack\) as a connector. Your organization's governance policies regarding tool execution mode should be configured at the client level.

## Usage tracking and observability

MCP server traffic, including billing, usage metrics, and debugging telemetry, is available in the AI Control Tower. CSM MCP Server usage visibility depends on your ServiceNow environment configuration and AI Control Tower setup.

## MCP Apps support

The CSM MCP Server tools return structured text and JSON responses. The platform natively supports MCP Apps \(custom HTML/UI\) in the latest release, allowing custom interfaces to be rendered by the client with configurable permissions \(microphone, camera, geolocation, clipboard\). Check with your ServiceNow administrator regarding whether CSM ships custom MCP App UI or relies on text/JSON-only responses.

## CSM MCP Server users

The following roles are required for CSM MCP Server users:

|Role|Description|
|----|-----------|
|admin|Activates the CSM MCP Server|
|sn\_customerservice\_agent|Reads CSM customer case records, work notes, and generates resolution notes for customer cases|
|sn\_customerservice.consumer\_agent|Reads CSM consumer case records, work notes, and generates resolution notes for consumer cases|
|sn\_csm\_mcp\_invoke|Required to invoke get\_customer\_service\_cases tool and get\_case\_tasks tool|
|sn\_csm\_mcp\_invoke|Required to invoke get\_case\_tasks tool|

## Server operation

The CSM MCP Server operates through the following process:

1.  A Customer Service Management MCP Server user asks a question using an MCP client. For example, a live agent opens their MCP client application such as Moveworks or Claude. The agent can ask for a list of open cases by priority or to summarize a case.
2.  The MCP client application sends the question to the CSM MCP Server using the Model Context Protocol.
3.  The CSM MCP Server authenticates the user against the ServiceNow role-based access control. Authentication uses OAuth 2.1 and JWT with mTLS transport for secure communication.
4.  The CSM MCP Server retrieves the requested data or performs the requested action in the ServiceNow instance.
5.  The CSM MCP Server returns the result to the AI client application, which displays the result to the user.

