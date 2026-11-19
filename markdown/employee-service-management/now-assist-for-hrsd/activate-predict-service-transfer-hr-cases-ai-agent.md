---
title: Activate the Predict service and transfer HR Cases AI agent
description: Use the guided setup in AI Agent Studio to review and activate the Predict service and transfer HR Cases AI agent. After activation, the agent routes HR cases to the appropriate HR service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/activate-predict-service-transfer-hr-cases-ai-agent.html
release: brazil
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-11-17"
reading_time_minutes: 2
breadcrumb: [Predict service and transfer HR cases AI agent, Use agentic workflows, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Activate the Predict service and transfer HR Cases AI agent

Use the guided setup in AI Agent Studio to review and activate the Predict service and transfer HR Cases AI agent. After activation, the agent routes HR cases to the appropriate HR service.

## Before you begin

Complete the prerequisites described in [Predict service and transfer HR cases AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/now-assist-for-hrsd/predict-service-transfer-hr-cases-ai-agent.md).

Role required: `admin`

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.

2.  Select **AI agents**, and then select **Predict service and transfer HR Cases**.

    The guided setup opens.

3.  On the **Define the specialty** page, review the AI agent name, description, role, and list of steps, and then select **Save and continue**.

    The name, description, role, and steps are preconfigured. You can also set unsupported LLM providers, access for third parties and AI specialists, and long-term memory options on this page.

    **Warning:** If you modify the role or the list of steps, the AI agent's memories about past executions are cleared.

4.  On the **Add tools and information** page, verify that the **Predict and transfer tool** is listed under **Scripts**, and then select **Save and continue**.

5.  On the **Define user access** page, verify that the `sn_hr_core.case_writer` role is listed and active, and then select **Save and continue**.

    Users with this role can access the AI agent. To change who can access it, edit the entry in the list.

6.  On the **Define data access** page, verify that **User identity type** is set to **AI user**, and then select **Save and continue**.

7.  On the **Add triggers** page, review the triggers, add or remove triggers as needed, and then select **Save and continue**.

    A trigger launches the AI agent without a user request. Triggers are optional. The table lists each trigger's name, trigger type, table, conditions, run-as user, channel, and status. By default, the AI agent has a trigger for each HR case table, such as `sn_hr_core_case_compensation` and `sn_hr_core_case_operations`, that runs when a case is created.

8.  On the **Select channels and status** page, select the channels where the AI agent is available, and then turn on **This AI agent is active**.

    Enter in-progress and completion messages that users see while the AI agent works.

9.  Select **Save and test**.


## Result

The AI agent is active. When a triggering HR case is created, the AI agent predicts the most suitable HR service and transfers the case if the prediction confidence meets the threshold.

