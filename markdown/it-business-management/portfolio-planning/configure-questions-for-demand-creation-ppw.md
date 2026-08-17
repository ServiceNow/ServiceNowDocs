---
title: Configure the questions for conversational demand creation
description: Add or modify an existing question for creating a demand through Agent assist in Virtual Agent using the conversational experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/configure-questions-for-demand-creation-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow Otto for Virtual Agent, Create a New Demand]
breadcrumb: [Configure, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Configure the questions for conversational demand creation

Add or modify an existing question for creating a demand through Agent assist in Virtual Agent using the conversational experience.

## Before you begin

-   Verify that AI Search is installed and provisioned for your instance by navigating to **All** &gt; **AI Search** &gt; **AI Search Status**.
-   ServiceNow Otto for Virtual Agent is set up. See [Configuring assistants overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).
-   Verify the following plugins are install.
    -   ServiceNow Otto for Platform \(v4.0.2\)
    -   ServiceNow Otto for IT Service Management \(ITSM\)
-   Configure ServiceNow Otto in Conversational Catalog Request. See [Configure ServiceNow Otto in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-gen-ai-catalog-item.md)

Role required: admin or catalog\_admin

## About this task

**Note:** If Microsoft Teams and Mobile are enabled as a display location for ServiceNow Otto for Virtual Agent, you can use the conversational experience to create a demand in those applications too.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Conversational catalog overview**.

2.  Select the **Create a New Demand** catalog item.

3.  Identify any unsupported conversational catalog item question types and suggestions to make them conversational by selecting ServiceNow Otto for Virtual Agent.

    For information on unsupported fields, see [Configure ServiceNow Otto in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-gen-ai-catalog-item.md).

4.  Select **Edit in advanced view**.

5.  Review the existing questions in the **Variables** related list and add or modify questions.


