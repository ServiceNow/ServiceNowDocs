---
title: Target tables for Microsoft
description: Target tables for storing Service Graph Connector for Azure and copilot data.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-02"
reading_time_minutes: 1
breadcrumb: [Microsoft, Service Graph Connectors for AI Control Tower, Enterprise AI discovery: Unlock Visibility, Governance &amp; Value, Explore, AI Control Tower, Enable AI experiences]
---

# Target tables for Microsoft

Target tables for storing Service Graph Connector for Azure and copilot data.

Both Azure Foundry and Copilot data sources use the following main target tables:

## Digital Asset Tables

-   alm\_ai\_system\_digital\_asset- AI System digital assets
-   alm\_ai\_prompt\_digital\_asset- AI Prompt digital assets

## Entity Tables

-   sn\_ent\_ai\_tool- AI Tools
-   sn\_ent\_ai\_system\_subcomponent\_m2m- AI System Subcomponent many-to-many relationships

## Usage Table

sn\_ai\_disc\_ai\_usage- AI Usage/Execution data.

## Additional information

-   Staging tables are import set tables where data is initially loaded from external sources.
-   Target tables are the destination where transformed data is stored.
-   Data flows from Data Source → Staging Table → Transform Map → Target Table
-   For the tools attached to AI Agents which are discovered, the tool names are suffixed to ensure uniqueness. This is the format for tool name- tool-name:tenantid:resource-name:project-name.

