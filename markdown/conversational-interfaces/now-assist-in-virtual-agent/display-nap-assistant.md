---
title: Display your assistant on Platform or ServiceNow Studio
description: Use a chat experience for your Now Assist panel - Platform \(default\) assistant or Now Assist panel - Developer assistant.
locale: en-US
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-06-24"
reading_time_minutes: 2
breadcrumb: [Select a display experience, Create a chat assistant, View assistants, Configuring assistants overview, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Display your assistant on Platform or ServiceNow Studio

Use a chat experience for your Now Assist panel - Platform \(default\) assistant or Now Assist panel - Developer assistant.

## Before you begin

See [Add assets to a chat assistant](add-assets.md).

Role required: virtual\_agent\_admin or admin

## About this task

For Now Assist panel – Platform assistant, new and upgrading customers have the option to opt into the premium chat experience. ServiceNow performs a set of readiness checks to confirm that your instance is eligible for premium chat. If your instance doesn’t meet the requirements, you can continue using your existing standard or enhanced chat experience. After an upgrade, there may be a delay before premium chat is available to choose from.

**Note:** Premium chat does not apply to instances in regulated markets \(Government Cloud Community\), instances that use domain separation, or regional data routing.

For more information about premium chat, see [Premium chat](https://www.servicenow.com/docs/access?context=now-assist-panel-premium&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), otherwise, proceed to step 1.

Due to the premium chat upgrade, legacy messages \(chat messages\) and legacy fallbacks \(chat fallbacks\) settings haven't been migrated and you must review, configure, and customize them in premium messages and premium fallbacks. See [Manage an assistant chat experience](manage-assistant-chat-experience.md). If you need help, contact Support.

For Now Assist panel – Developer assistant, premium chat is not available. Proceed to step 2.

## Procedure

1.  Select a chat experience for your Now Assist panel - Platform assistant \(default\).

    1.  The **Add ServiceNow platform** &gt; **Unified Navigation app shell** is preselected as the display experience. If you're a new customer, the **Unified Navigation App Shell** isn't preselected, and you will have to select it from the **Add ServiceNow platform** drop-down menu.

        ![Display experience for Now Assist panel - Platform](../image/NAinVA-nap-premium-0426.png "Display experience for Now Assist panel - Platform")

        **Note:** If you're a new or upgrading customer, you can edit your chat experience from premium chat to your previous chat experience \(standard or enhanced chat\). By default, the **sn\_nowassist\_va.enable\_nap\_aix\_experience** system property is set to `false`. Setting the system property to `true` disables chat experience editing.

    2.  Select the pencil icon if you want to edit the chat experience. The **Edit chat experience** modal appears.

        ![Select a chat experience from the modal.](../image/NAinVA-display-NAP-platform-modal-0426.png "Edit the chat experience")

2.  Use ServiceNow Studio with standard chat for your Now Assist panel Developer assistant.

    ServiceNow Studio with standard chat is the only available display experience for the Now Assist panel - Developer assistant.

    ![Display experience for Now Assist panel - Developer](../image/NAinVA-nap-dev-display-122025.png "Display experience for Now Assist panel - Developer") ![]( "Display experience for Now Assist panel - Developer")

3.  Select **Save and continue**.


## What to do next

See [Brand an assistant](brand-assistant.md).

