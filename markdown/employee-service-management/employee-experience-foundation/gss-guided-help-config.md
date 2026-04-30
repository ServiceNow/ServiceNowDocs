---
title: Configure Guided Self-Service
description: Guided Self-Service \(GSS\) helps create a playbook for all the useful content for employees.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Guided Self-Service in Employee Center, Setup browse experience features, Configure, Employee Center, Employee Service Management]
---

# Configure Guided Self-Service

Guided Self-Service \(GSS\) helps create a playbook for all the useful content for employees.

## Before you begin

Ensure you activate the Employee Center application first before installing the **Guided Self-Service** in Employee Center app from ServiceNow Store.

Role required: sn\_hr\_sp.esc\_admin

## Procedure

1.  Navigate to **All** &gt; **Employee Center** &gt; **Guided Self-Service**.

2.  Click **New** or open an existing record.

3.  On the form, fill in the fields.

<table id="table_ipr_bbk_4fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the record.**Note:** When you update or rename the name, ensure you \(re\)activate the GSS.

</td></tr><tr><td>

Active

</td><td>

Check the box to activate.**Note:** Only active items appear on the widget.

</td></tr><tr><td>

Oder

</td><td>

Option to display the order Guided Self-Service process available.

</td></tr><tr><td>

Description

</td><td>

Description that you enter in this field overrides the default short description of the GSS.

</td></tr><tr><td>

Process

</td><td>

Name of the process.

</td></tr><tr><td>

Application

</td><td>

Application scope.

</td></tr><tr><td>

Available for

</td><td>

Option to make GSS available for only the selected users, groups, roles, and more.

</td></tr><tr><td>

Not available for

</td><td>

Option to make the GSS unavailable for.

</td></tr></tbody>
</table>4.  Click **Save** or **Submit**.

    Related tabs Available For, Not Available For, and Assigned Topics appear.

    **Note:** By default, only sn\_hr\_sp.esc\_admin user role can add GSS to the topics and topic persona users \(such as Topic Managers and Contributors\) can't add GSS to the assigned topics.

5.  On the Assign Topics tab, click **Add**, select the topic, and click **OK**.

    **Note:** When you assign the guided process to a subtopic, the help process appears on the topic page and its parent topics. For example, in `Human resources > Benefits`, when a Guided Self-Service is assigned to a subtopic Benefits, the guided self-service appears on its parent topic also.

6.  On the **Available For** and **Not Available For** tab, select the users, groups, roles, and more.

    User criterion is defined for Guided Self-Service.

    **Note:** When a user or user group doesn't have permission to a catalog or a KB article, the `You do not have access to this item` message appears. You can contact the admin for permissions.

7.  Click **Save** or **Update**.

    Remember, you can't configure multiple questions within a single questionnaire.

    **Note:** The incomplete selections are cancelled daily by a schedule job.


## What to do next

Click the **Edit in Process Automation Designer** button to define and publish the process for the Guided Self-Service after you create the process. Proceed to edit the playbook from **Workflow Studio**.

**Note:** Ensure you mark the guided process and playbook active. Only when you activate the GSS process, the **Add** button is displayed on the Assigned Topics.

**Related topics**  


[Guided Self-Service reference](../reference/gss-guided-self-service-reference-info.md)

[Associate Guided Self-Service Process to a topic](associate-gss-guided-process-to-topic.md)

[Use Guided Self-Service](../concept/gss-guided-self-service-homepage.md)

