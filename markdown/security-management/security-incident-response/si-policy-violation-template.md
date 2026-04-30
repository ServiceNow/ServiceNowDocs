---
title: Security Incident Policy Violation workflow template
description: The Security Incident - Policy Violation - Template allows you to perform a series of tasks designed to handle security policy violations.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Policy Violation workflow template

The Security Incident - Policy Violation - Template allows you to perform a series of tasks designed to handle security policy violations.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Policy violation**. This action causes a response task to be created for the first activity in the workflow.

![Policy Violation Template](../image/policy-violation-wf-template.png "Policy violation")

## Procedure

1.  Open the security incident for the policy violation, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Policy violation**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_ors_srs_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Classify violation

</td><td>

Classify how this infraction violates your organization's security policies. Update the **State** field in the task after you have completed it.

</td><td>

The **Advise violator of infraction** response task is executed.

</td></tr><tr><td>

Advise violator of infraction

</td><td>

Communicate the nature of the infraction to the violator. Update the **State** field in the task after you have communicated it.

</td><td>

The **Obtain acknowledgement from violator** response task is executed.

</td></tr><tr><td>

Obtain acknowledgement from violator

</td><td>

Obtain an acknowledgement from the violator of the infraction. Update the **State** field in the task as appropriate.

</td><td>

The **HR process** response task is executed.

</td></tr><tr><td>

HR process

</td><td>

Communicate all necessary information about this violation to HR. Update the **State** field in the task as appropriate.

</td><td>

The **Set state to review** response task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action is necessary.

</td><td>

The **State** of the security incident is changed automatically to **Review**.

</td></tr><tr><td>

Schedule security awareness training

</td><td>

Conduct a security awareness training to educate staff on how to prevent similar security violations in the future. Update the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the flow ends.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template](si-confidential-data-exposure-template.md)

[Security Incident Denial of Service workflow template](si-denial-of-service-template.md)

[Security Incident Lost Equipment workflow template](si-lost-equip-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

