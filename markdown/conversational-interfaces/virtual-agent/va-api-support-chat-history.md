---
title: Configure to support chat history in Virtual Agent API
description: You can now support your live agents to see chat history in their conversations with the primary bot.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Configure to support chat history in Virtual Agent API

You can now support your live agents to see chat history in their conversations with the primary bot.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**, and then enter `sys_cs_provider_application.list` in the filter.

2.  Select the **VA Bot to Bot Provider Application** record to open it.

3.  In the Provider Channel Identity form, select the **Provider Identity Properties** related list and click **New**.

4.  On the Custom Adapter Property form, fill in the fields.

<table id="table_h1j_lfj_cgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the customer adapter property, such as `store_history_as`.

</td></tr><tr><td>

Value

</td><td>

Enter any one of the following inputs:-   `multi-text`: The chat history will be displayed in individual messages.
-   `text`: The chat history will be displayed in a single block.
-   `html`: The chat history will be displayed in HTML.


</td></tr><tr><td>

Description

</td><td>

Enter an explanation for this property: `The custom adapter property to display the chat history between the primary bot and the end user with enhancements.`

</td></tr></tbody>
</table>5.  Click **Submit**.


-   **[Setting logo for the primary bot in Virtual Agent API](va-api-support-set-logo.md)**  
You can customize your agent chat interface by setting a logo for the primary bot that appears in the chat history.

**Parent Topic:**[Using Virtual Agent API](../concept/use-virtual-agent-api.md)

