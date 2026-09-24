---
title: Export AI Guardian logs
description: Export logs from AI Guardian to get insights into how often different guardrails are being detected and used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/export-now-assist-guardian-logs.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Export, Now Assist Guardian, logs, Gen AI, Generative AI, admin, offensiveness, prompt injection]
breadcrumb: [AI Guardian, AI Admin Hub Settings, Exploring AI Admin Hub, AI Admin Hub, Generative AI skills, Enable AI Experiences]
---

# Export AI Guardian logs

Export logs from AI Guardian to get insights into how often different guardrails are being detected and used.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

AI Guardian creates logs for all three guardrails available. Reviewing the logs can help you determine how often offensive content is generated, prompt injection attack attempts occur, or sensitive topics are detected.

See [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-guardian.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Use the more options menu item \(\[Omitted image "more-options-menu-item.png"\] Alt text: More options icon.\) and select **Export**.

    1.  For the offensiveness guardrail, go to **Now Assist Guardian** &gt; **Offensiveness**.

        Use the list in the **Active** tab to choose which workflow you want to export logs for.

    2.  For the prompt injection guardrail, go to **Now Assist Guardian** &gt; **Prompt Injection**.


## Result

The log is exported as a .csv file to your computer.

## What to do next

If you do not see any log data, then it is most likely that the guardrail has not been triggered yet. If you believe you should be seeing data but aren't, reach out to Now Support.

**Parent Topic:**[AI Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-guardian.md)

