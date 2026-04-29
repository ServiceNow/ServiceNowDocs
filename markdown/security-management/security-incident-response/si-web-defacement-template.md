---
title: Security Incident Web/BBS Defacement workflow template
description: The Security Incident - Web/BBS Defacement - Template allows you to perform a series of tasks designed to handle vandalism directed against one of your organization's BBS or web sites.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Security Incident Response workflow templates, Understand Security Incident Response Orchestration workflows and workflow templates, Security Incident Response Orchestration, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Web/BBS Defacement workflow template

The Security Incident - Web/BBS Defacement - Template allows you to perform a series of tasks designed to handle vandalism directed against one of your organization's BBS or web sites.

## Before you begin

Role required: sn\_si.write

## About this task

The workflow is triggered when the **Category** in a security incident is set to **Web/BBS defacement**. This action causes a response task to be created for the first activity in the workflow.

![Web/BBS Defacement Template](../image/web-defacement-wf-template.png "Web/BBS defacement")

## Procedure

1.  Open the security incident for this occurrence of web or BBS defacement, or [create a new security incident](../../security-incident-response/task/t_ManuallyCreateSecurityIncident.md).

2.  In **Category**, select **Web/BBS defacement**.

3.  Save the record.

4.  Scroll down and open the **Response Tasks** related list.

    The first of a series of response tasks appears. Each time the record is saved, your response to the previous task either causes the next response task to be created or the workflow to end.

<table id="table_wvm_4ws_kbb"><thead><tr><th>

Response task

</th><th>

Action

</th><th>

Results

</th></tr></thead><tbody><tr><td>

Security incident assignment

</td><td>

Create a security incident for each reported incident of website or BBS defacement.

</td><td>

The next response task is executed.

</td></tr><tr><td>

Defacement verified?

</td><td>

Determine whether the website or BBS has in fact been defaced. In the task, select **Yes** or **No** in **Outcome**.

</td><td>

If you select **Yes**, the following response tasks are executed:-   **PR process**
-   **Law enforcement process**
-   **Determine and eradicate root cause**
If you select **No**, the flow ends.

</td></tr><tr><td>

PR process

</td><td>

Perform the steps necessary to notify the public that the website or BBS has been defaced. When you are finished with the PR process, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The **Lessons learned meeting** task is executed.

</td></tr><tr><td>

Law enforcement process

</td><td>

Perform the steps required to engage the appropriate law enforcement agencies regarding the attack. When you are finished, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The **Lessons learned meeting** task is executed.

</td></tr><tr><td>

Determine and eradicate root cause

</td><td>

Perform the steps necessary to discover and eliminate the root cause of the defacement. Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Restore site from backup

</td><td>

Perform the steps required to back up and restore the website or BBS. Update the **State** field in the task as appropriate.

</td><td>

If you changed the state of the task to **Closed Complete** or **Cancelled**, the next response task is executed.

</td></tr><tr><td>

Test and verify site is restored

</td><td>

Verify that the site is restored. When you are finished, set the state of the task to **Complete** or **Incomplete** as appropriate.

</td><td>

The **Lessons learned meeting** task is executed.

</td></tr><tr><td>

Lessons learned meeting

</td><td>

Conduct a lessons learned meeting to triage the work performed for this website/BBS defacement incident. Update the **State** field in the task as appropriate.

</td><td>

If you change the state of the task to **Closed Complete** or **Cancelled**, the **Set state to review** task is executed.

</td></tr><tr><td>

Set state to review

</td><td>

No action required.

</td><td>

The **State** of the security incident is changed automatically to **Review**. The flow ends.

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

[Security Incident Unauthorized Access workflow template](si-unauth-access-wf-template.md)

