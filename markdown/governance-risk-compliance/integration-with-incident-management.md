---
title: Reporting incidents from SOW and SIR Workspace in DRIR
description: When a high-impact, high-urgency incident is created or an existing incident is marked as high priority in the Service Operations Workspace \(SOW\) of Incident Management or Security Incident Response Workspace \(SIR Workspace\), it is classified as a major incident. These major incidents are then logged and reported in the Digital resilience incident reporting application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/integration-with-incident-management.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Reporting incidents from SOW and SIR Workspace in DRIR

When a high-impact, high-urgency incident is created or an existing incident is marked as high priority in the Service Operations Workspace \(SOW\) of Incident Management or Security Incident Response Workspace \(SIR Workspace\), it is classified as a major incident. These major incidents are then logged and reported in the Digital resilience incident reporting application.

## Incident reporting workflow

The following example shows a sample workflow for reporting an incident in Incident Management. \[Omitted image "dri-inci-repo-wf.png"\] Alt text: Incident workflow.

1.  Incident verification: Determine if the reported incident is a major ICT-related incident, a security breach, or an operational payment issue. Assess whether any critical services are impacted.
2.  Incident classification: If the critical services affected criterion is not met, the incident is not classified as major. If there is any report of malicious unauthorized access to the network and information systems, the incident is automatically classified as major.
3.  Incident record creation: Create an incident record. The **Details** tab includes information such as the case number, source, state, subtype, priority, requester, and other relevant details. Review actions related to the case which are documented in the Activities panel on the **Details** tab.
4.  Notification: Send an email notification to the DORA analyst to update them on the progress of the case.
5.  Initial report: Automatically collect initial report data. Generate an initial report no later than 24 hours once the incident is classified as major.
6.  Response activation: Activate the response steps for the incident.
7.  Intermediate report: Review the incident report, if the incident has been open for more than three days. Update the incident data in the intermediate report, which is generated no later than 72 hours after the incident is classified as major.
8.  Response review: If the incident is still open, review the response steps.
9.  Final report: Verify if the incident is closed and enrich the notes in the record. Update the final report with the revised notes, which is generated one month after the incident is classified as major.

## Incident reporting timelines

To report an incident, the following timelines are considered.

<table id="table_t3p_w5k_sdc"><thead><tr><th>

Report type

</th><th>

Timeline \(From the time the incident is classified as major\)

</th></tr></thead><tbody><tr><td>

Initial report

</td><td>

24 hours

</td></tr><tr><td>

Intermediate report

</td><td>

72 hours

 **Note:** The intermediate report is cyclical. A new intermediate assessment is generated every 72 hours \(3 days\) from the time the incident is classified as major until the source incident is closed or the termination conditions configured on the DRI Intermediate report template are met.

</td></tr><tr><td>

Final report

</td><td>

1 month

</td></tr></tbody>
</table>## Case generation in Digital resilience incident reporting

When an incident is marked as critical in the Service Operations Workspace of the Incident Management application as shown in the example, a case is generated in Digital resilience incident reporting.

\[Omitted image "inci-in-sow-ws.png"\] Alt text: Incident.\[Omitted image "drir-inci-case-op-ws.png"\] Alt text: Case.

The SIR Workspace deploys a similar workflow for reporting high-impact incidents which are then logged in Digital resilience incident reporting.

## Where to find the case status

The Regulatory reporting status of a DRI case \(Potentially reportable/Reportable/Not reportable\) is displayed in the Details panel of the Digital Resilience Incident Reporting case record in the Operational Resilience Workspace, and per regulation in the Regulation Mappings related list. The dedicated 'Reporting status' form section that existed in earlier releases has been removed; the same information is now in the Details panel.

