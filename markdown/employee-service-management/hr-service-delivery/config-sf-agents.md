---
title: Configure AI agents for HR Service Delivery Integration with SuccessFactors
description: Configure HCM AI agents to enable your employees to place requests to the SuccessFactors system using the HR Service Delivery AI agent collection.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, HR Service Delivery Integration with SuccessFactors, Integrate with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure AI agents for HR Service Delivery Integration with SuccessFactors

Configure HCM AI agents to enable your employees to place requests to the SuccessFactors system using the HR Service Delivery AI agent collection.

## Before you begin

View [Subflow-agent mapping for HR Service Delivery Integration with SuccessFactors](../reference/sf-agent-mapping.md).

Role required: flow\_designer, decision\_table\_admin, sn\_hr\_integr\_fw.admin, and sn\_hr\_core.admin

## Procedure

1.  Install the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\).

    For more information, see [Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md).

2.  Activate the Enterprise Service Management Integrations Framework\] application from the ServiceNow® Store.

3.  Configure the [SuccessFactors Spoke](https://www.servicenow.com/docs/access?context=successfactors-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) to pull data from SuccessFactors system.

4.  Create subflows aligning with Template Integration Gateway.

    For more information, see [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:** You can also use the default subflows that have been created for SuccessFactors.

5.  Add input choices and define conditions and results in a decision table for the Integration Gateway subflow.

    For more information, see [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md).

6.  Duplicate AI agents available for SuccessFactors to run them autonomously.

    For more information, see [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

    **Note:** In the Toggle display section, ensure the toggle beside Virtual Agent is enabled.


