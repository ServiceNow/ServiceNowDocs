---
title: Carbon calculations using AI agents
description: Using AI agents, you can create calculated metric definition \(CMD\) records and formulas automatically for Scope 3 carbon emissions categories. The carbon calculations agentic workflow uses AI-powered document analysis and semantic matching to confirm accuracy, which helps reduce manual effort for ESG Management program managers.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 2
breadcrumb: [Explore, Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Carbon calculations using AI agents

Using AI agents, you can create calculated metric definition \(CMD\) records and formulas automatically for Scope 3 carbon emissions categories. The carbon calculations agentic workflow uses AI-powered document analysis and semantic matching to confirm accuracy, which helps reduce manual effort for ESG Management program managers.

## Overview of carbon calculations agentic workflow

The carbon calculations agentic workflow enables you to generate calculated metric definition \(CMD\) records and formulas for Scope 3. The carbon calculations AI agent transforms how ESG and sustainability teams manage carbon emissions data.

Rather than relying on manual processes, this workflow automatically handles the complexity of Scope 3 emissions by integrating document intelligence, semantic search, and formula validation. It acts as a copilot, applying best practice methodologies, automating data ingestion, validating emission factors, and delivering actionable insights.

The carbon calculations agentic workflow consists of a sequence of AI-driven steps designed to automate carbon metric processing:

-   The document and visual insights AI agent uses DocIntel tools to retrieve attachments, answer document-related questions, and summarize content.
-   The calculation operands AI agent uses RAG-based search tools to fetch the metric definitions and emission factors required for carbon calculations.
-   The carbon calculations AI agent creates a calculated metric definition and stores it as a record.

## Use case for carbon calculations AI agents

When you submit a prompt for category 6 related to Scope 3 emissions, the system activates the appropriate agentic workflow and routes the request. This workflow coordinates multiple specialized agents and tools to guide the user through the process:

1.  The document intelligence AI agent identifies the prompt as business travel and extracts relevant calculation methods from the attached guidance document, such as fuel-based, distance-based, and spend-based methods.
2.  When you’re prompted to select a method, you select `distance-based`. The workflow extracts the following corresponding formula: `CO₂ emissions from business travel = Σ (distance traveled by each mode × emission factor for that mode)`.
3.  When you're prompted to select transportation types, such as air, car, or train, you select `air and train`. The workflow expands the formula to `CO₂ emissions = (distance traveled by air × air emission factor) + (distance traveled by train × train emission factor)`.
4.  A search tool presents matching MDs and EFs for your selection, refining the formula as needed. If no matches are found, the system suggests refining the input `CO₂ emissions = (employee air travel distance × employee air travel emission factor) + (employee train travel distance × employee train travel emission factor)`.
5.  After all components are confirmed, the workflow creates a CMD record in an inactive state and links it to the Operational Sustainability Workspace for review.

**Parent Topic:**[Exploring Now Assist for Operational Sustainability](exploring-now-assist-for-esg.md)

