---
title: Security Operations Integration - Email Search and Delete flow
description: The Security Operations Integration - Email Search and Delete flow returns the number of threat emails from an email server search and, optionally, return details for each email found. After the email search is completed, you can delete the emails.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration- Email Search and Delete capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - Email Search and Delete flow

The Security Operations Integration - Email Search and Delete flow returns the number of threat emails from an email server search and, optionally, return details for each email found. After the email search is completed, you can delete the emails.

## Before you begin

Role required: sn\_si.analyst

## About this task

The search query can take some time to complete. After the count is received, approval is required to delete emails from an email server.

This flow is triggered by the **Delete from Email Server\(s\)** and **Search on Email Server\(s\)** buttons on the **Email Search** form in a security incident. For more information, see [Search for and delete phishing emails](../../security-incident-response/task/search-delete-exchange-emails.md).

![Security Operations integration - Email Search and Delete flow](../image/email-search-and-delete-flow.png "Email Search and Delete")

Activities specific to this flow are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration Flow Actions](../concept/common-wf-activities.md).

The flow process activities include:

-   **[Execution Tracking Begin \(Mail Search\) activity](../../security-operations-integrations/reference/execution-tracking-begins-mail-search-activity.md)**  
The Execution Tracking - Begin \(Mail Search\) capability execution activity creates an execution tracking record and marks the record state as Started. This activity is used by all capability and implementation workflows to keep track of their state.

**Parent Topic:**[Security Operations Integration- Email Search and Delete capability](../concept/email-search-capability.md)

