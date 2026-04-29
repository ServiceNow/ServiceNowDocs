---
title: Security Incident Phishing workflow template
description: The Security Incident - Phishing - Template allows you to perform a series of tasks designed to handle spear phishing emails on your network.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Phishing workflow template

The Security Incident - Phishing - Template allows you to perform a series of tasks designed to handle spear phishing emails on your network.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Spear Phishing**. This action causes a response task to be created for the first activity in the workflow.

![Spear phishing workflow template](../image/spear-phishing-wf-template.png "Spear Phishing")

## Procedure

1.  Open the security incident for this potential spear phishing attack, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Spear Phishing**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_yqy_tqs_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Is this a Phishing attack?

</td><td>

Determine if this is a phishing attack. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the following tasks are executed in parallel:-   Scan Endpoint - Malware Found?
-   Update Email Protection Software
-   Remove Unread Phishing Email in Queue - For All Users
 If you select **No**, the flow ends.

</td></tr><tr><td>

Scan Endpoint - Malware Found?

</td><td>

After running a scan, determine whether malware was found.In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Remove Malware - Success?** task is executed. If you select **No**, the **Set State to Review** task is executed.

</td></tr><tr><td>

Remove Malware - Success?

</td><td>

Determine whether the malware was successfully removed. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Set State to Review** task is executed.If you select **No**, the **Wipe and reimage** task is executed.

</td></tr><tr><td>

Wipe and reimage

</td><td>

If you did not successfully remove the malware found, this task instructs you to perform a wipe and reimage on the computers infected with the malware.

</td><td>

After the task is complete, the **Set State to Review** task is executed.

</td></tr><tr><td>

Update Email Protection Software

</td><td>

If it was determined that this is a phishing attack, you are prompted to update your email protection software accordingly.

</td><td>

When the task is complete, the **Set State to Review** task is executed.

</td></tr><tr><td>

Remove Unread Phishing Email in Queue - For All Users

</td><td>

Perform the steps necessary to remove the phishing email still in the queue for all of your users.

</td><td>

When the task is complete, the **Set State to Review** task is executed.

</td></tr><tr><td>

Set State to Review

</td><td>

No action required.

</td><td>

The **State** of the security incident is changed automatically to **Review**. The **Schedule Security Awareness Training** task is executed.

</td></tr><tr><td>

Schedule Security Awareness Training

</td><td>

Schedule training to heighten security awareness by your employees. Update the **State** field in the task as appropriate.

</td><td>

When the task is complete, the flow ends.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template](si-confidential-data-exposure-template.md)

[Security Incident Denial of Service workflow template](si-denial-of-service-template.md)

[Security Incident Lost Equipment workflow template](si-lost-equip-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

