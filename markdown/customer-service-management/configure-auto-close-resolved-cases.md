---
title: Configure auto close resolved cases
description: Use the auto close resolved cases feature to close cases automatically in the Resolved state if customers choose not to take action.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure auto close resolved cases

Use the auto close resolved cases feature to close cases automatically in the Resolved state if customers choose not to take action.

## Before you begin

Role required: csm\_guided\_setup\_user and admin

## About this task

Enable this feature by activating the **Auto Close Resolved Cases** Flow Designer flow. You can also create a configuration that enables both the system and agents to exclude cases from auto closure.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, select **Get Started**

3.  In the Case Management category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate Auto Close Resolved Case Flow

</td><td>

Activate the Auto Close Resolved Cases Flow Designer Flow, which identifies cases in the Resolved state that are waiting for a customer response and takes the following actions:-   Sends a reminder notification to the customer after 5 days with no response that the case is pending solution acceptance.
-   Closes the case and sends a reminder notification to the customer after 10 days that the case has been auto closed.


</td></tr><tr><td>

Configure Business Rules for Auto Close Field

</td><td>

Configure the following business rules to enable or disable the **Auto Close** field on the Case form:-   Mark for Auto Close
-   Clear Auto Close


</td></tr><tr><td>

Configure Auto Close Flag

</td><td>

The **Auto Close Resolved Cases** Flow Designer flow uses the **Auto Close** flag to exclude cases from auto closure. This flag is hidden by default. To use this flag, configure the Case form to display the **Auto Close** field.

</td></tr></tbody>
</table>4.  To perform a task, select **Configure**.

    This button opens the page in your instance where the configuration is completed.


**Related topics**  


[Automatically close customer service cases](../concept/auto-close-customer-service-case.md)

