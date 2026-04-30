---
title: Live agent chat context variables
description: Use chat context variables to pass certain information from the topic to share with a live agent or to control how bot conversations are routed to live agents. Virtual Agent includes some default variables, and you can define new ones.
locale: en-US
release: yokohama
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: reference
last_updated: "2025-02-25"
reading_time_minutes: 4
keywords: [Live Agent, chat, context, variables, Virtual Agent, Interaction, Connect Support]
breadcrumb: [Configure context variables for storing chat-related information, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Live agent chat context variables

Use chat context variables to pass certain information from the topic to share with a live agent or to control how bot conversations are routed to live agents. Virtual Agent includes some default variables, and you can define new ones.

**Note:** The Interaction table is part of the interaction management framework, which is activated through the Interactions Management plugin \(com.glide.interaction\). This plugin is included with the Agent Chat \(com.glide.interaction.awa\) and Connect Support \(com.glide.connect.support\) plugins.

<table id="table_urp_2tg_rpb"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

application

</td><td>

Application scope of the chat. For example, **Global**, **HR**, **CSM**, or **ITSM**.

</td></tr><tr><td>

auto\_resolution\_context\_id

</td><td>

If Auto Resolution is enabled, the ID of the record created when a requester is redirected to Virtual Agent.

</td></tr><tr><td>

case

</td><td>

Case ID \(from the \[sn\_customerservice\_case\] table\) that is used with the Customer Service Management application when a case is related to the chat.

</td></tr><tr><td>

csp\_category

</td><td>

Category defined in the Consumer Service portal in the CSM application \(requires the com.glide.service-portal.consumer-portal plugin\).

 For more information, see [Using the Consumer Service Portal](https://www.servicenow.com/docs/access?context=use-consumer-service-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

csp\_email

</td><td>

Requester’s email address, as entered in a pre-chat survey on the Consumer Service Portal.

</td></tr><tr><td>

csp\_first\_name

</td><td>

Requester’s first name, as entered in a pre-chat survey on the Consumer Service Portal.

</td></tr><tr><td>

csp\_last\_name

</td><td>

Requester’s last name, as entered in a pre-chat survey on the Consumer Service Portal.

</td></tr><tr><td>

devicetype

</td><td>

Type of device being used for the chat. For example, **mweb** \(chat widget\), **android**, or **ios**.

</td></tr><tr><td>

esc\_pre\_chat\_ask\_a\_question

</td><td>

Requester response to a pre-chat survey selection from within the HR Service Delivery application ESC view of the HR Case record.

</td></tr><tr><td>

experience\_name

</td><td>

Name assigned to the Live Agent experience.

</td></tr><tr><td>

hr\_topic\_id

</td><td>

ID of the current topic. Used in Advanced Work Assignment to determine which HR queue to transfer the user for live agent chat.

</td></tr><tr><td>

interaction\_account

</td><td>

Used with CSM chats that are initiated by B2B users who are tracked as contacts for a particular account. Corresponds with the **Account** field on the Interaction \[interaction\] table, which references the Accounts \[customer\_account\] table.

</td></tr><tr><td>

interaction\_consumer

</td><td>

Used with CSM chats that are initiated by B2C users who are tracked as consumers. Matches the interaction.consumer field referencing the csm\_consumer table. Corresponds with the **Consumer** field on the Interaction \[interaction\] table, which references the Consumers \[csm\_consumer\] table.

</td></tr><tr><td>

interaction\_contact

</td><td>

Used with CSM chats that are initiated by B2B users who are tracked as contacts for a particular account. Corresponds with the **Contact** field on the Interaction \[interaction\] table, which references the Contacts \[customer\_contact\] table.

</td></tr><tr><td>

interaction\_id

</td><td>

Sys\_id of the interaction record associated with the chat session.For more information, see [Virtual Agent interaction records](../concept/va-interactions.md).

</td></tr><tr><td>

language

</td><td>

Two-letter language code for the requester's chat.**Note:** Language values use ISO standard two-character language codes. For more information, see [ISO 639.1 language codes](http://www.loc.gov/standards/iso639-2/php/code_list.php).

</td></tr><tr><td>

mandatory\_skills

</td><td>

Required skills and skill level for an agent.For example, German language proficiency with an associated high skill level may be required for German-speaking requesters. You can define mandatory skills and activate skill levels in Advanced Work Assignment. For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

optional\_skills

</td><td>

Skills and skill levels that would be useful for a given chat scenario.You can define optional skills in Advanced Work Assignment. For more information, see [Configure agent assignment rules](https://www.servicenow.com/docs/access?context=awa-create-assignment-rule&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

page

</td><td>

The specific page \(within a portal\) that the chat was accessed from.

</td></tr><tr><td>

portal

</td><td>

Name of the portal that the chat was accessed from.

</td></tr><tr><td>

post\_assessment\_instance

</td><td>

Reference to the post-chat survey \(Assessment Instances \[asmt\_assessment\_instance\] table\), if there is one.

</td></tr><tr><td>

post\_chat\_survey\_name

</td><td>

Name of a post-chat survey that is used to gather feedback from the requester.For information about creating surveys, see [Create chat surveys](../../conversational-interfaces/task/create-chat-surveys.md).

 For information about creating surveys in Connect Chat, see [Configure a survey in Connect Chat support](https://www.servicenow.com/docs/access?context=take-survey-connect-chat&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

pre\_assessment\_instance

</td><td>

Reference to the pre-chat survey \(Assessment Instances \[asmt\_assessment\_instance\] table\), if there is one.

</td></tr><tr><td>

pre\_chat\_survey\_name

</td><td>

Name of a pre-chat survey that is used to gather information from the requester.For information about creating surveys, see [Create chat surveys](../../conversational-interfaces/task/create-chat-surveys.md). To learn more about how chat context variables from pre-chat surveys are used in Advanced Work Assignment to route work to live agents, see [Work item queues](https://www.servicenow.com/docs/access?context=awa-queues&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

 For information about creating surveys in Connect Chat, see [Configure a survey in Connect Chat support](https://www.servicenow.com/docs/access?context=take-survey-connect-chat&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

queue

</td><td>

Sys\_id of the pre-built Connect Support chat queue \(deprecated\).

</td></tr><tr><td>

search\_text

</td><td>

Search terms entered by the requester. Used to search Virtual Agent topics.

</td></tr><tr><td>

short\_description

</td><td>

Used to set the short description in the interaction record associated with the chat.

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of a record that relates to the interaction. Typically, this is the record being viewed in the portal when the chat is requested.

</td></tr><tr><td>

table

</td><td>

Table containing the record that relates to the interaction. Typically, this is the record being viewed in the portal when the chat is requested.

</td></tr><tr><td>

url

</td><td>

URL from which the request originates.

</td></tr></tbody>
</table>## Additional resources

-   [How to transfer a chat to a specific queue using context variables](https://www.servicenow.com/community/virtual-agent-nlu-articles/how-to-transfer-a-chat-to-a-specific-queue-using-context/ta-p/2307392)
-   [Virtual Agent and Natural Language Understanding \(NLU\) community forum](https://community.servicenow.com/community?id=community_forum&sys_id=bf5abf94db54e3c42be0a851ca961915)
-   [Conversational Interfaces Academy](https://www.servicenow.com/community/virtual-agent-nlu-articles/conversational-interfaces-academy-live-builds-and-q-amp-a-join/ta-p/2345155)

**Parent Topic:**[Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md)

