---
title: Security Incident Malicious Software workflow template
description: The Security Incident - Malicious Software - Template allows you to perform a series of tasks designed to handle malicious software on your network.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Malicious Software workflow template

The Security Incident - Malicious Software - Template allows you to perform a series of tasks designed to handle malicious software on your network.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Malicious Software**. This action causes a response task to be created for the first activity in the workflow.

![Malicious Software workflow template](../image/malicious-software-template.png "Malicious Software")

## Procedure

1.  Open the security incident for this potential attack, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Malicious code activity**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_cxp_1ns_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Scan Endpoint - Malware Found?

</td><td>

After running a scan, determine whether malware was found.In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Remove Malware - Success?** task is executed. If you select **No**, the flow ends.

</td></tr><tr><td>

Remove Malware - Success?

</td><td>

Determine whether the malware was successfully removed. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Was there a larger breach?** task is executed.If you select **No**, the **Wipe &amp; Reimage** task is executed.

</td></tr><tr><td>

Wipe &amp; Reimage

</td><td>

If you did not successfully remove the malware found, this task instructs you to perform a wipe and reimage on the computers infected with the malware.

</td><td>

After the task is complete, the **Set State to Review** task is executed.

</td></tr><tr><td>

Was there a larger breach?

</td><td>

Determine whether the breach caused by the malicious software is larger than first believed. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the following tasks are executed in parallel:-   Legal Review
-   HR Review
-   Law Enforcement Review
 If you select **No**, the flow ends.

</td></tr><tr><td>

Legal ReviewHR Review

 Law Enforcement Review

</td><td>

Perform the steps necessary for each of these departments to review the process you followed to eradicate the malicious software.

</td><td>

When the tasks are complete, the **Set State to Review** task is executed.

</td></tr><tr><td>

Set State to Review

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

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

