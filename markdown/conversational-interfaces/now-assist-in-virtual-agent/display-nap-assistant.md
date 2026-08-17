---
title: Display your assistant on Platform or ServiceNow Studio
description: Use a chat experience for your ServiceNow Otto panel - Platform \(default\) assistant or ServiceNow Otto panel - Developer assistant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/display-nap-assistant.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2025-06-24"
reading_time_minutes: 2
breadcrumb: [Select a display experience, Create a chat assistant, View assistants, Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Display your assistant on Platform or ServiceNow Studio

Use a chat experience for your ServiceNow Otto panel - Platform \(default\) assistant or ServiceNow Otto panel - Developer assistant.

## Before you begin

See [Add assets to a chat assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/add-assets.md).

Role required: virtual\_agent\_admin or admin

## About this task

If your instance is eligible, you can opt into the premium chat experience. ServiceNow performs a set of readiness checks to see if your instance is eligible for premium chat. The default chat experience is enhanced chat. However, if you also previously had standard chat enabled, you still have that as an option.

**Note:** An alert is shown when:

-   The instance is eligible for premium chat.
-   There is a possible delay for premium chat to appear as an option on your instance.

Remember to refresh your browser to view the option to opt in to the premium chat experience. Premium chat is not available for instances in regulated markets \(Government Cloud Community\), instances that use domain separation, or regional data routing.

If your instance doesn’t meet the requirements, you can continue using your existing standard or enhanced chat experience. For more information about premium chat, see [Premium chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-premium.md), otherwise, proceed to step 1.

For premium chat, your premium messages and premium fallbacks are prefilled with what you had in your legacy messages and legacy fallbacks. Review the settings to ensure that everything was prefilled correctly.

For ServiceNow Otto panel – Developer assistant, premium chat is not available. Proceed to step 2.

## Procedure

1.  Select a chat experience for your ServiceNow Otto panel - Platform assistant \(default\).

    1.  The **Add ServiceNow platform** &gt; **Unified Navigation app shell** is preselected as the display experience.

        \[Omitted image "sno-nap-premium-0826.png"\] Alt text: Display experience for ServiceNow Otto panel - Platform

    2.  Select the pencil icon if you want to edit the chat experience. The **Edit chat experience** modal appears.

        \[Omitted image "NAinVA-display-NAP-platform-modal-0426.png"\] Alt text: Select a chat experience from the modal.

        In premium chat, catalog items have improved fluidity, but some will no longer be conversational. They’ll open in a catalog form instead. For more information, see [Conversational catalog item requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/explore.md).

2.  Use ServiceNow Studio with standard chat for your ServiceNow Otto panel Developer assistant.

    ServiceNow Studio with standard chat is the only available display experience for the ServiceNow Otto panel - Developer assistant.

    \[Omitted image "sno-nap-dev-display-0826.png"\] Alt text: Display experience for ServiceNow Otto panel - Developer

3.  Select **Save and continue**.


## What to do next

For help with installation, see [Solving installation and configuration issues with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-install-config-checklist.md).

See [Brand and personalize an assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/now-assist-in-virtual-agent/brand-assistant.md).

