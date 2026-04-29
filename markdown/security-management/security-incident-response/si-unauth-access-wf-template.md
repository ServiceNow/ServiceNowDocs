---
title: Security Incident Unauthorized Access workflow template
description: The Security Incident - Unauthorized Access - Template allows you to perform a series of tasks designed to handle unauthorized access to your network.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Unauthorized Access workflow template

The Security Incident - Unauthorized Access - Template allows you to perform a series of tasks designed to handle unauthorized access to your network.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Unauthorized access**. This action causes a response task to be created for the first activity in the workflow.

![Unauthorized access workflow template](../image/unauthorized-access.png "Unauthorized access")

## Procedure

1.  Open the security incident for this potential attack, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Unauthorized access**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_bjb_gws_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

User credentials compromised?

</td><td>

Determine whether any users credentials have been compromised.In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the following two tasks are executed in parallel:-   **Malicious software?**
-   **Deactivate user account**
 If you select **No**, the **Contact user and determine intent** task is executed.

</td></tr><tr><td>

Malicious software?

</td><td>

Determine whether the unauthorized access resulted in the introduction of malicious software. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Create malicious software incident** task is executed.If you select **No**, the **Set state to review** task is executed.

</td></tr><tr><td>

Create malicious software incident

</td><td>

Perform the steps necessary to create a security incident for the unauthorized access.

</td><td>

When this task is complete, the **Set state to review** task is executed.

</td></tr><tr><td>

Deactivate user account

</td><td>

Perform the steps necessary to deactivate the compromised user account.

</td><td>

When this task is complete, the **Set state to review** task is executed.

</td></tr><tr><td>

Contact user and determine intent

</td><td>

Perform the steps necessary to contact the user who responsible for the unauthorized access and determine the reason for the access attempt.

</td><td>

When this task is complete, the **HR process** task is executed.

</td></tr><tr><td>

HR process

</td><td>

Perform the steps necessary to contact human resources to implement disciplinary action if necessary.

</td><td>

When this task is complete, the **Set state to review** task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is changed automatically to **Review**, and the flow ends.

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

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

