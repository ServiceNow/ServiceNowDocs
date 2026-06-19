---
title: Security Incident Response form changes after ticket ingestion
description: After a Secureworks CTP ticket has been ingested, a security incident is created and the corresponding updates are made to the security incident record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/secureworks-ctp-sir-changes.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response form changes after ticket ingestion

After a Secureworks CTP ticket has been ingested, a security incident is created and the corresponding updates are made to the security incident record.

## Worknotes

A worknote is posted with details of the ticket that triggered the security incident.

select the ticket link to navigate to the internal Secureworks Ticket to Task record. The **Click here** hyperlink takes you to the Secureworks CTP dashboard where you can view the ticket details.

If you had selected the **Log work note for new ticket** option in the Ticket Aggregation Criteria as described in the Create Profile: Mapping page, a worknote is posted when the ticket is aggregated.

## Aggregated tickets

Select **Related Lists** &gt; **Secureworks Aggregated Tickets** to view the ticket aggregated to the security incident. select the ticket hyperlink to view the ticket in the Secureworks CTP dashboard.

Create security incident: Select a ticket from the list, select the **Actions** menu and select **Create security incident**. This option creates a new security incident for the ticket and this ticket is de-aggregated from the parent security incident.

Delete ticket record: Select a ticket from the list, select the **Actions** menu and select **Delete**. This option deletes the ticket record.

## Secureworks Ticket updates

This shows the standard ticket fields and tracks changes to the tickets during every polling interval. This is helpful as you can view any ticket updates directly without navigating to the Secureworks CTP dashboard. Any changes to the values are displayed in the Previous Value and Current Value fields.

## Secureworks Recent Events

Select the **Fetch Recent Secureworks Events** option under the **Related Links** to view the most recent Secureworks events.

By default, a maximum number of 50 events will be displayed. You can modify this default setting in the Secureworks Integration Settings.

