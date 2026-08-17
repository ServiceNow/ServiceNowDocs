---
title: Detect sensitive topics by using sensitivity detection in ServiceNow Otto for HR Service Delivery \(HRSD\)
description: Detect and fix sensitive topics that relate to your employee relation cases by using the sensitivity detection capability in the ServiceNow Otto for HR Service Delivery \(HRSD\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-sensitivity-detection.html
release: yokohama
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-09-17"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Detect sensitive topics by using sensitivity detection in ServiceNow Otto for HR Service Delivery \(HRSD\)

Detect and fix sensitive topics that relate to your employee relation cases by using the sensitivity detection capability in the ServiceNow Otto for HR Service Delivery \(HRSD\) application.

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

The store or app client should automatically take care of all the dependencies when you install ServiceNow Otto for HRSD. You must install ServiceNow Otto for HRSD version 5.0.7.

## Procedure

1.  Navigate to the table **sys\_gen\_ai\_filter** and set active to **true** for the filters.

2.  **Note:** sn\_hr\_gen\_ai.admin is required to perform the first step of setting active to **true** for the filters.

    \[Omitted image "sd-sys-gen-ai-filters.png"\] Alt text: Allows you to set active to 'true' for AI filters

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

**Parent Topic:**[Use ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Generate a chat reply recommendation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Generate a knowledge article from HR Agent Workspace with Now Assist]()

[Generate a knowledge article from multiple cases]()

[Generate an email reply recommendation by using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use Galileo Inside to answer HR-related questions]()

[Use the Now Assist panel in Agent Workspace for HR Case Management]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Configure sensitivity detection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/config-na-sd-filters.md)

[Sensitivity detection configuration table filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-config-shipment-tables.md)

[Sensitivity detection configuration tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-config-tables.md)

[Sensitivity detection filters mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/now-assist-for-hrsd/reference-sd-info-values.md)

