---
title: Activate the Event-Context Candidate Recommender
description: Enable AI-powered success play recommendations in Technology Account 360 and engagement records based on account context and lifecycle events.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-reco-actions-skill.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 1
keywords: [recommended actions skill, success play recommendation, ALE definition, recommendation skill, Signal to Action Recommender]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Activate the Event-Context Candidate Recommender

Enable AI-powered success play recommendations in Technology Account 360 and engagement records based on account context and lifecycle events.

## Before you begin

Role required: `sn_customerservice_agent`

**Note:** Configure the underlying subflows for each Customer Success definition to run as the logged-in user, not as a system user. This ensures that role-based access controls are enforced when a play is executed.

## About this task

The **Event-Context Candidate Recommender** skill compares an account's current context against categories defined in the Customer Success Definition table. Definitions correspond to subflows such as Scheduled Follow-up, Get to Green, and Initiate New Boarding Journey. The skill returns only genuine matches and does not force a result when no definition fits the account context.

When you open the **Recommendations** panel in Technology Account 360 or an engagement record, the skill uses four inputs: account events and their context, the pool of Customer Success definitions to match against, the recommendation mode, and optional matching guidance. The **recommendationMode** parameter controls whether suggestions are returned per event \(`individual`\), as a consolidated set \(`grouped`\), or both.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the **Event-Context Candidate Recommender** skill card, select **Activate**.

3.  Select the user role that can use this skill.

4.  Select **Save**.

    The skill is activated. The **Recommendations** panel in Technology Account 360 and engagement records generates success play suggestions based on the definitions in the Customer Success Definition table. Results are cached after the first call and served from the cache on subsequent panel opens.


## What to do next

For details on caching and refresh behavior, see .

**Parent Topic:**[Using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

