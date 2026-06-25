---
title: Accept an incoming chat request from the Source-to-Pay Workspace
description: As a supplier fulfiller, accept an incoming chat request from the Supplier Manager Workspace Inbox to start a chat session with a supplier contact.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/accept-chat-supp-ws.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Accept an incoming chat request from the Source-to-Pay Workspace

As a supplier fulfiller, accept an incoming chat request from the Supplier Manager Workspace Inbox to start a chat session with a supplier contact.

## Before you begin

Role required: sn\_slm.owner

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Select the Inbox icon \(\[Omitted image "agent-inbox-icon.png"\] Alt text: Agent inbox icon\).

3.  Select **Available** from **Status** to indicate that you are available to accept the incoming chat request.

4.  When a chat comes through the chat queue, select **Accept**.

    You are automatically connected to the supplier contact in the chat queue. The Active Chat panel displays a pre-chat message acknowledging the chat request. You can review the information before you enter a response in the Active Chat panel.

    A new interaction record is created and chat details are displayed on the **Details** tab of the interaction. For more information, see [Virtual Agent interaction records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/va-interactions.md).

<table id="table_ljw_tmp_wwb"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Displays details about the interaction.

</td></tr><tr><td>

Supplier Information

</td><td>

Displays information about the supplier.For more information, see [View information on supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-info-tab.md).

</td></tr><tr><td>

User's Tasks

</td><td>

When a supplier contact communicates with an agent through chat, phone call, or SMS, the User’s Task related list shows the agent all of the other tasks that have been created for the supplier contact.

</td></tr><tr><td>

Supplier cases

</td><td>

Shows all the supplier cases associated with the interaction record.

</td></tr></tbody>
</table>5.  From the Active Chat panel, interact with the contact who initiated the chat through the **Public Chat** tab or chat with another user for any information related to the current chat queries through the **Private Chat** tab.

    From the Agent Chat panel, do the following:

    -   To chat, enter a message and select the send icon \(\[Omitted image "send-chat-icon.png"\] Alt text: Send chat icon\).
    -   To send an attachment, select the send attachment to chat icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachment icon\), select the file to attach, and select Open.
    -   To transfer the chat to another available agent, select the transfer to agent icon \(\[Omitted image "transfer-agent-icon.png"\] Alt text: Transfer agent icon\) and select the agent name.
6.  Perform additional tasks by selecting the following UI actions:

    |UI action|Description|
    |---------|-----------|
    |Create Supplier Case|Creates a new supplier case. For more information, see [Create New Supplier Case form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/new-supplier-case.md).|
    |End Chat|Ends the current chat session.|
    |Save|Saves any updates you made to the chat information.|
    |More actions icon \(\[Omitted image "more-actions-icon.png"\] Alt text: More actions icon.\)|Select **Associate Record** to associate an interaction to a supplier case.|


## Result

The incoming chat request from the Supplier Manager Workspace Inbox is accepted and a chat session with the supplier contact is initiated.

**Parent Topic:**[Using Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/use-supp-mgr-wsp.md)

**Related topics**  


[Create a supplier from the Source-to-Pay Workspace]()

[Manage supplier details]()

[Manage internal stakeholders]()

[Manage supplier contacts from the Source-to-Pay Workspace]()

[Manage supplier cases from the Source-to-Pay Workspace]()

[Manage supplier tasks from the Source-to-Pay Workspace]()

[Offboard a supplier from the Source-to-Pay Workspace]()

[Interaction Management in Supplier Lifecycle Operations]()

[Composing emails with predefined content from the Source-to-Pay Workspace]()

[Overall supplier dashboard]()

[Create supplier case from Universal Request]()

[Emails view for supplier managers]()

[Using Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/use-supp-mgr-wsp.md)

