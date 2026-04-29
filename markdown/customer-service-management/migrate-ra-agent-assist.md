---
title: Enable AI search in Recommended Actions
description: As an admin, you can enable the Recommended Actions - AI search on the Front-line case page, CSM default record page, and CSM Interaction page \(for chat, video, walk-up, and email channels\) by setting the hideAgentAssistShowRA UX page property to true.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring AI search, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Enable AI search in Recommended Actions

As an admin, you can enable the Recommended Actions - AI search on the Front-line case page, CSM default record page, and CSM Interaction page \(for chat, video, walk-up, and email channels\) by setting the **hideAgentAssistShowRA** UX page property to true.

## Before you begin

Role required: admin

## About this task

The Recommended Actions - AI search is available for the following pages:

-   CSM default record page
-   Front-line case page
-   CSM Interaction record page for chat, video, email, and walk-up channels

The following table shows how you can avail Recommended Actions - AI search feature:

<table id="table_lyt_xwd_w2c"><thead><tr><th>

Version

</th><th>

Feature availability

</th></tr></thead><tbody><tr><td>

New customers starting with Yokohama release

</td><td>

Recommended Actions - AI Search is an integral part of the Contextual Side Panel by default. No additional manual configuration is required.

</td></tr><tr><td>

Customers who on-boarded before Yokohama release

</td><td>

Agent Assist is enabled by default with the option to manually migrate to Recommended Actions - AI search.To migrate from Agent Assist to Recommended Actions - AI Search create and set the **hideAgentAssistShowRA** UX page property to `True`.

**Note:** If you already created this property for enabling [Recommended Actions in the chat interaction record](../concept/ra-csm-chat-interaction-record.md), you need not create it again.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All**.

2.  Search for `sys_ux_page_property.LIST` and press Enter.

    **Note:** If the **hideAgentAssistShowRA** UX page property already exists, you need not create it again.

3.  Select **New**.

4.  Fill in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Page|Page for which the property is applicable. Select `CSM/FSM Configurable Workspace`.|
    |Name|Name of the page property. Give the name as `hideAgentAssistShowRA`.|
    |Type|True or False|
    |Value|Enables or disables the property. Set the value to `true` to enable the property.|
    |Application|Application scope in which the property is being created.|
    |Description|Brief description of the UX page property that you are creating.|

5.  Select **Save**.


