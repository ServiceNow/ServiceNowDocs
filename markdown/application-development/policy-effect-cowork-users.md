---
title: How policy affects ServiceNow Arc users
description: Your administrator's policies decide what ServiceNow Arc can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/policy-effect-cowork-users.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [approval prompts, Always Allow, user controls, second factor]
breadcrumb: [Policy management and governance in ServiceNow Arc, Explore, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# How policy affects ServiceNow Arc users

Your administrator's policies decide what ServiceNow Arc can do for you. You see the result as approval prompts and blocked actions, and you can narrow some permissions yourself.

You can't see or change policy records. What you experience is the result:

-   **Approval prompts**

    A card describes an action before it runs and asks you to approve or deny it. For some actions, the card gives the option to **Always Allow**, which remembers your decision.

-   **Blocked actions**

    When a policy blocks an action or an external network call, Arc tells you why.

-   **Read only work**

    Commands that only read are exempt from prompts, so routine work isn't interrupted.


## Controls you can set

These controls can only narrow what your administrator allows.

|Control|Where|What it does|
|-------|-----|------------|
|Microsoft 365 connector scopes|**Settings** &gt; **Connectors**|For each capability, choose **Allow**, **Ask me first**, or **Deny**. If your administrator limited a capability, it shows **Set by your organization**, and only the choices within that limit are available. For more information, see [Manage Microsoft 365 action permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/set-m365-permissions.md).|
|Remembered approvals|**Settings** &gt; **Approvals**|See every **Always Allow** decision you've made, and revoke any of them.|
|Approval mode|**Settings** &gt; **Approvals**|Choose whether new chats start in **Standard** or **Auto** mode, when your administrator makes auto mode available.|
|Soft deletes|**Settings** &gt; **General**|Keep deleted files recoverable in a dump folder instead of removing them right away.|

**Parent Topic:**[Policy management and governance in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/policy-management-cowork.md)

