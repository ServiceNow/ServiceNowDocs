---
title: Security Incident Confidential Data Exposure workflow template
description: The Security Incident - Confidential Data Exposure - Template allows you to perform a series of tasks designed to handle the exposure of sensitive data.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Confidential Data Exposure workflow template

The Security Incident - Confidential Data Exposure - Template allows you to perform a series of tasks designed to handle the exposure of sensitive data.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set or changed to **Confidential personal identity data exposure**. This action causes a response task to be created for the first activity in the workflow.

![Confidential Data Exposure Template](../image/confid-data-expos-wf-template.png "Confidential personal identity data exposure")

## Procedure

1.  Open the security incident for which you want to handle the exposure to sensitive data, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

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
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Denial of Service workflow template](si-denial-of-service-template.md)

[Security Incident Lost Equipment workflow template](si-lost-equip-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

