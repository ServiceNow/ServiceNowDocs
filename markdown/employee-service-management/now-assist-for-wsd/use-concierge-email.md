---
title: Use Workplace Concierge with email or calendar invite
description: Add the Workplace Concierge to an email thread or a calendar invite.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-22"
reading_time_minutes: 1
breadcrumb: [Workplace Concierge agentic workflow, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Use Workplace Concierge with email or calendar invite

Add the Workplace Concierge to an email thread or a calendar invite.

## Before you begin

Role required: sn\_wsd\_core.workplace\_user

## Procedure

1.  Open the email thread or calendar invite that you want to create a visit from.

2.  Add `Workplace Concierge` to the email thread or the calendar invite.

    The email address for Workplace Concierge is configured by your admin.

<table id="choicetable_lpt_w3n_r3c"><thead><tr><th align="left" id="d399779e75">

Choice

</th><th align="left" id="d399779e78">

Description

</th></tr></thead><tbody><tr><td id="d399779e84">

**Calendar invite**

</td><td>

Add Workplace Concierge as a guest to the calendar invite.Workplace Concierge extracts the meeting date and time, host identity, location, and attendee email addresses.

</td></tr><tr><td id="d399779e100">

**Email thread**

</td><td>

Add Workplace Concierge in the **CC** field of the email thread. Alternatively, forward the email thread to the Workplace Concierge.Workplace Concierge scans the email thread for words or phrases that indicate an in-person visit or meeting.

Workplace Concierge then scans for the date and time, location, visitor type, attendee email addresses, and other mandatory requirements set by the admin.

</td></tr></tbody>
</table>    If any required information is missing, Workplace Concierge sends an email to request clarification.

3.  Reply to the Workplace Concierge email clarifying the information.

    For example, if an email thread contains two locations, or if the location is not found in the Workplace Service Delivery location hierarchy, reply with the exact location name.

    After receiving all the information, Workplace Concierge sends an email with the visit details for confirmation.

4.  Verify the details of the visit, then reply with a confirmation.

    After you confirm the details, Workplace Concierge creates a visit and invites the visitors using the email addresses. For more information about visitor registrations, see [Registering a visitor](../../workplace-visitor-mgmt/concept/registerring-a-visitor.md).


## What to do next

Visitors can reply to the invitation email to provide information for their pre-check tasks. The Email Visitor Intake agent processes email replies and updates the visitor records.

If Workplace Concierge is included in any emails that are sent to the visitors, the Email Visitor Intake agent scans the email threads for relevant data and updates the visitor records.

**Parent Topic:**[Workplace Concierge agentic workflow](../concept/workplace-concierge-ai-agent.md)

