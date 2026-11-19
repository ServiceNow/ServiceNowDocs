---
title: Predict service and transfer HR cases AI agent
description: Analyze an HR case and automatically route it to the most appropriate HR service with the Predict service and transfer HR Cases AI agent. Use the agent to help ensure that cases are handled by the most appropriate teams.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/predict-service-transfer-hr-cases-ai-agent.html
release: brazil
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: concept
last_updated: "2026-11-17"
reading_time_minutes: 2
breadcrumb: [Use agentic workflows, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Predict service and transfer HR cases AI agent

Analyze an HR case and automatically route it to the most appropriate HR service with the Predict service and transfer HR Cases AI agent. Use the agent to help ensure that cases are handled by the most appropriate teams.

**Important:** The Predict service and transfer HR Cases AI agent replaces the deprecated Predict service and transfer HR cases agentic workflow. The agent supports the same HR case triage use case but runs as a standalone AI agent and no longer depends on the backend action framework. For information about the deprecated workflow, see [Deprecated Predict service and transfer HR cases agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/now-assist-for-hrsd/predict-transfer-hrcase.md).

## How the AI agent works

When a case is submitted, the AI agent enriches the case query with the employee, department, location, and employment details that are available for the case. It then compares the enriched query with the indexed HR cases and HR services to predict the most suitable HR service for the case.

The AI agent uses a confidence threshold to decide whether to transfer the case:

-   If the prediction confidence is equal to or greater than the threshold, the AI agent transfers the case to the predicted HR service.
-   If the prediction confidence is below the threshold, the AI agent leaves the case in its current service. The top three service recommendations are added to the work notes of the case.

The out-of-box confidence threshold is 85 percent.

For example, the AI agent predicts a service for a direct deposit inquiry with 65 percent confidence, so it does not transfer the case. For a medical benefits inquiry, the AI agent predicts a service with 95 percent confidence, so it transfers the case from General Inquiry to Medical Benefits Inquiry.

## Prerequisites

Before you activate the AI agent, make sure that the following requirements are met.

**Role**

Verify that the `sn_hr_core.case_writer` role includes the `sn_uxc_gen_ai.platform_ai_field_predictor` role. Otherwise, the AI agent does not operate as expected.

**Index the data sources**

Index the following data sources so that the AI agent can search them:

-   HR case
-   HR service

To index the data sources, select the sources, select **Index Selected Tables**, and then select **Index**.

After indexing, verify the status of each data source:

-   The **Keyword Ingestion State** and **Semantic Ingestion State** are both **Indexed**.
-   No errors appear in the ingestion histories.
-   Ingestion is 100 percent complete.

**Publish the search profile**

Publish the `[AIS] HR AI agent search profile` and verify that its state is **Published**.

## Activate and configure the AI agent

Activate and configure the AI agent by using the guided setup in AI Agent Studio. For the steps, see [Activate the Predict service and transfer HR Cases AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/now-assist-for-hrsd/activate-predict-service-transfer-hr-cases-ai-agent.md).

