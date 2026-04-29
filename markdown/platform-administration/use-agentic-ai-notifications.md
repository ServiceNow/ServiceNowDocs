---
title: Use email agentic workflow
description: Use email agentic workflow to intelligently analyze inbound emails, extract information, perform necessary actions, and draft responses.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, Agentic AI, generative AI, Gen AI, Agentic workflow, Intent to action]
breadcrumb: [Now Assist in Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Use email agentic workflow

Use email agentic workflow to intelligently analyze inbound emails, extract information, perform necessary actions, and draft responses.

## Email agentic workflows in email notifications

<table id="table_fx5_fn3_jhc"><thead><tr><th>

Agentic workflow name

</th><th>

Description

</th><th>

Available AI agents

</th></tr></thead><tbody><tr><td>

[Intent to action](../concept/email-agentic-workflow.md)

</td><td>

Triages tasks that are created via inbound emails by identifying intent, executing actions, and drafting appropriate email responses.

</td><td>

-   Intent Identification Agent
-   Intent Executor Agent
-   Email Generator Agent

</td></tr></tbody>
</table>## Role permissions and access

The execution role provides the minimum required permissions to execute intents. Additional intent execution roles can be added as needed to extend permissions for specific actions. Without these, the execution may fail due to insufficient permissions.

|Role|Description|
|----|-----------|
|sn\_notif\_agents.notification\_ai\_admin|Has permission to read and create intents, actions and map actions.|
|sn\_notif\_agents.notification\_ai\_reader|Has permission to read intents and actions.|
|sn\_notif\_agents.intent\_executor|Has permission to execute intents.|

**Note:** When an action runs, it uses the sender’s permission, guest users use the **guest\_email\_agent** role which is limited by default to **sn\_notif\_agents.intent\_executor**. If the execution action needs more access, those permissions must be added under the **sn\_notif\_agents.intent\_executor** role as a child role so it can run properly. The system masks the role based on user permissions, revealing only the roles common to both the user and the **sn\_notif\_agents.intent\_executor** roles.

**Email Generation for Reply Email Action**

After you connect an AI Search profile to the reply-email action, users can submit queries that can be answered using the profile’s content. AI Search check the sender’s permissions and returns only the information permitted for their role.

