---
title: Change an insight to use a different field for sentiment analysis
description: Change a sentiment analysis insight to display sentiment data from a different field, such as changing from channel to consumer, requiring updates to both the UI Builder component and Now Assist Skill Kit.
locale: en-US
release: yokohama
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 2
keywords: [Generative AI, Generative AI for Customer Service Management, Generative AI for customer service agents]
breadcrumb: [Configure sentiment analysis case, Activate Now Assist Skills, Configure, Now Assist for Customer Service Management \(CSM\), Customer Service Management]
---

# Change an insight to use a different field for sentiment analysis

Change a sentiment analysis insight to display sentiment data from a different field, such as changing from channel to consumer, requiring updates to both the UI Builder component and Now Assist Skill Kit.

## Before you begin

Role required: admin or maint

General ServiceNow platform knowledge is required for this procedure.

## About this task

For sentiment analysis insights, changing the field requires modifications to both the UI Builder component and the associated Now Assist Skill Kit skill. It involves cloning components, creating new skills, and modifying scripts. This procedure ensures proper configuration of the sentiment analysis insight with a different field.

The different UI Builder Component names for Sentiment analysis dashboard are OOB Sentiment Analysis Dashboard, Sentiment Over Time Visualization, Sentiment Breakdown Visualization, Sentiment Top Drivers Insight \(Negative sentiment and Positive sentiment drivers\), Sentiment by Assignment Group Insight, Sentiment After Escalation Insight, Sentiment by Channel Insight.

## Procedure

1.  Navigate to **All** &gt; **UI Builder**.

2.  Under **Components** tab search for the corresponding component.

    For example, open **Sentiment by Channel Insight**. Make a clone if needed.

3.  [Duplicate](https://www.servicenow.com/docs/access?context=duplicate-components&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) **Sentiment by Channel Insight**

4.  Rename all components to your desired field \(for example, Consumer\) or create a generalized component name.

    Update the following:

    -   UIB component name \(in Settings\) and **Save**
    -   Stylized text title \(in Editor\)
5.  In the **Get Sentiment by Field** **Data resource**, change the **Field\(s\)** value to your desired field ID.

    For example, consumer.

6.  In a new tab or window, navigate to **All** &gt; **Now Assist Skill Kit**.

7.  Under **ServiceNow skills**, search for **Sentiment by Channel Insight**.

8.  Select **Clone** to clone the skill under your desired field name.

9.  Under the **Tool editor**, select **SentimentChannelScript** and open the tool.

10. Replace every instance of the existing field \(contact\_type\) with your desired field \(consumer\).

11. Select **Continue** till the **Edit script tool** guided set up reaches summary page.

12. Select **Save changes**.

13. In the **Prompt editor** tab, replace every instance of "channel" except the very last occurrence in \{\{SentimentChannelScript.output\}\}.

14. Select **Finalize prompt**.

15. **Publish** the prompt.

16. Navigate to the sys\_one\_extend\_capability table and find the record corresponding to the Now Assist Skill Kit skill you just created.

    Right click to copy the sys\_id.

17. Return to the UI Builder page and in the **Get Sentiment Insight by Capability ID** data resource, paste the copied sys\_id from previous step into the **Capability ID** field.

18. Select **Save**.

    Now [add](https://www.servicenow.com/docs/access?context=add-components&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) the newly created component to any base system dashboard page or your own custom page, using other nearby insights as reference for the correct event handler and optimization setup.

    The sentiment analysis insight now uses the specified field to display data and the associated Now Assist skill has been properly configured.


**Related topics**  


[Add a new filter](add-a-new-filter.md)

[Change graph visualization](change-graph-visualization.md)

