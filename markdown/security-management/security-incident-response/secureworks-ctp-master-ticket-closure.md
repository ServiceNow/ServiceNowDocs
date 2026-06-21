---
title: Secureworks CTP Master Ticket Closure Notice
description: Before you close a security incident created by a Secureworks CTP master ticket, you must verify that all child tickets associated with the master ticket are closed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/security-incident-response/secureworks-ctp-master-ticket-closure.html
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View the Secureworks tickets and the corresponding security incidents, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Secureworks CTP Master Ticket Closure Notice

Before you close a security incident created by a Secureworks CTP master ticket, you must verify that all child tickets associated with the master ticket are closed.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Secureworks Ticket Ingestion** &gt; **Secureworks Ticket to Task**.

    The Secureworks CTP tickets with their corresponding security incidents are displayed.

    \[Omitted image "secureworks-ticket-to-task.gif"\] Alt text: Secureworks: Ticket to Tasks

2.  Click on the security incident with the **isGlobalParent** field set to **true.**

3.  Change the security incident State to **Closed**, specify the close codes and click **Save**.

    The following dialog box is displayed.

    \[Omitted image "secureworks-sir-master-ticket.gif"\] Alt text: Secureworks CTP: Master Ticket Closure

    This security incident is associated with a Secureworks Master Ticket. A Master Ticket may have one or more child tickets associated with it. Before the Master Ticket can be closed, you must first verify if all the child tickets associated with this Master Ticket are closed.

4.  Add a note requesting closure of the Master Ticket in Secureworks and click **Submit Request**.

    The Master Ticket is now reassigned to the Secureworks SOC team.

5.  Once the request has been submitted, you can close the security incident.

6.  Navigate to **Application** &gt; **Module**.


