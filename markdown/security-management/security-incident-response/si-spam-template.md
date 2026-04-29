---
title: Security Incident Spam workflow template
description: The Security Incident - Spam - Template allows you to perform a series of tasks designed to handle email spam on your network.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Spam workflow template

The Security Incident - Spam - Template allows you to perform a series of tasks designed to handle email spam on your network.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set or changed to **Spam source**. This action causes a response task to be created for the first activity in the workflow.

![Security incident spam workflow template](../image/spam-template.png "Spam source")

## Procedure

1.  Open the security incident for which you want to handle email spam, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Spam source**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_oxh_wvs_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Spam contains malicious content?

</td><td>

Determine whether the spam contains malicious software. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you selected **Yes**, the following response tasks are executed:-   **Quarantine email message**
-   **Create malicious software incident**
 If you selected **No**, the **Update email software** is executed.

</td></tr><tr><td>

Create malicious software incident

</td><td>

Perform the steps to create a security incident, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, this response task waits until the next three response tasks have been completed. The state of the security incident then transitions to **Review**.

</td></tr><tr><td>

Quarantine email message

</td><td>

Perform the steps to quarantine the spam, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Block source on firewall

</td><td>

Perform the steps to block the email address on the firewall, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Update email software

</td><td>

Add the email address to your block list, updating the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed. **Note:** This response task is also executed if you answered **No** to the **Spam contains malicious content?** response task.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is automatically changed to **Review**.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template](si-confidential-data-exposure-template.md)

[Security Incident Denial of Service workflow template](si-denial-of-service-template.md)

[Security Incident Lost Equipment workflow template](si-lost-equip-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

