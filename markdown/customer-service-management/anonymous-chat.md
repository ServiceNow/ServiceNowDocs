---
title: Anonymous chat
description: Anonymous chat allows guest users to initiate chat sessions with consumer service agents through the Consumer Service Portal without requiring authentication.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Customer Service Management]
---

# Anonymous chat

Anonymous chat allows guest users to initiate chat sessions with consumer service agents through the Consumer Service Portal without requiring authentication.

From the Consumer Service Portal, guest users can click the **Chat** link in the portal header to initiate a chat session with a consumer service agent. Clicking this link opens a form that requests some basic information, including the user's name, email address, and type of issue. Completing and submitting the form creates a chat request that is routed to the appropriate agent queue based on the selected issue type. Once the assigned agent accepts the request, a chat session is established. If necessary, the agent can create a consumer record or a case for the guest user, or transfer the chat to another agent.

## Setting up anonymous chat

Setting up the anonymous chat feature involves the following steps.

1.  Activate the Consumer Service Portal plugin \(com.glide.service-portal.consumer-portal\).
2.  Modify the default anonymous chat record producer or create a new record producer.
3.  Create one matching rule for each agent queue.
4.  Configure anonymous chat properties.
5.  If necessary, modify the Connect actions to provide the desired functionality for consumer service agents in chat conversations. The anonymous chat feature includes these actions: **Create Case for Guest** and **Create Consumer and Case for Guest**. For more information, see [Administer Connect actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/t_AdministerConnectActions.md).

## Anonymous chat plugins

The anonymous chat feature requires two plugins which are activated as part of the Consumer Service Portal plugin:

-   Anonymous Connect Support \(com.glide.connect.anonymous\_support\): enables the anonymous chat feature for Connect.
-   Connect Support Routing \(com.glide.connect.support.routing\): routes Connect Support requests to the appropriate chat queue.

## Anonymous chat record producer

The form used to request information from a guest user is a configurable record producer based on the Consumer Interaction table \(sn\_customerservice\_customer\_interaction\), which is a new table in the Istanbul release. When a guest user submits the form, the information provided is stored as a record in the Customer Interaction table. This record is used for routing the chat request.

The default anonymous chat record producer, **What can we help you with?**, is located at **Service Catalog** &gt; **Catalog Definition** &gt; **Record Producers**. This is a public record producer. You can modify this record producer or create your own. If you choose to create your own, see Section 3 in the [Making a record producer and catalog item public on a CMS page \[KB0551300\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsys_kb_id%3D8b93cb946fd20e0013568e4c2c3ee4c0%26sysparm_stack%3D%26sysparm_view%3D) article. You must also set the **glide.sc.use\_user\_criteria** property to **false**.

For more information, see [Record Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_RecordProducer.md).

## Anonymous chat routing

Information provided by the guest user assists with routing and also provides the context of the request to the consumer service agent. The chat request is routed to the appropriate agent queue based on the type of issue selected. The routing for anonymous chat requests uses [matching rules](c_CaseRouting.md). Create one matching rule for each queue and tie a chat request to a chat queue based on the selected issue type. Matching rules for anonymous chat are based on the Customer Interaction table.

The following matching rules are provided:

-   Anonymous Connect - Billing Support
-   Anonymous Connect - Order Support
-   Anonymous Connect - Product Support

These rules are based on the selections in the **Issue Type** field on the default anonymous chat record producer.

## Anonymous chat properties

There are two properties related to the anonymous chat feature. Set these properties to limit the number of chat requests created by guest users.

<table id="table_jzs_2kx_kt"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

connect.support.max\_guest\_sessions\_per\_hour

</td><td>

Limit maximum number of guest conversations created in the last hour.-   Type: integer
-   Default value: 200
-   Location: **Collaborate** &gt; **Connect Support** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.guest\_sessions\_rate\_limit\_reached\_message

</td><td>

Message shown to user when rate limit for guest conversations is breached. -   Type: string
-   Default value: Guest Chat is currently not available, please retry later.
-   Location: **Collaborate** &gt; **Connect Support** &gt; **Support Administration** &gt; **Properties**

</td></tr></tbody>
</table>**Related topics**  


[Record Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-catalog/c_RecordProducer.md)

[Connect Support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/connect/c_ConnectSupport.md)

[Routing and assigning customer service cases](c_CaseRouting.md)

