---
title: Extending AI with external systems and providers
description: Connect to external LLM providers through the Generative AI Controller and integrate AI agents with external tools and services using the Model Context Protocol \(MCP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-extending-ai-external-systems-providers.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Generative AI Controller, MCP Client, MCP Server Console, Model Context Protocol, external LLM providers]
breadcrumb: [Enable AI Experiences]
---

# Extending AI with external systems and providers

Connect to external LLM providers through the Generative AI Controller and integrate AI agents with external tools and services using the Model Context Protocol \(MCP\).

The ServiceNow AI Platform is designed to work with external systems and model providers, giving you flexibility to choose the LLM providers that meet your requirements and connect AI agents to tools and services beyond the platform.

## Generative AI Controller

The Generative AI Controller integrates third-party generative AI into the platform. The controller supports external LLM providers, including OpenAI, Azure OpenAI, Google Cloud \(AI Studio and Vertex\), IBM watsonx, and Amazon Bedrock. These capabilities are available in Workflow Studio flows, Virtual Agent topics, and scripting such as background scripts and business rules. The Generative AI Controller is installed automatically with any AI application.

To bring third-party LLM providers such as OpenAI, Google, and Amazon Bedrock into flows, Virtual Agent, and scripts, see [Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/generative-ai-controller/generative-ai-controller.md).

## MCP Client

The Model Context Protocol \(MCP\) is a standardized client-server protocol that enables AI applications to discover and interact seamlessly with external tools, data sources, and services. MCP Client manages communication between a host application, such as AI Agent Studio, and one or more MCP servers that expose specific capabilities. MCP tools enable you to connect your AI agent with a wide variety of external tools with minimal setup and add multiple MCP tools to an AI agent to perform a broader range of tasks.

To connect your AI agents to external tools, data sources, and services through the Model Context Protocol, see [Model Context Protocol Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/mcp-client.md).

## MCP Server Console

MCP Server Console console lets you create MCP servers on your instance and configure the tools they expose to external clients. Tools define which functionality and data a server makes available and the actions that can be performed on the instance. You can create tools based on existing capabilities such as generative AI skills, and you can create multiple servers that expose different tools for different use cases, such as HR or IT workflows, or for different clients.

Any AI application, such as Microsoft Copilot or AWS Claude, can call a server using OAuth 2.0 authentication and get a list of available tools. Employees using the MCP Client can then prompt the server for information from the instance or to perform an action, such as summarizing a list of recently closed incidents or cases.

**Note:** With AI Gateway in AI Control Tower, administrators can monitor MCP Server Console and access and view metrics for servers and their tools.

To create MCP servers that expose your instance's tools, including generative AI skills, to external clients such as Microsoft Copilot or AWS Claude, see [MCP Server Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).

