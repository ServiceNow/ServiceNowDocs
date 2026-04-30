---
title: Legal Virtual Agent Conversations
description: The ServiceNow Legal Virtual Agent Conversations application provides predefined conversation topics to enable automated chats with employees seeking legal services. You can build new topics or customize predefined topics to handle common legal requests from employees or guide them through self-service tasks.
locale: en-US
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Legal Virtual Agent Conversations

The ServiceNow® Legal Virtual Agent Conversations application provides predefined conversation topics to enable automated chats with employees seeking legal services. You can build new topics or customize predefined topics to handle common legal requests from employees or guide them through self-service tasks.

**Important:** Starting with the Australia release, Legal Virtual Agent Conversations is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. There is no replacement for this plugin.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Features

-   Automates handling of repetitive requests
-   Reduces the response time for your employee queries
-   Integrates with legal services to create requests on behalf of employees
-   Provides live agent chat support

## Predefined conversation topics for Legal Service Delivery

The Legal Virtual Agent Conversations application installs the following virtual agent conversation topics \(chatbot conversations\) to help employees with common self-service tasks in Legal Service Delivery. These conversation topics are grouped under the Legal Service Delivery category.

-   **Check Legal Request and Matter status**

    Displays the status of legal requests and matters submitted by employees for themselves or on behalf of another employee.

-   **General Legal Request**

    Helps employees create a general legal request. Based on the entered short description, it also provides links to relevant Legal knowledge base articles to resolve issues.

-   **Privacy Assessment**

    Helps employees create a legal request to review whether projects comply with an organization’s applicable privacy regulations and accepted privacy policy. The Legal department reviews such requests for potential risks and might recommend a mitigation plan if necessary.

-   **Stock Trading**

    Helps employees to know about the stock trading window of your organization and with stock pre-clearance requests.

    This virtual agent conversation topic is available only if you've installed the Legal Stock Preclearance application.

-   **Legal Knowledge Base**

    Finds and displays Legal knowledge base articles based on the entered search string.


**Note:** If [Universal Request for legal services is enabled](universal-requests-legal.md), the system creates a universal request and an associated legal request when an employee submits a legal request through virtual agent. General Legal Request, Privacy Assessment, and Stock Trading request types are supported.

-   **[Install Legal Virtual Agent Conversations](../task/install-legal-va-conv.md)**  
You can install the Legal Virtual Agent Conversations application \(sn\_lg\_va\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Configure Virtual Agent conversation topics for legal services](../task/configure-legal-va.md)**  
Create or modify Virtual Agent conversation topics for legal services.
-   **[Live agent support for legal services](legal-va-live-agent.md)**  
Employees can contact a live agent from the Legal department \(a paralegal staff or lawyer\) via the Virtual Agent chat window to seek legal help.
-   **[Start a chat session through Legal Counsel Center Inbox](../task/chat-employee-counsel-center.md)**  
Accept an incoming chat request through Legal Counsel Center Inbox to start a chat session with the requester.

**Parent Topic:**[Legal Service Delivery](legal-management-overview.md)

