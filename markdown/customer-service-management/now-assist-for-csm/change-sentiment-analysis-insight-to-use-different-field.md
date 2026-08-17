---
title: Change an insight to use a different field for sentiment analysis
description: Change a sentiment analysis insight to display sentiment data from a different field. This requires updates to both the UI Builder component and AI Skill Kit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/change-sentiment-analysis-insight-to-use-different-field.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
keywords: [Generative AI, Generative AI for Customer Service Management, Generative AI for customer service agents]
breadcrumb: [Sentiment analysis case, Activate ServiceNow Otto Skills, Configure, ServiceNow Otto for CSM, Customer Service Management]
---

# Change an insight to use a different field for sentiment analysis

Change a sentiment analysis insight to display sentiment data from a different field. This requires updates to both the UI Builder component and AI Skill Kit.

## Before you begin

Role required: admin or maint

General ServiceNow platform knowledge is required for this procedure.

## About this task

For sentiment analysis insights, changing the field requires modifications to both the UI Builder component and the associated AI Skill Kit skill. It involves cloning components, creating new skills, and modifying scripts. This procedure confirms proper configuration of the sentiment analysis insight with a different field.

The Sentiment analysis dashboard includes the following UI Builder components:

-   Default Sentiment Analysis Dashboard
-   Sentiment Over Time Visualization
-   Sentiment Breakdown Visualization
-   Sentiment Top Drivers Insight \(Negative sentiment and Positive sentiment drivers\)
-   Sentiment by Assignment Group Insight
-   Sentiment After Escalation Insight
-   Sentiment by Channel Insight

## Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Under **Components** tab search for the corresponding component.

    For example, open **Sentiment by Channel Insight**. Make a clone if needed.

3.  [Duplicate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/duplicate-components.md) **Sentiment by Channel Insight**

4.  Rename all components to your desired field \(for example, Consumer\) or create a generalized component name.

    Update the following:

    -   UIB component name \(in Settings\) and **Save**
    -   Stylized text title \(in Editor\)
5.  In the **Get Sentiment by Field** **Data resource**, change the **Field\(s\)** value to your desired field ID.

    For example, consumer.

6.  In a new tab or window, navigate to **All** &gt; **AI Skill Kit**.

7.  Under **ServiceNow skills**, search for **Sentiment by Channel Insight**.

8.  Select **Clone** to clone the skill under your desired field name.

9.  Under the **Tool editor**, select **SentimentChannelScript** and open the tool.

10. Replace every instance of the existing field \(contact\_type\) with your desired field \(consumer\).

11. Select **Continue** till the **Edit script tool** guided set up reaches summary page.

12. Select **Save changes**.

13. In the **Prompt editor** tab, replace every instance of "channel" except the very last occurrence in \{\{SentimentChannelScript.output\}\}.

14. Select **Finalize prompt**.

15. **Publish** the prompt.

16. Navigate to the sys\_one\_extend\_capability table and find the record corresponding to the AI Skill Kit skill you just created.

    Right click to copy the sys\_id.

17. Return to the UI Builder page and in the **Get Sentiment Insight by Capability ID** data resource, paste the copied sys\_id from previous step into the **Capability ID** field.

18. Select **Save**.

    Now [add](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/add-components.md) the newly created component to any base system dashboard page or your own custom page. Use other nearby insights as reference for the correct event handler and optimization setup.

    The sentiment analysis insight now uses the specified field to display data and the associated AI skill has been properly configured.


**Related topics**  


[Add a filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/add-a-new-filter.md)

[Change graph visualization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/change-graph-visualization.md)

