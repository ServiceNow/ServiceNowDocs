---
title: Ingesting the sample Secureworks tickets
description: Select the sample tickets that are to be ingested.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mapping of ticket fields for the SecureWorks CTP integration, Create a profile, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Ingesting the sample Secureworks tickets

Select the sample tickets that are to be ingested.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  You can either pull the five most recent sample tickets or provide the unique ticket IDs for the specific tickets that you want to use for your mapping experience.

    From the **Ingestion Preference** choice list, select one of the following:

    -   Retrieve most recent tickets: The 5 most recent tickets are retrieved.
    -   Select tickets based on ticket ID: Specify the ticket ID for the ticket to be retrieved. You can specify a maximum of 5 ticket ids separated by commas.
3.  Click **Fetch Sample Data** to pull the latest sample ticket data from the Secureworks CTP server.

    The pull for sample tickets may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen. The retrieved tickets are displayed as individual tabs. Click on a tab to view the ticket data. For each ticket, you can see the ticket fields and their values, and details of the contributing event that triggered the ticket.

    **Note:** You will see details of contributing events only if they have occurred in the last 7 days. Events older than 7 days are not displayed.


## What to do next

After you have fetched the sample data, the next step is map the ticket fields to the security incident.

