---
title: Block ServiceNow Arc on user devices
description: Stop ServiceNow Arc from starting on specific machines when you need to contain its use, without affecting other installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/disc-block-arc-instances.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use, Arc, block]
breadcrumb: [Working with ServiceNow Arc agent records, Discover and manage AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Block ServiceNow Arc on user devices

Stop ServiceNow Arc from starting on specific machines when you need to contain its use, without affecting other installations.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Assets**.

2.  Open the ServiceNow Arc agent record.

3.  Select the **Fleet** tab.

4.  Select the check box for each instance that you want to block.

    You can block only instances with an **Install Status** of **Installed**. Any instance already in maintenance that you select is left out of the block.

5.  Select **Block**.

6.  In the confirmation dialog box, review the people listed under **Fleet**.

7.  Select **Block** to confirm.


## Result

The Install Status of each blocked instance changes to **In Maintenance**. Arc can't start on those devices, and the people using them can't launch it until you unblock the instances.

