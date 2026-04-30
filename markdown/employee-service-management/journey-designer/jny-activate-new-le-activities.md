---
title: Activate new Lifecycle Events activities
description: Journey designer customers must activate the following Lifecycle Events activities to enable support for the Pre-hire experience: Account/role setup and notification and Transition pre-hire to employee. These activities facilitate the transition of roles through which the employee navigates during the preboarding process.
locale: en-US
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Enable and configure the Pre-hire Experience, Configure, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Activate new Lifecycle Events activities

Journey designer customers must activate the following Lifecycle Events activities to enable support for the Pre-hire experience: Account/role setup and notification and Transition pre-hire to employee. These activities facilitate the transition of roles through which the employee navigates during the preboarding process.

## Before you begin

Role required: admin \[sn\_jny.admin\]

## About this task

The Account/role setup and notification activity is used to facilitate the employee's transition from the applicant role to the pre-hire role. This activity performs the following actions when the Pre-hire activity set is triggered:

-   Creates an account for the employee to enable access to the onboarding portal.
-   Adds the sn\_jny.pre\_hire and snc\_external roles to the employee's user record.
-   Sends an email to the employee with a link to the onboarding portal.

The activity set in which this activity is nested is triggered immediately after you create an onboarding journey that uses the following Lifecycle Events type: Onboarding \(Demo\).

The Transition pre-hire to employee activity is used to facilitate the employee's transition from the pre-hire role to the internal employee role. This activity performs the following actions when the Day 1 activity set is triggered:

-   Removes the sn\_jny.pre\_hire and snc\_external roles from the employee's user record.
-   Adds the snc\_internal role to the employee's user record.

The activity set in which this activity is nested is triggered when the date in the **Employment start date** field in the HR profile record of the onboarding employee is equal to the system date.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Lifecycle Events**.

2.  Select **Onboarding \(Demo\)**.

3.  Select the **Activity Sets** tab.

4.  In the Pre-Hire activity set column, select the **Edit Activity** icon associated with the Account/role setup and notification activity.

    The Activity record appears.

5.  Select the **Active** check box and then select **Update**.

    The Account/role setup and notification activity is active.

6.  In the Day 1 activity set column, select the **Edit Activity** icon associated with the Transition pre-hire to employee activity.

    The Activity record appears.

7.  Select the **Active** check box and select **Update**.

    The Transition pre-hire to employee activity is active.


## What to do next

Configure the widgets for the Pre-hire experience to ensure that they meet your organization's specifications.

**Parent Topic:**[Enable and configure the Pre-hire Experience](../concept/jny-pre-hire-enable-configure.md)

