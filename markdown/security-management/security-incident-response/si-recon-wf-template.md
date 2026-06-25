---
title: Security Incident Reconnaissance workflow template
description: Reconnaissance is usually a preliminary step toward a further attack seeking to exploit a device or system. The Security Incident - Reconnaissance - Template allows you to perform a series of tasks designed to handle reconnaissance on your network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/si-recon-wf-template.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Reconnaissance workflow template

Reconnaissance is usually a preliminary step toward a further attack seeking to exploit a device or system. The Security Incident - Reconnaissance - Template allows you to perform a series of tasks designed to handle reconnaissance on your network.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Reconnaissance activity**. This action causes a response task to be created for the first activity in the workflow.

\[Omitted image "reconnaissance-workflow.png"\] Alt text: Reconnaissance workflow template

## Procedure

1.  Open the security incident for this potential attack, or [create a new security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Reconnaissance activity**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_atp_55s_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Reconnaissance activity verified?

</td><td>

Determine whether any observed reconnaissance has been verified.In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Identify impacted systems** task is executed. If you select **No**, the flow ends.

</td></tr><tr><td>

Identify impacted systems

</td><td>

Determine the systems impacted by the reconnaissance.

</td><td>

When this task is complete, the **Allow reconnaissance for law enforcement analysis?** task is executed.

</td></tr><tr><td>

Allow reconnaissance for law enforcement analysis?

</td><td>

Determine whether you want the reconnaissance to be analyzed by law enforcement agencies. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Law enforcement process** task is executed.If you select **No**, the **Update system\(s\) to prevent reconnaissance** task is executed.

</td></tr><tr><td>

Law enforcement process

</td><td>

Perform the law enforcement process as defined by your company.

</td><td>

When this task is complete, the **Update system\(s\) to prevent reconnaissance** task is executed.

</td></tr><tr><td>

Update system\(s\) to prevent reconnaissance

</td><td>

Perform the steps necessary to update the systems affected by the reconnaissance.

</td><td>

When this task is complete, the **Set state to review** task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is changed automatically to **Review**, and the **Lessons learned meeting** task is executed.

</td></tr><tr><td>

Lessons learned meeting

</td><td>

Conduct a lessons learned meeting to triage the work performed for this reconnaissance incident. Update the **State** field in the task as appropriate.

</td><td>

When this task is complete, the flow ends.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template]()

[Security Incident Denial of Service workflow template]()

[Security Incident Lost Equipment workflow template]()

[Security Incident Malicious Software workflow template]()

[Security Incident Phishing workflow template]()

[Security Incident Policy Violation workflow template]()

[Security Incident Rogue Server or Service workflow template]()

[Security Incident Spam workflow template]()

[Security Incident Unauthorized Access workflow template]()

[Security Incident Web/BBS Defacement workflow template]()

