---
title: View information in a security incident
description: You can perform several other actions on an existing security incident using the related links.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 3
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View information in a security incident

You can perform several other actions on an existing security incident using the related links.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident you want to update.

2.  Within **Related Links**, you can perform the following tasks,

<table id="choicetable_k4s_q45_c5"><tbody><tr><td id="d214069e60">

**[View Manual Runbook](../reference/setup-assistant-reference.md#)**

</td><td>

View a list of runbooks available for this security incident.

</td></tr><tr><td id="d214069e76">

**Response Workflow**

</td><td>

View any workflow associated with this incident.

</td></tr><tr><td id="d214069e85">

**[Add Multiple Observables](add-multiple-si-observables.md)**

</td><td>

Adds a list of observables in comma, new line, tab, or pipe delimited formats.

</td></tr><tr><td id="d214069e101">

**[Add to Security Case](../../threat-intelligence-case-management/concept/case-mgmt.md)**

</td><td>

Adds the security incident to one or more security cases. You can also create a new security case and add this security incident to it.

</td></tr><tr><td id="d214069e119">

**Get QRadar IP Summaries**

</td><td>

If a QRadar integration is available, and contains valid CIs, source, and destination IP addresses, it triggers the QRadar workflows and displays the results in work notes.

</td></tr><tr><td id="d214069e129">

**Run Orchestration**

</td><td>

Choose and run a Security Operations workflow.

</td></tr><tr><td id="d214069e138">

**[View SLA timeline](https://www.servicenow.com/docs/access?context=t_ViewSLATimeline&version=australia&pubname=australia-it-service-management&ft:locale=en-US)**

</td><td>

You can view an SLA timeline from a Task SLA record or from an SLA definition.

</td></tr><tr><td id="d214069e152">

**Show All Related Lists**

</td><td>

Displays all standard related lists and any lists added manually. **Note:** Manually added items are available only in this view.

</td></tr><tr><td id="d214069e164">

**[Show Affected Items](show-affected-items-for-si.md)**

</td><td>

Displays the lists of CIs, users, and services directly affected by this incident

</td></tr><tr><td id="d214069e180">

**[Show Related Items](show-related-items-for-si.md)**

</td><td>

Displays the lists of related incidents, CIs, users, and groups affected by this incident.

</td></tr><tr><td id="d214069e196">

**[Show IoC](show-ioc-info-for-si.md)**

</td><td>

Displays the lists of observables, indicators, malware, modes and methods, and security scan requests associated with this incident.

</td></tr><tr><td id="d214069e213">

**[Show Enrichment Data](show-enrich-data-for-si.md)**

</td><td>

Displays the lists of enrichment data, processes, services, statistics, lookups, firewall logs, and compromised user information associated with this incident.

</td></tr><tr><td id="d214069e229">

**[Show Response Tasks](show-response-tasks-for-si.md)**

</td><td>

Displays the lists of tasks, SLAs, risk score audits, outages, and Exchange searches associated with this incident.

</td></tr><tr><td id="d214069e245">

**View Details in External System**

</td><td>

If this security incident was generated from an external application, directly or by events, and a link to the originating data was provided, the **View Details in External System** action opens the URL. You can view and search through the logs that generated this incident.

</td></tr><tr><td id="d214069e260">

**[Scan for Vulnerabilities](t_SubmitThrtReqFromSecInc.md)**

</td><td>

If Vulnerability Response is activated, and you have selected at least one affected CI for the security incident, you can submit a scan request to determine what vulnerabilities exist on the CI.

</td></tr></tbody>
</table>
