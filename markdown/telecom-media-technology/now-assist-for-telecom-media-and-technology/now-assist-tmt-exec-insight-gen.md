---
title: Activate the Executive Insight Generator skill
description: Enable AI-generated engagement briefs that summarize recent signals across risk, adoption, and market activity on the engagement record page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-exec-insight-gen.html
release: australia
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-08-31"
reading_time_minutes: 1
keywords: [Executive Insight Generator, engagement brief, AI skill activation, engagement updates]
breadcrumb: [Use generative AI skills, ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\), Telecommunications, Media, and Technology \(TMT\)]
---

# Activate the Executive Insight Generator skill

Enable AI-generated engagement briefs that summarize recent signals across risk, adoption, and market activity on the engagement record page.

## Before you begin

Role required: admin

## About this task

The **Executive Insight Generator** skill is inactive by default. After activation, the **Engagement updates** component on the engagement record page generates and displays an AI brief for users with the `sn_acct_lc.agent` role. The brief loads automatically when the page opens and is cached for 15 days.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Hub** &gt; **AI Skills**.

2.  In the **Executive Insight Generator** skill card, select **Activate**.

3.  Select the user role that can use this skill.

4.  Select **Save**.

    The skill is activated. The **Engagement updates** component on the engagement record page generates an AI brief the next time a user with the required role opens an engagement record.


## What to do next

For information about insight categories, trigger types, and refresh behavior, see .

To create custom triggers for the Executive Insight Generator, see .

To activate the **Recommendations** panel on the engagement record page, activate the Signal to Action Recommender skill. See [Activate the Event-Context Candidate Recommender](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-tmt-reco-actions-skill.md) for details.

**Parent Topic:**[Using ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/now-assist-for-telecom-media-and-technology/now-assist-spm-using.md)

