---
title: How policy affects ServiceNow Cowork users
description: Your administrator's policies decide what ServiceNow Cowork can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/policy-effect-cowork-users.html
release: zurich
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [approval prompts, Allow always, user controls, second factor]
breadcrumb: [Policy management and governance in ServiceNow Cowork, Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# How policy affects ServiceNow Cowork users

Your administrator's policies decide what ServiceNow Cowork can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.

You can't see or change policy records. What you experience is the result:

-   **Approval prompts**

    A card describes an action before it runs and asks you to approve or deny it. For some actions, the card also offers **Allow always**, which remembers your decision. Other actions ask every time.

-   **Blocked actions**

    When a policy blocks an action or an external network call, Cowork tells you why.

-   **Read only work**

    Commands that only read are exempt from prompts, so routine work isn't interrupted.


## Controls you can set

These controls can only narrow what your administrator allows.

|Control|Where|What it does|
|-------|-----|------------|
|Microsoft 365 connector scopes|**Settings** &gt; **Microsoft 365**|Turn off individual scopes your administrator enabled, for example letting Cowork read mail but not send it. You can't turn on a scope your administrator hasn't enabled.|
|Remembered approvals|**Settings** &gt; **Approvals**|See every **Allow always** decision you've made, and revoke any of them.|
|Soft deletes|**Settings** &gt; **General**|Keep deleted files recoverable in a dump folder instead of removing them right away.|

**Parent Topic:**[Policy management and governance in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/policy-management-cowork.md)

