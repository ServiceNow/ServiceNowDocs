---
title: Configure HCM AI agents for HR Service Delivery Advanced Integration with Oracle HCM
description: Configure HCM AI agents to enable your employees to place requests to the Oracle system using the HR Service Delivery AI agent collection.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Service Delivery Advanced Integration with Oracle HCM, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure HCM AI agents for HR Service Delivery Advanced Integration with Oracle HCM

Configure HCM AI agents to enable your employees to place requests to the Oracle system using the HR Service Delivery AI agent collection.

## Before you begin

View [Subflow-agent mapping for HR Service Delivery Advanced Integration with Oracle HCM](../reference/oracle-agent-mapping.md).

Role required: flow\_designer, decision\_table\_admin, sn\_hr\_integr\_fw.admin, and sn\_hr\_core.admin

## Procedure

1.  Install the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\).

    For more information, see [Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md).

2.  Activate the \[Enterprise Service Management Integrations Framework\] application from the ServiceNow® Store.

3.  Configure the [Oracle HCM Cloud Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/oracle-hcm.md) to pull data from Oracle system.

4.  Create subflows aligning with Template Integration Gateway.

    For more information, see [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:** You can use also the default subflows that have been created for Oracle.

5.  Add input choices and define conditions and results in a decision table for the Integration Gateway subflow.

    For more information, see [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md).

6.  Duplicate AI agents available for Oracle to run them autonomously.

    For more information, see [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md).

    **Note:** In the Toggle display section, ensure the toggle beside Virtual Agent is enabled.


