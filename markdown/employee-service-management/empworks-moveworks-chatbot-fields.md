---
title: Moveworks chat bot configuration fields
description: Field reference for the Moveworks web chat bot record and the internal setup record that Employee Slate for Moveworks uses.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-24"
reading_time_minutes: 1
keywords: [Moveworks chat bot fields, chat bot record, internal setup, trusted issuer]
breadcrumb: [Configure the Moveworks chat bot for Employee Slate, Employee Slate for Moveworks, Employee Slate setup flow, Employee Slate, Employee Service Management]
---

# Moveworks chat bot configuration fields

Field reference for the Moveworks web chat bot record and the internal setup record that Employee Slate for Moveworks uses.

## Chat bot record fields

|Field|Description|
|-----|-----------|
|Channel|Set to Moveworks web chat for the Employee Slate surface.|
|Selected connector|Set to Moveworks web chat.|
|Bot ID|Enter `1234`. The Moveworks Setup application replaces this placeholder with a randomized numerical value after you save the record.|
|Bot name|Unique identifier for the chat bot. The recommended pattern is `<org-name>-employee-slate-web-chat`.|
|Bot friendly name|Customer-facing display name for the assistant. The default placeholder is `Moveworks Assistant`.|
|Channel configuration|Set to Moveworks web chat bars. The system generates this value automatically when you save the record.|
|Surface|Set to **Unified Front Door**. This value is required so that Employee Slate renders the chat bot.|
|File attachment|Turn on this control so that employees can attach files in the Moveworks chat.|

## Internal setup fields

|Field|Description|
|-----|-----------|
|Chatbot|Selects the chatbot record that this internal setup applies to.|
|User Inbox|Turn on this control to activate the notifications experience for the chat bot.|
|Connector|Select the ServiceNow connector that replicates ServiceNow users into the Moveworks identity roster. The default label is **snow**.|
|Trusted issuer|Enter the ServiceNow instance URL. The trusted issuer lets Employee Slate and the Moveworks assistant authenticate seamlessly. Add multiple trusted issuers if you deploy the same chatbot across multiple ServiceNow instances.|
|Universal Assistance suggested prompts|Enter up to four suggested prompts on the Employee Slate home page. The Moveworks Setup application enforces a character limit on each prompt.|

**Related topics**  


[Configure the Moveworks chat bot for Employee Slate](../task/empworks-configure-moveworks-chatbot.md)

