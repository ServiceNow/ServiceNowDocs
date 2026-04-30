---
title: Agent Chat reference
description: Reference topics provide descriptions about Agent Chat.Domain separation is supported in the Agent Chat application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.Create a report that tracks the number of help requests.The Interaction related record \[interaction\_related\_record\] table tracks tasks and Knowledge Base \(KB\) articles that are created, updated, or viewed in the context of a particular interaction. The Interaction related record table references the interaction, related document, whether the relationship is to a task or KB article, and what type of operation on the related document formed the basis for the relationship.
locale: en-US
release: xanadu
product: Agent Chat
classification: agent-chat
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Agent Chat, Conversational Interfaces]
---

# Agent Chat reference

Reference topics provide descriptions about Agent Chat.

## Domain separation and Agent Chat

Domain separation is supported in the Agent Chat application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

### Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

### Requirements

All domain support features require the Domain Support - Domain Extensions Installer \[com.glide.domain.msp\_extensions.installer\] plugin. For details, see [Request domain separation](https://www.servicenow.com/docs/access?context=t_ActivateDomainSeparation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

### Configuring Agent Chat with domain separation

Domain separation allows organizations to segment their data and processes based on specific criteria such as business unit, geography, or other factors.

A service provider \(SP\) has one chat setting \(Agent Chat\) record in the global domain when the instance is provisioned.

The admin of a subdomain can specify Agent Chat settings for that subdomain, such as work queues and assignment groups. For details, see [Setting up Agent Chat](../task/ac-configure-agent-chat.md).

When a user logs into a subdomain, a seeded Agent Chat settings record is created.

When using domain separation in Agent Chat, keep the following points in mind:

-   Domain Separation applies to both the agent side and the customer side of the chat. This means that agents will only be able to access chat records and data that are in their domain, and customers will only be able to see chat records that are associated with their domain.
-   Agent Chat records are automatically tagged with the domain of the agent who handled the chat. This ensures that the chat record is associated with the correct domain, and that agents can only view chat records that are associated with their domain.
-   When an agent is assigned to a chat, the chat is automatically assigned to the domain of the agent. This ensures that the chat record is associated with the correct domain from the start.
-   If an agent needs to transfer a chat to another agent or escalate the chat to a higher level of support, the chat is transferred to an agent who is in the same domain as the original agent. This ensures that the chat record stays within the correct domain.

## Building a report to track the number of help requests

Create a report that tracks the number of help requests.

### Before you begin

Role required: admin

### Procedure

1.  Activate the Interaction Events business rule.

    1.  Navigate to **Interaction** &gt; **All**.

    2.  Right-click the **Number** heading.

    3.  Click **Configure** &gt; **Business Rules**.

    4.  On the Business Rules screen under the **Name** column, click **Interaction Events**.

    5.  On the Business Rules - Interaction Events screen, select the **Active** check box if it is not already selected.

    6.  Click **Update**.

2.  Create a new metric definition for Interaction "help requested" on the Metric Definition - New record screen by entering `Interaction` in the **Table** field and selecting **Help Requested** from the **Field** list.

    For detailed steps on creating metric definitions, see [Define a metric](https://www.servicenow.com/docs/access?context=create-metric&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

3.  Create a new chat as a requester.

4.  Accept the same chat as an agent.

5.  While still logged in as that agent, enter the quick action `/help`.

6.  Navigate to **Metrics** &gt; **Instances** and record the ID of the single instance record created for help\_requested=true.

7.  Navigate to the Admin window and open the interaction from the previous step.

8.  Join the conversation \(either privately or publicly\).

9.  Navigate to **Metrics** &gt; **Instances** and observe that one instance record was created for help\_requested=true.

    For more information about using the Metric Instance Table, see [Metric instance](https://www.servicenow.com/docs/access?context=c_MetricInstance&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).


## Agent Chat Interaction related records

The Interaction related record \[interaction\_related\_record\] table tracks tasks and Knowledge Base \(KB\) articles that are created, updated, or viewed in the context of a particular interaction. The Interaction related record table references the interaction, related document, whether the relationship is to a task or KB article, and what type of operation on the related document formed the basis for the relationship.

### Interaction related record table overview

The Interaction related record table tracks task and KB article records that were created, updated, or viewed in a particular interaction. The Interaction related record table records

-   the interaction
-   the related document
-   whether the relationship is to a KB article or a task
-   what type of operation on the related document formed the basis of the relationship

### Creating Interaction related records

Interaction related records can be created manually or automatically.

-   Manually - records are manually created via an Interaction related record form. The form is opened on a workspace through an Associated record UI action. When this form is used to create the relationship, the operation field is not set to any value.
-   Automatically created via business rules
-   Automatically created via client calls from a workspace

### Configuring automatic creation of interaction related records

You can update or create entries in the Interaction relationship policy \[interaction\_relationship\_policy\] table to manage which types of operations result in the auto-creation of interaction related records. These determine whether interaction related records may be created for each of the following actions:

-   Insert - record created from workspace in the context of the interaction.
-   Update - record updated from workspace in the context of the interaction.
-   Mention - record number mentioned in a chat, resulting in the rendering of a record card.
-   Open - record opened in workspace in the context of the interaction.
-   Unknown - interaction related record created by automated logic other than via agent actions from workspace.

Two policies that are included with the base system govern behavior for relationships to the task and kb\_knowledge table. To override behavior for a particular task type, you can add an additional entry for the appropriate Document table.![Interaction relationship policies screenshot](../image/interaction_relationship_policies.png)

The com.glide.interaction.autocreate\_relationships property is set to true by default. If it is set to false, only relationships created via the interaction\_related\_record form are created. All others are blocked by the "Block relationship autocreation" business rule.

