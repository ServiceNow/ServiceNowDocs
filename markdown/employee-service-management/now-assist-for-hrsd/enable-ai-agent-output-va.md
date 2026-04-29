---
title: Display AI agent output in Virtual Agent conversations
description: Use the sn\_aia.enable\_va\_conversation system property to display output from AI agents that are used in agentic workflows when you converse with Now Assist in Virtual Agent.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate onboarding ramp-up plan agentic workflow, Use agentic workflows, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Display AI agent output in Virtual Agent conversations

Use the **sn\_aia.enable\_va\_conversation** system property to display output from AI agents that are used in agentic workflows when you converse with Now Assist in Virtual Agent.

## Before you begin

Role required: admin \[virtual\_agent\_admin\]

## Procedure

1.  In the **Filter navigator**, enter `sys_properties.list`.

    The System Properties \[sys\_properties\] table appears.

2.  Select **Name** from the drop-down list associated with the **Search** field.

3.  In the **Search** field, enter `*sn_aia.enable`.

    A list of system properties associated with Now Assist AI Agents appears.

4.  Select the **sn\_aia.enable\_va\_conversation** system property.

5.  Set the **Value** field to **True** to enable output from AI agents during the conversations that you have with Now Assist in Virtual Agent.

6.  Select **Update**.


