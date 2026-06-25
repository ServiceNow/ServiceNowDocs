---
title: Getting started with Moveworks for Employee Center
description: Moveworks integration adds an AI assistant to Employee Center replacing the standard Virtual Agent with Moveworks conversational AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/moveworks-ec-getting-started.html
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Moveworks for Employee Center, Unified Employee Experience, Employee Service Management]
---

# Getting started with Moveworks for Employee Center

Moveworks integration adds an AI assistant to Employee Center replacing the standard Virtual Agent with Moveworks conversational AI.

A new plugin, Moveworks for Employee Center \(sn\_ex\_mw\_chat\_int\) assistant, lets your entire workforce ask questions, get instant answers, and complete tasks end-to-end.

Using the Moveworks chat assistant, you can access knowledge articles, requests, and tasks. Verify that you activate the EC applications before installing the Moveworks app from ServiceNow Store.

-   Employee Center \(sn\_ex\_sp\)
-   Employee Center Pro \(sn\_ex\_sp\_pro\)

You can complete the integration process in three steps:

-   Install the plugin from store \(`sn_ex_mw_chat_int`\).
-   Upload the Java KeyStore \(JKS\) certificate and create JWT provider.
-   Configure the bot ID and Embedded AI Assistant.

**Note:** You must have purchased Moveworks and implemented it for the self-signing to work.

## Understand Moveworks basics

Familiarity with the following Moveworks concepts helps with successful configuration:

-   User identity management: How Moveworks identifies and authenticates users.
-   Content ingestion: Process for indexing knowledge articles.
-   Group actions: Configuring bulk operations for common tasks.
-   Hand-off configuration: Setting up live agent escalation.
-   Multilingual support: Enabling conversations in multiple languages.

For more information, see [Moveworks documentation](https://help.moveworks.com/) and [Moveworks academy](https://academy.moveworks.com/learn).

## Useful tips and information

Before getting started, see the reference information available at [Moveworks for Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-ec-integration-reference.md), for settings, observations, and troubleshooting.

**Note:** Moveworks for Employee Center is available on both Employee Center and Employee Center Pro.

**Related topics**  


[Getting started with Moveworks for Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/moveworks-ec-getting-started.md)

[Install Moveworks for Employee Center app from store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-install-app.md)

[Upload Java KeyStore certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-upload-jks-cert.md)

[Configure bot ID and AI assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-setup-botid.md)

[Use Moveworks on employee portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-employee-chat-ui.md)

[Moveworks for Employee Center reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-experience-foundation/mw-ec-integration-reference.md)

