---
title: Create response tasks
description: After a security incident has been created, you can create response tasks to track separate actions to be performed to respond to the security issue.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create response tasks

After a security incident has been created, you can create response tasks to track separate actions to be performed to respond to the security issue.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  Navigate to the appropriate location to open the security incident for which you want to create tasks.

    For example:

    -   To create a response task based on a security incident assigned to you, select **Security Incident** &gt; **Incidents** &gt; **Assigned to Me**.
    -   To create a response task based on a security incident assigned to your team, select **Security Incident** &gt; **Incidents** &gt; **Assigned to Team** &gt; **Incidents**.
    -   To create a response task based on an unassigned security incident, select **Security Incident** &gt; **Incidents** &gt; **Unassigned Incidents**.
2.  Open the security incident for which you want to add response tasks.

3.  Click the **Add Response Task** button in the form header.

    **Note:** To create any other task, click the **Tasks** tab in the incident Related List. For more information on creating other types of tasks, see [Create a task](https://servicenow.com/docs/bundle/xanadu-platform-administration/page/administer/task-table/task/t_CreateATask.html).

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

The skill required to perform this task. Click the lock icon and select the skill required. After you have completed your selections, click the lock icon again.

</td></tr><tr><td>

Assignment group

</td><td>

The assignment group from which the assigned worker is selected.

</td></tr><tr><td>

Assigned to

</td><td>

The individual assigned to perform the task.

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

The work notes that are not visible to the customer.

</td></tr><tr><td>

Additional comments

</td><td>

Comments that you want to be visible to the customer.

</td></tr></tbody>
</table>5.  When you have completed your entries, click **Submit**.

    **Note:** After you have created Security Incident Response tasks, you can view them using any of the following applications under the **Response Tasks** module:

    -   **Assigned to Me**.
    -   **Assigned to Team**.
    -   **Show Open Tasks**
    -   **Show All Tasks**
    -   **Unassigned Tasks**.

