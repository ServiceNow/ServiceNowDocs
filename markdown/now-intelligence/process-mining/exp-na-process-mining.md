---
title: Exploring Now Assist for Process Mining
description: Use ServiceNow Now Assist for Process Mining to minimize time, maximize effort, and reduce complexity in project setup, identifying bottlenecks and retrieving process inefficiencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/process-mining/exp-na-process-mining.html
release: zurich
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for Process Mining, Using Process Mining, Process Mining, Platform Analytics]
---

# Exploring Now Assist for Process Mining

Use ServiceNow Now Assist for Process Mining to minimize time, maximize effort, and reduce complexity in project setup, identifying bottlenecks and retrieving process inefficiencies.

## Now Assist for Process Mining overview

Identifying the root cause of inefficient transitions is challenging and time-consuming, requiring manually examining numerous records for each transition. With thousands of transitions in a process, this task becomes overwhelming and leads to missed opportunities.

This feature is accessible to customers with both Process Mining and GenAI.

## Work Notes Analysis skill

Now Assist for Process Mining includes the Work Notes Analysis skill. This skill must be activated to use Now Assist for Process Mining to analyse work notes. For more information, see [Activate work notes analysis skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/activate-na-skill.md).

**Note:** You can use the Now Assist feature for work notes analysis with 5-50 eligible work notes. If there are less than 25 eligible work notes, the system will not run clustering, but will put all the work notes into one LLM call, otherwise clustering will be performed before calling the LLM.

Once activated and configured, Now Assist for Process Mining uses an LLM to:

-   Analyze all work notes related to inefficient transitions and provide the most important reasons for the transition. This feature is visible in the Process Mining workspace and Platform Analytics Process Mining components.

    When a transition analysis job is initiated, relevant work notes from records in the transition are gathered. Work notes are grouped into clusters, and one LLM call is used for each cluster to explain why the transition occurred.

-   Highlight anomalies and deviations in a process inefficiency by comparing it with the standard process and use Generative AI to provide details.

## Process Inefficiency Highlights skill

Now Assist for Process Mining includes the Process Inefficiency Highlights skill. This skill must be activated to use Now Assist for Process Mining to generate highlights for improvement opportunities. For more information, see [Activate Process Inefficiency Highlights skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/activate-highlight-skills.md).

## What to explore next

To learn more about configuring and using Now Assist for Process Mining, see:

-   [Configuring Now Assist for Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/config-na-proc-min.md)
-   [Using Now Assist for Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/use-na-process-mining.md)

**Parent Topic:**[Now Assist for Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/process-mining/now-assist.md)

