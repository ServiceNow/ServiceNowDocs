---
title: Add your bot to a portal
description: Give your users a place to interact with your bot and human agents. Choose a Service Portal chat configuration provided with your base system, such as the Service Portal Agent Chat configuration used for Agent Chat and Virtual Agent. Your end users can initiate and maintain a bot or Agent Chat conversation in any page of the portal.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, Service Portal, Agent Chat, bot, portal, com.glide.cs.chatbot, com.glide.interaction.awa]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Add your bot to a portal

Give your users a place to interact with your bot and human agents. Choose a Service Portal chat configuration provided with your base system, such as the Service Portal Agent Chat configuration used for Agent Chat and Virtual Agent. Your end users can initiate and maintain a bot or Agent Chat conversation in any page of the portal.

## Before you begin

Activate the Glide Virtual Agent \(com.glide.cs.chatbot\) or the Agent Chat \(com.glide.interaction.awa\) plugin. You can activate the Glide Virtual Agent plugin only if you have a subscription.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Home**.

2.  Under **Add your bot to a portal**, select **Add to portal** to configure the base system portal.

    For example, to configure the portal used for Agent Chat and Virtual Agent, select Service Portal Agent Chat Config.

3.  On the form, update the portal configuration.

<table id="table_g4z_ldq_zgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Option to make the configuration active. The base system Service Portal configurations are automatically active.

</td></tr><tr><td>

Name

</td><td>

Unique name for the configuration record.

</td></tr><tr><td>

Portals

</td><td>

The portals in which you would like to use this chat configuration. If no portal is selected, the configuration applies to all portals in the system.

</td></tr><tr><td>

Application

</td><td>

Read-only application scope for the record.

</td></tr><tr><td>

Public

</td><td>

Option to make the portal available to users before they log in.

</td></tr><tr><td>

Roles

</td><td>

Roles that a user must have to use the portal. If you don't select a role, Agent Chat and Virtual Agent is available to all users regardless of their role.

</td></tr><tr><td>

Order

</td><td>

Number that indicates the order in which the configurations should run. Only one configuration applies per portal. If there are multiple configurations on a portal, the system runs the first configuration found from lowest to highest.

</td></tr><tr><td>

Server script

</td><td>

A script that passes page and widget data to an Agent Chat conversation when a user initiates the conversation. For example, pass a field to the chat conversation to enable Agent Chat to access the value. Data passed in this script is available to every page in the portal associated with this record. This script has access to the GlideSPScriptable API.

 **Note:** The portal suffix, page ID, and language are automatically available to Agent Chat and do not require a custom script. Sys ID and table are automatically available to Agent Chat when they are present in the URL.

 The following example returns an object containing the list of catalogs associated with the portal to the current conversation.

 ```
(function ($sp) {    
   return {        
      catalogs: $sp.getValue(‘catalogs’) 
   };
})($sp);
```

 When Agent Chat opens in an `iframe` HTML element, the list of catalogs is included in the `iframe` URL. Parameters from this field override any conflicting page data passed to Agent Chat.

</td></tr></tbody>
</table>4.  Select **Update**.


## Result

Your end users can initiate and maintain an Agent Chat or Virtual Agent conversation from any page in the selected portal.

## What to do next

-   **See your portal in action**

    Return to Conversational Interfaces Home and under **Add your bot to a portal**, select the second navigation dot at the bottom of the card. When the card changes to **Interact with your bot**, use the **Open portal** menu to select the portal to view. When the specified portal page opens, select the chat icon in the lower right corner to start a bot conversation.

-   **Configure other Service Portal Agent Chat features**

    In Service Portal, you can customize the Agent Chat button and pass page data to Agent Chat. For more information, see Configure Agent Chat in Service Portal.


**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

