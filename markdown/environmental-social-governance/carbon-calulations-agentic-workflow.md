---
title: Carbon calculations using AI agents
description: Automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions categories. Uses AI-powered document analysis and semantic matching to confirm accuracy, reducing manual effort for ESG program managers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Carbon calculations using AI agents

Automates the creation of calculated metric definition \(CMD\) records and formulas for Scope 3 carbon emissions categories. Uses AI-powered document analysis and semantic matching to confirm accuracy, reducing manual effort for ESG program managers.

## Understanding carbon calculations AI agents

The carbon calculations AI agent enables you to generate calculated metric definitions \(CMDs\) for Scope 3. The carbon calculations AI agent transforms how operational sustainability teams manage carbon emissions data. Rather than relying on manual processes, this workflow introduces automation and intelligence to handle the complexity of Scope 3 emissions. It acts as a co-pilot, applying best-practice methodologies, automating data ingestion, validating emission factors, and delivering actionable insights. This feature helps teams save time, improve accuracy, and scale sustainability reporting and compliance efforts.

The carbon calculations agentic workflow consists of a sequence of AI-driven steps designed to automate carbon metric processing.

-   It begins with the Document and Visual Insights AI Agent, which uses docIntel tools to retrieve attachments, answer document-related questions, and summarize content.
-   Next, the Calculation Operands AI Agent performs data retrieval through RAG-based search tools to fetch metric definitions and emission factors required for carbon calculations.
-   Finally, the workflow creates a calculated metric definition and stores it as a record. This integrated process confirms accurate data extraction, efficient retrieval of key parameters, and streamlined creation of carbon calculation metrics.

The Carbon calculations require dynamic decision-making, contextual understanding, and guided user input. At its core, the workflow integrates document intelligence, semantic search, and formula validation into a unified experience. Using AI agents and matching techniques, the workflow confirms that emission factors and metric definitions align with enterprise data, bridging regulatory standards and operations.

## Usecase for carbon calculations AI agents

When you submit a prompt for category 6 related to Scope 3 emissions, the system activates the appropriate agentic workflow and routes the request. This workflow coordinates multiple specialized agents and tools to guide the user through the process. The sequence of events in the workflow is as follows:

1.  The Document Intelligence Agent in the workflow identifies it as “business travel” and extracts relevant calculation methods from the attached guidance document, such as fuel-based, distance-based, and spend-based methods.
2.  You’re prompted to select a method, after which the workflow extracts the corresponding formula. You select `distance-based` then the formula is `CO₂ emissions from business travel = Σ (distance traveled by each mode × emission factor for that mode)`.
3.  The workflow then prompts for transportation types such as air, car, or train. It expands the formula accordingly and proceeds to match metric definitions and emission factors for each component.
4.  When you select `air and train` as modes, the expanded formula becomes `CO₂ emissions = (distance traveled by air × air emission factor) + (distance traveled by train × train emission factor)`.
5.  A search tool presents matching MDs and EFs for your selection, refining the formula as needed. If no matches are found, the system suggests refining the input `CO₂ emissions = (employee air travel distance × employee air travel emission factor) + (employee train travel distance × employee train travel emission factor)`.
6.  Once all components are confirmed, the workflow creates a Calculated Metric Definition \(CMD\) in an inactive state and links it to the Operational Sustainability Workspace for review.

## Carbon calculations AI agent benefits

The benefits are as follows:

-   Reduces manual effort by eliminating tedious extraction and mapping of Scope 3 calculation logic.
-   Improves accuracy and consistency by leveraging AI-driven document analysis and semantic matching.
-   Accelerates sustainability processes by streamlining CMD creation.
-   Promotes transparency and traceability by providing step-by-step guidance and workflow audit logs.
-   Simplifies user experience through an intuitive conversational assistant embedded in the Now Assist Panel.

**Parent Topic:**[Exploring Now Assist for Operational Sustainability \(formerly ESG\)](exploring-now-assist-for-esg.md)

