---
title: Using Virtual Agent for Public Sector Digital Services
description: As an admin, you can use Virtual Agent to create chatbot conversations tailored to public sector use cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Public Sector Digital Services \(PSDS\)]
---

# Using Virtual Agent for Public Sector Digital Services

As an admin, you can use Virtual Agent to create chatbot conversations tailored to public sector use cases.

With Virtual Agent for Public Sector Digital Services, which is available by subscription, you can build conversation topics that assist your constituents with self-service tasks. For example, you can create Virtual Agent topics that enable constituents to submit government service cases or help them find relevant information on government regulations or benefits.

As admins or topic authors, you can build your own custom, public sector conversation topics. Or, you can use pre-built conversations that are available with the Virtual Agent platform and Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\) and modify them for public sector use cases.

When you’re creating or modifying topics, you can also use pre-built components called topic blocks. These blocks are subflows that run conversational elements or common tasks in a conversation, such as adding or retrieving records. Pre-built topic blocks are included with the Virtual Agent platform and Customer Service conversations. Topic blocks enable topic authors to quickly add standard functions to Virtual Agent conversations, simplifying conversation design and maintenance.

The Public Sector Digital Services Core application provides several topic blocks that you can use in public sector conversations:

-   Prompt Service for Constituent – Asks constituents to select a type of government service.
-   Create Public Sector Additional Members – Prompts constituents to add other persons who have an authorized interest in an issue or case.

To learn more about topic blocks and how to use them in Virtual Agent conversations, see [Maximizing code reuse with topic blocks](https://www.servicenow.com/docs/access?context=topic-blocks-overview&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Before building Virtual Agent topics for public sector use cases

Before creating Virtual Agent conversations, review the following prerequisites and the basic process for working with pre-built topics and topic blocks in Virtual Agent Designer.

-   [Activate the Customer Service Virtual Agent Conversations plugin](https://www.servicenow.com/docs/access?context=activate-virtual-agent-csm&version=australia&pubname=australia-customer-service-management&ft:locale=en-US) \(com.sn\_csm.virtualagent\) to access pre-built Customer Service conversations and topic blocks.
-   Determine the public sector use cases for topics to be created.
-   In Virtual Agent Designer:
    -   [Preview \(test\) pre-built topics and topic blocks](https://www.servicenow.com/docs/access?context=va-designer-testing&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US), such as the public sector blocks, to see how they work. Use the **Type** filter to sort the list of items, such as topic blocks, in the Topics page.
    -   If you want to use a pre-built topic or topic block, [duplicate](https://www.servicenow.com/docs/access?context=duplicate-virtual-agent-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) and [publish](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) it.
    -   Add the appropriate copies of topic blocks, such as the public sector topic blocks, to the originating \(calling\) topic. To learn more about adding topic blocks to a conversation, see [Add a reusable topic block to a calling topic or topic block](https://www.servicenow.com/docs/access?context=add-topic-blocks-to-topic&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US)

        **Note:** You can use both public sector topic blocks in a conversation.


## Prompt Service for Constituent topic block

Use this topic block in a conversation to ask constituents to select a service from a list of available government services, for example permits or licenses. Activate the Customer Service Virtual Agent Conversations \(com.sn\_csm.virtualagent\) plugin to use this topic block.



## Create Public Sector Additional Members topic block

Use this topic block to let your constituents specify other people, such as family members or other authorized individuals, who can view a case or issue. Activate the Customer Service Virtual Agent Conversations \(com.sn\_csm.virtualagent\) plugin to use this topic block.



When you use this topic block in a conversation, you specify the input parameters from the originating \(calling\) topic to the topic block.

<table id="table_g4n_lhh_3tb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

case\_id

</td><td>

sys\_id of the public sector case record created.

</td></tr><tr><td>

case\_type

</td><td>

Extension of the base public sector service.

</td></tr></tbody>
</table>