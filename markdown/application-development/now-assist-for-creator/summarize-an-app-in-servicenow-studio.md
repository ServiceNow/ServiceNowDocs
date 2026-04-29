---
title: Summarize the contents of an app in ServiceNow Studio
description: Generate a summary of your app using Now Assist for Creator in ServiceNow Studio. After reviewing the summary, you can use it as a description for your app.
locale: en-US
release: australia
product: Now Assist for Creator
classification: now-assist-for-creator
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, generative AI, servicenow studio]
breadcrumb: [App summary generation, Use generative AI, Now Assist for Creator, Vibe coding and AI app development on the ServiceNow AI Platform, Building applications]
---

# Summarize the contents of an app in ServiceNow Studio

Generate a summary of your app using Now Assist for Creator in ServiceNow Studio. After reviewing the summary, you can use it as a description for your app.

## Before you begin

Role required: sn\_app\_summary.app\_summary\_user, and admin or delegated\_developerwith Write access to the app record

## About this task

If your company has a robust citizen development program and has many developers creating apps, you might have some duplicate apps. Good app descriptions are one of the best and easiest ways to be able to scan your list of apps for duplicates. Using Now Assist to generate a good app description can enable you to have more governance over app creation.

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **ServiceNow Studio**.

2.  Open an application.

3.  On the **App details** page, select **Summarize**.

    The App summary modal shows that an app summary is being generated, which may take a few moments.

    The app summary generation times out after two minutes by default. If this occurs, you will receive an error notification. An administrator can adjust the timeout duration.

4.  After the app summary appears, review it for accuracy and take one of the following actions.

    |Action|Result|
    |------|------|
    |**Rate the summary as helpful**|Rating summaries helps enable Now Assist to create better summaries.|
    |**Rate the summary as unhelpful**|Rating summaries helps enable Now Assist to create better summaries.|
    |**Copy to clipboard**|Copy the summary to use it elsewhere in your app development.|
    |**Regenerate summary**|Regenerate the summary if the initial attempt wasn't accurate or needed major changes.|
    |**Use as app description**|If the summary is complete, accurate, and helpful, select **Use as app description**, and the description is populated with the summary.|

5.  Select **Done**.


## Result

After you create an initial app summary, the **Summarize** button becomes the **Summary** button. If you see **Summary**, know that an app summary has already been created and can be edited as needed.

**Parent Topic:**[App summary generation](../../now-assist-app-summarize/concept/sns-now-assist-app-summarize-landing.md)

