---
title: Application development with Figma MCP server
description: Connect the Figma MCP server to the Build Agent to accelerate the transition of your Figma designs to enterprise-grade applications on the ServiceNow AI Platform.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-01"
reading_time_minutes: 1
breadcrumb: [Explore, Build Agent, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Application development with Figma MCP server

Connect the Figma MCP server to the Build Agent to accelerate the transition of your Figma designs to enterprise-grade applications on the ServiceNow AI Platform®.

The Figma MCP \(Model Context Protocol\) server establishes a secure connection between the Build Agent and Figma using OAuth for login authentication. This server enables the Build Agent to access structured design data directly from Figma files, rather than relying on static screen captures. With the available data, the Build Agent can effectively create new applications.

The Figma MCP server translates Figma data, such as components, styles, and variables, into a machine-readable format. The Build Agent uses the translated data to generate code, gather design context, or develop design systems directly from Figma. Consequently, developers can create more accurate and consistent application UIs faster than with traditional approaches.

## Process overview

The process of converting Figma designs to applications is as follows:

-   Designers use Figma to create user interface \(UI\) components, styles, and variables.
-   The Figma MCP server employs OAuth to securely access design data from Figma.
-   The Figma MCP server acts as an intermediary, converting Figma’s design data into the Build Agent ’s context.
-   The Build Agent, which is installed on your ServiceNow® instance, receives the translated data and uses it to generate applications.
-   The Build Agent creates applications based on the design data provided by Figma.

For more information, see [Connect Figma MCP server to Build Agent](../tasks/connect-figma-mcp-server-to-build-agent.md#)

**Parent Topic:**[Exploring Build Agent](exploring-build-agent.md)

