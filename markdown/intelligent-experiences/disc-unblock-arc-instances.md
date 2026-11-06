---
title: Unblock ServiceNow Arc on user devices
description: Let users launch ServiceNow Arc again on machines where you previously blocked it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/disc-unblock-arc-instances.html
release: australia
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, use, Arc, unblock]
breadcrumb: [Working with ServiceNow Arc agent records, Discover and manage AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Unblock ServiceNow Arc on user devices

Let users launch ServiceNow Arc again on machines where you previously blocked it.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Assets**.

2.  Open the ServiceNow Arc agent record.

3.  Select the **Fleet** tab.

4.  Select the check box for each instance that you want to unblock.

    You can unblock only instances with an **Install Status** of **In Maintenance**.

5.  Select the more actions icon.

6.  Select **Unblock**.

7.  In the confirmation dialog box, review the people listed under **Fleet**.

8.  Select **Unblock** to confirm.


## Result

The Install Status of each unblocked instance changes to **Installed**, and the people on those devices can launch Arc again.

