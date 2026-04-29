---
title: Configure small talk filters
description: Redirect users to different Virtual Agent topics if small talk, such as greetings, expressions of gratitude, complaints, or requests to close, are detected in conversations.
locale: en-US
release: australia
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Configure small talk filters

Redirect users to different Virtual Agent topics if small talk, such as greetings, expressions of gratitude, complaints, or requests to close, are detected in conversations.

## Before you begin

Role required: admin

## About this task

When engaging with generative AI, many people send conversational messages that are ultimately unhelpful for the Virtual Agent when determining how to help the user achieve their goals. You can configure small talk filters that catch these conversational messages. When a user is sending a message such as a greeting or expressing complaints about the conversation, you can redirect them to serve their needs.

## Procedure

1.  In the navigator, go to the Generative AI Filter \[sys\_gen\_ai\_filter\] table by entering `sys_gen_ai_filter.list`.

2.  Open the record for the small talk filter that you want to configure or select **New** to create one.

    By default, the four available filters for small talk are Greetings, Gratitude, Complaint, and Closure. If you see other filters, those filters are sensitive topic filters that can be set up with the Now Assist Admin console. See Configure subject filters for generative AI for more information.

3.  If creating a filter, add a **Name** and **Description** for the filter.

4.  Choose the Filter Error Topic that you want to redirect users to when the small talk filter is detected.

    By default, the user is redirected to the Small Talk Response Processor topic.

5.  For the **Order** field, choose the order to apply the filters.

    Filters are processed by lowest order to highest. A filter with order 100 is processed before a filter with order 200.

6.  In the **Filter Configurations** field, use the name "portal" to determine where the filter should be run, such as setting "portal" to value "sp" to apply only the filter on the sp portal.

    Use a comma-separated list to select multiple values.

    ![Small talk filter record for the Gratitude filter](../image/configure-small-talk-filters-record.png)

7.  Select **Save** to save any changes.

8.  In the navigator, go to the Generative AI Filter Sample \[sys\_gen\_ai\_filter\_sample\] table by entering `sys_gen_ai_filter_sample.list`.

9.  Review the sample phrases for each filter.

    Statements that match these sample phrases activate the selected filter. You can create sample phrases manually by creating records on the table or by using generative AI to generate samples for you.

    1.  To create a sample manually, select **New**.

    2.  In the **Sample text** field, enter the sample text of what you want to be caught by the filter.

    3.  In the **Filter** field, select the filter you want the sample to be applied to.

    4.  If you want to generate more sample phrases with generative AI, open a record for a sample phrase for the desired filter.

        An example might be the "Thanks for your assistance with my task" sample filter for the Gratitude filter.

        ![Small talk sample record for the Gratitude filter that says "Thanks for your assistance with my task"](../image/configure-small-talk-filters-sample-record.png)

    5.  Select **Generate Samples** to create additional example statements to trigger the filter.

        The more sample statements that you provide, the more likely that the filter aligns with your expectations of its behavior.


## Result

When engaging in conversations with generative AI, users are redirected to a new topic when filtered subjects or sentiments are detected.

