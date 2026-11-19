---
title: Configure the questions for demand creation in ServiceNow Otto for Strategic Portfolio Management
description: Add a new question or modify an existing question for Now Assist to ask the user while creating a demand using conversational experience in Virtual Agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/configure-questions-for-demand-creation.html
release: yokohama
product: Now Assist for Strategic Portfolio Management \(SPM\)
classification: now-assist-for-strategic-portfolio-management-spm
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Now Assist for Virtual Agent, Create a New Demand]
breadcrumb: [Enable conversational demand creation using Now Assist in Virtual Agent, Configure, ServiceNow Otto for Strategic Portfolio Management, Strategic Portfolio Management]
---

# Configure the questions for demand creation in ServiceNow Otto for Strategic Portfolio Management

Add a new question or modify an existing question for Now Assist to ask the user while creating a demand using conversational experience in Virtual Agent.

## Before you begin

Ensure that the following plugins are installed:

-   Now Assist for Platform \(v4.0.2\)
-   Now Assist for IT Service Management \(ITSM\)
-   Now Assist in Conversational Catalog Request

    **Note:** Installing Now Assist in Conversational Catalog Request automatically installs all the other dependent plugins.

-   Activate the Now Assist Multi-Turn Catalog Ordering skill. See [Configure ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/configure-now-assist-for-spm.md).
-   Configure Now Assist in Virtual Agent. For more information, see [Configure Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/configure-now-assist-va.md).

Role required: admin or catalog\_admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Conversational catalog overview**.

2.  Select the **Create a New Demand** catalog item.

3.  Identify any unsupported conversational catalog item question types and suggestions to make them conversational by selecting **Now Assist for Virtual Agent**.

    For information on unsupported fields, see [Configure Now Assist in Conversational Catalog Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/configure-gen-ai-catalog-item.md).

4.  Review the existing questions in the Variables related list and add or modify questions by selecting **Edit in advanced view**.


**Related topics**  


[Create demands by using the conversational experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/now-assist-for-strategic-portfolio-management-spm/demand-creation-using-now-assist.md)

