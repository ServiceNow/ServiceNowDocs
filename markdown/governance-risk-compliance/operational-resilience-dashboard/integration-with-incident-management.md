---
title: Reporting incidents from SOW and SIR Workspace in DRIR
description: When a high-impact, high-urgency incident is created or an existing incident is marked as high priority in the Service Operations Workspace \(SOW\) of Incident Management or Security Incident Response Workspace \(SIR Workspace\), it is classified as a major incident. These major incidents are then logged and reported in the Digital resilience incident reporting application.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Reporting incidents from SOW and SIR Workspace in DRIR

When a high-impact, high-urgency incident is created or an existing incident is marked as high priority in the Service Operations Workspace \(SOW\) of Incident Management or Security Incident Response Workspace \(SIR Workspace\), it is classified as a major incident. These major incidents are then logged and reported in the Digital resilience incident reporting application.

## Incident reporting workflow

The following example shows a sample workflow for reporting an incident in Incident Management. ![Incident workflow.](../image/dri-inci-repo-wf.png)

1.  Determine if the reported DRI case is a major ICT-related incident, a security breach, or an operational payment issue. Assess whether any critical services are impacted.
2.  If the critical services affected criterion is not met, the DRI case is not classified as major. If there is any report of malicious unauthorized access to the network and information systems, the incident is automatically classified as major.
3.  Create a DRI case record. The **Details** tab includes information such as the case number, source, state, subtype, priority, requester, and other relevant details. Review actions related to the case which are documented in the Activities panel on the **Details** tab.
4.  Notification: Send an email notification to the DORA analyst to update them on the progress of the case.
5.  Initial report: Automatically collect initial report data. Generate an initial report no later than 24 hours once the incident is classified as major.
6.  Response activation: Activate the response steps for the incident.
7.  Intermediate report: Review the incident report, if the incident has been open for more than three days. Update the incident data in the intermediate report, which is generated no later than 72 hours after the incident is classified as major.
8.  Response review: If the incident is still open, review the response steps.
9.  Final report: Verify if the incident is closed and enrich the notes in the record. Update the final report with the revised notes, which is generated one month after the incident is classified as major.

## Incident reporting timelines

To report an incident, the following timelines are considered.

|Report type|Timeline \(From the time the incident is classified as major\)|
|-----------|--------------------------------------------------------------|
|Initial report|24 hours|
|Intermediate report|72 hours|
|Final report|1 month|

## Case generation in Digital resilience incident reporting

When an incident is marked as critical in the Service Operations Workspace of the Incident Management application as shown in the example, a case is generated in Digital resilience incident reporting.

![Incident.](../image/inci-in-sow-ws.png)![Case.](../image/drir-inci-case-op-ws.png)

The SIR Workspace deploys a similar workflow for reporting high-impact incidents which are then logged in Digital resilience incident reporting.

