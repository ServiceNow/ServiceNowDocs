---
title: Specify the action workflow timeout
description: Set the length of time before the Workflow Studio Integration Hub action workflow times out.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Virtual Agent with Workflow Studio workflows, Exploring other Virtual Agent features, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Specify the action workflow timeout

Set the length of time before the Workflow Studio Integration Hub action workflow times out.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  Enter `sys_properties.list` in the filter.

3.  Select **New** to add the **com.glide.cs.fdih.interactive.timeout** property.

    1.  On the form, fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Enter the system property name: `com.glide.cs.fdih.interactive.timeout`.|
        |Description|Enter an explanation for this property, such as: `Virtual Agent Workflow Studio IntegrationHub workflow timeout (in seconds)`.|
        |Type|Enter `integer`.|
        |Value|Enter the number of seconds before the workflow action times out. The default value is 120 seconds. This value should not exceed the value set in the **com.glide.cs.convesation\_idle\_timeout** system property. The **com.glide.cs.convesation\_idle\_timeout** property's default timeout value is 7,200 seconds.|

    2.  Select **Submit**.


**Parent Topic:**[Integrating Virtual Agent with Workflow Studio workflows](../concept/va-flow-designer-integration.md)

