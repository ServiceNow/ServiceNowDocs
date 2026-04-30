---
title: Add a participant role for the scenario analysis
description: Add a participant role for your scenario analysis in the Operational Resilience application so that you can collect the observations and recommendations of the participants by their roles and functions.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Completing general administrative tasks, Configure, Operational Resilience, Governance, Risk, and Compliance]
---

# Add a participant role for the scenario analysis

Add a participant role for your scenario analysis in the Operational Resilience application so that you can collect the observations and recommendations of the participants by their roles and functions.

## Before you begin

Role required: sn\_oper\_res.admin

## About this task

Depending on the scenario analysis type, such as a scenario analysis for critical services, you can add the participants from the associated business functions and assign various roles. For example, you can add HR, Legal, Finance, or Procurement roles to your participants.

## Procedure

1.  Navigate to **All** &gt; **Operational Resilience** &gt; **Admin** &gt; **Participant Roles** and click **New**.

2.  In the **Set** field, select **Operational Resilience**.

3.  In the **Name** field, enter the name for the participant role.

4.  In the **Label** field, enter a label for the participant role.

5.  In the **Choice category** field, select **Role**.

6.  In the **Value** field, enter the value of the choice for the participant role.

7.  In the **Order** field, enter an order for the participant role.

    This field displays the order of the participant role in the GRC Choice table.

8.  In the **Parent** lookup list options, select a parent service.

    See the sample configuration for a participant role as shown in the following example.

    ![Sample configuration for the GRC Choice New record form.](../image/participant-role-record-choice.png "Sample configuration for the GRC Choice New record form")

9.  Click **Submit**.


## Result

In the Participant Roles module in the application UI, the participant role is listed in the Roles list view.

