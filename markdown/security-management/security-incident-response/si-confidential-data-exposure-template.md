---
title: Security Incident Confidential Data Exposure workflow template
description: The Security Incident - Confidential Data Exposure - Template allows you to perform a series of tasks designed to handle the exposure of sensitive data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/si-confidential-data-exposure-template.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Confidential Data Exposure workflow template

The Security Incident - Confidential Data Exposure - Template allows you to perform a series of tasks designed to handle the exposure of sensitive data.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set or changed to **Confidential personal identity data exposure**. This action causes a response task to be created for the first activity in the workflow.

\[Omitted image "confid-data-expos-wf-template.png"\] Alt text: Confidential Data Exposure Template

## Procedure

1.  Open the security incident for which you want to handle the exposure to sensitive data, or [create a new security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Confidential personal identity data exposure**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the flow to end.

<table id="table_ggx_l2s_kbb"><thead><tr><th>

Response task

</th><th>

Description

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Is the data sensitive?

</td><td>

Determine whether the data associated with this security incident is sensitive or confidential. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you selected **Yes**, the next response task is executed.If you selected **No**, the flow ends.

</td></tr><tr><td>

Determine root cause and prevent egress

</td><td>

Determine the root cause of the attack and add egress filtering to stop the exfiltration, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Eliminate exposure related to root cause

</td><td>

Based on the root cause, perform the steps to eliminate the exposure, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Quarantine residual artifacts

</td><td>

Perform the steps to quarantine any residual artifacts, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Legal process

</td><td>

Perform the steps to satisfy the legal requirements of this analysis, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

PR process

</td><td>

Perform the steps to satisfy the PR requirements of this analysis, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is automatically changed to **Review**.

</td></tr><tr><td>

Lessons learned meeting

</td><td>

Conduct a lessons learned meeting to triage the work performed on this sensitive data, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the security incident remains in the **Review** state until you close it.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Denial of Service workflow template]()

[Security Incident Lost Equipment workflow template]()

[Security Incident Malicious Software workflow template]()

[Security Incident Phishing workflow template]()

[Security Incident Policy Violation workflow template]()

[Security Incident Reconnaissance workflow template]()

[Security Incident Rogue Server or Service workflow template]()

[Security Incident Spam workflow template]()

[Security Incident Unauthorized Access workflow template]()

[Security Incident Web/BBS Defacement workflow template]()

