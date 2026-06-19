---
title: Update personal records with the AI assistant
description: Update personal records such as home address and emergency contact in one conversation with the AI assistant. You don't log in to a separate HR system or file a ticket.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/empworks-update-hr-records.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-04-24"
reading_time_minutes: 1
keywords: [update HR records, change address, emergency contact, SAP SuccessFactors]
breadcrumb: [Working with Moveworks capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Update personal records with the AI assistant

Update personal records such as home address and emergency contact in one conversation with the AI assistant. You don't log in to a separate HR system or file a ticket.

## Before you begin

Before you start, verify the following:

-   Verify that the admin configures the Agent Studio plugin.
-   Your organization has connected the HR system of record, such as SAP SuccessFactors, to the Moveworks AI assistant.

Role required: Employee

## About this task

The AI assistant uses the reasoning engine to identify the records that must change. It collects the inputs in the conversation and confirms before it updates the system of record. For background, see [AI assistant reasoning engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/empworks-moveworks-capabilities.md).

## Procedure

1.  On the home page, select the chat bar.

2.  Enter a natural-language request that describes the records to update, for example, `Update my address and add an emergency contact`.

3.  Provide the details that the assistant asks for in the chat conversation.

    The assistant collects the new address and the emergency contact information directly in the chat. You don't have to navigate, fine, or open a separate form.

4.  Review the summary of the intended changes.

    The assistant lists the exact updates before any record changes. You review, edit, or cancel the updates at this step.

5.  Select **Confirm**.

    The assistant commits the updates to the connected system of record. Both the address and the emergency contact update at the same time.

6.  Review any related content that the assistant surfaces after the update.

    The assistant proactively surfaces related knowledge. For example, it shows the employee handbook and payroll FAQs after an address change that crosses a state line.


## Result

The personal records update in the connected HR system of record. The assistant confirms the outcome in the conversation and surfaces related knowledge that is relevant to the change.

