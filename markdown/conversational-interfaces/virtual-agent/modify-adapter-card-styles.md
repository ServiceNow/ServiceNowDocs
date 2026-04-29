---
title: Modify adapter card styles for Virtual Agent
description: Adapter cards are defined in the Adapter Cards \[sys\_cs\_adapter\_card\] table. Each card has a template for each supported channel to ensure it displays correctly. You can modify the channel templates to accommodate your organization's style requirements.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Modify, adapter card, templates, styles, Virtual Agent]
breadcrumb: [Conversational custom chat integrations, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Modify adapter card styles for Virtual Agent

Adapter cards are defined in the Adapter Cards \[sys\_cs\_adapter\_card\] table. Each card has a template for each supported channel to ensure it displays correctly. You can modify the channel templates to accommodate your organization's style requirements.

## Before you begin

Adapter card templates are stored in the Adapter Card Templates \[sys\_cs\_adapter\_card\_template\] table, which is available from the Adapter Cards table as a related list. For example, the YouTube Video Card adapter has three default templates, for the chat widget, iOS, and Android devices.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_adapter_card.list` in the navigation filter.

    The Adapter Cards page opens.

2.  Select an entry in the **Card Name** column.

3.  In the **Adapter Cards Template** related list, select the channel you want to view or modify.

    For example, select the active link for **Chat Widget** or **Android Device** to view the corresponding style sheet.

4.  Make any changes in the **Template Definition** field.

5.  Select **Update**.


**Parent Topic:**[Creating conversational custom chat integrations in Virtual Agent](../concept/va-custom-adapter-framework.md)

