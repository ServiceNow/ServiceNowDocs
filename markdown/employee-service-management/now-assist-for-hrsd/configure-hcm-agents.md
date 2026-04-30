---
title: Configure HCM agents for HR Service Delivery AI Agent Collection
description: Enable your employees to place requests to the Human Capital Management \(HCM\) system using the HR Service Delivery AI agent collection.
locale: en-US
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-06-25"
reading_time_minutes: 3
breadcrumb: [Configure, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Configure HCM agents for HR Service Delivery AI Agent Collection

Enable your employees to place requests to the Human Capital Management \(HCM\) system using the HR Service Delivery AI agent collection.

## Before you begin

Role required: admin

## Procedure

1.  Install the Now Assist for HR Service Delivery \(HRSD\) plugin \(sn\_hr\_gen\_ai\).

    For more information, see [Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md).

2.  Activate the Enterprise Service Management Integrations Framework\] application from the ServiceNow® Store.

3.  Configure the required ServiceNow spokes or customize spokes to pull data from HCM systems.

    For more information, see [Integration of HR Service Delivery with third-party systems](../concept/integrate-third-party-systems.md).

4.  Create subflows aligning with Template Integration Gateway.

    For more information, see [Create a subflow using Template Integration Gateway](configure-integration-gateway.md).

    **Note:** The subflows for Oracle HCM can be used as a reference to build subflows for any other HCM systems.

5.  Add input choices and define conditions and results in a decision table for the Integration Gateway subflow.

    For more information, see [Configure Integration Provider Mapping \(Decision table\)](configure-integration-mapping.md).

6.  Duplicate available HCM agents to run them autonomously.

    For more information, see [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

    **Note:** In the Toggle display section, ensure the toggle beside Virtual Agent is enabled.


**Parent Topic:**[Configure Now Assist for HR Service Delivery \(HRSD\)](configure-now-assist-hr.md)

**Related topics**  


[Skill inputs and triggers for Now Assist for HR Service Delivery \(HRSD\)](../concept/now-assist-hrsd-skill-inputs.md)

[RCA approvals for Now Assist for HR Service Delivery \(HRSD\)](run-rca-now-assist-hrsd.md)

[Restrict Now Assist capabilities for employee relations cases](restrict-now-assist-skills-er-cases.md)

[Configure resolution notes generation for Now Assist for HRSD](resolution-notes-nacm-config.md)

[Configure sensitivity detection](config-na-sd-filters.md)

[Configure Gen AI Virtual Agent for HRSD](use-genai-ec.md)

[Configure the Now Assist for HRSD Virtual Agent topics](config-va-topics.md)

[Configure Now Assist AI Helper – Galileo Inside](configuring-galileo-inside.md)

