---
title: Create response tasks
description: After a security incident has been created, you can create response tasks to track separate actions to be performed to respond to the security issue.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create response tasks

After a security incident has been created, you can create response tasks to track separate actions to be performed to respond to the security issue.

## Before you begin

**Important:** If you are unable to create a response task, verify that no custom ACLs on the task table are blocking access.

Role required: sn\_si.basic

## Procedure

1.  Navigate to the appropriate location to open the security incident for which you want to create tasks.

    For example:

    -   To create a response task based on a security incident assigned to you, select **Security Incident** &gt; **Incidents** &gt; **Assigned to Me**.
    -   To create a response task based on a security incident assigned to your team, select **Security Incident** &gt; **Incidents** &gt; **Assigned to Team** &gt; **Incidents**.
    -   To create a response task based on an unassigned security incident, select **Security Incident** &gt; **Incidents** &gt; **Unassigned Incidents**.
2.  Open the security incident for which you want to add response tasks.

3.  Select the **Add Response Task** button in the form header.

    **Note:** To create any other task, select the **Tasks** tab in the incident Related List.

4.  Fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select security tag

</td><td>

If you set up and activated [security tags](../../security-operations-common/task/create-class-group-and-tags.md), you can select one or more tags to add metadata to the record or specify the degree of sensitivity of the response task. If you did not set up or activate security tags, this drop-down list is not displayed.

</td></tr><tr><td>

Number

</td><td>

\[Read only\] The automatically generated Security Incident Response number.

</td></tr><tr><td>

Parent

</td><td>

\[Read only\] The number of the related security incident.

</td></tr><tr><td>

Configuration Item

</td><td>

The configuration item \(resource\) affected by the security issue.

</td></tr><tr><td>

Affected User

</td><td>

The person affected by the security issue.

</td></tr><tr><td>

Priority

</td><td>

The priority used to determine when this task is performed.

</td></tr><tr><td>

State

</td><td>

The current state of the security response task. Upon task creation, this field defaults to **Draft**.

</td></tr><tr><td>

Skills

</td><td>

The skill required to perform this task. Select the lock icon and select the skill required. After you have completed your selections, select the lock icon again.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group from which the assigned worker is selected.**Note:** Select an external group if you want to provide the read-only access of the parent security incident of this response task.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to perform the task.

</td></tr><tr><td>

Access to security incident

</td><td>

Option to provide the read-access to the parent security incident of this response task.

</td></tr><tr><td>

Short description

</td><td>

A description of the Security Incident Response task.

</td></tr><tr><td>

Description

</td><td>

A description for the selected task.

</td></tr><tr><td>

Secure notes

</td><td>

The work notes that are encrypted and not visible to the customer.

</td></tr><tr><td>

Work notes

</td><td>

The work notes that aren’t visible to the customer.

</td></tr><tr><td>

Comments

</td><td>

Comments that you want to be visible to the customer.

</td></tr><tr><td>

Email

</td><td>

Option to send email to the stakeholders.

</td></tr></tbody>
</table>5.  When you have completed your entries, select **Submit**.

    **Note:** After you have created Security Incident Response tasks, you can view them using any of the following applications under the **Response Tasks** module:

    -   **Assigned to Me**.
    -   **Assigned to Team**.
    -   **Show Open Tasks**
    -   **Show All Tasks**
    -   **Unassigned Tasks**.

