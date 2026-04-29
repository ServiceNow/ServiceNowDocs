---
title: Setting up automatic capture of emails in CRM using redirect rules
description: Automate the process of capturing sales-related emails by configuring redirecting rules in your Microsoft Outlook so emails can be logged in the CRM without manual associations from the Microsoft Outlook add-in by the agent.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activity Management, Lead and opportunity management apps, Configure, Sales and Order Management]
---

# Setting up automatic capture of emails in CRM using redirect rules

Automate the process of capturing sales-related emails by configuring redirecting rules in your Microsoft Outlook so emails can be logged in the CRM without manual associations from the Microsoft Outlook add-in by the agent.

## Overview of capturing emails with redirecting rules

Sales representatives often receive important customer communications directly in their personal inbox. Manually associating each email with CRM records can be time‑consuming and can lead to missed or incomplete logging. ServiceNow AI Platform enables you to use standard email client redirect rules to capture CRM-relevant emails from an agent's personal mailbox by automatically routing selected emails from the agent's inbox to a shared forwarding mailbox. Internal mailboxes are monitored through a user mailbox integration framework.

## Benefits

-   Reduces manual effort required to associate emails with CRM entities.
-   Improves the consistency and completeness of CRM activity tracking.
-   Enables agents to continue working primarily from their Microsoft Outlook client.
-   Complements the Microsoft Outlook add-in by handling routine email capture automatically.
-   Improves the ability to process emails and identify customer or prospect senders correctly compared to forwarding rules. The original sender's email address is preserved in the From field, unlike forwarding rules, which change the From field to the forwarding mailbox.

## Comparison of email capture methods

Although the Microsoft Outlook remains the primary tool for precise record association and advanced actions, redirect rules improve baseline email capture. The following table provides a comparison of these approaches.

|Aspect|Manual \(Microsoft Outlook add-in\)|Automatic \(Redirect rules\)|
|------|-----------------------------------|----------------------------|
|How it works|Agent selects **Associate** in the Microsoft Outlook add-in|Rules redirect emails automatically|
|Best for|Selective, high-value emails|High-volume bulk capture|
|Effort|Per-email action|One-time rule setup|
|Control|Agent decides what to log|Rules decide what to log based on predefined criteria|

## Key capabilities

Standard Microsoft Outlook client redirect rules provide the following capabilities:

-   Redirect emails from a personal mailbox to ServiceNow CRM
-   Preserve original sender, recipients, and message headers
-   Centralize inbound email ingestion through a shared mailbox.
-   Process redirected emails using an inbound email pipeline
-   Make redirected emails available for CRM association in the Staged Email \[sys\_email\_staging\] table

## How redirecting emails work

The workflow for how redirected emails move from a personal mailbox into ServiceNow CRM is as follows:

1.  An agent receives an email in their personal mailbox.
2.  Microsoft Outlook evaluates configured redirect rules.
3.  Matching emails are redirected to a shared forwarding mailbox.
4.  ServiceNow retrieves emails from the shared mailbox using Post Office Protocol version 3 \(POP3\) or Internet Message Access Protocol \(IMAP\).
5.  Emails are processed and staged in the Staged Email \[sys\_email\_staging\] table for CRM association.

## Limitations

Redirect rules are configured in the Microsoft Outlook email client and the following limitations are due to how redirect rules work:

-   Redirect rules can’t query data on your ServiceNow instance such as leads, accounts, or opportunities.
-   Microsoft Outlook redirect rules can’t evaluate CRM ownership or relationships.
-   Advanced logic such as domain-to-account matching isn’t supported.

## Sample redirect rule scenarios

Common redirection rules might include:

-   Recipient-based: Redirect emails where the To or CC field contains the CRM forwarding address.
-   Keyword-based: Redirect external emails where the subject or body contains sales-related keywords such as quote, pricing, RFI \(request for information\), demo, product, trial, lead, opportunity, evaluate, interest, deal, or proposal.
-   Domain-based: Redirect business emails while excluding personal email domains such as gmail.com or yahoo.com.

For information about how to set up redirect rules for Microsoft Outlook, refer to the official product documentation on forwarding rules.

