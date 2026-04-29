---
title: Export Now Assist Guardian logs
description: Export logs from Now Assist Guardian to get insights into how often different guardrails are being detected and used.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Export, Now Assist Guardian, logs, Gen AI, Generative AI, admin, offensiveness, prompt injection]
breadcrumb: [Now Assist Guardian, Now Assist Admin Settings, Exploring Now Assist Admin, Now Assist, Enable AI experiences]
---

# Export Now Assist Guardian logs

Export logs from Now Assist Guardian to get insights into how often different guardrails are being detected and used.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Now Assist Guardian logs all three types of guardrails available. Reviewing the logs can help you determine how often offensive content is generated, prompt injection attack attempts occur, or sensitive topics are detected.

See [Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Select the more options menu icon \(![More options icon.](../../now-assist-platform/images/more-options-menu-item.png)\) and select **Export**.

    1.  For the offensiveness guardrail, go to **Now Assist Guardian** &gt; **Offensiveness**.

        Use the list in the **Active** tab to select which workflow you want to export logs for.

    2.  For the prompt injection guardrail, go to **Now Assist Guardian** &gt; **Prompt Injection**.

    3.  For the sensitive topics, go to **Now Assist Guardian** &gt; **Filters**.


## Result

The log is exported as a .csv file to your computer.

## What to do next

If you do not see any log data, then it is most likely that the guardrail has not been triggered yet. If you believe you should be seeing data but aren't, reach out to Now Support.

**Parent Topic:**[Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md)

