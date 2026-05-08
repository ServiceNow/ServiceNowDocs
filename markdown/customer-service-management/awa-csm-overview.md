---
title: AWA for CSM
description: Use the ServiceNow Advanced Work Assignment \(AWA\) for Customer Service Management feature to automatically assign work items to agents based on their availability, capacity, and skills. AWA for CSM pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Case routing and assignment, Organize agent workspaces, Configure, Customer Service Management]
---

# AWA for CSM

Use the ServiceNow® Advanced Work Assignment \(AWA\) for Customer Service Management feature to automatically assign work items to agents based on their availability, capacity, and skills. AWA for CSM pushes work to qualified agents using work item queues, routing conditions, and assignment criteria that you define. Agents see their assignments in their Agent Workspace inbox.

## Plugins

The Advanced Work Assignment for CSM feature is available with the Customer Service plugin \(com.sn\_customerservice\).

To use the shift-based assignment feature for customer service cases, you must enable the Workforce Optimization for Customer Service plugin \(com.snc.wfo.csm\) in addition to the Advanced Work Assignment plugin \(com.glide.awa\). For more information, see [Activate Workforce Optimization for Customer Service](../../workforce-optimization-for-customer-service-configurable/task/request-configurable-wfo-cs.md).

To use the chat feature with Advanced Work Assignment for CSM, you must also activate the Agent Chat plugin \(com.glide.interaction.awa\).

For more information, see Activate related plugins for Advanced Work Assignment.

## Inbox layouts

Three chat inbox layouts are included with the Chat service channel.

|Chat Layout|Included Fields|
|-----------|---------------|
|Default Chat Layout|Short description|
|Contact Chat Layout|Short description, Contact, Account|
|Consumer Chat Layout|Short description, Consumer|

Two case inbox layouts are included with the Case service channel.

|Case Layout|Included Fields|
|-----------|---------------|
|Default Case Layout|Short description, Contact, Account, Priority, Category|
|Consumer Case Layout|Short description, Consumer, Priority, Category|

## Variable work item sizing

Organizations may like to size cases based on the complexity of the case, time and effort required to complete work. This helps in estimating agent utilization accurately. Advance work assignment currently treats every case as one unit of work. However, sometimes, certain cases may require more work than others. These cases may account for a greater share of an agent’s capacity. Work item sizing allows to size the case differently based on the case attributes. For more information, see Service channel capacity and utilization.

## Agent affinity

Agent Affinity is an Advanced Work Assignment enhancement that enables you to streamline the routing of work items. Advanced Work Assignment automatically assigns work items based on historical, task-based, or account team affinity. For more information about agent affinity, see Using Agent Affinity.

**Related topics**  


[bundle-convint.awa-overview]

