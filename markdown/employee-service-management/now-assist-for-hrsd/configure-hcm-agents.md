---
title: Configure HCM AI agents from the HR Service Delivery AI Agent Collection
description: Enable your employees to place requests to the Human Capital Management \(HCM\) system using the Now Assist for HR Service Delivery \(HRSD\) agent collection.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure HCM AI agents from the HR Service Delivery AI Agent Collection

Enable your employees to place requests to the Human Capital Management \(HCM\) system using the Now Assist for HR Service Delivery \(HRSD\) agent collection.

## Before you begin

Role required: flow\_designer, decision\_table\_admin, sn\_hr\_integr\_fw.admin, and sn\_hr\_core.admin

## Procedure

1.  Install the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\).

    For more information, see [Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md).

2.  Activate the \[Enterprise Service Management Integrations Framework\] application from the ServiceNow® Store.

3.  Configure the required ServiceNow spokes or customize spokes to pull data from HCM systems.

    For more information, see [Integration of HR Service Delivery with third-party systems](../concept/integrate-third-party-systems.md).

4.  Create subflows aligning with Template Integration Gateway, or use default subflows that have been created for your HCM system.

    For more information, see [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:** The subflows for Oracle HCM can be used as a reference to build subflows for any other HCM systems.

5.  Add input choices and define conditions and results in a decision table for the Integration Gateway subflow.

    For more information, see [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md).

6.  Duplicate available HCM AI agents to run them autonomously.

    For more information, see [Duplicate an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/clone-ai-agent.md) For list of available agents, see [Using agentic workflows in Now Assist for HRSD](../concept/now-assist-hrsd-ai-agents-use-cases.md).

    **Note:** In the Toggle display section, ensure the toggle beside Virtual Agent is enabled.


**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

