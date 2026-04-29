---
title: Use Workplace Concierge with Now Assist in Virtual Agent
description: Invoke Workplace Concierge from Now Assist in Virtual Agent to invite visitors to your organization.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-22"
reading_time_minutes: 1
breadcrumb: [Workplace Concierge agentic workflow, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Use Workplace Concierge with Now Assist in Virtual Agent

Invoke Workplace Concierge from Now Assist in Virtual Agent to invite visitors to your organization.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user and now\_assist\_panel\_user

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  From the Employee Center portal home page, select the Now Assist in Virtual Agent chat interface.

3.  Enter an utterance or query to invite visitors.

    You can invite visitors using a single utterance or prompt. For example, enter `Invite Abel Tuter to Building A at 3pm on Wednesday`.

    While the LLM processes the utterance, animated dots in the chat window let employees know that the Workplace Concierge is working on the request. Based on the provided information, a synthesized response may appear. If any required information is missing, the Chat Visit Agent agent prompts you to enter the information.

    **Note:** The questions asked by the Chat Visit Agent agent are based on the initial requirements that are set by your admin.

    For example, if the visitor email is missing, the Chat Visit Agent agent prompts you to enter the email, then you can enter `abel.tuter@example.com`.

    After all the required information is provided, the visit information is displayed for confirmation.

    Each response includes feedback icons. You can indicate if the response was helpful by selecting thumbs up or select thumbs down if the response wasn't helpful.

4.  Verify the details of the visit, then select the confirm option to create the visit.

    After you confirm the details, Workplace Concierge creates a visit and invites the visitors using the email addresses. For more information about visitor registrations, see [Registering a visitor](../../workplace-visitor-mgmt/concept/registerring-a-visitor.md).


## What to do next

Visitors can reply to the invitation email to provide information for their pre-check tasks. The Email Visitor Intake agent processes email replies and updates the visitor records.

If Workplace Concierge is included in any emails that are sent to the visitors, the Email Visitor Intake agent scans the email threads for relevant data and updates the visitor records.

**Parent Topic:**[Workplace Concierge agentic workflow](../concept/workplace-concierge-ai-agent.md)

