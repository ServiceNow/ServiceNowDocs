---
title: Security Incident Lost Equipment workflow template
description: The Security Incident - Lost Equipment - Template allows you to perform a series of tasks designed to handle lost equipment.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Lost Equipment workflow template

The Security Incident - Lost Equipment - Template allows you to perform a series of tasks designed to handle lost equipment.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Equipment loss**. This action causes a response task to be created for the first activity in the workflow.

![Lost Equipment Template](../image/lost-equip-wf-template.png "Equipment loss")

## Procedure

1.  Open the security incident for the equipment loss, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Equipment loss**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the flow to end.

<table id="table_s33_4ls_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Did the equipment contain sensitive data?

</td><td>

Determine whether the equipment associated with this security incident contained any sensitive or confidential information. In the task, select **Yes** or **No** in **Outcome** as appropriate.

</td><td>

If you select **Yes** the **Was the data encrypted?** task is executed.If you select **No**, the flow ends.

</td></tr><tr><td>

Was the data encrypted?

</td><td>

Determine if the sensitive data on the lost device was encrypted. In the task, select **Yes** or **No** in **Outcome** as appropriate.

</td><td>

If you select **Yes**, the **Remote wipe created?** response task is executed.If you select **No**, the **Create potential data loss incident**response task is executed.

</td></tr><tr><td>

Create potential data loss incident

</td><td>

Perform the steps necessary to create a potential data loss incident. After you have finished, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The **Remote wipe created?** response task is executed.

</td></tr><tr><td>

Remote wipe created?

</td><td>

Perform the steps necessary to execute a remote wipe of the lost equipment. In the task, select **Yes** or **No** in **Outcome** as appropriate.

</td><td>

The **Legal process - Disclosure required** task is executed .

</td></tr><tr><td>

Legal process - Disclosure required?

</td><td>

Perform the steps to satisfy the legal requirements of this analysis. Select **Yes** if a legal disclosure is required, **No**if it is not.

</td><td>

The **Lessons learned meeting** task is executed.

</td></tr><tr><td>

PR process

</td><td>

Perform the steps necessary to satisfy the PR requirements of this analysis. After you have finished, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The **Set state to review** task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action is necessary.

</td><td>

The **State** of the security incident is changed automatically to **Review**.

</td></tr><tr><td>

Lessons learned meeting

</td><td>

Conduct a lessons learned meeting to triage the work performed for this lost equipment incident. After you have finished, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The flow ends.

</td></tr></tbody>
</table>
**Parent Topic:**[Security Incident Response workflow templates](../concept/sir-orch-workflow-templates.md)

**Related topics**  


[Security Incident Confidential Data Exposure workflow template](si-confidential-data-exposure-template.md)

[Security Incident Denial of Service workflow template](si-denial-of-service-template.md)

[Security Incident Malicious Software workflow template](si-malic-sftwr-template.md)

[Security Incident Phishing workflow template](si-phishing-template.md)

[Security Incident Policy Violation workflow template](si-policy-violation-template.md)

[Security Incident Reconnaissance workflow template](si-recon-wf-template.md)

[Security Incident Rogue Server or Service workflow template](si-rogue-wf-template.md)

[Security Incident Spam workflow template](si-spam-template.md)

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

[Security Incident Web/BBS Defacement workflow template](si-web-defacement-template.md)

