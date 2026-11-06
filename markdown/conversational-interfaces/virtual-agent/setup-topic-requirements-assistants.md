---
title: Setup topic requirements for assistants
description: Setup topics handle the basic parts of a chat, such as greeting users, ending the chat, and responding when the assistant can't interpret a request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/virtual-agent/setup-topic-requirements-assistants.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Virtual Agent reference, Reference, Virtual Agent, Conversational Interfaces]
---

# Setup topic requirements for assistants

Setup topics handle the basic parts of a chat, such as greeting users, ending the chat, and responding when the assistant can't interpret a request.

You can create custom versions of these topics. For the assistant to use them, they must be set up correctly.

If a setting is missing, the assistant skips the topic and doesn't show an error. For example, you create a custom topic, such as a live agent topic, but the assistant doesn't show or run it. The topic is likely missing one of the required settings.

Make sure your custom topic meets the requirements. The custom topics that the requirements apply to are:

-   Custom greeting topic
-   Closing topic
-   Survey topic
-   Live agent topic
-   Custom fallback topic
-   Error topic \(legacy experiences only\). Legacy refers to standard and enhanced chat.

The requirements apply to assistants that use standard, enhanced, or premium chat.

## What to set

To find these settings, go to **Assistant Designer** &gt; **Asset Library** and create a topic, or open an existing topic and select the **Properties** tab.

|Setting|What to choose|
|-------|--------------|
|Type|Setup Topic|
|Status|Active and published|
|Model type|LLM|
|System roles|The `public` role, so that all users can use the topic|
|Application scope|Global \(recommended, because other scopes can cause access problems\)|
|Topic context|A context that returns `true` for every user who uses the assistant|
|Assistant|The LLM assistant \(recommended, so the assistant can find the topic\)|

**Note:** If your fallback topic uses a record producer catalog item, make sure the item is active and that the assistant can access its scope.

## Add your topics to the assistant

1.  In **Assistant Designer**, select an assistant, and go to the **Chat experience** page.
2.  Add your setup topics on the **Messages** and **Fallbacks** tabs.

Each tab has a legacy section and a premium section. If both enhanced and premium chat are turned on, your setup topics appear in all four places: **Legacy messages**, **Premium messages**, **Legacy fallbacks**, and **Premium fallbacks**.

## Test your topic

Test as a regular user, not as an administrator. Administrators can sometimes see topics that other users can't, which hides problems. Use the Auto Eval feature to check that the assistant can find and use your topic.

**Parent Topic:**[ServiceNow Otto for Virtual Agent reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/conversational-interfaces/virtual-agent/now-assist-in-va-reference.md)

