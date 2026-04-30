---
title: Advanced Work Assignment for Supplier Lifecycle Operations
description: Use the Advanced Work Assignment for Supplier Lifecycle Operations feature to automatically assign work items to agents based on availability and capacity.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Advanced Work Assignment for Supplier Lifecycle Operations

Use the Advanced Work Assignment for Supplier Lifecycle Operations feature to automatically assign work items to agents based on availability and capacity.

Advanced Work Assignment for Supplier Lifecycle Operations pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. For more information, see [Exploring Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-overview&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Prerequisites for installing Advanced Work Assignment for Supplier Lifecycle Operations

Before you install Advanced Work Assignment for Supplier Lifecycle Operations, ensure that you activate the Agent Chat application and load the demo data during installation. For more information, see [Activate Agent Chat and load demo data](../task/load-demo-agent-chat.md).

## Required plugins

Install the Advanced Work Assignment for Supplier Lifecycle Operations \(com.snc.sn\_slm\_awa\) plugin if you have the admin role. Installing this plugin also installs the following dependent plugins:

-   Advanced Work Assignment \(com.glide.awa\)
-   Agent Chat \(com.glide.interaction.awa\)
-   Glide Virtual Agent \(com.glide.cs.chatbot\)
-   Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\)

-   **[Source-to-Pay Workspace agent inbox](agent-inbox-ws.md)**  
Use the agent inbox to manage your incoming work items, such as chats, cases, incidents, and more.
-   **[Activate Agent Chat and load demo data](../task/load-demo-agent-chat.md)**  
Activate Agent Chat and load demo data.
-   **[Setting up Advanced Work Assignment for Supplier Lifecycle Operations](awa-slm-config.md)**  
Plan and configure your implementation of Advanced Work Assignment for Supplier Lifecycle Operations.
-   **[Using Advanced Work Assignment for Supplier Lifecycle Operations](use-awa-slm.md)**  
Enables supplier contacts to interact with supplier owners and resolve their issues and get answers to questions.

**Parent Topic:**[Configuring Supplier Lifecycle Operations](config-supp-mgmt.md)

**Related topics**  


[Install Supplier Lifecycle Operations](../task/install-supp-mgmt.md)

[Install Supplier Collaboration Portal](../task/install-supp-central.md)

[Supplier Document Management](supp-doc-mgmt-overview.md)

[Configure the document template for the Sign document action type for supplier task](../task/configure-pdf-template-sign-doc-task.md)

[Enable M2M mapping between supplier contact and suppliers](../task/enable-m2m-supplier-contacts.md)

[Configure Supplier Relationship and Performance Management](configuring-supplier-performance-mgmt.md)

