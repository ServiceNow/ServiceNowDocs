---
title: Security Incident Denial of Service workflow template
description: The Security Incident - Denial of Service - Template allows you to perform a series of tasks designed to handle Denial of Service \(DOS\) attacks.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Security Incident Response workflow templates, Workflows and workflow template, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Denial of Service workflow template

The Security Incident - Denial of Service - Template allows you to perform a series of tasks designed to handle Denial of Service \(DOS\) attacks.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Denial of Service**. This action causes a response task to be created for the first activity in the workflow.

![Denial of ServiceTemplate](../image/denial-of-service-wf-template.png "Denial of Service (DOS)")

## Procedure

1.  Open the security incident for this denial of service occurrence, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Denial of Service**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the flow to end.

<table id="table_ihp_5ds_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Is target business critical?

</td><td>

Determine if the target of this DOS attack is business critical. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Set priority to critical** task is executed. If you select **No**, the **Is a vulnerability being exploited?** task is executed.

</td></tr><tr><td>

Set priority to critical

</td><td>

No action required.

</td><td>

The **Priority** of the security incident is changed automatically to **Critical**, and the **Is a vulnerability being exploited?** task is executed.

</td></tr><tr><td>

Is a vulnerability being exploited?

</td><td>

Determine whether this DOS attack exploits a software vulnerability. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Emergency patch request** task is executed. If you select **No**, the **Internal attacker?** task is executed.

</td></tr><tr><td>

Emergency patch request

</td><td>

Issue an emergency patch request for the system\(s\) being attacked.Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Internal attacker?

</td><td>

Determine if the source of this DOS attack is internal to your organization. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the **Isolate attacking host\(s\)** task is executed. If you select **No**, the **Notify DOS protection provider and/or ISP** task is executed.

</td></tr><tr><td>

Isolate the attacking host\(s\)

</td><td>

Perform the steps necessary to isolate the internal host\(s\) responsible for the attack. Update the **State** field in the task as appropriate.

</td><td>

After you complete this step, the **Validate system integrity of attacked systems** task is executed.

</td></tr><tr><td>

Notify DOS protection provider and/or ISP

</td><td>

Perform the steps necessary to contact your Denial of Service protection provider and/or your Internet Service Provider to notify them of the attack. Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Validate system integrity of attacked systems

</td><td>

Perform the steps necessary to assess and validate the integrity of the attacked computers. Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Review DOS protections

</td><td>

Conduct a review of your existing DOS protections and procedures. Make any necessary changes. Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is changed automatically to **Review**. The **Lessons learned meeting** task is executed.

</td></tr><tr><td>

Lessons learned meeting

</td><td>

Conduct a lessons learned meeting to triage the work performed for this Denial of Service incident. Update the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the flow ends.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template](si-confidential-data-exposure-template.md)

[Security Incident Lost Equipment workflow template](si-lost-equip-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

