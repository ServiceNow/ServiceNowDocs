---
title: Reporting incidents from SOW and SIR Workspace in DRIR
description: High-impact, high-urgency incidents created in Service Operations Workspace \(SOW\) or Security Incident Response Workspace \(SIR Workspace\) are classified as major incidents. These major incidents are logged and reported in the Digital resilience incident reporting application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/integration-with-incident-management.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Reporting incidents from SOW and SIR Workspace in DRIR

High-impact, high-urgency incidents created in Service Operations Workspace \(SOW\) or Security Incident Response Workspace \(SIR Workspace\) are classified as major incidents. These major incidents are logged and reported in the Digital resilience incident reporting application.

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

## Tracking field-level changes on linked source records

Starting with Digital resilience incident reporting \(DRIR\), version 23.0.4, you can maintain DRIR cases current with evolving incident data by tracking field-level changes in linked source records.

The DRIR application detects modifications to incidents after case creation. It generates audit-trail records with full information \(field name, old and new values, changed\_by, changed\_at\). A banner displays in the case workspace prompting you to review the latest changes.

The banner shows the total number of pending updates, the timestamp of the last generated report, and the timestamp of the most recent source-record change. Select **Review updates** to open the Updates tab of the action task with the most pending updates \(or the case-level Updates view, if all pending updates are case-level\). Select **Dismiss** to hide the banner for your current session; the underlying pending updates remain, and the banner reappears the next time you open the case.

If the oldest pending update is more than 30 days old, the banner switches to a warning visual style and adds an "oldest update is N days old" sub-line to call out the stale data.

No banner is displayed when the case has no pending updates, or when the case is in a terminal state \(Closed or Cancelled\). Applying updates against a closed case is blocked at the point you try to apply them.

\[Omitted image "incident-form.png"\] Alt text: Incident record showing example field changes in the activity log: state, impact, and urgency.

For example, if the state, impact, or urgency changes on the linked incident, a banner appears in the DRIR case the next time you open it.

\[Omitted image "incident-form-with-notification.png"\] Alt text: DRIR case displaying the banner: "The linked source record has been updated. Please review the latest changes."

This keeps the case current with the incident without requiring manual re-checks, which supports meeting the initial \(24-hour\), intermediate \(72-hour\), and final \(1-month\) regulatory reporting timelines.

A "DRI Source Record Change - Email Notification" is also sent to the case's watch list and analyst whenever a tracked field changes on the linked source record. The email lists the case number, the source record, who made the change and when, and the old and new value for each changed field. It also includes a link back to the case. For the full notification entry, see [Email notifications in Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/email-notifications-in-opres.md).

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

The Regulatory reporting status of a DRI case \(Potentially reportable/Reportable/Not reportable\) is displayed in the Details panel of the Digital Resilience Incident Reporting case record. The status also appears per regulation in the Regulation Mappings related list. The dedicated 'Reporting status' form section that existed in earlier releases has been removed; the same information is now in the Details panel.

