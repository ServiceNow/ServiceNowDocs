---
title: Manage the AI services registry
description: Manage the AI services that your organization want to track by marking an entry as not shadow AI, or by making it active again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/sh-ai-manage-registry.html
release: zurich
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 1
keywords: [registry, Shadow AI, Track AI services]
breadcrumb: [Assess AI exposure, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Manage the AI services registry

Manage the AI services that your organization want to track by marking an entry as not shadow AI, or by making it active again.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

The registry is the catalog Shadow AI checks against to recognize a domain as an AI service. Selecting **Mark as not Shadow AI** has the same effect as choosing **This is not Shadow AI** from a detected service's record. When an entry is identified this way, the system stops flagging it going forward.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Shadow AI**.

2.  On the **Track AI services** card, select the arrow icon.

3.  In the Track AI services page, find or search for the entry that you want to change.

    **Match type** tells you how broadly an entry matches. **Exact** matches only that domain, and **Contains** matches any URL containing the pattern, which is how one entry covers a provider's many subdomains.

4.  Control whether AI-related traffic is detected for the service by updating the status.

<table id="choicetable_ydw_3cx_3kc"><thead><tr><th align="left" id="d63123e133">

Option

</th><th align="left" id="d63123e136">

Steps

</th></tr></thead><tbody><tr><td id="d63123e142">

**Mark as active**

</td><td>

1.  Select the check box next to the entry that you want to manage.
2.  Select **Actions**.
3.  Enable traffic detection by selecting **Mark as active**.


</td></tr><tr><td id="d63123e169">

**Mark as not Shadow AI**

</td><td>

1.  Select the check box next to the entry that you want to manage.
2.  Select **Actions**.
3.  Disable traffic detection by selecting **Mark as not Shadow AI**.


</td></tr></tbody>
</table>
## What to do next

If you selected **Mark as active**, review traffic from the AI service in the Shadow AI overview. See [Shadow AI overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-overview.md).

**Parent Topic:**[Assessing AI exposure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-assessing-ai-exposure.md)

