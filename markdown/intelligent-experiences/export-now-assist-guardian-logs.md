---
title: Export Now Assist Guardian logs
description: Export logs from Now Assist Guardian to get insights into how often different guardrails are being detected and used.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-11-22"
reading_time_minutes: 1
keywords: [Export, Now Assist Guardian, logs, Gen AI, Generative AI, admin, offensiveness, prompt injection]
breadcrumb: [Configuring Now Assist settings and features, Now Assist, Enable AI experiences]
---

# Export Now Assist Guardian logs

Export logs from Now Assist Guardian to get insights into how often different guardrails are being detected and used.

## Before you begin

Role required: sn\_generative\_ai.nsa\_admin

## About this task

Now Assist Guardian creates logs for all three guardrails available. Reviewing the logs can help you determine how often offensive content is generated, prompt injection attack attempts occur, or sensitive topics are detected.

See [Now Assist Guardian](../../now-assist-platform/concept/now-assist-guardian.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  Use the more options menu item \(![More options icon.](../../now-assist-platform/images/more-options-menu-item.png)\) and select **Export**.

    1.  For the offensiveness guardrail, go to **Now Assist Guardian** &gt; **Offensiveness**.

        Use the list in the **Active** tab to choose which workflow you want to export logs for.

    2.  For the prompt injection guardrail, go to **Now Assist Guardian** &gt; **Prompt Injection**.


## Result

The log is exported as a .csv file to your computer.

## What to do next

If you do not see any log data, then it is most likely that the guardrail has not been triggered yet. If you believe you should be seeing data but aren't, reach out to Now Support.

**Parent Topic:**[Configuring Now Assist settings and features](../concept/configuring-na-landing.md)

