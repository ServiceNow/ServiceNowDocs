---
title: Activate the Data Sensitivity Check
description: Activate the Data Sensitivity Check so that AI Gateway helps filter personally identifiable information in transactions with the MCP servers that you choose.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-gw-activate-dsc.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [Data Sensitivity Check, sensitive data]
breadcrumb: [AI Gateway settings, Configure, AI Gateway, Configure, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Activate the Data Sensitivity Check

Activate the Data Sensitivity Check so that AI Gateway helps filter personally identifiable information in transactions with the MCP servers that you choose.

## Before you begin

AI Gateway must be on. While it's paused, the policy can't be changed.

Role required: sn\_ai\_governance.ai\_steward or admin

## Procedure

1.  In AI Control Tower, navigate to **Settings** &gt; **AI Gateway**.

2.  Select the **Policies** tab.

3.  Optional: To define which data the policy detects, select **Configure sensitive data types**. The Data Privacy configuration opens in a new browser tab.

4.  Turn on the toggle in the policy banner, and then select **Activate** in the confirmation dialog.

    The banner reads **This policy is activated**. The change can take a few minutes to apply.

5.  In the **Servers running under this policy** list, turn on the **Active** toggle for each server that the policy should apply to, and then select **Activate** in the confirmation dialog for each one.


## Result

The policy applies to every tool on the servers whose **Active** toggle is on, and AI Gateway helps filter personally identifiable information in their transactions. To exclude individual tools on a server, see [Apply the Data Sensitivity Check to a server's tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-gw-apply-dsc-tools.md).

