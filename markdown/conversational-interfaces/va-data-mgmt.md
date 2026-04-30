---
title: Data management in Conversational Interfaces
description: Use data management tools, such as table cleaners, to maintain Conversational Interfaces tables.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Conversational Interfaces reference, Conversational Interfaces Console, Conversational Interfaces]
---

# Data management in Conversational Interfaces

Use data management tools, such as table cleaners, to maintain Conversational Interfaces tables.

## Virtual Agent table cleaning

Virtual Agent has a data retention policy that automatically deletes records from certain base system tables when they reach a specific age, to prevent tables from growing to an unmanageable size. Some Virtual Agent and related Conversational Interfaces tables are not automatically cleaned. You can activate table cleaning for the following tables.

<table id="table_n51_xgr_xpb"><thead><tr><th>

Table label

</th><th>

Table name

</th><th>

Description

</th><th>

Default record age \(seconds\)

</th></tr></thead><tbody><tr><td>

Chat Server Analytics

</td><td>

sys\_cs\_analytics

</td><td>

Server records that include sys IDs for messages, threads, conversations, users, and events.

</td><td>

7,776,000

</td></tr><tr><td>

Conversations

</td><td>

sys\_cs\_conversation

</td><td>

Conversation details, including topic definition, device used, and consumer \(user\).**Note:** Table cleaner also automatically deletes the related records for the following:

-   Conversation Messages
-   Conversation Tasks
-   Conversation Members
-   Session bindings
-   Profane message logs if using the Profanity Filter

</td><td>

5,184,000

</td></tr><tr><td>

Message Last Reads

</td><td>

sys\_cs\_message\_last\_read

</td><td>

Message IDs of the last messages read by users in chat and messaging channels.

</td><td>

15,552,000

</td></tr><tr><td>

CI Analytics

</td><td>

sys\_ci\_analytics

</td><td>

Conversation details used in Conversational Analytics. If the conversation ID is available, table cleaner removes closed, complete, and faulted conversations from the Conversations \[sys\_cs\_conversation\] table.

</td><td>

604,800

</td></tr></tbody>
</table>The Auto Flushes \[sys\_auto\_flush\] table lists the base system tables and their corresponding record ages. When table cleaning is activated, the Table Cleaner scheduled job triggers the table cleaner to remove the records that meet the default record age. If needed, you can change the record age for a table and specify any conditions to filter the records to be removed. For details, see [Activate table cleaning for Virtual Agent tables](../task/activate-va-table-cleaning.md).

If a table has related child tables, the table cleaner automatically performs a cascade delete to remove the related child tables. For example, when table cleaning is activated for the Conversation \[sys\_cs\_conversation\] table, the table cleaner runs automatically when the table is 60 days \(5,184,000 seconds\) old. The table cleaner also performs a cascade delete to remove the related child tables. To learn more about table cleaning in the ServiceNow AI Platform, see [Table cleaner](https://www.servicenow.com/docs/access?context=table-cleaner&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   **[Activate table cleaning for Virtual Agent tables](../task/activate-va-table-cleaning.md)**  
Activate table cleaning for certain tables used in Virtual Agent and Conversational Interfaces.

**Parent Topic:**[Conversational Interfaces reference](../../conversational-interfaces/concept/ci-reference-parent.md)

