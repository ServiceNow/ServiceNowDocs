---
title: Configure Virtual Agent for Public Sector Digital Services
description: Set up ServiceNow Virtual Agent so that conversation designers \(topic authors\) can create and modify automated conversations for public sector use cases. Virtual Agent for Public Sector Digital Services also helps your constituents complete common self-service tasks on the Government Service Portal with predefined Government Service Virtual Agent topics \(chatbot conversations\).
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Enable communication channels, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Virtual Agent for Public Sector Digital Services

Set up ServiceNow® Virtual Agent so that conversation designers \(topic authors\) can create and modify automated conversations for public sector use cases. Virtual Agent for Public Sector Digital Services also helps your constituents complete common self-service tasks on the Government Service Portal with predefined Government Service Virtual Agent topics \(chatbot conversations\).

**Note:** The Virtual Agent plugin \(com.glide.cs.chatbot\) must be activated.

## What to do before building Virtual Agent topics for public sector use cases

As admins or topic authors \(users with the virtual\_agent\_admin role\), you can do the following with Virtual Agent:

-   Use prebuilt conversations and topic blocks \(components that run subflows or common functions in a conversation\). Prebuilt conversations and topic blocks are available with the Virtual Agent platform, Customer Service Virtual Agent Conversations plugin \(com.sn\_csm.virtualagent\), and Service Request Playbook application. Prebuilt Public Sector topic blocks are available with the Public Sector Digital Services Core application.
-   Build your own custom, public sector conversation topics. You can duplicate prebuilt topics and topic blocks and then customize them as needed.

Before you or your topic authors \(users with the virtual\_agent\_admin role\) create or modify Virtual Agent conversations, meet the following prerequisites for working with prebuilt topics and topic blocks in Virtual Agent Designer:

-   [Activate the Glide Virtual Agent plugin](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) \(com.glide.cs.chatbot\) to access platform topics and topic blocks and run Virtual Agent Designer.
-   [Activate the Customer Service Virtual Agent plugin](https://www.servicenow.com/docs/access?context=activate-virtual-agent-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US) \(com.sn\_csm.virtualagent\) to access prebuilt Customer Service Management conversations and topic blocks.
-   [Become familiar with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) to create and update conversation topics.
-   [Install Public Sector Digital Services Core](../task/install-public-sector-digital-services-core.md) application to access public sector topic blocks that can be used in public sector conversations.
-   [Install Service Request Playbook for Public Sector Digital Services](../task/install-psds-service-request-playbook.md) to access the prebuilt topic, **Create a Service Request**.
-   [Install License and Permit Playbook for Public Sector Digital Services](../task/install-psds-license-permit-request-playbook.md) to access the prebuilt topic, **Start a License/Permit Application**.

## Configure Virtual Agent conversations for public sector users

As admins or topic authors \(users with the virtual\_agent\_admin role\), you can deploy prebuilt conversation topics to your end users, such as the **Create a Service Request** topic provided with the Service Request Playbook application, as well as custom conversation topics that you create.

These blocks are subflows that run conversational elements or common tasks in a conversation, such as adding or retrieving records. Topic blocks enable topic authors to add standard functions to Virtual Agent conversations, simplifying conversation design and maintenance.

1.  Configure Agent Chat in the Government Service Portal.
    1.  Navigate to **All** &gt;**Service Portal** &gt;**Agent Chat**.
    2.  Locate **GSP Chat**, and select the check box to set the record to **Active**.
2.  In Virtual Agent Designer, search for the corresponding topic block.
    -   For Service Request Playbook requests, search for and select **Create a Service Request**.
    -   For License and Permit Playbook requests, search for and select **Start a License/Permit Application**. For more information, see [Configure Virtual Agent for License and Permit Playbook](psds-lpr-configure-va.md).
3.  Select **Publish** to set the topic block to Active and make it available to your end users. For more information on creating and publishing Virtual Agent topics, see [Publish a Virtual Agent topic](https://www.servicenow.com/docs/access?context=publish-virtual-agent-topic&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

For more information on working with topics in Virtual Agent Designer, see [Getting Started with Virtual Agent Designer](https://www.servicenow.com/docs/access?context=conversation-designer-virtual-agent&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

## Example Virtual Agent topics

The Public Sector Digital Services Core application provides several base system topic blocks that you can use in public sector conversations:

-   Prompt Service for Constituent – Asks constituents to select a type of government service.
-   Create Public Sector Additional Members – Prompts constituents to add other persons who have an authorized interest in an issue or case.

-   **Prompt Service for Constituent topic block**

    Use this topic block in a conversation to ask constituents to select a service from a list of available government services, for example permits or licenses. Activate the Customer Service Virtual Agent Conversations \(com.sn\_csm.virtualagent\) plugin to use this topic block.

-   **Create Public Sector Additional Members topic block**

    Use this topic block to let your constituents specify other people, such as family members or other authorized individuals, who can view a case or issue. Activate the Customer Service Virtual Agent Conversations \(com.sn\_csm.virtualagent\) plugin to use this topic block.

    When you use this topic block in a conversation, you specify the input parameters from the originating \(calling\) topic to the topic block.

<table id="table_g4n_lhh_3tb"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

case\_id

</td><td>

Sys\_id of the public sector case record created.

</td></tr><tr><td>

case\_type

</td><td>

Extension of the base public sector service.

</td></tr></tbody>
</table>
To learn more about topic blocks and how to use them in Virtual Agent conversations, see [Maximizing code reuse with topic blocks](https://www.servicenow.com/docs/access?context=topic-blocks-overview&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

