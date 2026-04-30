---
title: Detect sensitive topics by using sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)
description: Detect and fix sensitive topics that relate to your employee relation cases by using the sensitivity detection capability in the Now Assist for HR Service Delivery \(HRSD\) application.
locale: en-US
release: xanadu
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2024-10-30"
reading_time_minutes: 5
breadcrumb: [Using Now Assist for HR Service Delivery \(HRSD\), Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Detect sensitive topics by using sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)

Detect and fix sensitive topics that relate to your employee relation cases by using the sensitivity detection capability in the Now Assist for HR Service Delivery \(HRSD\) application.

## Before you begin

Role required:

-   sn\_hr\_gen\_ai.admin
    -   sn\_hr\_core.case\_writer
    -   sn\_hr\_core.case\_reader
    -   sn\_hr\_er.case\_reader
    -   sn\_hr\_er.case\_writer

## About this task

This capability helps you detect sensitive cases such as the harassment complaints, discrimination allegations, workplace violence, safety, employee behavior, and employee personal issues. You can also block Now LLM Service from engaging with these sensitive case types.

**Note:**

The store or app client should automatically take care of all the dependencies when you install Now Assist for HRSD. You must install Now Assist for HRSD version 5.0.7.

## Procedure

1.  Navigate to the table **sys\_gen\_ai\_filter** and set active to **true** for the filters.

2.  **Note:** sn\_hr\_gen\_ai.admin is required to perform the first step of setting active to **true** for the filters.

    ![Allows you to set active to 'true' for AI filters](../image/sd-sys-gen-ai-filters.png "Generative AI Filters")

3.  Verify that the following system properties are set to true.

    -   com.glide.genai.semantic\_filter.enabled
    -   com.glide.cs.semantic\_search.enabled
4.  Navigate to the **sys\_one\_extend\_capability table** and select the **VA skill search** capability.

    In the capability attributes, set the **apply filter** field for the utterance to be true.

    **Note:** Repeat this step for the **user\_message** attribute in the Virtual Agent free-form capability and the **search\_text** attribute in Virtual Agent Semantic Search.

5.  Navigate to **Now Assist Admin Console &gt; Features &gt; Platform &gt; Conversation Interfaces**.

6.  Set up **Now LLM Service**.

7.  Navigate to **Virtual Agent** on one of the portals and enter **Sensitive Phrases**.

    **Note:** You enter `Sensitive Phrases` at the beginning of a conversation. This action should trigger the Sensitivity Detection Fallback topic. When sensitive phrases are entered in the now assist panel, it should be detected as sensitive and the LLM should not respond and should allow you to redirect to a live agent or create a case.


## Result

The Sensitive Phrases are automatically detected so that your group can properly handle sensitive cases.

**Parent Topic:**[Using Now Assist for HR Service Delivery \(HRSD\)](../concept/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation by using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-chat.md)

[Summarize a Sidebar discussion by using Now Assist for HR Service Delivery \(HRSD\)](sidebar-discussion-nahr.md)

[Generate a chat reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](chat-recommendations-nahr.md)

[Generate a knowledge article from HR Agent Workspace with Now Assist](gen-kb-now-assisthr.md)

[Generate a knowledge article from multiple cases](gen-kb-now-assisthr-multi-case.md)

[Generate an email reply recommendation by using Now Assist for HR Service Delivery \(HRSD\)](email-recommendation-nahr.md)

[Summarize a case by using Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-summarize-case.md)

[View employee summary reports](../../td-leader-hub/task/employee-summary-lh.md)

[Summarize actions while transferring an HR case](tcase-now-assist-hr.md)

[Generate the resolution notes for a case by using the Now Assist for HR Service Delivery \(HRSD\)](now-assist-hrsd-res-note.md)

[Use Knowledge Graph in Now Assist for HRSD](na-kb-graph.md)

[Use the Now Assist panel in Agent Workspace for HR Case Management](now-assist-panel-hr.md)

[Submit an HR request with Gen AI Virtual Agent](use-genai-hrsd.md)

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework](../concept/integ-now-assist-hrsd.md)

[Configure sensitivity detection in Now Assist for HR Service Delivery \(HRSD\)](config-na-sd-filters.md)

[Sensitivity detection configuration tables](../reference/reference-sd-config-tables.md)

[Sensitivity detection configuration table filters](../reference/reference-sd-config-shipment-tables.md)

[Sensitivity detection human resource value types](../reference/reference-sd-info-values.md)

