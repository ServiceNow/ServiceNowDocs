---
title: Test the Predict service and transfer HR Cases AI agent
description: Run a test case in AI Agent Studio to verify that the AI agent predicts an HR service and transfers the case as expected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/test-predict-service-transfer-hr-cases-ai-agent.html
release: brazil
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-11-17"
reading_time_minutes: 1
breadcrumb: [Predict service and transfer HR cases AI agent, Use agentic workflows, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Test the Predict service and transfer HR Cases AI agent

Run a test case in AI Agent Studio to verify that the AI agent predicts an HR service and transfers the case as expected.

## Before you begin

Role required: admin

Activate the AI agent. You need an HR case number to test with.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  In the **Choose a test type** field, select **AI agent or workflow**.

3.  In the **Name of the AI agent or agentic workflow** field, search for and select **Predict service and transfer HR Cases**.

4.  In the **Version** field, select the active version.

5.  In the **Task** field, enter a request that includes one HR case number, for example: `Predict and transfer HR case HRC0001234`.

    The AI agent accepts only one HR case number for each request.

6.  Select **Continue to test chat response**.

7.  Review the response.

    The AI agent lists the outcome of the prediction in the response.


## Result

If the prediction confidence meets the threshold, the case is transferred to the predicted HR service. If it does not, the case stays in its current service and the top three recommendations are added to the work notes of the case.

