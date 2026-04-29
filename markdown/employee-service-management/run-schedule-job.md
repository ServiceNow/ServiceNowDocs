---
title: Set up a scheduled job for applicant deactivation
description: Set up a scheduled job, at regular intervals, to deactivate applicants no longer viable to the system.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Applicant Center, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Set up a scheduled job for applicant deactivation

Set up a scheduled job, at regular intervals, to deactivate applicants no longer viable to the system.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Select **MarkApplicantInactive**.

3.  View and download the `HiringDeleteRoles.xml` file from the Applicant Center application page on ServiceNow Store.

4.  Import the XML file in the Script Include \[sys\_script\_include\] table.

5.  Modify the frequency of the scheduled job in **Time** and **Run**.

6.  Change the **Value** of the system property \(sn\_ta\_hiring\_core.markApplicantInactive.noOfDays\).

    The base system value to mark an applicant as inactive is 30 days.

7.  Mark the **Active** check box as enabled and select **Update**.

    **Note:** The base system condition of the scheduled job is active. You can deactivate it.


## Result

The applicant records are deactivated.

**Note:** If a deactivated applicant applies again using the same email id that was earlier used to create the sys-user record, all the existing roles are deleted and an external applicant role is assigned during reactivation. For this to happen, you must download the `HiringDeleteRoles.xml` file from the Applicant Center application page on ServiceNow Store.

**Parent Topic:**[Configuring Applicant Center](../concept/config-applicant-center.md)

