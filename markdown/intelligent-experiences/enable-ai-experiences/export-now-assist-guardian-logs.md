---
title: Export Now Assist Guardian logs
description: Export logs from Now Assist Guardian to get insights into how often different guardrails are being detected and used.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/enable-ai-experiences/export-now-assist-guardian-logs.html
release: zurich
product: Enable AI Experiences
classification: enable-ai-experiences
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

See [Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-guardian.md) for more information.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Settings**.

2.  In the side panel, select Now Assist Guardian.

3.  Export logs for the guardrail.

<table><thead><tr><th align="left" id="d32817e136">

Option

</th><th align="left" id="d32817e139">

Description

</th></tr></thead><tbody><tr><td id="d32817e145">

**Export offensive content detection logs**

</td><td>

1.  Select **Now Assist Guardian** &gt; **Offensiveness**.
2.  In the **Active** tab, select the workflow you want to export logs for, and then select **Export**.


</td></tr><tr><td id="d32817e178">

**Export Prompt injection logs**

</td><td>

1.  Select **Now Assist Guardian** &gt; **Prompt Injection**.
2.  Select **Export Log**.


</td></tr><tr><td id="d32817e208">

**Export sensitive topic logs**

</td><td>

1.  Select **Now Assist Guardian** &gt; **Filters**.
2.  Select **Export Log**.


</td></tr></tbody>
</table>
## Result

The log is exported as a .csv file to your computer.

## What to do next

If you do not see any log data, then it is most likely that the guardrail has not been triggered yet. If you believe you should be seeing data but aren't, reach out to Now Support.

**Parent Topic:**[Now Assist Guardian](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/enable-ai-experiences/now-assist-guardian.md)

